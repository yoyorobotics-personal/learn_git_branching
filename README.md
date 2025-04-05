# learn_git_branching
git branching notes from learngitbranching
基础篇
1. `git commit`
	**新的版本**
2. `git branch <branchName>`
	虽然是叫做分支，但是不会生成新的提交
3. `git checkout <branchName>` 
	把HEAD指向这个分支
	git switch 最终会取代这个命令
4. `git checkout -b <your-branch-name>`
	创建一个新的分支同时指向新创建的分支
5. `git merge <branchName>`
	合并分支会创建一个**新的版本**，此版本会包含branchName这个分支的内容，分支完全合并，每一个分支都包含所有修改，还需要指向branchName，并合并到最终的main
6. `git rebase <branchName>`
	复制HEAD指向的branchWithStar到branchName下，会创建一个**副本**，同时将branchWithStar和HEAD指向这个副本通过HEAD指向main，再进行`git rebase <branchName>`实现主分支的最终合并
进阶篇
7. `cat .git/HEAD`
	1. 看HEAD指向
8. `git symbolic-ref HEAD`
	1. 看HEAD指向的引用
9. `git checkout <ID>`
	1. 关于HEAD指向哈希值
10. `git checkout HEAD^~<num>`
	1. 向上移动，相对引用
11. `git branch -f <branchName> HEAD~<num>`
	1. 强制移动branchName分支
12. `git reset HEAD~1`
	1. 向上移动一个版本，指向的版本被忽略
13. `git revert HEAD`
	2. 复制上一个版本的**副本**，用于团队合作
2025-04-05
