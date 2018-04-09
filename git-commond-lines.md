## Git Commond line notes

### 1.自报家门
#### 1.$ git config --global user.name "Your Name"
#### 2.$ git config --global user.email "email@example.com"
### 2.创建空目录
#### $ mkdir [Name]
#### $ cd [Name]
### 3.显示当前文件夹所在目录(如果使用windows系统，为了避免遇到各种莫名其妙的问题，请确保目录名-包括父目录-不包含中文)
#### pwd
### 4. 初始化，把这个目录变成Git可以管理的仓库
#### $ git init
#### 默认当前目录下会多了一个.git的目录，这个目录是Git用来跟踪管理版本库的，默认是隐藏的
#### $ ls -ah 显示当前目录下的文件及子目录
### 5. 随时查看当前目录的状态
#### $ git status
### 6. 查看文件更改情况
#### $ git diff [filename]
### 7.查看仓库修改历史记录, 显示从最近到最远的提交日志
#### $ git log
#### $ git log --pretty=oneline
### 8. 时光穿梭机,HEAD 表示当前版本，也就是最新提交的版本
#### $ git reset --hard HEAD
#### $ git reset --hard HEAD^
#### $ git reset --hard HEAD^^
#### $ git reset --hard HEAD~100
### 9. 查看文件的内容
#### $ cat [filename]
### 10. 从commit id 直接回退
#### $ git reset --hard [commit id]
### 11. 回查每一次命令
#### $ git reflog
### 12. 撤销更改
#### $ git checkout -- [filename] ——————此命令用于git add 后，还没有进行提交操作，可以直接恢复
### 13. 删除文件
#### $ git rm [filename]
#### 然后
#### $ git commit -m "comments"——————此命令用于删除文件，但是可以从快照（commit id）恢复
### 14. 生成ssh密钥
#### $ ssh-keygen -t rsa -C "bht_xyk@126.com", 可以一直回车下去，中间可以设置密钥保存的目录
### 15. 关联远程仓库
#### 首先在github上注册账号，并新建仓库，使用如下命令关联
#### $ git remote add origin https://github.com/xiongyaokun/learngit.git
#### $ git push -u origin master    (因为是第一次提交，所以加上-u 参数， 以后提交的时候就不需要了)



## Issues

1. **Error Message:** fatal: remote origin already exists.
   原因可能是重复添加了origin
   查看origin: git remote -v
   更改origin：git remote set-url origin [git-url]