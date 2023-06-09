# HaxKali

## Features

- KVM + QCOW2 base ( [[KVM Setup]] )
- Xanmod Kernel Edge ( [[Debian Optimizations]] )
- SSD & VM optimizations ( [[Debian Optimizations]] )
- Sand-boxed Common Apps ( [[Debian Optimizations]] )
- 500+ New Packages
- Preconfigured Custom Tools
- App Execution Security Improvements ( [[App Optimizations]] )
- App Customized For Privacy ( [[App Optimizations]] )

[[Debian Optimizations]]

[[App Optimizations]]

## Other VM Customization

### 'LS' Replaced By LSDeluxe

- `sudo apt install lsd`
- Setup alias in `~/.zshrc` and `~/.bashrc` :
	- Add the following line: `alias ls='lsd'`

## Shared Clipboard - KVM Linux

In guest, run: `sudo apt install spice-vdagent` & restart

## Installed Tools & Packages

- Initial Setup
	- Apt Package Setup
	- Deb Package Setup
	- Flatpaks Setup
	- Github Repos Setup

## Install.sh

```bash
sudo apt install -y locate
sudo apt install -y xdg-desktop-portal-gtk
sudo apt install -y mono-devel
sudo apt install -y spice-vdagent
sudo apt install -y apt-transport-https
sudo apt install -y ttf-mscorefonts-installer
sudo apt install -y lsd
sudo apt install -y preload
sudo apt install -y keepassxc
sudo apt install -y stacer
sudo apt install -y python3-pip
sudo apt install -y tor
sudo apt install -y proxychains
sudo apt install -y flatpak
sudo apt install -y terminator
sudo apt install -y gdebi
sudo apt install -y gparted
sudo apt install -y qbittorrent
sudo apt install -y htop
sudo apt install -y axel
sudo apt install -y neofetch
sudo apt install -y usbtop
sudo apt install -y kali-anonsurf
sudo apt install -y sirikali
sudo apt install -y dbeaver
sudo apt install -y git
sudo apt install -y sqlitebrowser
sudo apt install -y ruby
sudo apt install -y powershell
sudo apt install -y golang-go
sudo apt install -y arp-scan
sudo apt install -y 0trace
sudo apt install -y amap
sudo apt install -y arping
sudo apt install -y braa
sudo apt install -y thc-ipv6
sudo apt install -y dmitry
sudo apt install -y dnsenum
sudo apt install -y dnsmap
sudo apt install -y enum4linux
sudo apt install -y etherape
sudo apt install -y fping
sudo apt install -y gobuster
sudo apt install -y hping3
sudo apt install -y ike-scan
sudo apt install -y intrace
sudo apt install -y irpas
sudo apt install -y lbd
sudo apt install -y maltego
sudo apt install -y masscan
sudo apt install -y nbtscan
sudo apt install -y netdiscover
sudo apt install -y nmap
sudo apt install -y onesixtyone
sudo apt install -y p0f
sudo apt install -y recon-ng
sudo apt install -y smbmap
sudo apt install -y smtp-user-enum
sudo apt install -y snmpcheck
sudo apt install -y ssldump
sudo apt install -y sslh
sudo apt install -y sslscan
sudo apt install -y sslyze
sudo apt install -y swaks
sudo apt install -y theharvester
sudo apt install -y unicornscan
sudo apt install -y ismtp
sudo apt install -y python3-shodan
sudo apt install -y emailharvester
sudo apt install -y instaloader
sudo apt install -y inspy
sudo apt install -y sherlock
sudo apt install -y certgraph
sudo apt install -y nmapsi4
sudo apt install -y afl
sudo apt install -y doona
sudo apt install -y thc-ipv6
sudo apt install -y dhcpig
sudo apt install -y enumiax
sudo apt install -y gvm
sudo apt install -y iaxflood
sudo apt install -y inviteflood
sudo apt install -y dsniff
sudo apt install -y ohrwurm
sudo apt install -y protos-sip
sudo apt install -y rtpbreak
sudo apt install -y rtpflood
sudo apt install -y rtpinsertsound
sudo apt install -y rtpmixsound
sudo apt install -y sipp
sudo apt install -y slowhttptest
sudo apt install -y spike
sudo apt install -y sipvicious
sudo apt install -y thc-ssl-dos
sudo apt install -y unix-privesc-check
sudo apt install -y voiphopper
sudo apt install -y yersinia
sudo apt install -y siparmyknife
sudo apt install -y sctpscan
sudo apt install -y cisco-ocs
sudo apt install -y cisco-torch
sudo apt install -y copy-router-config
sudo apt install -y burpsuite
sudo apt install -y commix
sudo apt install -y davtest
sudo apt install -y dirb
sudo apt install -y dirbuster
sudo apt install -y gobuster
sudo apt install -y joomscan
sudo apt install -y jsql-injection
sudo apt install -y nikto
sudo apt install -y padbuster
sudo apt install -y skipfish
sudo apt install -y wfuzz
sudo apt install -y whatweb
sudo apt install -y wig
sudo apt install -y wpscan
sudo apt install -y xsser
sudo apt install -y zaproxy
sudo apt install -y wafw00f
sudo apt install -y parsero
sudo apt install -y armitage
sudo apt install -y beef-xss
sudo apt install -y commix
sudo apt install -y thc-ipv6
sudo apt install -y jsql-injection
sudo apt install -y king-phisher
sudo apt install -y mdbtools
sudo apt install -y metasploit-framework
sudo apt install -y oscanner
sudo apt install -y pompem
sudo apt install -y set
sudo apt install -y shellnoob
sudo apt install -y sidguesser
sudo apt install -y sqlmap
sudo apt install -y websploit
sudo apt install -y unicorn-magic
sudo apt install -y backdoor-factory
sudo apt install -y ncat-w32
sudo apt install -y powercat
sudo apt install -y dns2tcp
sudo apt install -y hyperion
sudo apt install -y iodine
sudo apt install -y laudanum
sudo apt install -y nishang
sudo apt install -y proxychains
sudo apt install -y proxytunnel
sudo apt install -y ptunnel
sudo apt install -y pwnat
sudo apt install -y sbd
sudo apt install -y shellter
sudo apt install -y socat
sudo apt install -y sslh
sudo apt install -y stunnel4
sudo apt install -y udptunnel
sudo apt install -y webacoo
sudo apt install -y weevely
sudo apt install -y windows-binaries
sudo apt install -y webshells
sudo apt install -y mimikatz
sudo apt install -y powersploit
sudo apt install -y passing-the-hash
sudo apt install -y wce
sudo apt install -y xspy
sudo apt install -y lynis
sudo apt install -y linux-exploit-suggester
sudo apt install -y brutespray
sudo apt install -y cewl
sudo apt install -y changeme
sudo apt install -y chntpw
sudo apt install -y cmospwd
sudo apt install -y crackle
sudo apt install -y crunch
sudo apt install -y fcrackzip
sudo apt install -y hashcat
sudo apt install -y hashid
sudo apt install -y hydra
sudo apt install -y john
sudo apt install -y johnny
sudo apt install -y pack
sudo apt install -y medusa
sudo apt install -y onesixtyone
sudo apt install -y ophcrack-cli
sudo apt install -y ophcrack
sudo apt install -y pdfcrack
sudo apt install -y pipal
sudo apt install -y pixiewps
sudo apt install -y rainbowcrack
sudo apt install -y rarcrack
sudo apt install -y rcracki-mt
sudo apt install -y rsmangler
sudo apt install -y samdump2
sudo apt install -y sipcrack
sudo apt install -y sucrack
sudo apt install -y thc-pptp-bruter
sudo apt install -y truecrack
sudo apt install -y twofi
sudo apt install -y wordlists
sudo apt install -y device-pharmer
sudo apt install -y statsprocessor
sudo apt install -y aircrack-ng
sudo apt install -y airgeddon
sudo apt install -y asleap
sudo apt install -y bluelog
sudo apt install -y blueranger
sudo apt install -y bluesnarfer
sudo apt install -y btscanner
sudo apt install -y bluez-hcidump
sudo apt install -y bully
sudo apt install -y cowpatty
sudo apt install -y crackle
sudo apt install -y eapmd5pass
sudo apt install -y fern-wifi-cracker
sudo apt install -y hackrf
sudo apt install -y inspectrum
sudo apt install -y king-phisher
sudo apt install -y mdk3
sudo apt install -y mfcuk
sudo apt install -y mfoc
sudo apt install -y mfterm
sudo apt install -y libfreefare-bin
sudo apt install -y libnfc-bin
sudo apt install -y pixiewps
sudo apt install -y reaver
sudo apt install -y redfang
sudo apt install -y rfcat
sudo apt install -y rtlsdr-scanner
sudo apt install -y ubertooth
sudo apt install -y wifi-honey
sudo apt install -y wifite
sudo apt install -y yersinia
sudo apt install -y bettercap
sudo apt install -y chaosreader
sudo apt install -y darkstat
sudo apt install -y dnschef
sudo apt install -y dsniff
sudo apt install -y sniffjoke
sudo apt install -y tcpflow
sudo apt install -y driftnet
sudo apt install -y etherape
sudo apt install -y ettercap-graphical
sudo apt install -y thc-ipv6
sudo apt install -y fiked
sudo apt install -y hamster-sidejack
sudo apt install -y hexinject
sudo apt install -y isr-evilgrade
sudo apt install -y mitmproxy
sudo apt install -y netsniff-ng
sudo apt install -y rebind
sudo apt install -y responder
sudo apt install -y sslsniff
sudo apt install -y sslsplit
sudo apt install -y tcpreplay
sudo apt install -y wifi-honey
sudo apt install -y wireshark
sudo apt install -y yersinia
sudo apt install -y afflib-tools
sudo apt install -y dumpzilla
sudo apt install -y extundelete
sudo apt install -y rifiuti
sudo apt install -y ewf-tools
sudo apt install -y cabextract
sudo apt install -y autopsy
sudo apt install -y binwalk
sudo apt install -y sleuthkit
sudo apt install -y dc3dd
sudo apt install -y dcfldd
sudo apt install -y ddrescue
sudo apt install -y dex2jar
sudo apt install -y ewf-tools
sudo apt install -y extundelete
sudo apt install -y foremost
sudo apt install -y galleta
sudo apt install -y gtkhash
sudo apt install -y guymager
sudo apt install -y hashdeep
sudo apt install -y magicrescue
sudo apt install -y missidentify
sudo apt install -y pasco
sudo apt install -y pdf-parser
sudo apt install -y pdfid
sudo apt install -y pev
sudo apt install -y recoverjpeg
sudo apt install -y reglookup
sudo apt install -y regripper
sudo apt install -y rifiuti
sudo apt install -y rifiuti2
sudo apt install -y safecopy
sudo apt install -y scalpel
sudo apt install -y scrounge-ntfs
sudo apt install -y vinetto
sudo apt install -y xplico
sudo apt install -y inetsim
sudo apt install -y forensic-artifacts
sudo apt install -y galleta
sudo apt install -y gpp-decrypt
sudo apt install -y guymager
sudo apt install -y smartmontools
sudo apt install -y yara
sudo apt install -y gscanbus
sudo apt install -y clang
sudo apt install -y dex2jar
sudo apt install -y edb-debugger
sudo apt install -y gdb
sudo apt install -y javasnoop
sudo apt install -y rizin
sudo apt install -y rizin-cutter
sudo apt install -y smali
sudo apt install -y eyewitness
sudo apt install -y faraday-cli
sudo apt install -y faraday
sudo apt install -y vokoscreen
sudo apt install -y impacket-scripts
sudo apt install -y ngrep
sudo apt install -y netsed
sudo apt install -y osslsigncode
sudo apt install -y arpwatch
sudo apt install -y vlan
sudo apt install -y nginx
sudo apt install -y arping
sudo apt install -y crunch
sudo apt install -y davtest
sudo apt install -y dc3dd
sudo apt install -y dhcpig
sudo apt install -y dirb
sudo apt install -y dirbuster
sudo apt install -y dmitry
sudo apt install -y dns2tcp
sudo apt install -y dnschef
sudo apt install -y dnsenum
sudo apt install -y dnsmap
sudo apt install -y dos2unix
sudo apt install -y eapmd5pass
sudo apt install -y enumiax
sudo apt install -y ethtool
sudo apt install -y fcrackzip
sudo apt install -y fping
sudo apt install -y hashcat
sudo apt install -y hping3
sudo apt install -y iaxflood
sudo apt install -y impacket-scripts
sudo apt install -y iodine
sudo apt install -y isr-evilgrade
sudo apt install -y john
sudo apt install -y joomscan
sudo apt install -y laudanum
sudo apt install -y links
sudo apt install -y lynis
sudo apt install -y maskprocessor
sudo apt install -y medusa
sudo apt install -y metasploit-framework
sudo apt install -y miredo
sudo apt install -y miredo-server
sudo apt install -y mitmproxy
sudo apt install -y nasm
sudo apt install -y nbtscan
sudo apt install -y ncrack
sudo apt install -y netdiscover
sudo apt install -y nikto
sudo apt install -y nmap
sudo apt install -y openssh-server
sudo apt install -y ophcrack-cli
sudo apt install -y oscanner
sudo apt install -y p0f
sudo apt install -y powersploit
sudo apt install -y proxychains
sudo apt install -y proxytunnel
sudo apt install -y ptunnel
sudo apt install -y pwnat
sudo apt install -y crackmapexec
sudo apt install -y rainbowcrack
sudo apt install -y reaver
sudo apt install -y sbd
sudo apt install -y set
sudo apt install -y sfuzz
sudo apt install -y siege
sudo apt install -y skipfish
sudo apt install -y smbclient
sudo apt install -y smbmap
sudo apt install -y smtp-user-enum
sudo apt install -y snmpcheck
sudo apt install -y socat
sudo apt install -y spiderfoot
sudo apt install -y sqlmap
sudo apt install -y ssldump
sudo apt install -y sslscan
sudo apt install -y sslsniff
sudo apt install -y tcpdump
sudo apt install -y t50
sudo apt install -y thc-ipv6
sudo apt install -y thc-ssl-dos
sudo apt install -y theharvester
sudo apt install -y traceroute
sudo apt install -y whois
sudo apt install -y truecrack
sudo apt install -y udptunnel
sudo apt install -y unix-privesc-check
sudo apt install -y webacoo
sudo apt install -y webshells
sudo apt install -y websploit
sudo apt install -y weevely
sudo apt install -y whatweb
sudo apt install -y etherwake
sudo apt install -y wpscan
sudo apt install -y xprobe
sudo apt install -y xsser
sudo apt install -y yersinia
sudo apt install -y beef-xss
sudo apt install -y saidar
sudo apt install -y hexinject
sudo apt install -y arping
sudo apt install -y asleap
sudo apt install -y doona
sudo apt install -y bully
sudo apt install -y chntpw
sudo apt install -y cowpatty
sudo apt install -y creddump7
sudo apt install -y crunch
sudo apt install -y cymothoa
sudo apt install -y davtest
sudo apt install -y dc3dd
sudo apt install -y dcfldd
sudo apt install -y ddrescue
sudo apt install -y dhcpig
sudo apt install -y dirb
sudo apt install -y dirbuster
sudo apt install -y dmitry
sudo apt install -y dns2tcp
sudo apt install -y dnschef
sudo apt install -y dnsenum
sudo apt install -y dnsrecon
sudo apt install -y dnstracer
sudo apt install -y dnswalk
sudo apt install -y dos2unix
sudo apt install -y dsniff
sudo apt install -y eapmd5pass
sudo apt install -y enumiax
sudo apt install -y ethtool
sudo apt install -y ettercap-graphical
sudo apt install -y fcrackzip
sudo apt install -y ferret
sudo apt install -y fierce
sudo apt install -y foremost
sudo apt install -y fping
sudo apt install -y hexinject
sudo apt install -y hping3
sudo apt install -y htshells
sudo apt install -y iaxflood
sudo apt install -y impacket-scripts
sudo apt install -y iodine
sudo apt install -y isr-evilgrade
sudo apt install -y john
sudo apt install -y joomscan
sudo apt install -y laudanum
sudo apt install -y libnet1-dev
sudo apt install -y libpcap-dev
sudo apt install -y links
sudo apt install -y lynis
sudo apt install -y maskprocessor
sudo apt install -y mdk3
sudo apt install -y medusa
sudo apt install -y miredo
sudo apt install -y mitmproxy
sudo apt install -y nasm
sudo apt install -y nbtscan
sudo apt install -y netdiscover
sudo apt install -y nishang
sudo apt install -y nmap
sudo apt install -y openssh-server
sudo apt install -y oscanner
sudo apt install -y outguess
sudo apt install -y p0f
sudo apt install -y payloadsallthethings
sudo apt install -y powercat
sudo apt install -y powersploit
sudo apt install -y proxychains
sudo apt install -y proxytunnel
sudo apt install -y ptunnel
sudo apt install -y pwnat
sudo apt install -y reaver
sudo apt install -y reglookup
sudo apt install -y rig
sudo apt install -y safecopy
sudo apt install -y sbd
sudo apt install -y scalpel
sudo apt install -y sfuzz
sudo apt install -y shellinabox
sudo apt install -y siege
sudo apt install -y sipcrack
sudo apt install -y sipvicious
sudo apt install -y skipfish
sudo apt install -y smbmap
sudo apt install -y smbclient
sudo apt install -y smtp-user-enum
sudo apt install -y snmpcheck
sudo apt install -y socat
sudo apt install -y spiderfoot
sudo apt install -y sqldict
sudo apt install -y sqlmap
sudo apt install -y ssldump
sudo apt install -y sslscan
sudo apt install -y sslsniff
sudo apt install -y steghide
sudo apt install -y t50
sudo apt install -y tcpxtract
sudo apt install -y tcpick
sudo apt install -y tlssled
sudo apt install -y tcptrace
sudo apt install -y thc-ipv6
sudo apt install -y thc-ssl-dos
sudo apt install -y theharvester
sudo apt install -y themole
sudo apt install -y traceroute
sudo apt install -y whois
sudo apt install -y udptunnel
sudo apt install -y unix-privesc-check
sudo apt install -y wce
sudo apt install -y webacoo
sudo apt install -y webshells
sudo apt install -y websploit
sudo apt install -y weevely
sudo apt install -y whatweb
sudo apt install -y wireshark
sudo apt install -y etherwake
sudo apt install -y wpscan
sudo apt install -y xprobe
sudo apt install -y xsser
sudo apt install -y yersinia
sudo apt install -y zaproxy
sudo apt install -y zulucrypt
sudo apt install -y ftester
sudo apt install -y smali
sudo apt install -y geany
sudo apt install -y soundmodem
sudo apt install -y minimodem
sudo apt install -y mat2
sudo apt install -y shcheck
sudo apt install -y kazam
sudo apt install -y gnome-software-plugin-flatpak
sudo apt install -y seclists
sudo apt install -y dev-essential
sudo apt install -y devscripts
pip3 install arjun
git clone --depth=1 https://github.com/1N3/Sn1per.git
git clone --depth=1 https://github.com/six2dez/reconftw.git
git clone --depth=1 https://github.com/TryCatchHCF/PacketWhisper.git
git clone --depth=1 https://github.com/haxerzin/ChayaV2.git
git clone --depth=1 https://github.com/swisskyrepo/PayloadsAllTheThings.git
sudo apt install gnome-software-plugin-flatpak
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
searchsploit -u

```
