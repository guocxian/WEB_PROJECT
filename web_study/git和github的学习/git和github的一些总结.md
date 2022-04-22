#git和github的一些总结

   --------------------------初试添加、提交操作-------------------------------------------

1. git init ：初始化git文件操作
2. git status 能查看不是当前路径下的工作区文件的改变
3. git add <filename> 只能add当前路径下的向缓存区文件(或者写全文件的路径)
4. git commit -m "提交的备注"(提交到本地的仓库了)
5. git push -u origin\master
6. git pull --rebase WEB_PROJECT master  出现拒绝访问的时候

   ---------------------------撤销操作----------------------------------------------------
commit之前的撤销 
1. git reset HEAD <filename> and git restore --staged <file_name> 来取消文件暂存，回到工作区
2. git checkout -- <filename>（逐渐会被淘汰，一个是分支的管理一个是文件的恢复，现在用switch和store） and git restore <file_name>  放弃对工作区的文件修改
commit之后的撤销
3. git reset --hard <commit_id> 回到commit_id提交之后的场景，在这之后的commit全失效，工作区的内容消失，提交的文件退出了缓存区
4. git reset --mixed <commit_id>回到commit_id提交之后的场景,但是之后的commit对于工作区的内容保存下来，只是退出了缓存区
5. git reset --soft <commit_id>回到commit_id提交之后的场景,但是之后的commit对于工作区的内容保存下来，提交文件在缓存区

   ---------------------------分支的管理--------------------------------------------------

6. git branch <分支名> ：创建分支
7. git switch <分支名> git checkout <分支名> ：切换分支
8. git checkout  -b <分支名> ：创建并切换分支
9.  git branch -d <分支名>:删除分支
10. git merge <分支名>：合并<分支名>到master上面
11. ![](2022-04-21-18-11-48.png)
12. git branch --merged 与 git branch --no-merged 这两个有用的命令可以过滤这个列表中已经合并或尚未合并到当前分支的分支
13. git pull = git fetch +git merge
14. 