
rock64
rock64

root@rockpro64:~# uname -a
Linux rockpro64 4.4.167-1169-rockchip-ayufan-g3cde5c624c9c #1 SMP Thu Apr 4 19:38:24 UTC 2019 aarch64 aarch64 aarch64 GNU/Linux

root@rockpro64:~# cat /proc/cmdline 
earlycon=uart8250,mmio32,0xff1a0000 swiotlb=1 rw panic=10 init=/sbin/init coherent_pool=1M ethaddr=0e:13:e8:96:73:23 eth1addr= serial=347eb8075d3213f cgroup_enable=cpuset cgroup_memory=1 cgroup_enable=memory swapaccount=1 root=LABEL=linux-root rootwait rootfstype=ext4

root@rockpro64:~# lsmod
Module                  Size  Used by
lzo                    16384  36
zram                   24576  6
bcmdhd               1220608  0
midgard_kbase         638976  0
dw_hdmi_i2s_audio      16384  0
rockchip_saradc        16384  0
ip_tables              24576  0
x_tables               32768  1 ip_tables
autofs4                40960  2
uas                    20480  0
usb_storage            65536  1 uas
phy_rockchip_pcie      16384  0




