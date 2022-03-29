# git使用技巧

## error : src refspec master does not match any
目录中没有文件，无法提交空目录上去。

增加文件
git add text
git add 文件夹/ 添加整个文件夹及内容
git add 文件夹/*.md
添加以md为后缀的所有文件。



添加注释
git commit -m 'comment_name'

推上去
git push origin master



## error : failed to push some refs to 'https://github.com/name/Demo_name.git'
先拉后推

先将远程仓库pull进本地仓库

然后再push出去



## fatal : remote origin already exists
已经建立了远程连接



## fatal : 'oringin' does not appear to be a git repository
存储库不对

重新调整存储库



## fatal : Could not read from remote repository

该点与上点一起

## fatal : Updating an unborn branch with changes added to the index
致命的：更新未出生的分支，并将更改添加到索引
    
在拉仓库时发生这个，不需要在意2333














