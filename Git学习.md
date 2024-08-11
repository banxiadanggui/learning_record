# 基础操作
基础命令参考[[Bush学习]]
学习资料参考
1. [Git基础使用教程 - 老_张 - 博客园 (cnblogs.com)](https://www.cnblogs.com/imyalost/p/8762522.html)
2. [环境部署（六）：Git关联github - 老_张 - 博客园 (cnblogs.com)](https://www.cnblogs.com/imyalost/p/8777684.html)

git基础操作如下：
1. 将目录变为git可管理的仓库`git init`
2. 将文件上传到暂存区`git add <文件名>/.`
3. 丢弃文件中的更改，恢复文件`git restore<文件名>`
4. 将已经更改的文件暂存并且上传到仓库:`git commit -a '上传信息'`
5. 将暂存区文件上传到仓库`git commit -m '上传注释的信息'`
6. 回退到上一个版本或指定版本`git reset --hard HEAD^/指定版本号`

查看信息：`
1. 检查该版本库内是否有未上传的信息:`git status`
2. 检查文件修改的内容`git diff`
3. 获得历史修改记录`git log`/获得修改记录精简版`git log --pretty=oneline`
4. 查看文件内容`git cat <文件名>`
5. 获取历史版本号`git reflog`

远程仓库与本地仓库间的通信
1. 基础知识：远程仓库默认名称origin,本地仓库默认名称master
2. 查看连接的远程仓库`git remote -v`
3. 推送到远程仓库`git push origin(远程仓库分支名) master(本地分支名)`
4. 下载最新的更新到本地`git push origin master`

分支知识
1. 分支是用来将特性开发绝缘开来的。在创建仓库的时候，_master_ 是默认的分支。在其他分支上进行开发，完成后再将它们合并到主分支上。
2. 查看有哪些分支`git branch`
3. 查看远程分支或所有分支`git branch -r/-a`
4. 新建分支`git branch testbranch`
5. 创建并切换分支`git checkout -b testbranch  
6. 切换分支 `git checkout master`  
7. 删掉新建的分支 `git branch -d testbranch

标签
1. 命名标签`git tag name 版本号前十位（通过log获取）`
