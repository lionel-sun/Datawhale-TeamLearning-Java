# Task01 Java����뻷������

## Linux������װ

### jdk��װ

����ʹ��VMware��װ�������Ubuntu 18��Ϊ������

[jdk���ص�ַ](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)��ѡ��jdk-8uxxx-linux-x64.tar.gz��

���ն������������

```
��ѹjdkѹ����
tar zxvf jdk-8uxxx-linux-x64.tar.gz
���û�������
sudo vim /etc/profile
```

��vim������������ݣ�����������vim��ô�ã���

```
#Java Env
export JAVA_HOME=/usr/���JDK·��
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
export PATH=$PATH:$JAVA_HOME/bin
```

### ��������ʹ��idea

[idea���ص�ַ](https://www.jetbrains.com/idea/download/#section=linux)��ѡ�������档

���ն������������

```
��idea�ļ���ѹ��optĿ¼,�м�ideaxxx�����ص��ļ���
sudo tar -zxvf ideaxxxx.tar.gz -C /opt
�л���idea��binĿ¼
cd /opt/ideaxxxx/bin
����idea.sheet-sch
./idea.sh
```

### vim�༭��ʹ��

vim��Ϊ����ģʽ������ģʽ������ģʽ����������ģʽ

- ����ģʽ

vim���������������ģʽ����ʱ�û�����ʶ��Ϊ����������i�л�������ģʽ��xɾ����ǰ�ַ������л�����������ģʽ

- ����ģʽ

��ģʽ�������ַ���ESC�˳�����ģʽ������ģʽ��

- ��������ģʽ

�������q�˳�����w�����ļ���

![vim ����ͼ](https://www.runoob.com/wp-content/uploads/2015/10/vi-vim-cheat-sheet-sch.gif)

### �����������ͺͱ���

#### �����������Ͱ���

���ͣ�byte, short, int, long

�����ͣ�float, double

�ַ��ͣ�char

�����ͣ�bollean

���и������ַ������ͣ�String

```java
public class HelloWorld {
    public static void main(String[] args) {
        /*������������8��*/
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

#### ��������


- �ֲ��������෽���еı������ھֲ�ʹ��ִ�к����١�

- ʵ�������������ڷ���֮�⣬û��static���Ρ���һ������ʵ������ʵ��������ֵ��ȷ���ˡ�
����ʵ�������ٶ����١�

- ������������ڷ���֮�⣬��static���Ρ���̬�������ഴ����ÿ��������������ĸ��ơ���ֵ���������һ����

- ����ת����

![](https://github.com/datawhalechina/team-learning-program/blob/master/Java/img/i0.hdslb.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg)

ǿ������ת����

```java
double x = 9.997;
int nx = (int)x;
/*ʹ��Math.round����������������*/
int nx = (int) Math.round(x);
```

- ��������������ʱ�����޸ġ���final�ؼ������Ρ�

#### ö������

ö����һ����������ʾһ�鳣����

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

�ο�����
1. [����̳� ��������](https://www.runoob.com/java/java-variable-types.html)