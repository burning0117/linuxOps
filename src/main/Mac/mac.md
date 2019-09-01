1:mac没有了任何来源的选项  
    sudo spctl --master-disable
2:Mac显示.开头的文件
	defaults write com.apple.Finder AppleShowAllFiles YES      
	killall Finder    
3:brew安装的软件在Application文件夹中添加快捷方式  
    ln -Fs `find /usr/local -name "MacVim.app"` /Applications/MacVim.app  
4：mac挂载ntf格式硬盘  
    1：列出硬盘名称    
	    diskutil list    
    2：编辑配置文件,在文件中加入一行配置文件，其中Elements是磁盘名称     
	    sudo vim /etc/fstab    
        LABEL=Elements none ntfs rw,auto,nobrowse    