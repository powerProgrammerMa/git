svn是集中式的

git是分布式的，每个开发本地也有自己完整的版本库
TortoiseGit-2.12.0.0-64bit  ---乌龟的git可视化界面
公司提交代码时：先commit在pull

git init ---初始化本地仓库
git status ---查看本地库状态
git reflog ---查看历史记录  也可以使用git log查看更加全面的版本信息
git reset --hard 版本号 ----版本穿梭
git add 文件名 --添加到暂存区
git commit -m "提交说明" 文件名 --提交到本地仓库，这就形成了历史版本

git push 别名/地址 分支名 ---推送到远程库

git config --global user.name 用户名  ---设置用户签名
git config --global user.email 邮箱  ---设置用户签名

git rm --cached 文件名  ---删除暂存区的文件

git branch 分支名  --创建分支
git branch -v  --查看本地分支
git branch -a  --查看所有分支
git checkout 分支名  --切换分支
git merge 分支名  ---把指定的分支合并到当前分支
git pull origin master :在当前分支拉取master分支的代码
git pull 别名/地址 分支名---更新远程代码库的代码（推送人必须在项目成员中）
git push --set-upstream origin 分支名 ：设置本地分支追踪远程分支
git clone 远程地址 ---clone之后会自动创建地址别名 为origin



跨团队之间协作需要fork——》pullrequest(提交给另外一个团队)->merge pullrequest（合并别人提交过来的代码）

创建本地公钥和私钥：
    生成 ssh-keygen -t rsa -C mjs1706@sina.com  
    查看公钥：cat ~/.ssh/id_rsa.pub
    然后在git配置到SSH

创建远程仓库别名：
git remote -v 查看当前所有远程地址别名
git remote add 别名 远程地址  ---创建别名


//git忽略文件  git.gitignore文字中配置
.idear //忽略idear文件夹下的所有文件
*.zip  //过滤所有.zip文件

列出所有标签：git tag 
新建tag：git tag tagName
新建带备注的标签：git tag tagName -m "备注"
推送tag到远程：git push --tags
本地删除：git tag -d v1.0
远程删除：git push origin :refs/tags/v1.0



git remote -v:查看远程仓库详细信息，可以看到仓库名称，关联地址
git remote remove origin：删除origin仓库（比如名称错误）
git remote add origin 仓库地址：重新添加远程仓库地址
gti push -u origin master： 提交到远程仓库的master主干
