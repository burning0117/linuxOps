1:intellij窗口过宽无法显示  
    删掉 workspace.xml中的ProjectFrameBounds
2:远程调试  
    启动命令：java -Xdebug -Xnoagent -Djava.compiler=NONE -Xrunjdwp:transport=dt_socket,address=5005,server=y,suspend=n -jar myProject.jar   
    intellij +remote  
     
