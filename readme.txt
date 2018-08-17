Git is a version control system.
Git is free software.

$ mkdir learngit   
#建一个文件夹
$ cd learngit
#cd 到这个文件夹里
$ pwd
#显示当前目录

#通过git init命令把这个目录变成Git可以管理的仓库：
$ git init

#用命令git add告诉Git，把文件添加到仓库：
$ git add readme.txt

用命令git commit告诉Git，把文件提交到仓库：
$ git commit -m "wrote a readme file"
[master (root-commit) eaadf4e] wrote a readme file
1 file changed, 2 insertions(+)
create mode 100644 readme.txt

运行git status命令看看结果

#查看不同
$ git diff readme.txt

修改完成后继续 git add 添加到仓库

#git log命令显示从最近到最远的提交日志
 git log --pretty=oneline
 一大串类似1094adb...的是commit id（版本号），和SVN不一样
 Git的commit id不是1，2，3……递增的数字
 而是一个SHA1计算出来的一个非常大的数字，用十六进制表示.
 
 #退回上一版本
 git reset --hard HEAD^
 
 #跳到某一版本
 git reset --hard (commit id 版本号 见 git log指令)
 
 #查看命令历史
 git reflog
 
#rm命令,直接删除
$ rm test.txt

#git rm 类似git add 从版本库中删除
git rm test.txt

#直接用notepad++打开文本文件，将文本文件默认打开文件设置成NOTEPAD++
start readme.txt

#远程仓库
1、创建SSH KEY 
$ ssh-keygen -t rsa -C "youremail@example.com（github注册邮件地址）"
在目录下打开 id_rsa.pub 复制其中的SSH Key 添加到github账户的SSH Keys页面。
2、先在github新建git仓库
3、在本地仓库运行 git remote add origin git@github.com:(github账户名）/仓库名.git
4、git push -u origin master(把本地库内容推送到远程库)
5、以后推送只需要输入 git push origin master

#git clone 远程仓库克隆
git clone git@github.com:u-lee-hsu/Hello-world.git
将远程仓库克隆到本地

查看分支：git branch

创建分支：git branch <name>

切换分支：git checkout <name>

创建+切换分支：git checkout -b <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>

<<<<<<< HEAD
git branch test master
=======
branchtest
>>>>>>> branchtest
