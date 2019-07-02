# A OpenWRT firmware based on Lean's source
### Welcome to my Telegram Group: [@openwrt\_discuss](https://t.me/openwrt_discuss).

# Tips
You'd better not use **root** to make it, or you may be not able to use.<br/>
Default username is **root** and password is **password**, login address: 192.168.1.1.

# How to make it
## OS require
Ubuntu 14.04 LTS x86\_64 (16.04 LTS is OK)<br>
At least 2G RAM & 2 CPU Cores<br>
At least 25G HDD<br>

## Install the necessary software
```bash
sudo apt-get -y install build-essential asciidoc binutils bzip2 gawk gettext git libncurses5-dev libz-dev patch unzip zlib1g-dev lib32gcc1 libc6-dev-i386 subversion flex uglifyjs git-core gcc-multilib p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev xmlto qemu-utils upx libelf-dev autoconf automake libtool autopoint
```

## Clone the source
```bash
git clone https://github.com/shell-script/lede && cd lede
./scripts/feeds update -a && ./scripts/feeds install -a
```

## Configure your firmware
```bash
make menuconfig
```

## Make it
```bash
make -j1 V=s
```

# Origin source
### Based on: [coolsnowwolf/lede](https://github.com/coolsnowwolf/lede).<br/>
luci-app-koolproxy source: [openwrt-develop/luci-app-koolproxy](https://github.com/openwrt-develop/luci-app-koolproxy).<br/>
luci-app-udp2raw source: [sensec/luci-app-udp2raw](https://github.com/sensec/luci-app-udp2raw).<br/>
luci-app-haproxy source: [AlexZhuo/luci-app-haproxy-tcp](https://github.com/AlexZhuo/luci-app-haproxy-tcp).<br/>
luci-app-udpspeederv2 source: [haodong/luci-app-speederv2](https://github.com/haodong/luci-app-speederv2).<br/>
luci-theme-netgearv2 source: [tracemouse/luci-theme-netgear](https://github.com/tracemouse/luci-theme-netgear).

# License
### [GPL v3](https://www.gnu.org/licenses/gpl-3.0.html).