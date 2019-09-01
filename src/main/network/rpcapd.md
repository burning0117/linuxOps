centos下wireshark远程抓取网络包  
1：下载编译安装  
yum install glibc-static  
wget http://www.winpcap.org/install/bin/WpcapSrc_4_1_2.zip  
unzip WpcapSrc_4_1_3.zip  
cd winpcap/wpcap/libpcap  
chmod +x configure runlex.sh  
CFLAGS=-static ./configure  
make  
cd rpcapd  
make  

2：配置防火墙 iptable规则  
iptables -A INPUT -p tcp --dport 22 -j ACCEPT  
iptables -A OUTPUT -p tcp --sport 22 -j ACCEPT  

3：以指定端口启动  
./rpcapd -n -p 2002  

4：安装lsof  
yum install lsof  
查看指定端口   
lsof -i:8080  


