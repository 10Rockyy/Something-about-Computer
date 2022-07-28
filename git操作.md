### 电脑Git初始化

1. 电脑安装Git

2. 配置用户信息：

   ```
   $ git config --global user.name "runoob"
   $ git config --global user.email test@runoob.com
   ```

   * 用户名和邮箱只是起“显示”作用



### [Github](https://www.runoob.com/git/git-remote-repo.html)

1. 生成SSH Key：

   ```
   $ ssh-keygen -t rsa -C "youremail@example.com"
   ```

   * 后面的 **your_email@youremail.com** 改为在 Github 上注册的邮箱，之后会要求确认路径和输入密码，我们这使用默认的一路回车就行。成功的话会在 **~/** 下生成 **.ssh** 文件夹，进去，打开 **id_rsa.pub**，复制里面的 **key**。

   * Winsows系统打开.ssh文件夹可能需要打开“显示隐藏文件”

     

2. 打开Github，添加SSH Key

   * 建议将SSH的Title设置为易辨识的机器名称

3. 创建GitHub新仓库

4. 创建本地仓库

   ```
   git init 
   git add README.md
   git commit -m "添加 README.md 文件" 
   ```

5. 提交到Github

   ```
   git remote add origin git@github.com:Rockyyyyyyyyyy/Something-about-Computer.git
   #origin会成为远程仓库的名字，可以自行修改
   git push -u origin master
   
   #如果git push之后报错，则先设定分支
   #git branch -M main
   #git push -u origin master
   ```

6. 查看当地文件夹有哪些远程仓库

   ```
   git remote -v
   
   #删除远程仓库（例如删除origin）
   #git remote rm origin
   ```
   
   