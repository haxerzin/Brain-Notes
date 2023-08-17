# FFUF Cheatsheet

## Basic Bruteforce

```bash
ffuf -c -w /usr/share/wordlists/dirb/small.txt -u https://ffuf.io.fi/FUZZ
```

## Mass subdomain fuzzing

```bash
cat ~/RECON/usgov/doms.txt | while read line; do ffuf -c -t 100 -mc 200,204,301,302,307 -w ~/Desktop/pays/FUZZSUBS.txt -u https://FUZZ.$line -o fuzzed_subs.txt; done
```
## Recursive Scanning

```bash
ffuf -c -w /path/to/wordlist -u https://ffuf.io.fi/FUZZ -recursion -recursion-depth 2
```

## Extensions

```bash
ffuf -c -w /path/to/wordlist -u https://ffuf.io.fi/FUZZ -e .bak, .zip
```

## Multiple Paths

```bash
ffuf -u https://W2/W1 -w ./wordlist.txt:W1,./domains.txt:W2
```

## Subdomains

```bash
ffuf -c -w /path/to/wordlist -u https://ffuf.io.fi -H "Host: FUZZ.ffuf.io.fi"
```

## Filters

### Filter via HTTP status codes

```bash
ffuf -c -w /path/to/wordlist -u https://ffuf.io.fi -mc 200,301
```

### Filter via amount of lines in response

```bash
ffuf -c -w /path/to/wordlist -u https://ffuf.io.fi -ml 50
```

### Filter via HTTP response size

```bash
ffuf -c -w /path/to/wordlist -u https://ffuf.io.fi -ms 350
```

### Filter via words count in response

```bash
ffuf -c -w /path/to/wordlist -u https://ffuf.io.fi -mw 200
```

### Filter via regular expressions

```bash
ffuf -c -w /path/to/wordlist -u https://ffuf.io.fi -mr "root:"
```

## HTTP Based Fuzzing

### Cookie-based Authentication

```bash
ffuf -c -w /path/to/wordlist -u https://ffuf.io.fi -b "sessionId=cookie_val"
```

###  GET parameter fuzzing

```bash
ffuf -c -w /path/to/wordlist -u https://ffuf.io.fi?FUZZ=test_value
```

###  POST data fuzzing

```bash
ffuf -c -w /path/to/wordlist -X POST -d "username=admin&password=FUZZ" -u https://ffuf.io.fi/login.php
```

### JSON POST data fuzzing

```bash
ffuf -w wordlist.txt -X  PUT -u http://test.site/api/users/6 -H "Content-Type: application/json" -d "{'FUZZ':'test_val'}"
```

### Pass Success Commands To BURP

```bash
ffuf -request ~/Desktop/request.txt -w ./wordlist.txt -replay-proxy http://127.0.0.1:8080
```
