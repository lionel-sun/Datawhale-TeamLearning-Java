# ���������ļ���

## ������

������������еĶ�����ͨ������ʵ�ֵģ����ǲ��������е��඼����ʵ������
��������Կ�����һ�����͵ĳ�����Ҳ������Ա�����������͹��췽�������������ܱ�ʵ������
���뱻�̳в���ʹ�á���java������ʹ��abstract class����������ࡣ

- ���󷽷�

�����Ҫĳһ�������һ������ķ������÷���Ҫ������ȷ�����Ϳ����ڸ��������÷���Ϊ���󷽷���

Abstract�������γ��󷽷������������󷽷�������һ���ǳ����࣬�������������д����ĳ��󷽷�������������Ϊ�����ࡣ

```java
public abstract class animal
{
	private String name;
	private String sex;
	private String age;
	
	public abstract void eat();

}
// �ϻ���ӳ����ද���м̳в�ʵ���˳��󷽷��ԣ����⡣
public abstract class tiger
{
	public void eat(){
		System.out.println("eat meat");
	}
}
// ������ӳ����ද���м̳в�ʵ���˳��󷽷��ԣ��Բˡ�
public abstract class rabbit
{
	public void eat(){
		System.out.println("eat vegetable");
	}
}

```

�����಻һ���������󷽷������ǰ������󷽷���һ���ǳ����ࡣ
�������еĳ���ֻ������������ʵ�֡����췽�����෽����������Ϊ���󷽷���

## �ӿ�

�ӿ���java����һ�����󷽷��ļ��ϡ��������еķ�����û��ʵ�֡�
����ʵ�ֽӿڵ�ʱ�����ʵ�ֽӿ������еķ������������ͱ�������Ϊ�����ࡣ
�������Ƕ�һ�����ĳ��󡣽ӿ��Ƕ�һϵ����Ϊ�ĳ���

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
// ѧ��ʵ����ѧϰ��˯������������
public class Student implements Sleep,Study{
	@Override
	public void sleepBed(){
		System.out.println("��˯����");
	}
	
	@Override
	public void studied(){
		System.out.println("����ѧϰ");
	}
}
// ��ʦ��ʵ���˽̿κ�˯������������
public class Teacher implements Sleep,Teach{
	@Override
	public void sleepBed(){
		System.out.println("��˯����");
	}
	
	@Override
	public void teaching(){
		System.out.println("���ڽ̿�");
	}
}

```

## �쳣����

�������й����л����һЩ�����쳣��������ڳ��ִ���ʱ���ռȶ��߼��������С�

�쳣����ԭ��ͨ���������û�����Ƿ����ݡ�Ҫ�򿪵��ļ������ڡ�����ͨ���жϣ�JVM�ڴ������

java���������͵��쳣��������쳣������ʱ�쳣������

�쳣�����г��õĹؼ��֣�try, catch, finally, throw, throws��

�쳣��������̣�

```java
try{
	// �������
}catch(exceptiontype name){
	// �������
}finally{
	// �������
}

```
