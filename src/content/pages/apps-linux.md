---
title: IVPN for Linux - Open-source VPN app for Linux
description: IVPN for Linux offers you comprehensive privacy leak protection with the IVPN firewall, automatic connection on insecure Wi-Fi and Multi-hop.
h1: IVPN for Linux
subtitle: supports 64-bit Linux 3.10+
url: /apps-linux/
platform: linux
layout: apps-single
imageLight: /images-static/uploads/apps/linux-app-3.3.7-light@2x.png
imageDark: /images-static/uploads/apps/linux-app-3.3.7-dark@2x.png
contents:
- item:
    title: Features
    anchor: features
- item:
    title: Packages
    anchor: packages
- item:
    title: Install from IVPN Repository
    anchor: install
    subitems:
    - item:
        title: Ubuntu
        anchor: ubuntu
    - item:
        title: Debian
        anchor: debian
    - item:
        title: Mint
        anchor: mint
    - item:
        title: Fedora
        anchor: fedora
    - item:
        title: CentOS
        anchor: centos
    - item:
        title: Arch Linux
        anchor: arch
- item:
    title: Install from Binaries
    anchor: binaries
- item:
    title: Install from Source Code
    anchor: source
- item:
    title: Useful Links
    anchor: useful-links
---
## Features {#features}

* WireGuard or OpenVPN protocols.
* GUI or CLI (command-line interface).
* WireGuard privacy controls - Define automatic key and IP address rotation schedule.
* AntiTracker that blocks ads, adware, malicious websites and data harvesting trackers.
* Firewall / killswitch - Ability to configure as on-demand or always-on. Offers comprehensive protection against DNS, IPv6, disconnection and WebRTC leaks.
* Ability to define trusted Wi-Fi networks and create rules for automatic VPN connection/disconnection.
* Multi-hop VPN routes. Connect through multiple servers in separate jurisdictions for enhanced privacy.
* Allow LAN traffic when connected to VPN.
* Port forwarding for OpenVPN, reserved on all servers.
* Pause VPN for when disabling VPN connection temporarily is required.
* Obfsproxy option to circumvent censorship.

## Packages {#packages}

### Base Package  

