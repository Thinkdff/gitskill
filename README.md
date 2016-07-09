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
///////

git stash//可以把当前工作现场“储藏”起来，等以后恢复现场后继续工作.前提是没有提交（add）
git stash pop//把储藏起来的分支恢复过来并删掉储藏区
git stash apply//恢复但没有删除
git stash drop//删除储藏区


多人协作：
首先，可以试图用git push origin branch-name推送自己的修改；
如果推送失败，则因为远程分支比你的本地更新，需要先用git pull试图合并；
如果合并有冲突，则解决冲突，并在本地提交；
没有冲突或者解决掉冲突后，再用git push origin branch-name推送就能成功！
如果git pull提示“no tracking information”，
则说明本地分支和远程分支的链接关系没有创建，
用命令git branch --set-upstream branch-name origin/branch-name。

查看远程库信息，使用git remote -v；
本地新建的分支如果不推送到远程，对其他人就是不可见的；
从本地推送分支，使用git push origin branch-name，如果推送失败，先用git pull抓取远程的新提交；
在本地创建和远程分支对应的分支，使用git checkout -b branch-name origin/branch-name，本地和远程分支的名称最好一致；
建立本地分支和远程分支的关联，使用git branch --set-upstream branch-name origin/branch-name；
从远程抓取分支，使用git pull，如果有冲突，要先处理冲突。