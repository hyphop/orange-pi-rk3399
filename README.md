# orange-pi-rk3399

## dirs

+ dtb	
+ utils		

## compatable images

+ https://github.com/ayufan-rock64/linux-build/releases
+ https://github.com/ayufan-rock64/linux-build/releases/download/0.8.0rc9/bionic-minimal-rockpro64-0.8.0rc9-1120-armhf.img.xz
+ https://libreelec.tv/downloads_new/rockchip/
+ http://releases.libreelec.tv/LibreELEC-RK3399.arm-8.90.014-rockpro64.img.gz


## write image bionic-minimal-rockpro64-0.8.0rc9-1120-armhf

NOTE: ethernet 1Gbit buggy! use 100Mbit only
NOTE: wrong dtb / audio / usb 2.0 
NOTE: usb2.0 ports not work only USB Type C
NOTE: power BTN work but same as reboot not suspend

```
cd images
wget https://github.com/ayufan-rock64/linux-build/releases/download/0.8.0rc9/bionic-minimal-rockpro64-0.8.0rc9-1120-armhf.img.xz
cd ..
sudo utils/image_write_xz images/bionic-minimal-rockpro64-0.8.0rc9-1120-armhf.img.xz

utils/serial_rk

# login rock64:rock64

sudo apt install bash-completion
sudo bash

echo PermitRootLogin yes >> /etc/ssh/sshd_config
echo PubkeyAuthentication yes >> /etc/ssh/sshd_config
service ssh restart

# change root passwork
passwd

## now we can ssh login as root
## 
## on host
## ssh-copy-id -i ~/.ssh/id_ecdsa.pub root@rock
## ssh root@rock

install_desktop.sh i3
## i3 pango font buggy

## on host
## scp root@rock:/boot/dtbs/4.4.167-1169-rockchip-ayufan-g3cde5c624c9c/rockchip/rk3399-rockpro64.dtb dtb/

sudo apt-get install glmark2-es2

rock64@rockpro64:~$ DISPLAY=:0 glmark2-es2
rock64@rockpro64:~$ DISPLAY=:0 gl4es glmark2

## gpu test OK

# https://www.youtube.com/watch?v=h6yrcdAlRWY
youtube-dl https://www.youtube.com/watch?v=h6yrcdAlRWY
DISPLAY=:0 gl4es mpv https://www.youtube.com/watch?v=h6yrcdAlRWY
DISPLAY=:0 gl4es ffplay its\ the\ end\ of\ the\ noise-h6yrcdAlRWY.mp4

## resize root fs on HOST

# e2fsck -f /dev/mmcblk0p7
# resize2fs /dev/mmcblk0p7 4G
# fdisk /dev/mmcblk0
# e2fsck -f /dev/mmcblk0p7
## OK now 4G only

## WIFI fix

curl https://raw.githubusercontent.com/hyphop/orange-pi-rk3399/master/fw/fw_download_wifi | sh -


```
