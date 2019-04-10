# git 上传项目

## 1. 初始化
  + 命令
  ` git init `
## 2. 设置签名
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
## 3. 查看文件的暂存情况
  `git status`

## 4. 添加文件到暂存区
  `git add 文件名`

## 5. 移出暂存区
  `git rm --cached <file>...`
