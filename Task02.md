# Task02 初始Java语言基础

## 运算符和表达式

- 四则运算

Java中+,-,*,/,%分别表示加、减、乘、除和取余。
```java
    public static void day03(){
//        加减乘除
        int a = 10+2, b = 10-2, c = 10*2;
        double d = 10.0/2;
		int e = 10%2;
        System.out.println("10+2="+a);
        System.out.println("10-2="+b);
        System.out.println("10*2="+c);
        System.out.println("10/2="+d);
		System.out.println("10%2="+e);
    }
```

输出结果如下：
```
10+2=12
10-2=8
10*2=20
10/2=5.0
10%2=0
```

- 数学函数

在math类中包含了很多数学函数:平方根，幂运算，三角函数，指数函数和一些常量。

```java
    public static void day03(){
//        math函数: 
        double a = Math.sqrt(4);
        double b = Math.pow(2,3);
        double c = Math.sin(2);
        double d = Math.cos(2);
        double e = Math.tan(2);
        double f = Math.atan(2);
        double g = Math.log(2);
        double Pi = Math.PI;
        double E = Math.E;
    }
	
- 结合赋值和运算符以及自增减

可以使用+=，*=，%=等简便形式；
```java
int x = 1;
x +=4;
x = x + 4;
x++;
++x;
x = x+1;
int i =9
int a = 2* ++i;// a=20, i = 10 
int b = 2* i++;// b=20, i = 11
```
++在前会先完成加1在进行运算，++在后则先使用变量原来的值进行运算.

- 关系和boolean运算符以及位运算

关系运算符：相等==，不等!=，大于>，小于<，大于等于>=，小于等于<=。
!表示非，&&表示“与”，||表示“或”。
三目运算符x?y:z，当x返回结果为true时就返回y，当x返回结果为false时就返回z。

处理整数时候，可以对各个位进行运算。位运算符包括：&("and")、|("or")、^("xor")、~("not")。
另外还有>>和<<运算符将位模型左移或右移。

## 控制流程

- 块作用域

Java中使用｛｝中的变量作用域就在对应｛｝内。但是不能在嵌套的｛｝中使用同名变量。

- 条件语句

```java
	public static void  day04(){
//        条件语句
        int i = 10;
        if (i > 10){
            i = 9;
        }else if (0<i && i <10){
            i = -1;
        }else{
            System.out.println(i);
        } 
    }
```

- 循环语句

```java
	public static void  day04(){
//        循环语句
        int i = 10;
        while(i < 100){
            i = i + i/10;
        }
        System.out.println(i);
    }
```

- 确定循环(for循环)

for循环语句第一部分声明一个变量，第二部分是循环条件，第三部分是更新的计数器。
如果想要在for循环以外使用计数器的值，需要在循环体前声明该变量。

```java
	public static void  day04(){
//        for循环
        for (int i = 1; i <= 10; i++){
			System.out.println(i);
		}
    }
```

- 中断控制流程语句

```java
	public static void  day04(){
//        中断控制
        int i = 1;
        while(i<100){
            i++;
            if (i>10) break;
        }
        System.out.println(i);

        while(i<20){
            i++;
            if (i%2 == 0) continue;
            System.out.println(i);
        }
        for (int n=0; n<10; n++){
            if (n%2!=0) continue;
            System.out.println(n);
        }
	}
```

break语句可以退出当前循环。continue中断本次循环，将执行循环内的第一条代码。在for循环中可以跳到更新部分。

- 多重选择：switch语句 

```java
	public static void  day04(){
//        switch语句
        int i = 1, j =2;
        switch (i+j){
            case 3:
                i = 2;
                System.out.println("run case 1");
            case 4:
                j = 3;
                System.out.println("run case 2");
            default:
                System.out.println("run case default");
                break;
        }
    }
```
