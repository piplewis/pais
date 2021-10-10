# pais
Pip's Arch install script - work in porogress.
Does what I need, edit as you feel.

Forked Doc10's code and added what I needed too.

Boot off installation media, partition drive, connect to internet.

> pacman -Syy
> arch-chroot /mnt
> mount /dev/sda2 /mnt
> pacstrap /mnt base linux-lts git
> genfstab -U /mnt >> /mnt/etc/fstab

Put this together on a Windows machine unfotunately so after using git clone I use dos2unix to convert, easily done. I will get this sorted though.

> git clone https:/github.com/piplewis/pais
> pacman -S dos2unix
> dos2unix pais
> dos2unix paisdwm
> chmod +x pais
> chmod +x paisdwm
> ./pais
Not sure if needed but I reboot then and after reboot...
> ./paisdwm

