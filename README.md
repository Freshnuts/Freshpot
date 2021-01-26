# FreshPot
SSH Honeypot

Equipment
---------

0. DMZ (optional)
1. Raspberry Pi
2. Internet Connection


Setup Guide
-----------

Contents

0. Setup DMZ/Port Forwarding (Optional, for public facing)
1. Raspbian Installation
2. SSH/SSHd installation
3. SSH/SSHd Config
4. Users
5. Log Intruder Attempts/Successes



Steps
-----

1. Raspbian Setup

:# sudo dd bs=4M if=2020-12-02-raspios-buster-armhf-full.img of=/dev/mmcblk0p1 conv=fsync
:# 1557  sudo fdisk /dev/mmcblk0
:# 1558  sudo mkfs.ext4  -L honeypot /dev/mmcblk0p1


2. Install SSH

:# sudo apt-get install ssh


3. SSHd Server Config

- PasswordAuthentication yes
- PermitEmptyPasswords yes
- PermitRootLogin yes
- (Everything else default)

4.  Create/Configure Users

root:toor<br>
pi:honey<br>
guest:[no password]<br>

5. Logging & Archiving Activity:

- Try 3 different honeypot frameworks
	- Malware Collector
	- Snort - Detect Attempts & Established Connections
	- 
- Obtain Intruder information
- Create a logging solution for SSH service.
