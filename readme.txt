''' CMDs for Git '''

__author__ = Yan
__time__ = 2021.02.01



git init
# 将指定目录设为Git仓库repo

git add <filename>
# 把文件从工作区添加进版本库的暂存区（stage）

git commit -m ""
# 从暂存区提交到当前master分支（引号内添加描述）

git status
# 查看当前repo状态

git diff <filename>
# 查看对文件做的修改

git diff HEAD -- <filename>
# 查看工作区和版本库最新版本的区别（HEAD是版本库主分支的当前版本）

git log --pretty=oneline
# 日志（每次版本用一行描述）

git reset --hard HEAD^
# 退回到上一版本（^表示上一个，^^表示上2个，以此类推）

git reset --hard <commit_id>
# 每个版本都有个用哈希算法SHA1算出的commit_id，使用该命令（commit_id只要输入前3~5位）即可返回指定版本

git reset HEAD <filename>
# 将最新版本退回到工作区

git reflog
# 记录最近的N次命令

cat <filename>
# 文本输出，concatenate缩写

git checkout -- <filename>
# 将文件在工作区的修改全部撤销 （--前后都必须有空格！否则，变成切换分支的命令）

git rm <filename>
# 版本库中删除文件 （该命令要加上commit才是真的删除）
git commit -m "remove the object file"



