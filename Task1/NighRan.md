#Git学习
##基础命令
+ mkdir 创建目录
+ git init 管理仓库
+ git add 放置缓冲区
+ git commit  -u "**  ....  **"上传并且注释
+ git status 查看当前库的状态
+ git diff 查看diff
+ git log 提交日志
+ git reset --hard HEAD^退档  HEAD^^两档  HEAD~100 100档
+ git checkout -- file   直接工作区撤销
+ git rm file 删除
+ git push origin master提交至github 前提是已提交至本地库
+ git checkout -b **branchname** 创建 -d删除分支
+ git stash 存放工作   apply恢复 drop删除   pop恢复并删除
+ git tag **name** 标签
#Github使用
1.未创建ssh key； $ ssh-keygen -t rsa -C "your_email@email.com"

2.库的创建基本没难度

3.接下来就是git上传文件，上文git命令。

附带链接[Git教程-廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/896043488029600)




