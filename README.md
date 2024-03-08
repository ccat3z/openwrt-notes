# Mi Wifi Router 3a

## Prepare for Flashing Custom ROM

1. Enable root access.

   ```
   git clone https://github.com/acecilia/OpenWRTInvasion.git --depth 1
   cd OpenWRTInvasion
   docker build -t openwrtinvasion .
   docker run --rm --network host -it openwrtinvasion
   ```

   This script will start frp on port 21 and ssh on port 22.
   See also [OpenWRTInvasion](https://github.com/acecilia/OpenWRTInvasion).

1. Backup eeprom. eeprom block can be found in `/proc/mtd`.
   The dev named Factory is eeprom.

   ```
   dd if=/dev/mtd4 of=/tmp/eeprom.bin
   ```

   Then backup `/tmp/eeprom.bin` via ftp.

1. Flash [breed](https://www.right.com.cn/forum/thread-161906-1-1.html) bootloader.

   1. Download [breed-mt7628-hiwifi-hc5661a.bin](https://breed.hackpascal.net/breed-mt7628-hiwifi-hc5661a.bin) and copy to router.
   2. Flash bootloader: `mtd write /tmp/breed.bin Bootloader`
   3. Reboot. Breed web ui can be accessed on [http://192.168.1.1](http://192.168.1.1).

1. Flash eeprom in breed web ui.

## Build and Flash OpenWrt

Download sources and update feeds:

```
git clone https://github.com/ccat3z/openwrt-xiaomi-router-3a.git --depth 1
cd openwrt
docker run --rm -ti -v "$PWD:/src" --workdir /src openwrt/imagebuilder
./scripts/feeds update -a
./scripts/feeds install -a
```

Config openwrt by `make menuconfig`. Here is an example `.config`:

``` Makefile
CONFIG_TARGET_ramips=y
CONFIG_TARGET_ramips_mt76x8=y
CONFIG_TARGET_ramips_mt76x8_DEVICE_xiaomi_mi-router-3a=y
CONFIG_PACKAGE_cgi-io=y
CONFIG_PACKAGE_etherwake=y
CONFIG_PACKAGE_iperf3=y
CONFIG_PACKAGE_kmod-tun=y
CONFIG_PACKAGE_libiperf3=y
CONFIG_PACKAGE_liblucihttp=y
CONFIG_PACKAGE_liblucihttp-ucode=y
CONFIG_PACKAGE_luci=y
CONFIG_PACKAGE_luci-app-firewall=y
CONFIG_PACKAGE_luci-app-opkg=y
CONFIG_PACKAGE_luci-app-wol=y
CONFIG_PACKAGE_luci-base=y
CONFIG_PACKAGE_luci-light=y
CONFIG_PACKAGE_luci-mod-admin-full=y
CONFIG_PACKAGE_luci-mod-network=y
CONFIG_PACKAGE_luci-mod-status=y
CONFIG_PACKAGE_luci-mod-system=y
CONFIG_PACKAGE_luci-proto-ipv6=y
CONFIG_PACKAGE_luci-proto-nebula=y
CONFIG_PACKAGE_luci-proto-ppp=y
CONFIG_PACKAGE_luci-theme-bootstrap=y
CONFIG_PACKAGE_nebula=y
CONFIG_PACKAGE_nebula-proto=y
CONFIG_PACKAGE_rpcd=y
CONFIG_PACKAGE_rpcd-mod-file=y
CONFIG_PACKAGE_rpcd-mod-iwinfo=y
CONFIG_PACKAGE_rpcd-mod-luci=y
CONFIG_PACKAGE_rpcd-mod-rrdns=y
CONFIG_PACKAGE_rpcd-mod-ucode=y
CONFIG_PACKAGE_ucode-mod-html=y
CONFIG_PACKAGE_ucode-mod-math=y
CONFIG_PACKAGE_uhttpd=y
CONFIG_PACKAGE_uhttpd-mod-ubus=y
# CONFIG_TARGET_ROOTFS_INITRAMFS is not set
```

Build image:

```
# Build the firmware image
make -j$(nproc) defconfig download clean world
```

The firmware image will be save in `openwrt/bin/targets/ramips/mt76x8/openwrt-ramips-mt76x8-xiaomi_mi-router-3a-squashfs-sysupgrade.bin`.
Upload it to breed.
OpenWRT should work after an automatic reboot.

## References

* [OpenWRTInvasion](https://github.com/acecilia/OpenWRTInvasion)
* [小米路由器3A（R3A）&3C（R3C）软件root，刷入Openwrt教程](https://www.right.com.cn/forum/thread-5459952-1-1.html)
* [【小渔】无需拆机或u盘！ssh小米路由3G 3a 3c 4c 4a百兆和千兆版本等开启 telnet 刷breed](https://yuos.top/d/39-xiao-yu-wu-xu-chai-ji-huo-upan-sshxiao-mi-lu-you-3g-3a-3c-4c-4abai-zhao-he-qian-zhao-ban-ben-deng-kai-qi-telnet-shua-breed)
* [OpenWRT Build system usage](https://openwrt.org/docs/guide-developer/toolchain/use-buildsystem)
* [yuos openwrt](https://github.com/yuos-bit/AutoBuild-OpenWrt)
