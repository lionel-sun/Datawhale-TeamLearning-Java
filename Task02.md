# Task02 ��ʼJava���Ի���

## ������ͱ��ʽ

- ��������

Java��+,-,*,/,%�ֱ��ʾ�ӡ������ˡ�����ȡ�ࡣ
```java
    public static void day03(){
//        �Ӽ��˳�
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

���������£�
```
10+2=12
10-2=8
10*2=20
10/2=5.0
10%2=0
```

- ��ѧ����

��math���а����˺ܶ���ѧ����:ƽ�����������㣬���Ǻ�����ָ��������һЩ������

```java
    public static void day03(){
//        math����: 
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
	
- ��ϸ�ֵ��������Լ�������

����ʹ��+=��*=��%=�ȼ����ʽ��
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
++��ǰ������ɼ�1�ڽ������㣬++�ں�����ʹ�ñ���ԭ����ֵ��������.

- ��ϵ��boolean������Լ�λ����

��ϵ����������==������!=������>��С��<�����ڵ���>=��С�ڵ���<=��
!��ʾ�ǣ�&&��ʾ���롱��||��ʾ���򡱡�
��Ŀ�����x?y:z����x���ؽ��Ϊtrueʱ�ͷ���y����x���ؽ��Ϊfalseʱ�ͷ���z��

��������ʱ�򣬿��ԶԸ���λ�������㡣λ�����������&("and")��|("or")��^("xor")��~("not")��
���⻹��>>��<<�������λģ�����ƻ����ơ�

## ��������

- ��������

Java��ʹ�ã����еı�����������ڶ�Ӧ�����ڡ����ǲ�����Ƕ�׵ģ�����ʹ��ͬ��������

- �������

```java
	public static void  day04(){
//        �������
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

- ѭ�����

```java
	public static void  day04(){
//        ѭ�����
        int i = 10;
        while(i < 100){
            i = i + i/10;
        }
        System.out.println(i);
    }
```

- ȷ��ѭ��(forѭ��)

forѭ������һ��������һ���������ڶ�������ѭ�����������������Ǹ��µļ�������
�����Ҫ��forѭ������ʹ�ü�������ֵ����Ҫ��ѭ����ǰ�����ñ�����

```java
	public static void  day04(){
//        forѭ��
        for (int i = 1; i <= 10; i++){
			System.out.println(i);
		}
    }
```

- �жϿ����������

```java
	public static void  day04(){
//        �жϿ���
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

break�������˳���ǰѭ����continue�жϱ���ѭ������ִ��ѭ���ڵĵ�һ�����롣��forѭ���п����������²��֡�

- ����ѡ��switch��� 

```java
	public static void  day04(){
//        switch���
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
