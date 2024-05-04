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

