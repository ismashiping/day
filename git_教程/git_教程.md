## git_教程

### 001.git安装

Ubuntu 或者Debian 下载

```github
sudo apt-get install git 
```

windows安装 git，有一个git bash

安装后需要进行设置，在命令行输入:

```bash
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
```

git 是一个版本控制软件，每一个文件的修改、删除都可以被追踪

### 002.git创建版本库

```bash
mkdir learngit
cd learngit
pwd # 显示路径
```

将该路径变成git可以管理的仓库

```bash
git init 
```

此时,仓库为空仓库

将一个文件放到git仓库:

```bash
git add 文件名
git commit -m "wrote a readme file"  # -m 对该次提交的说明
```

### 003.版本回退

```bash
git log #查看提交记录
git reset --hard HEAD^ # HEAD^表示上一个版本,HEAD^^表示上上个版本 也可以加commit id
cat 文件名 # 可以显示文件中的内容
git reflog # 可以记录命令历史
```

### 004.git修改

只有将修改add到暂存区才能commit到分支

```bash
git checkout -- 文件名  # 文件未被放到暂存区,此时撤销到与版本一致;文件被放在暂存区后修改,撤销到上一次暂存区的状态
```

工作区就是文件夹

### 005.git删除文件

```bash
git rm test.txt
git commit -m "删除了test.txt"
```

### 006.git远程仓库

关联远程仓库

```bash
git remote add origin git@github.com:michaelliao/learngit.git
```

将本地所有内容推送到远程库:

```bash
git push -u origin master # 其中 -u 将本地master 与远程master分支关联起来 只需要一次
git push origin master 
```

删除远程库---不是真的删除,只是解除关联

```
# 查看远程库信息
git remote -v
git remote rm origin
```

### 007.分支管理

创建分支:

```bash
git checkout -b dev # 创建分支dev 
# 等价于创建dev并切换到dev
git branch dev
git checkout dev
```

查看当前分支:

```
git branch
```

切换分支:

```bash
git checkout master
```

合并分支:

```bash
git merge dev
```

删除分支:

```bash
git branch -d dev
```

### 008.解决冲突



<img src="C:\Users\ma\AppData\Roaming\Typora\typora-user-images\image-20240505160003548.png" style="zoom:43%;" />

只有解决冲突后才能合并