git init  #创建git仓库
#把文件放入git仓库
git add XXX  
git commit -m "提交的说明"
#需要add， commit 两步，可以add多个文件
#add 把修改放到暂存区  commit 一次性把暂存区的修改提交到分支

git status  #掌握库状态
git diff   #查看修改

git reset --hard HEAD^  #回退到上个版本
git reset --hard HEAD^^ #回退上上个版本
git reset --hard HEAD~100 #回退前100个版本

git log #查看版本库状态详情
git log --pretty=oneline  #查看版本库状态概况
git reset --hard xxxx  #回到某个版本
git reflog  #命令日志

git restore <file>  #撤销工作区修改
git restore staged <file>  #撤销暂存区的修改

rm <file>
git rm <file>
git commit         #删除操作,误删则 restore 撤销工作区修改


ssh-keygen -t rsa -C "youremail@example.com" #在用户目录下，创建SSH Key

git remote add origin git@github.com:2muchmustard/learngit.git   #将当前git库关联到远程库

git push -u origin master  #第一次推送分支

git puash origin master #推送

git pull  #拉取

git clone git@github.com:2muchmustard/gitskill.git  #先创建远程库，再克隆到本地

git checkout -b <dev>  #创建一个分支dev
git branch #查看所有分支，当前分支标*
git checkout <dev>  #切换到<>分支
git merge <dev>  #把<>分支合并到当前分支上，无法自动合并时要先解决冲突，再提交。
git branch -d <dev>  #删除该分支
git branch -D <dev>  #强制删除已经提交的分支
git switch -c <dev>  #创建并切换到分支<>,该命令旨在代替checkout
git switch <dev>   #转到分支<>
git log    #查看分支合并情况

git merge --no-ff -m "<>" <dev>    #合并分支时会留下分支信息

git stash  #存储工作区
git stash list  #查看存储列表,列表为栈，即最近的一次存储为stash@{0}
git stash apply  #恢复
git stash drop   #删除
git stash pop   #恢复并删除
git cherry-pick <commit>    #将特定的提交合并到当前分支

git checkout -b <dev> origin/<dev>                #在本地创建与远程分支对应的分支
git branch --set-upstream-to=origin/<dev> <dev>   #绑定远程库分支到本地库分支

git rebase  #把本地未push的分叉提交历史整理成直线