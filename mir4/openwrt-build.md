Repo: https://github.com/ccat3z/openwrt

Branch: openwrt-23.05

Commit: 24fc912b0af1c41f91a838a862de3f0766e3c802

`.config`:

``` makefile
CONFIG_TARGET_ramips=y
CONFIG_TARGET_ramips_mt7621=y
CONFIG_TARGET_ramips_mt7621_DEVICE_xiaomi_mi-router-4=y
CONFIG_OPENSSL_ENGINE=y
CONFIG_OPENSSL_PREFER_CHACHA_OVER_GCM=y
CONFIG_OPENSSL_WITH_ASM=y
CONFIG_OPENSSL_WITH_CHACHA_POLY1305=y
CONFIG_OPENSSL_WITH_CMS=y
CONFIG_OPENSSL_WITH_DEPRECATED=y
CONFIG_OPENSSL_WITH_ERROR_MESSAGES=y
CONFIG_OPENSSL_WITH_IDEA=y
CONFIG_OPENSSL_WITH_MDC2=y
CONFIG_OPENSSL_WITH_PSK=y
CONFIG_OPENSSL_WITH_SEED=y
CONFIG_OPENSSL_WITH_SRP=y
CONFIG_OPENSSL_WITH_TLS13=y
CONFIG_OPENSSL_WITH_WHIRLPOOL=y
CONFIG_PACKAGE_cgi-io=y
CONFIG_PACKAGE_etherwake=y
CONFIG_PACKAGE_git=y
CONFIG_PACKAGE_iperf3=y
CONFIG_PACKAGE_kmod-tun=y
CONFIG_PACKAGE_libatomic=y
CONFIG_PACKAGE_libbz2=y
CONFIG_PACKAGE_libffi=y
CONFIG_PACKAGE_libgdbm=y
CONFIG_PACKAGE_libiperf3=y
CONFIG_PACKAGE_liblua=y
CONFIG_PACKAGE_liblucihttp=y
CONFIG_PACKAGE_liblucihttp-lua=y
CONFIG_PACKAGE_liblucihttp-ucode=y
CONFIG_PACKAGE_liblzma=y
CONFIG_PACKAGE_libncurses=y
CONFIG_PACKAGE_libopenssl=y
CONFIG_PACKAGE_libpython3=y
CONFIG_PACKAGE_libreadline=y
CONFIG_PACKAGE_librt=y
CONFIG_PACKAGE_libsqlite3=y
CONFIG_PACKAGE_libubus-lua=y
CONFIG_PACKAGE_libuuid=y
CONFIG_PACKAGE_lua=y
CONFIG_PACKAGE_luci=y
CONFIG_PACKAGE_luci-app-commands=y
CONFIG_PACKAGE_luci-app-firewall=y
CONFIG_PACKAGE_luci-app-opkg=y
CONFIG_PACKAGE_luci-app-radicale2=y
CONFIG_PACKAGE_luci-app-wol=y
CONFIG_PACKAGE_luci-base=y
CONFIG_PACKAGE_luci-compat=y
CONFIG_PACKAGE_luci-lib-base=y
CONFIG_PACKAGE_luci-lib-ip=y
CONFIG_PACKAGE_luci-lib-jsonc=y
CONFIG_PACKAGE_luci-lib-nixio=y
CONFIG_PACKAGE_luci-light=y
CONFIG_PACKAGE_luci-lua-runtime=y
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
CONFIG_PACKAGE_python3=y
CONFIG_PACKAGE_python3-asyncio=y
CONFIG_PACKAGE_python3-base=y
CONFIG_PACKAGE_python3-cgi=y
CONFIG_PACKAGE_python3-cgitb=y
CONFIG_PACKAGE_python3-codecs=y
CONFIG_PACKAGE_python3-ctypes=y
CONFIG_PACKAGE_python3-dateutil=y
CONFIG_PACKAGE_python3-dbm=y
CONFIG_PACKAGE_python3-decimal=y
CONFIG_PACKAGE_python3-distutils=y
CONFIG_PACKAGE_python3-email=y
CONFIG_PACKAGE_python3-light=y
CONFIG_PACKAGE_python3-logging=y
CONFIG_PACKAGE_python3-lzma=y
CONFIG_PACKAGE_python3-multiprocessing=y
CONFIG_PACKAGE_python3-ncurses=y
CONFIG_PACKAGE_python3-openssl=y
CONFIG_PACKAGE_python3-passlib=y
CONFIG_PACKAGE_python3-pkg-resources=y
CONFIG_PACKAGE_python3-pydoc=y
CONFIG_PACKAGE_python3-readline=y
CONFIG_PACKAGE_python3-setuptools=y
CONFIG_PACKAGE_python3-six=y
CONFIG_PACKAGE_python3-sqlite3=y
CONFIG_PACKAGE_python3-unittest=y
CONFIG_PACKAGE_python3-urllib=y
CONFIG_PACKAGE_python3-uuid=y
CONFIG_PACKAGE_python3-vobject=y
CONFIG_PACKAGE_python3-xml=y
CONFIG_PACKAGE_radicale2=y
CONFIG_PACKAGE_rpcd=y
CONFIG_PACKAGE_rpcd-mod-file=y
CONFIG_PACKAGE_rpcd-mod-iwinfo=y
CONFIG_PACKAGE_rpcd-mod-luci=y
CONFIG_PACKAGE_rpcd-mod-rad2-enc=y
CONFIG_PACKAGE_rpcd-mod-rrdns=y
CONFIG_PACKAGE_rpcd-mod-ucode=y
CONFIG_PACKAGE_shadow-common=y
CONFIG_PACKAGE_shadow-su=y
CONFIG_PACKAGE_shadow-utils=y
CONFIG_PACKAGE_swconfig=y
CONFIG_PACKAGE_terminfo=y
# CONFIG_PACKAGE_uboot-envtools is not set
CONFIG_PACKAGE_ucode-mod-html=y
CONFIG_PACKAGE_ucode-mod-lua=y
CONFIG_PACKAGE_ucode-mod-math=y
CONFIG_PACKAGE_uhttpd=y
CONFIG_PACKAGE_uhttpd-mod-ubus=y
CONFIG_PACKAGE_zlib=y
CONFIG_SQLITE3_COLUMN_METADATA=y
CONFIG_SQLITE3_DYNAMIC_EXTENSIONS=y
CONFIG_SQLITE3_FTS3=y
CONFIG_SQLITE3_FTS4=y
CONFIG_SQLITE3_FTS5=y
CONFIG_SQLITE3_RTREE=y
# CONFIG_TARGET_ROOTFS_INITRAMFS is not set
# CONFIG_PACKAGE_shadow-chage is not set
# CONFIG_PACKAGE_shadow-chfn is not set
# CONFIG_PACKAGE_shadow-chgpasswd is not set
# CONFIG_PACKAGE_shadow-chpasswd is not set
# CONFIG_PACKAGE_shadow-chsh is not set
# CONFIG_PACKAGE_shadow-expiry is not set
# CONFIG_PACKAGE_shadow-faillog is not set
# CONFIG_PACKAGE_shadow-gpasswd is not set
# CONFIG_PACKAGE_shadow-groupadd is not set
# CONFIG_PACKAGE_shadow-groupdel is not set
# CONFIG_PACKAGE_shadow-groupmems is not set
# CONFIG_PACKAGE_shadow-groupmod is not set
# CONFIG_PACKAGE_shadow-groups is not set
# CONFIG_PACKAGE_shadow-grpck is not set
# CONFIG_PACKAGE_shadow-grpconv is not set
# CONFIG_PACKAGE_shadow-grpunconv is not set
# CONFIG_PACKAGE_shadow-lastlog is not set
# CONFIG_PACKAGE_shadow-login is not set
# CONFIG_PACKAGE_shadow-logoutd is not set
# CONFIG_PACKAGE_shadow-newgidmap is not set
# CONFIG_PACKAGE_shadow-newgrp is not set
# CONFIG_PACKAGE_shadow-newuidmap is not set
# CONFIG_PACKAGE_shadow-newusers is not set
# CONFIG_PACKAGE_shadow-nologin is not set
# CONFIG_PACKAGE_shadow-passwd is not set
# CONFIG_PACKAGE_shadow-pwck is not set
# CONFIG_PACKAGE_shadow-pwconv is not set
# CONFIG_PACKAGE_shadow-pwunconv is not set
# CONFIG_PACKAGE_shadow-useradd is not set
# CONFIG_PACKAGE_shadow-userdel is not set
# CONFIG_PACKAGE_shadow-usermod is not set
# CONFIG_PACKAGE_shadow-vipw is not set
# CONFIG_shadow-all is not set
```