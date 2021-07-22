# 面向对象核心技术

## 抽象类

面向对象中所有的对象都是通过类来实现的，但是并不是所有的类都可以实例化。
抽象类可以看做对一个类型的抽象。他也包括成员变量，方法和构造方法。但是它不能被实例化，
必须被继承才能使用。在java语言中使用abstract class来定义抽象类。

- 抽象方法

如果想要某一个类包含一个特殊的方法，该方法要由子类确定，就可以在父类声明该方法为抽象方法。

Abstract可以修饰抽象方法的声明。抽象方法所在类一定是抽象类，所有子类必须重写父类的抽象方法或者声明自身为抽象类。

```java
public abstract class animal
{
	private String name;
	private String sex;
	private String age;
	
	public abstract void eat();

}
// 老虎类从抽象类动物中继承并实现了抽象方法吃，吃肉。
public abstract class tiger
{
	public void eat(){
		System.out.println("eat meat");
	}
}
// 兔子类从抽象类动物中继承并实现了抽象方法吃，吃菜。
public abstract class rabbit
{
	public void eat(){
		System.out.println("eat vegetable");
	}
}

```

抽象类不一定包含抽象方法，但是包含抽象方法的一定是抽象类。
抽象类中的抽象法只声明，不包括实现。构造方法，类方法不能声明为抽象方法。

## 接口

接口在java中是一个抽象方法的集合。其中所有的方法都没有实现。
当类实现接口的时候必须实现接口中所有的方法，否者类型必须声明为抽象类。
抽象类是对一类对象的抽象。接口是对一系列行为的抽象。

```java
public interface Sleep{
	public void sleepBed();
}

public interface Study{
	public void studied();
}

public interface Teach{
	public void teaching();
}
// 学生实现了学习和睡觉两个方法。
public class Student implements Sleep,Study{
	@Override
	public void sleepBed(){
		System.out.println("我睡觉了");
	}
	
	@Override
	public void studied(){
		System.out.println("我在学习");
	}
}
// 教师类实现了教课和睡觉两个方法。
public class Teacher implements Sleep,Teach{
	@Override
	public void sleepBed(){
		System.out.println("我睡觉了");
	}
	
	@Override
	public void teaching(){
		System.out.println("我在教课");
	}
}

```

## 异常处理

程序运行过程中会出现一些错误。异常处理可以在出现错误时候按照既定逻辑进行运行。

异常发生原因通常包括：用户输入非法数据。要打开的文件不存在。网络通信中断，JVM内存溢出。

java中三种类型的异常：检查性异常；运行时异常；错误。

异常处理中常用的关键字：try, catch, finally, throw, throws。

异常处理的流程：

```java
try{
	// 程序代码
}catch(exceptiontype name){
	// 程序代码
}finally{
	// 程序代码
}

```
