# Day1：安装环境 for Mac

## - JDK安装

1. 前往 https://www.oracle.com/java/technologies/java-se-glance.html下载JDK并且安装

   <img src="image-20210809140234544.png" alt="image-20210809140234544" style="zoom:50%;" />



2. 环境变量设置

   前往MacBook 终端，修改环境

   <img src="image-20210809140318620.png" alt="image-20210809140318620" style="zoom:50%;" />



3. 验证安装配置结果
   运行Terminal，执行java -version 命令查看 

   显示以下内容为成功：

   <img src="image-20210809140505667.png" alt="image-20210809140505667" style="zoom:50%;" />

   ## - IDE安装

   1. 前往https://www.eclipse.org 下载 eclipse installer for mac

      

   

<img src="image-20210809140628874.png" alt="image-20210809140628874" style="zoom:50%;" />



2. 打开 eclipse，安装Eclipse IDE for Java Developer

   <img src="image-20210809140648700.png" alt="image-20210809140648700" style="zoom: 50%;" />



3.  IDE启动优化：

   下载Spring Tool Suite 4 到

   /Applications/SpringToolSuite4.app/Contents/Eclipse/SpringToolSuite4.ini

   编辑 SpringToolSuite4.ini，更新以下内容：

   -Xms2048m
   -Xmx2048m
   -XX:+UseG1GC
   -XX:MaxGCPauseMillis=100 
   -XX:GCPauseIntervalMillis=500
   -XX:MetaspaceSize=512M 
   -Xverify:none
   -XX:+DisableExplicitGC
   -XX:-UseBiasedLocking

   <img src="image-20210809140707761.png" alt="image-20210809140707761" style="zoom:50%;" />

   

   

   ## - Git 安装

   1. 前往 https://git-scm.com/download/mac下载git 客户端

   2. 前往https://brew.sh查看安装homebrew需求
   
   3. 在terminal中输入 /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)" 安装homebrew
   
   4. 在terminal中输入以下代码安装git：
   
      1）、brew install git
      2）、brew install git-gui

   
   
   ## -  Git与Github链接

   1. 设置SSH keys 将git与github链接

      ```shell
      $ ssh-keygen -t ed25519 -C "lexieli577@163.com"
      ```
   
   
   
   2. 复制SSH pubic key 到 click board
   
      ```shell
      $ pbcopy < ~/.ssh/id_ed25519.pub
      # Copies the contents of the id_ed25519.pub file to your clipboard
      ```
   
   3. 去profile，setting查看SSH，添加 SSH keys
   4.  git clone SSH

