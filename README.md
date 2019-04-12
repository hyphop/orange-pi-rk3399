# orange-pi-rk3399

## dirs

+ dtb	
+ utils		

## compatable images

+ https://github.com/ayufan-rock64/linux-build/releases
+ https://github.com/ayufan-rock64/linux-build/releases/download/0.8.0rc9/bionic-minimal-rockpro64-0.8.0rc9-1120-armhf.img.xz
+ https://libreelec.tv/downloads_new/rockchip/
+ http://releases.libreelec.tv/LibreELEC-RK3399.arm-8.90.014-rockpro64.img.gz


## write image

```
cd images
wget https://github.com/ayufan-rock64/linux-build/releases/download/0.8.0rc9/bionic-minimal-rockpro64-0.8.0rc9-1120-armhf.img.xz
cd ..
sudo utils/image_write_xz images/bionic-minimal-rockpro64-0.8.0rc9-1120-armhf.img.xz

```
