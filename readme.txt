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
