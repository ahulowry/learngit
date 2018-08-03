## 第一课 环境准备

建议的环境是Linux环境，如果使用windows，请直接跳到4. windows环境准备：

1. 可以远程ssh登录的Linux环境

Windows下使用git要考虑编码，不适合入门。入门建议使用Linux。

2. Linux环境使用utf-8编码

utf-8是通用的编码，windows下更乱，所以建议使用Linux入门
````
$ echo $LANG
en_US.utf-8
````

只要vi之类的编辑器可以输入中文即可。

3. 安装git软件

对于CentOS，配置好epel库后，执行`yum install git`就可以安装。

对于Debian类系统，执行`apt-get install git`可以安装。

其他系统可以自行google/baidu。

4. Windows环境准备（厦门大学郑海山老师贡献本节内容）（Linux环境可以跳过这一步到5. 注册github账号）

* 首先从[https://git-for-windows.github.io/](https://git-for-windows.github.io/),（网速慢的同学请移步[国内镜像](https://pan.baidu.com/s/1dFAE1Jb)），然后按默认选项安装即可。下载安装 windows下的Git命令行

* 安装完成后，还需要最后一步设置，在命令行输入：
	$ git config --global user.name "Your Name"
	$ git config --global user.email "email@example.com"

* 创建版本库
	1.创建一个版本库非常简单，首先，选择一个合适的地方，创建一个空目录：
		$ mkdir test
		$ cd test
	2.通过git init命令把这个目录变成Git可以管理的仓库：
		$ git init
		Initialized empty Git repository in /Users/test/.git/
    瞬间Git就把仓库建好了，而且告诉你是一个空的仓库（empty Git repository），细心的读者可以发现当前目录下多了一个.git的目录，这个目录是Git来跟踪管理版本库的，没事千万不要手动修改这个目录里面的文件，不然改乱了，就把Git仓库给破坏了。

    如果你没有看到.git目录，那是因为这个目录默认是隐藏的，用ls -ah命令就可以看见。
	3.把文件添加到版本库


5. 注册github账号

浏览器访问 [https://github.com](https://github.com), 输入想要的账号、邮件、密码，单击 "Sign up for GitHub" 注册。

## 课程完成检查点

1. 可以远程登录Linux，输入中英文

执行以下命令，可以输出本文
````
curl https://raw.githubusercontent.com/bg6cq/learngit/master/1/README.md
````
2. 执行`git`有显示
```
$ git
usage: git [--version] [--help] [-c name=value]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p|--paginate|--no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           <command> [<args>]

The most commonly used git commands are:
   add        Add file contents to the index
   bisect     Find by binary search the change that introduced a bug
   branch     List, create, or delete branches
   checkout   Checkout a branch or paths to the working tree
   clone      Clone a repository into a new directory
   commit     Record changes to the repository
   diff       Show changes between commits, commit and working tree, etc
   fetch      Download objects and refs from another repository
```

3. 有github账号可以登录
   
浏览器访问 [https://github.com](https://github.com)，单击 "Sign in", 输入自己账号、密码，可以登录。

