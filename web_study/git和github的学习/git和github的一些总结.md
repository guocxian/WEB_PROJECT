#git和github的一些总结

1.  git pull --rebase WEB_PROJECT master  出现拒绝访问的时候
2. git reset HEAD <file> and git restore --staged <file_name> 来取消暂存
3. git checkout -- <file>（逐渐会被淘汰，一个是分支的管理一个是文件的恢复，现在用switch和store） and git restore <file_name>  放弃对工作区的文件修改
4. git add <filename> 只能add当前路径下的向缓存区的文件(或者写全文件的路径)
5. 