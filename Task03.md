# ����

## ʲô������

�����Ǵ��һ��ͬ�������ݵ����ݽṹ��Java�������ṩ�洢�̶���С��ͬ�������ݡ�

����Ķ��巽��:

```java
dataType[] arr = new dataType[n];//��ѡ������n�����鳤��

dataType arr[] = new dataType[n];//Ч����ͬ������ѡ����
```

new�������������������ݿռ�ġ�

## �����ʼ��

�����ַ������Ը����������͸�ֵ�����鷶Χ��ʼֵ��0��ʼ������5���ȵ������±�ֱ��ǣ�0��1��2��3��4����

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
            System.out.println("��"+i+"��������arr1��arr2��");
            System.out.println(arr1[i]);
            System.out.println(arr2[i]);
        }
    }
```

## ��ά����

��ά������Կ�����������飬��������ÿһ��Ԫ��Ҳ�����顣

��ά����ĸ�ʽ��dataType[][][] name = new dataType[length1][length2][length3]

��ά����ȿ����ǹ��򳤶ȣ�Ҳ�����ǲ����򳤶ȡ�������ʱ������������С��ĳ���,����ʡ���еĳ��ȣ�int a[][] = new int[2][]��

��ά���鴴���ж��ַ�ʽ��ǰ�����ڴ���ʱ��ֵ���������ȷ���ռ䣬Ȼ�������ֵ����������ʹ��forѭ������������д�����¡�

```java
    public static void day05(){
//        ��ά����
		/* ��һ�ַ�ʽ */
		int tdarr1[][] = { { 1, 3, 5 }, { 5, 9, 10 } };
		/* �ڶ��ַ�ʽ */
		int tdarr2[][] = new int[][] { { 65, 55, 12 }, { 92, 7, 22 } };
		/* �����ַ�ʽ */
        String[][][] juzi = new String[1][2][3];
        for(int i=0; i<1; i++){
            for(int j=0; j<2; j++){
                for(int k=0; k<3; k++){
                    juzi[i][j][k] = "��Ϊ�������꣨"+i+","+j+","+k+")";
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