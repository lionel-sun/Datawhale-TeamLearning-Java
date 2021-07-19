# 面向对象编程基础

将变成中涉及到的事物抽象成一个一个的对象，这样更符合人的思维，使编程更容易。
面向对象编程主要体现三个特性：封装；继承；多态。

## 类

Java是面向对象语言，它的源程序是由若干类组成。类声明的变量被称作对象，类就是模板。

类的定义：

```java
public class People {
	// 成员变量
    private String sex;
    private String name;
    private boolean fly;
    private int age;
	//成员方法
    public void ShowAge(){
        System.out.println(age);
    }
    public void ChangeSex(){
        if(this.sex=="F") this.sex = "M";
        else if(this.sex=="M") this.sex = "F";
        else System.out.println("unknown sex");
    }
	// 构造方法等其他内容
    public  People(String name, String sex, int age){
		fly = false;
        this.name = name;
        this.sex = sex;
        this.age = age;
    }
}
```

成员变量： [权限修饰符] [类型] [成员名]

成员方法： 
[权限修饰符] [返回值类型]方法名([参数类型 参数名])[throws 异常类型]{
	//方法体
	return 返回值;
}

其中权限修饰符可以是private, public, protected。

构造方法：

构造方法是和类名同名的方法。构造方法可以有参数，也可以无参数。

this关键字，在方法中出现局部变量和成员变量同名的时候，需要使用this关键字指向成员变量。

static关键字： 

使用static修饰的变量是静态变量，在类声明时候就固定的值。

使用static修饰的方法是静态方法，在某些环境下无法创建类，但是需要调用某些方法来实现业务逻辑。
这时候需要使用静态方法。


类的主方法是程序入口。它指定了程序从何开始。

## 继承

继承是面向对象的特征之一。从已有的类中派生出新的类。新的类具有父类的方法，
同时也增加新的方法。

```java
class father{
}

class son extends father{
}
```

implements: java不支持多重继承，但是使用implements可以实现多个接口。类似多继承的特性。

```java
public interface f1{
}
public interface f2{
}

public class f3 implements f1,f2{
}
```

super指向父类成员。this指向当前成员。

final修饰的类是不可继承的，也可以用于修饰方法，方法不能被重写。

## 多态

多态是同一个行为有多种的表现方法。多态转型有向上和向下两种。

- 向上转型

当不需要面对子类类型时，通过提高扩展性，或者使用父类的功能就能完成相应的操作。

父类类型 变量名=new 子类类型()

- 向下转型

当要使用子类特有功能时。

子类类型 变量名=（子类类型） 父类类型的变量；