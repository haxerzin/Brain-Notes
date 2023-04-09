# KVM Setup Guide

- Bash script: https://github.com/xerohackcom/QuickKVM\
- KVM Optimization ( [[KVM Optimization]] )

## Host Setup
Install following packages:
```bash
sudo apt-get install qemu-kvm bridge-utils virt-manager qemu virt-viewer spice-vdagent
```

### KVM without root access
Type the following one by one into terminal:
```
sudo sed -i "s/#user = \"root\"/user = \"$(id -un)\"/g" /etc/libvirt/qemu.conf

sudo sed -i "s/#group = \"root\"/group = \"$(id -gn)\"/g" /etc/libvirt/qemu.conf

sudo usermod -a -G kvm $(id -un)

sudo usermod -a -G libvirt $(id -un)

sudo systemctl restart libvirtd

sudo ln -s /etc/apparmor.d/usr.sbin.libvirtd /etc/apparmor.d/disable/
```

### Making networking available to KVM
Type the following commands into terminal:
```
wget https://gitlab.com/apparmor/apparmor/-/blob/master/profiles/apparmor.d/usr.sbin.dnsmasq -O ~/usr.sbin.dnsmasq

sudo mv ~/usr.sbin.dnsmasq /etc/apparmor.d/

sudo sed -i "s/\/usr\/libexec\/libvirt_leaseshelper m,/\/usr\/libexec\/libvirt_leaseshelper mr,/g" /etc/apparmor.d/usr.sbin.dnsmasq
```

### Create libvirt config
Type the following in terminal:
```
mkdir -p ~/.config/libvirt

echo "uri_default = \"qemu:///system\"" >> ~/.config/libvirt/libvirt.conf
```

Restart the system!

## VM Setup (Windows)
- Download virtio-win from: `https://fedorapeople.org/groups/virt/virtio-win/direct-downloads/` 
- Download Windows 10
- Follow instructions: https://github.com/casualsnek/cassowary/blob/main/docs/1-virt-manager.md#creating-a-virtual-machine

## Cassowary Setup (Win10)
### Inside Windows Guest
- Turn on Remote Desktop using Settings/
- Download and extract ZIP: https://github.com/casualsnek/cassowary/releases/
- Click setup.bat

### Inside Linux Host
Download .whl file: https://github.com/casualsnek/cassowary/releases/ & open terminal in the location.

Type the following commands in terminal:
```
sudo apt install freerdp2-x11 python3-pip python3-libvirt

pip3 install PyQt5

pip install cassowary*

echo "PATH=\$PATH:$HOME/.local/bin" >> $HOME/.profile

python3 -m cassowary -a
```

## Optimization using Tuned

In Linux host and guest, install the following:
```
sudo apt update

sudo apt install tuned tuned-utils tuned-utils-systemtap
```

Check the status of `tuned` service using: 
```
systemctl status tuned
```

### Host Setup

Check your active profile using: `tuned-adm active` and change the profile for KVM maximum performance using: 
```
sudo tuned-adm profile virtual-host
```

### Guest Setup

Check your active profile using: `tuned-adm active` and change the profile for KVM maximum performance using: 
```
sudo tuned-adm profile virtual-guest
```

#### Enable clipboard on Linux Guest
```bash
sudo apt install spice-vdagent
```

## Converting QCOW2 to VDI

```
qemu-img convert -O vdi /var/lib/libvirt/images/kali.qcow2 ~/Documents/kali.vdi
```
