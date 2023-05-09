# Error Management Cheatsheet

## Debian Specific Commands

### User not in sudoers to issue 'sudo' command

This issue will usually occur in these common situations:

1. You have installed GNU/Linux OS and logged in as a user
2. You have created a new user and logged in as that user
3. Your administrator has provided you with a user and restricted what you may run with 'sudo' command
4. Your administrator does not want you to run 'sudo' or any elevated command

In all of the above sitations, there is one single solution! We add your user to sudoers file.

- Open the terminal and enter the SU session using the following command (you will require admin password for this to work):

```bash
su -
```

- You will be in root shell. You can confirm this by seeing: `root@` in your terminal
- Add your user to sudoers group using:

```bash
sudo usermod -aG sudo your_username
```

- Open sudoers file using `sudo nano /etc/sudoers` and we will add our user here. Don't worry if there is a message saying "it's ment for view-only etc..". Just add the following at the end of the file and save using CRRL+S

```bash
your_username ALL=(ALL: ALL) ALL
```

- Exit root shell by closing the current terminal. Open a new terminal and sudo should work for the user.

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
