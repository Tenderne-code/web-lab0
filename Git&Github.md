# Git&Github

## Git
Git 是一个开源的分布式版本控制系统，常用于便捷高效地处理任何或大或小的项目。

Git 是 Linus Torvalds 为了帮助管理 Linux 内核开发而开发的一个开放源码的版本控制软件。

我们强烈推荐你使用 git 管理你的项目。

### Git 基本操作

#### 创建仓库

`git init` 用于创建并初始化一个新的仓库，你可以在该仓库开始构建项目。

在任意位置新建文件夹 `mkdir lab0` ，在该目录下执行 `git init` 会在该位置创建本地 git 仓库

``` shell
$ mkdir lab0
$ cd lab0
$ git init
```

除了新建一个仓库，你也可以使用 `git clone` 命令拷贝一个现有仓库，我们以 Lab0 的模板仓库为例，在任意位置执行以下指令
``` shell
$ git clone https://github.com/N2Sys-EDU/Lab0-Introduction-To-Classroom.git
```
这条指令将位于 `https://github.com/N2Sys-EDU/Lab0-Introduction-To-Classroom.git` 的远程仓库克隆到本地，你将会在当前目录下发现目录 `Lab0-Introduction-To-Classroom/`

#### 提交与修改
当你在项目中做了一些修改后，比如创建一个新文件 `touch README.md` ，你可以使用 `git add` 命令来将你的修改添加到暂存区，例如 `git add README.md` ，你也可以使用 `git add .` 来将所有修改添加到暂存区。
``` shell
$ touch README.md
$ git add README.md
```

在确认了你的改动之后，你可以将文件提交到仓库中，但在此之前，你需要先设置你的用户信息
``` shell
git config --global user.name "labman008"
git config --global user.email "labman008@pku.edu.cn"
```
`--global` 用于指明作用域为全局，相应的你也可以使用 `--local` 来使得配置仅在当前仓库生效。

之后，你可以使用 `git commit` 指令将暂存区的文件提交到本地仓库中，这将会在仓库中创建一个快照，或者说项目的一个版本，你可以利用 git 在不同版本之间快捷的切换，换言之你不用再担心因为反复修改而失去了第一份能运行的代码了。
``` shell
$ git commit -m "first commit"
```
`git commit -m [message]` 用于为你的提交添加一些说明。另外，你也可以使用 `git commit -a` 来跳过 `git add`

现在，你已经掌握了使用 git 管理本地仓库的基本方法。

## Github

## More git