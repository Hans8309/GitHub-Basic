# GitHub-Basic
GitHub 学习笔记
2019年7月开始学习 Git，GitHub，搜了一些大神的指南，都有点不得要领。
直到看到这个入门级别的文章，才基本上弄明白.    
GitHub教程 Git Bash详细教程（上）  https://blog.csdn.net/qq_36667170/article/details/79085301  
官方英文帮助，Set up Git  https://help.github.com/en/articles/set-up-git     

---------------------------------------------------------------------------------------------

1. 下载Git 软件，  https://git-scm.com/ ， windows下载  Git for Windows Setup的64位版本  
    64-bit Git for Windows Setup.    
2. 安装Git 软件, 全部按照默认选项安装.
3. 可选项，下载 GitHub Desktop， https://desktop.github.com/    
4. 在任意空白地方，点击鼠标右键，选择菜单" Git Bash Here"，打开Git Bash窗体，  
   然后输入你的GitHub用户名和邮箱：    
   git config --global user.name "Your Name"（注意前边是“- -global”，有两个横线）  
   git config --global user.email "email@example.com"     
   不放心的话，用下面两行命令验证确认用户名和邮箱   
   git config --global user.name  
   git config --global user.email  
5. 创建SSH Key （如果你电脑上有了，你就可以直接跳过这一步）  
   输入  $ ~/.ssh   查看电脑上SSH Key的存放目录，默认目录是本地用户文件夹，  
   打开看看有一个目录 .ssh,打开这个文件夹，看看里边是否有SSH Key文件.  
   首先创建一个SSH，在Git Bash中输入：       
   $ ssh-keygen -t rsa -C "你的邮箱"
   然后连续按3次回车确认，不要输入任何字符  
   这时看到目录 .ssh 中已经生成2个文件， id_ras, id_rsa.pub   
6. 添加SSH Key到GitHub   
   首先打开Github网页, ........    
7. 测试一下该SSH key   
   在git Bash 中输入以下代码:  
   $ ssh -T git@github.com   
   注意是git@github.com，不是你的邮箱。  
   
8. 克隆一个远程库到本地  
    打开一个本地目录，例如d:\code，在空白处点击右键菜单，选择菜单" Git Bash Here"，打开Git Bash窗体.
    执行命令： $ git clone git@github.com:Hans8309/LearnGolang.git
    将会新建一个和远程库同名的目录，例如LearnGolang，并将项目下载到本地库目录中，关闭Git Bash窗体.
    打开本地库，就会看到文件夹里有了克隆下载的库文件，还有个隐藏目录  .git 
    在本地库目录中，在空白处点击右键菜单，选择菜单" Git Bash Here"，重新打开Git Bash窗体
    执行$ git remote -v，就会出现2行提示如下，说明库已经连接正常，可以pull和push了
        origin  git@github.com:Hans8309/LearnGolang.git (fetch)
        origin  git@github.com:Hans8309/LearnGolang.git (push)
           
9. 交互式模拟练习git的网站：  https://learngitbranching.js.org/   