Base package contains everything you need to connect to IVPN with command line interface. IVPN GUI app is provided as a separate package you can find below.  
[Changelog](https://github.com/ivpn/desktop-app/blob/master/CHANGELOG.md)  

### IVPN GUI App  

Please note: base package is required to be installed prior to installing GUI app.  
[Changelog](https://github.com/ivpn/desktop-app/blob/master/CHANGELOG.md)  

## Install from IVPN Repository {#install}

### Ubuntu {#ubuntu}

{{< highlight shell >}}
# Add IVPN's GPG key
$ curl -fsSL https://repo.ivpn.net/stable/ubuntu/generic.gpg | gpg --dearmor > ~/ivpn-archive-keyring.gpg
$ sudo mv ~/ivpn-archive-keyring.gpg /usr/share/keyrings/ivpn-archive-keyring.gpg
# Add the IVPN repository
$ curl -fsSL https://repo.ivpn.net/stable/ubuntu/generic.list | sudo tee /etc/apt/sources.list.d/ivpn.list
# Update APT repo info
$ sudo apt-get update
# To install IVPN software (CLI and UI)
$ sudo apt-get install ivpn-ui
# To install only IVPN CLI
$ sudo apt-get install ivpn
{{< /highlight >}}

### Debian {#debian}

{{< highlight shell >}}
# Add IVPN's GPG key
$ curl -fsSL https://repo.ivpn.net/stable/debian/generic.gpg | gpg --dearmor > ~/ivpn-archive-keyring.gpg
$ sudo mv ~/ivpn-archive-keyring.gpg /usr/share/keyrings/ivpn-archive-keyring.gpg
# Add the IVPN repository
$ curl -fsSL https://repo.ivpn.net/stable/debian/generic.list | sudo tee /etc/apt/sources.list.d/ivpn.list
# Update APT repo info
$ sudo apt-get update
# To install IVPN software (CLI and UI)
$ sudo apt-get install ivpn-ui
# To install only IVPN CLI
$ sudo apt-get install ivpn
{{< /highlight >}}

### Mint {#mint}

{{< highlight shell >}}
# Add IVPN's GPG key
$ curl -fsSL https://repo.ivpn.net/stable/mint/generic.gpg | gpg --dearmor > ~/ivpn-archive-keyring.gpg
$ sudo mv ~/ivpn-archive-keyring.gpg /usr/share/keyrings/ivpn-archive-keyring.gpg
# Add the IVPN repository
$ curl -fsSL https://repo.ivpn.net/stable/mint/generic.list | sudo tee /etc/apt/sources.list.d/ivpn.list
# Update APT repo info
$ sudo apt-get update
# To install IVPN software (CLI and UI)
$ sudo apt-get install ivpn-ui
# To install only IVPN CLI
$ sudo apt-get install ivpn
{{< /highlight >}}

### Fedora {#fedora}

{{< highlight shell >}}
# Add the IVPN repository
$ sudo dnf config-manager --add-repo https://repo.ivpn.net/stable/fedora/generic/ivpn.repo
# To install IVPN software (CLI and UI)
$ sudo dnf install ivpn-ui
# To install only IVPN CLI
$ sudo dnf install ivpn
{{< /highlight >}}

### CentOS {#centos}

{{< highlight shell >}}
# Install Yum-utils
$ sudo yum install yum-utils
# Add the IVPN repository
$ sudo yum-config-manager --add-repo https://repo.ivpn.net/stable/centos/generic/ivpn.repo
# To install IVPN software (CLI and UI)
$ sudo yum install ivpn-ui
# To install only IVPN CLI
$ sudo yum install ivpn
# Required for CentOS 8
$ sudo yum install libXScrnSaver
{{< /highlight >}}

### Arch Linux {#arch}

AUR - ArchLinux User Repository. Can be used by distributions based on ArchLinux: (e.g. ArchLinux, Manjaro ...)

Base package: [ivpn](https://aur.archlinux.org/packages/ivpn/)  
UI package: [ivpn-ui](https://aur.archlinux.org/packages/ivpn-ui/)  

Using a AUR helper/Pacman wrapper  automates the installation process:

{{< highlight shell >}}
$ yay -S ivpn
$ yay -S ivpn-ui
{{< /highlight >}}

Note: Other AUR helper/Pacman wrapper utilities are available.

## Install from Binaries {#binaries}

### .DEB

[Base package](https://repo.ivpn.net/stable/pool/ivpn_3.4.0_amd64.deb)  
SHA256: fad328c95679c983d162d117e909c4c0b5eacd7b5dd54b8de7e1a1c4dbeca64c  

[UI package](https://repo.ivpn.net/stable/pool/ivpn-ui_3.4.0_amd64.deb)  
SHA256: 7e50c58ed16c5817e79b253e7b198a76c4660218a1e236598a59a288eaaf89e3  

### .RPM

[Base package](https://repo.ivpn.net/stable/pool/ivpn-3.4.0-1.x86_64.rpm)  
SHA256: 933c397078be24eba87cce63c3d49b507e62efb623a34f9349725461de719130  

[UI package](https://repo.ivpn.net/stable/pool/ivpn-ui-3.4.0-1.x86_64.rpm)  
SHA256: cf95c4e07912aa03c7596d56b31d323664efbf44469cc9fee54771800d96d1db  

## Install from Source Code {#source}

[Daemon + CLI](https://github.com/ivpn/desktop-app#compilation_linux_daemon)  
[UI](https://github.com/ivpn/desktop-app#compilation_linux_ui)  

## Useful Links {#useful-links}

If you prefer not to use the IVPN app please follow the relevant setup guide below.

If you are using OpenVPN download the latest OpenVPN [UDP](/releases/config/ivpn-openvpn-config.zip) or [TCP](/releases/config/ivpn-openvpn-config-tcp.zip) configuration files. In most cases, you want to use the UDP Protocol.

* [WireGuard using terminal](/setup/linux-wireguard/)
* [WireGuard using NetworkManager](/setup/linux-wireguard-netman/)
* [OpenVPN using terminal](/setup/linux-terminal/)
* [OpenVPN using NetworkManager](/setup/linux-netman/)
* [IPSec with IKEv2](/setup/linux-ipsec-with-ikev2/)
