# Task01 Java简介与环境配置

## Linux环境安装

### jdk安装

本人使用VMware安装了虚拟机Ubuntu 18作为环境。

[jdk下载地址](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)中选择jdk-8uxxx-linux-x64.tar.gz。

打开终端输入以下命令：

```
解压jdk压缩包
tar zxvf jdk-8uxxx-linux-x64.tar.gz
设置环境变量
sudo vim /etc/profile
```

在vim中添加下面内容（后面会介绍下vim怎么用）：

```
#Java Env
export JAVA_HOME=/usr/你的JDK路径
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
export PATH=$PATH:$JAVA_HOME/bin
```

### 开发工具使用idea

[idea下载地址](https://www.jetbrains.com/idea/download/#section=linux)中选择社区版。

打开终端输入以下命令：

```
将idea文件解压到opt目录,中间ideaxxx是下载的文件名
sudo tar -zxvf ideaxxxx.tar.gz -C /opt
切换到idea的bin目录
cd /opt/ideaxxxx/bin
运行idea.sheet-sch
./idea.sh
```

### vim编辑器使用

vim分为三种模式：命令模式，输入模式，底线命令模式

- 命令模式

vim刚启动便进入命令模式，此时敲击键盘识别为命令。常见命令：i切换到输入模式，x删除当前字符，：切换到底线命令模式

- 输入模式

该模式下输入字符，ESC退出输入模式到命令模式。

- 底线命令模式

常用命令：q退出程序，w保存文件。

![vim 键盘图](https://www.runoob.com/wp-content/uploads/2015/10/vi-vim-cheat-sheet-sch.gif)

### 基本数据类型和变量


```java
```