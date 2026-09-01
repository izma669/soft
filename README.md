19.07

cd && git clone -b 19.07 https://github.com/izma669/Lienol-openwrt 19.07 && cd 19.07 && ./scripts/feeds update -a && ./scripts/feeds install -a && ./scripts/feeds install -a && make menuconfig

18.06

cd && git clone -b openwrt-18.06 https://github.com/izma669/immortalwrt-openwrt 18.06 && cd 18.06 && ./scripts/feeds update -a && ./scripts/feeds install -a && ./scripts/feeds install -a && make menuconfig

21.02

cd && git clone -b openwrt-21.02 https://github.com/izma669/immortalwrt-openwrt 21.02 && cd 21.02 && ./scripts/feeds update -a && ./scripts/feeds install -a && ./scripts/feeds install -a && make menuconfig

25.12

cd && git clone -b openwrt-25.12 https://github.com/izma669/immortalwrt-openwrt 25.12 && cd 25.12 && ./scripts/feeds update -a && ./scripts/feeds install -a && ./scripts/feeds install -a && make menuconfig

lede

cd && git clone -b master https://github.com/izma669/lede-openwrt lede && cd lede && ./scripts/feeds update -a && ./scripts/feeds install -a && ./scripts/feeds install -a && make menuconfig

下载DLL库，全核心编译

make download V=s -j8 && make V=s -j$(nproc)


删除配置

rm -rf .config

清理方法（由轻到重）

清理临时文件 
rm -rf ./tmp
删除编译过程中的临时文件。这是最轻量的清理，可以快速尝试。

清理编译产物 
make clean
清除已生成的固件镜像和根文件系统，但保留已编译好的工具链和软件源码。适用于发现配置错误后重新编译，能节省一些时间。

深度清理 
make dirclean
在make clean的基础上，还会删除所有已解压的软件源码和内核源码。这会强制系统在下次编译时重新下载和解压所有软件包，能有效清除大部分因依赖关系残留导致的体积问题。

完全重置 
make distclean
这是最彻底的清理方法。它会删除所有内容，包括已下载的源码包、编译工具链，以及你的编译配置文件（.config）。效果等同于将源码目录恢复到刚克隆时的状态
