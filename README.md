# gitskill
skill

git clone git@github.com:Thinkdff/gitskill.git // 用远程仓库在本地克隆一个本地仓库

git checkout -b dev 
// 从当前分支的基础上创建一个新的dev分支并切换到dev分支
// 加上 -b 相当于以下两个命令
// git branch dev
// git checkout dev

git branch // 列出所有分支，当前分支前有一个*

git merge dev // 将当前分支指针指向dev分支的指针即合并分支，即合并dev分支到当前分支

git branch -d dev //删除dev分支

///////
查看分支：git branch
创建分支：git branch <name>
切换分支：git checkout <name>
创建+切换分支：git checkout -b <name>
合并某分支到当前分支：git merge <name>
删除分支：git branch -d <name>
/////