BBR安装教程
使用 SSH 客户端连接你的服务器，运行以下脚本。

wget -N --no-check-certificate "https://gist.github.com/zeruns/a0ec603f20d1b86de6a774a8ba27588f/raw/4f9957ae23f5efb2bb7c57a198ae2cffebfb1c56/tcp.sh" && chmod +x tcp.sh && ./tcp.sh



安装xray
CentOS系统请输入 
yum install -y curl

Ubuntu/Debian系统请输入
apt install -y curl

bash <(curl -Ls https://github.com/izma669/soft/blob/master/vps/xray.sh)
