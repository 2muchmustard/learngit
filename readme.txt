git init  #创建git仓库
#把文件放入git仓库
git add XXX  
git commit -m "提交的说明"
#需要add， commit 两步，可以add多个文件

git status  #掌握库状态
git diff   #查看修改

git reset --hard HEAD^  #回退到上个版本
git reset --hard HEAD^^ #回退上上个版本
git reset --hard HEAD~100 #回退前100个版本

git log #查看版本库状态详情
git log --pretty=oneline  #查看版本库状态概况
git reset --hard xxxx  #回到某个版本
git reflog  #命令日志


add something