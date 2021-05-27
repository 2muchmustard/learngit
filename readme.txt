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

git clone git@github.com:2muchmustard/gitskill.git  #先创建远程库，再克隆到本地

git checkout -b <dev>  #创建一个分支dev
git branch #查看所有分支，当前分支标*
git checkout <dev>  #切换到<>分支
git merge <dev>  #把<>分支合并到当前分支上
git branch -d <dev>  #删除该分支
git switch -c <dev>  #创建并切换到分支<>,该命令旨在代替checkout
git switch <dev>   #转到分支<>

