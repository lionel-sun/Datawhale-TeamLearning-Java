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


```java
```