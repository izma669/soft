debian 9k可用源
deb http://archive.debian.org/debian/ stretch main contrib non-free
deb-src http://archive.debian.org/debian/ stretch main contrib non-free
deb http://archive.debian.org/debian-security/ stretch/updates main contrib non-free
deb-src http://archive.debian.org/debian-security/ stretch/updates main contrib non-free
deb http://archive.debian.org/debian/ stretch-backports main contrib non-free

修复损坏的包
sudo apt -f install
或
apt --fix-broken install

清理无用的包
sudo pat autoremove
或
sudo apt autocliean

修改DNS
sudo nano /etc/resolv.conf


BBR安装教程
使用 SSH 客户端连接你的服务器，运行以下脚本。

wget -N --no-check-certificate "https://gist.github.com/zeruns/a0ec603f20d1b86de6a774a8ba27588f/raw/4f9957ae23f5efb2bb7c57a198ae2cffebfb1c56/tcp.sh" && chmod +x tcp.sh && ./tcp.sh



安装xray
CentOS系统请输入 
yum install -y curl

Ubuntu/Debian系统请输入
apt install -y curl

bash <(curl -s -L https://raw.githubusercontent.com/xyz690/v2ray/master/onestep.sh)
