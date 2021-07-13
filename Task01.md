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

#### 基本数据类型八种

整型：byte, short, int, long

浮点型：float, double

字符型：char

布尔型：bollean

还有个常见字符串类型：String

```java
public class HelloWorld {
    public static void main(String[] args) {
        /*基本数据类型8种*/
        boolean bool = false;
        byte by = 1;
        char ch = 'c';
        double d = 2.0;
        float f = 0.1f;
        int i = 1;
        long l = 2;
        short sh = 3;
        String str = "string";
        System.out.println("Bool :" + bool);
        System.out.println("Byte :" + by);
        System.out.println("Character:" + ch);
        System.out.println("Double :" + d);
        System.out.println("Float :" + f);
        System.out.println("Integer :" + i);
        System.out.println("Long :" + l);
        System.out.println("Short :" + sh);
        System.out.println("String :" + str);
    }
}
```

#### 变量类型


- 局部变量：类方法中的变量，在局部使用执行后被销毁。

- 实例变量：独立于方法之外，没有static修饰。当一个对象被实例化后，实例变量的值就确定了。
随着实例被销毁而销毁。

- 类变量：独立于方法之外，用static修饰。静态变量，类创建的每个对象都有类变量的复制。（值不变和类中一样）

- 类型转换：

![](https://github.com/datawhalechina/team-learning-program/blob/master/Java/img/i0.hdslb.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg)

强制类型转换：

```java
double x = 9.997;
int nx = (int)x;
/*使用Math.round方法进行舍入运算*/
int nx = (int) Math.round(x);
```

- 常量：程序运行时不能修改。用final关键字修饰。

#### 枚举类型

枚举是一个特殊的类表示一组常量。

```java
enum Color
{
	RED, GREEN, BLUE, YELLOW, BLACK;
}
public static void main(String[] args)
{
	Color c1 = Color.RED, c2 = Color.BLUE;
    System.out.println("color1: "+c1+" color2: "+c2);
}

```

参考索引
1. [菜鸟教程 变量类型](https://www.runoob.com/java/java-variable-types.html)