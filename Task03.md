# 数组

## 什么是数组

数组是存放一组同类型数据的数据结构。Java语言中提供存储固定大小的同类型数据。

数组的定义方法:

```java
dataType[] arr = new dataType[n];//首选方法，n是数组长度

dataType arr[] = new dataType[n];//效果相同，非首选方法
```

new操作符是用来开辟数据空间的。

## 数组初始化

有两种方法可以给数组声明和赋值，数组范围起始值从0开始，如下5长度的数组下标分别是｛0，1，2，3，4｝。

```java
    public static void day05(){
        int[] arr1 = new int[5];
        int[] arr2 = new int[]{0,1,2,3,4};
        arr1[0]=0;
        arr1[1]=10;
        arr1[2]=20;
        arr1[3]=30;
        arr1[4]=40;
        for(int i=0; i<5; i++){
            System.out.println("第"+i+"个数字在arr1和arr2中");
            System.out.println(arr1[i]);
            System.out.println(arr2[i]);
        }
    }
```

## 多维数组

多维数组可以看成数组的数组，即数组中每一个元素也是数组。

多维数组的格式：dataType[][][] name = new dataType[length1][length2][length3]

多维数组既可以是规则长度，也可以是不规则长度。声明的时候必须声明“行”的长度,可以省略列的长度：int a[][] = new int[2][]。

多维数组创建有多种方式：前两种在创建时候赋值。第三种先分配空间，然后遍历赋值。遍历可以使用for循环遍历，两种写法如下。

```java
    public static void day05(){
//        多维数组
		/* 第一种方式 */
		int tdarr1[][] = { { 1, 3, 5 }, { 5, 9, 10 } };
		/* 第二种方式 */
		int tdarr2[][] = new int[][] { { 65, 55, 12 }, { 92, 7, 22 } };
		/* 第三种方式 */
        String[][][] juzi = new String[1][2][3];
        for(int i=0; i<1; i++){
            for(int j=0; j<2; j++){
                for(int k=0; k<3; k++){
                    juzi[i][j][k] = "多为数组坐标（"+i+","+j+","+k+")";
                }
            }
        }

        for(String[][] ele1:juzi){
            for(String [] ele2:ele1){
                for(String ele3:ele2){
                    System.out.println(ele3);
                }
            }
        }

    }
```