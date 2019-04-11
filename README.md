# git 上传项目

## 基本操作
- 1. 初始化
    + 命令
    ` git init `
- 2. 设置签名
    + 用户名 email地址
    + 区分不同开发人员
    + 与托管代码中心账号无关
    + 命令
     * 项目级别/仓库级别：仅在当前本地库范围内有效
     `git config user.name 用户名`
     `git config user.email 邮箱`
      * 保存到 ./.git/config 中
     * 系统用户级别：登录当前操作系统的用户范围
     `git config --global ser.name 用户名`
     `git config --global user.email 邮箱`
      * 保存到家目录下 查看家目录cat ~/.gitconfig
     * 级别优先级
      + 就近原则：项目级别优先于系统用户级别，二者都有采用项目级别的签名
      + 都没有是不允许的
- 3. 查看工作区或者暂存区
    `git status`
- 4. 添加文件到暂存区 从工作区添加到暂存区
    `git add 文件名`
- 5. 移出暂存区
    `git rm --cached <file>...`
- 6. 提交修改信息 从暂存区提交到本地库
    `git commit （-m "提交的修改的信息"） 文件名`
- 7. 显示日志 查看历史记录 一行显示
  `git log --pretty=oneline`
  `git log --oneline`
- 8. 基于索引值的前进后退版本
  `git reflog`
  `git reset --hard 哈希值[局部索引值]`
- 9. 分支
  + 查看分支
    `git branch -v`
  + 创建分支
    `git branch [分支名]]`
    `git branch hot_fix`
  + 切换分支
    `git checkout [分支名]`
  + 合并分支 必须在接收修改的分支上 被合并的分支 增加新内容
    * 第一步`git checkout [被合并的分支名]`
    * 第二步 `git merge [有新内容的分支名，准备把它合并到另一个分支上]`
  + 合并冲突解决
    * 第一步 编辑文件 删除特殊符号
    * 第二步 把文件修改到满意的程度 保存退出
    * 第三步 `git add 文件名`
    * 第四步 `git commit -m "日志信息"`
      注意 此时 commit 一定不能带具体的文件名
- 10. 远程登录 新建别名  origin 代表我的地址
  `git remote add origin https://github.com/amieeee/git.git`
  `git remote -v`
- 11. 推送到GitHub 下载到本地 克隆
  * `git push origin master(上传到的分支名):我的分支`
  * `git pull <远程主机名> <远程分支名>:<本地分支名>`  
  * `git clone ttps://github.com/amieeee/git.git`
- 问题: The following untracked working tree files would be overwrit ten by merge怎么解决
  * 解决：git clean -d -fx
- 我呦呦呦再一次尝试
