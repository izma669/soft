19.07

cd && git clone -b 19.07 https://github.com/izma669/Lienol-openwrt 19.07 && cd 19.07 && ./scripts/feeds update -a && ./scripts/feeds install -a && ./scripts/feeds install -a && make menuconfig

21.02

cd && git clone -b openwrt-21.02 https://github.com/izma669/immortalwrt-openwrt 21.02 && cd 21.02 && ./scripts/feeds update -a && ./scripts/feeds install -a && ./scripts/feeds install -a && make menuconfig

25.12

cd && git clone -b openwrt-25.12 https://github.com/izma669/immortalwrt-openwrt 25.12 && cd 25.12 && ./scripts/feeds update -a && ./scripts/feeds install -a && ./scripts/feeds install -a && make menuconfig


下载DLL库，全核心编译

make download V=s -j8 && make V=s -j$(nproc)


删除配置

rm -rf .config
