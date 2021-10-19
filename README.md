# pais
Pip's Arch install script (UK based) - work in progress.

A simple install script to automate an arch and dwm installation with UK keyboard/language settings. 

Really only to help me as I often forget to install what is needed to meet my requirements.

Boot off installation media, partition drive, connect to internet.

pacstrap base, linux and git

Clone this repo

Change my username (piplewis) to yours, edit the bootloader section for either bios or uefi (I use bios for testing on a virtual machine and uefi on my linux box.)

Forked Doc10's code and added what I needed https://github.com/document10/scriptsrep.

Fixed the line endings issues with my version so no need for dos2unix :-)

The process for me after booting off arch install media ia as follows...

loadkeys uk

mkfs.ext4 /dev/sda2 -- I've already partitioned the drive for uefi. Change this to your partition/setup

iwctl -- wifi setup - may need rfkill unblock all

station wlan0 connect ******

password > ******

pacman -Syy

mount /dev/sda2 /mnt

pacstrap /mnt base vim git

genfstab -U /mnt >> /mnt/etc/fstab

arch-chroot /mnt

git clone https://github.com/piplewis/pais

chmod +x pais

chfmod +x paisdwm

./pais

REBOOT after pais script complete
Log in as new user then run paisdwm as root

> sudo ./paisdwm

Reboot again and bobs your uncle.
