# git 教程

## 中二开头

一日，mt改了群友电脑上的代码qwq

有群友高呼：你做了什么mt！你这样我该如何应对！

只见mt淡淡一笑：很简单，你用 git, 不就好了。

说罢，他的命令行终于不再掩饰————git指令！群友为之一寂！

忽然吟道：

早岁已知开发难，代码记录藏心间。

平日开发无人问，日日冲突遭责问。

提交推送勤修炼，回滚重置似梦难。

今朝代码无敌路，是我Git修行人。

顷刻炼化，终于成尊！

## 友情提示

- 如果你听说过 github，首先忘掉它！
- 如果你还没安装 git，现在就来安装！
- 如果你使用过 gui，那么关掉 gui！
- 以后你的 vscode 里要装好几个 git 插件，但建议只用来看，不用来操作！
- 以及我也不知道该咋讲 git 的概念，但先用起来再说！

## 安装 git

### windows

https://git-scm.com/download/win

下载下来安装就行了

### linux

#### ubuntu

```bash
sudo apt install git
```

#### 其他

其他 linux 系统自己想办法，毕竟你都会linux了qwq

## git 使用

如果你是 windows 用户，在一个"合适的文件夹"，右键并选择 'Git Bash Here'；
如果你是 linxu 用户，打开你的终端，cd 到一个"合适的文件夹"

### 注意

除非特别说明，目前我们的操作都只在我们自己的电脑上（本地）生效。

### 代码仓库

如果你也像这样下载过 github 的代码，那么以后你再也不会这么做了！

![直接下载了zip](images/download_zip.png)

↑↑↑↑↑↑ 不要这样做！！！ ↑↑↑↑↑↑

#### 什么是代码仓库(repository)

因为这样下载的文件夹内，只有代码文件，而没有文件的“历史记录”。

由 git 管理的代码仓库内，git 忠实地“记录”了每一个文件、每一行的修改记录，就像下面这样，我知道这行 bug (并不是bug) 是谁在什么时候写的！

![not_a_bug](images/history.png)

就算某次代码更新时删掉了一个文件，（由于git 记录了这个文件的信息，）只要回到以前的"版本"(而且只需要一行命令！)，这个文件就又会回来了qwq。而这些信息，都存放在代码仓库目录下的隐藏文件夹 .git/ 里（名字以.开头就是隐藏文件、隐藏文件夹啦）

#### git clone

为了完整地下载代码仓库，需要使用 git clone 命令

```bash
git clone https://github.com/martellz/git_tutorial.git
```

这条命令会把链接上的"代码仓库"克隆到你所在的"合适的文件夹"。
其实这个链接就是这个教程的代码仓库的链接啦。

#### git init

既然能下载别人的仓库，当然也能自己创建仓库。

在你“不是代码仓库”的文件夹下，执行 git init 指令，就会这个文件夹变成一个代码仓库。