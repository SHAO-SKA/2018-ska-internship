#git learning

--by Cheqiu Lyu, 20180812

https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000

##基本操作：

运行git bash,命令git到达git的目录下
通过git init命令把这个目录变成Git可以管理的仓库：
git add <file> 加到仓库
git commit -m <message>
git status查看修改状态
git diff可以查看修改内容。
git log命令显示从最近到最远的提交日志

##回退与修改版本：

git log --pretty=oneline回退到上一个版本
用git log可以查看提交历史，以便确定要回退到哪个版本。
用git reflog查看命令历史，以便确定要回到未来的哪个版本
git reset --hard “版本号”
提交后，用git diff HEAD -- readme.txt命令可以查看工作区和版本库里面最新版本的区别
git checkout -- file丢弃工作区的修改
git reset HEAD <file>可以把暂存区的修改撤销，重新放回工作区

##删除文件：

确定删除时，用命令git rm删掉，并且git commit
git checkout -- 把误删的文件恢复到最新版本（在上一步之前）

创建SSH Key，ssh-keygen -t rsa -C "youremail@example.com"
用户主目录里找到.ssh目录，里面有id_rsa和id_rsa.pub

连接好github之后
只要本地作了提交，通过命令git push origin master
要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；
关联后，使用命令git push -u origin master第一次推送master分支的所有内容；

##添加到远程：三步add commit push

从远程库克隆：git clone git@github.com:account/repositoryname.git
此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改
