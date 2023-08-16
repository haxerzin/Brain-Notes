# Regex Cheatsheet

## Sublime Text Specific Only

### Find all lines starting with # comments

```
^#.*\n
```

### All words starting with specific character

```
P[\w]+
```

### Find all email addresses in a document

```
[\w\-\.]+@([\w-]+\.)+[\w\-]{2,4}
```

### Full dates in document

```
[\d]{1,2} [ADFJMNOS]\w* [\d]{4}
```

### Match all line containing a word

```
[\s\S].(WORD).*[\s\S]
```

### Match everything before the word including the word itself

```
^(.*?WORD) ?
```

### Lookup Table
| Name | Symbol | Pure Regex |
| --- | --- | --- |
| Caret | ^ | ^ |
| Digit | \d | [0-9] |
| Not Digit | \D | ```[^\d]``` |
| Word | \w | [a-zA-z0-9] |
| Not Word | \W | ```[^\w]```|
| Whitespace | \s | [\f\n\r\t\v] |
| Not Whitespace | \S | ```[^\s]``` |

