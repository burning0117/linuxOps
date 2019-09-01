# mac+virtualBox+centos7
1:virtualBox preference->Network->增加Net Networks和Host-only Networks
2:centos7->Network->Adapter1->NAT,Adapter2->Bridged Adapter,Adapter2->Host-only Adapter
  该打勾打勾,下拉选合适的

#man手册又臭又长，推荐使用tldr,常用例子加注释，非常好用


# 查找历史输入命令
```
history | grep ''
```

find[PATH][option][action]

#在根目录下查找指定名称文件
find / -name ""

```
 #du和df的区别是du可以加文件深度，信息少，df指定文件夹底下所有文件
 
 #深度为1的文件和文件夹大小
 du / --max-depth=1   
 #人类可读的/目录下所有文件和文件夹的大小
 df / -h
```
