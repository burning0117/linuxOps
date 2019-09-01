1:mac intellij git需要反复输入密码  
````
$ git config --global credential.helper store
````
2:部分检出  
````
$ git init  
$ git remote add -f origin http://git.xxxx.com/dev/IF.git   //添加远程仓库地址  
$ git config core.sparsecheckout true    //开启sparse checkout功能  
$ echo "IFClient/" >> .git/info/sparse-checkout   //将nginx-conf/目录写入到该文件中  
$ cat .git/info/sparse-checkout   //确认查看该文件内容  
$ git pull origin master //拉取远程master分支  
````
3:深度为1检出  

````
$ git clone --depth=1 http://git.xxxx.com/dev/IF.git
````
