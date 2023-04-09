# Error Management Cheatsheet

## Debian Specific Commands

### APT timezone or cert mismatch error (temporary fix) solution

```shell
sudo apt-get -o Acquire::Check-Valid-Until=false -o Acquire::Check-Date=false update
```

### Screen tear solutions

1. Add the following line

```bash
i915.enable_psr=0
```

Inside:

```bash
GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"
```

After ***splash***

2. Install Compton compositor

```bash
sudo apt -y install compton
```

For XFCE:

```bash
xfconf-query -c xfwm4 -p /general/use_compositing -s false

rm -rf ~/.config/xfce4/ && sudo reboot
```

3. Goto compositor options of your ‘display settings’ and select ‘no compositor’ or any other option (IF you don't want any compositor!)
4. ONLY use if driver issues persist - disable nouveau modeset

```bash
nouveau.modeset=0
```

Inside the line after ***splash***

```bash
GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"
```

### Restart networking

```shell
sudo systemctl restart NetworkManager.service
```

### Name resolution failure solution
1. Try to restart dnsmasq service:  ```sudo service dnsmasq restart```
2. Create and add google dns in resolver: ```sudo touch /etc/resolv.conf``` and add ```nameserver 8.8.8.8``` inside it.
	1. Restart resolv service: ```sudo systemctl restart systemd-resolved.service && sudo service systemd-resolved status```

### List network service running on specific port

```shell
sudo netstat -ltnp | grep -w ':8080'
```

### List service running on port

```shell
lsof -i :8080
```

### List running process by name

```shell
ps -fA | grep python
```

### Kill a process using process ID

```shell
kill 81211
```

### Kill all specific application name processes

```shell
kill -9 $(ps -A | grep python | awk '{print $1}')
```

### Kill all specific application name processes

```shell
kill -9 $(ps -A | grep python | awk '{print $1}')
```
