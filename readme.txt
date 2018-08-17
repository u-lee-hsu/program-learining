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