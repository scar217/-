##  第一题

```
编程实现简单的计算器功能，要求用户按如下格式从键盘输入算式：
操作数1  运算符op  操作数2
计算并输出表达式的值，其中算术运算符包括：加（+）、减（-）、乘（*）、除（/）、^(次幂）。
要求使其能进行浮点数的算术运算，同时允许使用字符*、x与X作为乘号，并且允许输入的算术表达式中的操作数和运算符之间可以加入任意多个空格符。 
**输入格式要求："%f %c%f" 提示信息："Please enter the expression:\n"
**输出格式要求："%f + %f = %f \n" "%f - %f = %f \n" "%f * %f = %f \n" "%f / %f = %f \n" "Division by zero!\n"  "%f ^ %f = %f \n" "Invalid operator! \n"
程序运行示例1如下：
Please enter the expression: 2.0 + 4.0
2.000000 + 4.000000 = 6.000000
程序运行示例2如下：
Please enter the expression: 2.0 - 4.0
2.000000 - 4.000000 = -2.000000
程序运行示例3如下：
Please enter the expression: 2.0 * 4.0
2.000000 * 4.000000 = 8.000000
程序运行示例4如下：
Please enter the expression: 2.0 x 4.0
2.000000 * 4.000000 = 8.000000
程序运行示例5如下：
Please enter the expression: 2.0 X 4.0
2.000000 * 4.000000 = 8.000000
程序运行示例6如下：
Please enter the expression: 2.0 / 4.0
2.000000 / 4.000000 = 0.5000000
程序运行示例7如下：
Please enter the expression: 2.0 / 0
Division by zero! 
程序运行示例8如下：
Please enter the expression:2.0 ^5.0
2.000000 ^ 5.000000 = 32.000000 
程序运行示例9如下：
Please enter the expression: 2.0 \ 4.0
Invalid operator!
```

~~~c
#include<stdio.h>
#include<math.h>
int main(){
     float dat1,dat2;
    char op,x,X;
    x='*';
    X='*';

    printf("Please enter the expression:\n");
    scanf("%f %c%f",&dat1,&op,&dat2);

    if (op=='+')
        printf("%f %c %f = %f\n",dat1,op,dat2,dat1+dat2);
    else if(op=='-')
        printf("%f %c %f = %f\n",dat1,op,dat2,dat1-dat2);
    else if((op=='*')||(op=='x')||(op=='X')){
        op = '*';
        printf("%f %c %f = %f\n",dat1,op,dat2,dat1*dat2);
    }
    else if(op=='/'){
        if(dat2==0)
        printf("Division by zero!\n");
    else
        printf("%f %c %f = %f\n",dat1,op,dat2,dat1/dat2);
    }
    else if(op=='^')
        printf("%f %c %f = %f\n",dat1,op,dat2,pow(dat1,dat2));
    else
        printf("Invalid operator!");




    return 0;
}
~~~

##  第二题 九九乘法表打印

```c
//九九乘法表
//先打印一行，再打印多行
#include <stdio.h>
#include <stdlib.h>
int main()

{

    int i,j;
    for(i=1;i<=9;i++){//因为每一行都在增加算式，所以使用for循环，且一行的列数由i来决定
        for(j=1;j<=i;j++){
            printf("%d*%d=%d  ",j,i,i*j);//最后一个%d后面空格，为同行中的下一列留间隙
        }
        printf("\n");//每行所有列输出后退出内循环并换行
    }

        return 0;

}
```

####  输入一行字符，分别统计其中每个元音字母（a、e、i、o、u不分大小写）的个数。
**输入格式要求：信息提示："Input a line of characters:\n"
**输出格式要求："%4d"
程序的运行示例如下：
Input a line of characters:
How old are you?
   1   1   0   3   

```c
#include<stdio.h>
#include<math.h>
int main(void)
{
    int a=0,i=0,j=0,x=0,c=0;
    char ch;
    printf("Input a line of characters:\n");


    do{
            scanf("%c",&ch);
        if(ch=='a'||ch=='A'){
            i++; 
        }
        if(ch=='e'||ch=='E'){
            j++;  
        }
        if(ch=='i'||ch=='I'){
            a++;
        }
        if(ch=='o'||ch=='O'){
            x++;
        }
        if(ch=='u'||ch=='U'){
            c++;
        }
    }while(ch!=10);
    printf("%4d%4d%4d%4d%4d",i,j,a,x,c);

    return 0;
}
```

##  第三题  打印金字塔

```c
//金字塔
/*    *      //1个* (2*i-1)=2*1-1=1 空格有4个 （总的层数-i）=5-1=4
     ***     //3个* (2*i-1)=2*2-1=3 空格有3个 （总的层数-i）=5-2=3
    *****    //5个* (2*i-1)=2*3-1=5 空格有2个 （总的层数-i）=5-3=2
   *******   //7个* (2*i-1)=2*4-1=7 空格有1个 （总的层数-i）=5-4=4
  *********  //9个* (2*i-1)=2*5-1=9 空格有0个 （总的层数-i）=5-5=0
*/
#include <stdio.h>
#include <stdlib.h>
int main()
{
    int i,j;
    int a;
    for(i=1;i<=5;i++){//可以把‘5’改成输入值，随意改变其金字塔层数
        for(a=1;a<=5-i;a++){//输出空格
            printf(" ");
        }
        for(j=1;j<=2*i-1;j++){
                printf("*");
        }
        printf("\n");
    }
        return 0;
}
```

##  第四题  素数

###  第7章实验任务4：
##  任意输入一个整数m，若m不是素数，则输出其所有不包括1和自身的因子；否则输出“没有因子，是素数”的相关提示信息。

输入提示信息："Please enter a number:"
输入格式："%d"
输出格式：
有因子时："%d\n"
无因子时："It is a prime number.No divisor!\n"
输入为1，0，-1时："It is not a prime number.No divisor!\n"

程序运行示例：
Please enter a number:8![img](file:///C:\Users\asus\AppData\Roaming\Tencent\QQTempSys\{G]K_~VQ2`J3FND@QJ6C9GT.png)
2
4

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int i,j;
    int k=0;

    printf("Please enter a number:");
    scanf("%d",&i);

    if(i==1||i==0||i==-1){
        printf("It is not a prime number.No divisor!\n");
    }
    else{
        for(j=2;j<i;j++){
            if(i%j==0)
            {
                printf("%d\n",j);
                k++;
            }
        }
        if(k==0){
            printf("It is a prime number.No divisor!\n");
        }

    }

    return 0;
}

```

##  第五题 字符串的比较

***函数strcmp()***

``` c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    char name[10];
    char password[10];
    int i,chance=3;//i循环变量
    int loginCount=chance;//值传递

    for(i=1;i<=loginCount;i++){
        printf("\n请输入名字：");
        scanf("%s",name);
        printf("\n请输入密码：");
        scanf("%s",password);

        if(strcmp("周泳屹",name)==0&&strcmp("888",password)==0){//判断字符串相同使用strcmp
        printf("登录成功");
        break;//for+break
        }
        else{//机会次数减少
            chance--;
        printf("你还有%d次机会",chance);
        }
  }

    return 0;
}
```

## 第六题 上三角九九乘法表

#### ****输入提示信息**: "Input n:\n"

****输入数据格式**: "%d"
****表头第一行输出格式"%4d" （需要循环，行尾有回车）
**** 表头第二行输出格式"   -"   （需要循环，行尾有回车）
****输出数据格式: "%4d"          （需要循环，行尾有回车）

>```c
>编写程序，打印输出如下图所示的乘法九九表：
>   1   2   3   4   5   6   7   8   9
>   -   -   -   -   -   -   -   -   -
>   1   2   3   4   5   6   7   8   9
>       4   6   8  10  12  14  16  18
>           9  12  15  18  21  24  27
>              16  20  24  28  32  36
>                  25  30  35  40  45
>                      36  42  48  54
>                          49  56  63
>                              64  72
>                                  81
>****输入提示信息**: "Input n:\n"
>****输入数据格式**: "%d"
>****表头第一行输出格式"%4d" （需要循环，行尾有回车）
>**** 表头第二行输出格式"   -"   （需要循环，行尾有回车）
>****输出数据格式: "%4d"          （需要循环，行尾有回车）
>注：
>   1)若输入9，则打印结果为：
>   1   2   3   4   5   6   7   8   9
>   -   -   -   -   -   -   -   -   -
>   1   2   3   4   5   6   7   8   9
>       4   6   8  10  12  14  16  18
>           9  12  15  18  21  24  27
>              16  20  24  28  32  36
>                  25  30  35  40  45
>                      36  42  48  54
>                          49  56  63
>                              64  72
>                                  81
>   2)若输入6，则打印结果为：
>   1   2   3   4   5   6
>   -   -   -   -   -   -
>   1   2   3   4   5   6
>       4   6   8  10  12
>           9  12  15  18
>              16  20  24
>                  25  30
>                      36
>   3)若输入4，则打印结果为：
>   1   2   3   4
>   -   -   -   -
>   1   2   3   4
>       4   6   8
>           9  12
>              16
>```

```c
#include <stdio.h>
int main(void){
    int i,j=0;
    int a,b;
    int n,k;

    printf("Input n:\n");
    scanf("%d",&n);

    for(a=1;a<=n;a++){
        printf("%4d",a);
    }
    printf("\n");
    for(b=1;b<=n;b++){
        printf("   -");
    }
    printf("\n");
    for(i=1;i<=n;i++){
            for(k=1;k<i;k++){
                printf("    ");//空隙递增
            }

        for(j=i;j<=n;j++){
            printf("%4d",i*j);
        }
        printf("\n");

    }

    return 0;
}

```

## 第七题：

**递推法。 8除不尽的自然数。一个自然数被8除余1，所得的商被8除也余1，再将第二次的商被8除后余7，最后得到一个商为a，又知这个自然数被被17除余4，所得的商被17除余15，最后得到一个商为a的2倍，求这个自然数。**

**输出格式要求："The required number is :%d\n"

```c
//先将所有需要除的数作除，并保留最后的商，最后用选择控制语句进行余数是否达标筛选，第二个选择控制语句同理。
#include <stdio.h>
int main(void)
{
    int i,j,k;
    int a,b,c,n;
    for(n=15;;n++)
    {
        a=n/8;
        b=a/8;
        c=b/8;
        if(n%8==1 && a%8==1 && b%8==7)
        {
            i=n/17;
            j=i/17;
            if(n%17==4 && i%17==15 && j==2*c){
                printf("The required number is :%d\n",n);
                break;
            }
        }
    }
    return 0;
}

```

## 第八题 函数调用：

**在一种室内互动游戏中，魔术师要每位观众心里想一个三位数abc（a、b、c分别是百位、十位和个位数字），然后魔术师让观众心中记下acb、bac、bca、cab、cba五个数以及这5个数的和值。只要观众说出这个和是多少，则魔术师一定能猜出观众心里想的原数abc是多少。例如，观众甲说他计算的和值是1999，则魔术师立即说出他想的数是443，而观众乙说他计算的和值是1998，则魔术师说：“你算错了！”。请编程模拟这个数字魔术游戏。
提示：参数是五个数的和，返回值是abc,如果找不到 abc, 返回-1.**
**输入格式要求："%d" 提示信息："Input a sum:"
**输出格式要求："The sum you calculated is wrong!\n" "The number is %d\n"
程序运行示例如下：
Input a sum:1999
The number is 443

```c
#include<stdio.h>
int cal(int sum1);//声明被调原函数
int main()
{
    int sum,abc;
    printf("Input a sum:");
    scanf("%d",&sum);
    abc = cal(sum);//函数调用
    if(abc!=-1){
        printf("The number is %d\n",abc);
    }
    else
        printf("The sum you calculated is wrong!\n");

    return 0;
}
int cal(int sum1)//被调函数的定义
{
    int a,b,c;
    int sum2,sum3,sum4,sum5,sum6,sum7;
    for(a=1;a<10;a++){
        for(b=1;b<10;b++){
            for(c=1;c<10;c++){
                    sum7=a*100+b*10+c;
                    sum2=a*100+c*10+b;
                    sum3=b*100+a*10+c;
                    sum4=b*100+c*10+a;
                    sum5=c*100+a*10+b;
                    sum6=c*100+b*10+a;

                if(sum1==sum2+sum3+sum4+sum5+sum6){
                    return sum7;//满足条件，返回sum7
                }

            }
        }
    }
        return -1;//不满足条件，推出循环后，返回-1，结合主函数的条件控制，输出不同的语句

}
```

## 第九题  将一维数组逆序：

**定义函数ReverseOrder将一维数组逆序（对应位置数据交换）。
主函数中输入10个整数，然后调用函数ReverseOrder将其逆序并输出逆序后的结果。
输入提示："input 10 numbers:"
输入格式："%d"
输出格式："%5d"**

**程序运行结果示例：
input 10 numbers: 5 8 7 6 5 4 2 8 0 9
  9  0  8  2  4  5  6  7  8  5**

```c
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
void ReverseOrder(int arr[]);
int main()
{
    int i,arr[10];
    printf("input 10 numbers:");
    for(i=0;i<10;i++){
        scanf("%d",&arr[i]);
    }
    ReverseOrder(arr);//无返回值的函数调用
    return 0;

}
void ReverseOrder(int arr[])
{
    int i,j=9;
    int sum;
    for(i=0;i<=4;i++){
        sum=arr[i];
        arr[i]=arr[i+j];
        arr[i+j]=sum;
        j-=2;
    }
    for(i=0;i<10;i++){
        printf("%5d",arr[i]);
    }
}
```

## 第十题：

```
删除数组中的重复元素
给定一维整型数组array（数组大小不超过100），如果数组中的某个元素与排在它之后的元素重复，则对其进行删除，直到数组中没有重复元素为止。保证剩余元素的相对次序保持不变，输出删除重复元素后的数组。首先输入数组大小，输入格式为"%d"，然后依次输入数组中的元素，输入格式为“%d”，依次输出删除重复元素后的数组中的每个元素，输出格式为“%d ”
程序运行示例：
6↙
4 6 3 9 6 8↙
4 3 9 6 8
```

```c
#include <stdio.h>
#define N 1000
#define FLAG -1
void main( )
{		         	   
    int r[N], length, i, j;
    scanf("%d", &length); //1
    for (i = 0; i < length; i++)
        scanf("%d", &r[i]); //1
    for (i = length-1; i >=0 ; i--)
    {		         	   
        if (r[i] != FLAG) //1
        {		         	   
            for (j = i - 1; j >=0; j--) //1
                if (r[j] == r[i]) r[j] = FLAG; //1
        }
    }
    for (i = 0; r[i] != FLAG; i++); //1
    for (j = i + 1; j < length;)
    {		         	   
        if (r[j] != FLAG)  //1
           r[i++] = r[j++]; //1
        else j++; //1
    }
    length = i;
    for (i = 0; i < length; i++)
        printf("%d ", r[i]); //1
}	
```

## 第十一题：

```
程序：检查数中重复出现的数字。
用户输入数后，程序显示信息Repeated digit或No Repeated digit：
Enter a number: 28212
Repeated digit
数28212有一个重复的数字（2），而数9357则没有。
**输入格式要求："%ld" 提示信息："Enter a number :"
**输出格式要求："Repeated digit\n\n" "No Repeated digit\n\n"

程序运行示例1：
Enter a number :67
No Repeated digit
程序运行示例2：
Enter a number :2556
Repeated digit
```

```c
#include<stdio.h>
#include<stdlib.h>
int main()
{
    long n;
    int i=0,a,sum=0;
    int j,b=0;
    int arr[20];
    printf("Enter a number :");
    scanf("%ld",&n);
    do{
        a = n%10;
        n = n/10;
        arr[i] = a;
        i++;
        sum++;
    }while(n!=0);
    for(i=0;i<sum;i++){
        for(j=i+1;j<sum;j++){
            if(arr[i]==arr[j]){
                printf("Repeated digit\n\n");
                b++;
                exit(0);
            }
            else
                continue;
        }
    }
    if(b==0){
        printf("No Repeated digit\n\n");
    }
    return 0;

}
```

## 第十二题：递归函数

```题目
根据如下性质，设计函数MaxCommonFactor()，计算两个正整数的最大公约数。
性质1：当a>b时，计算a与b的公约数等价于计算a-b与b的公约数。
性质2：当a<b时，计算a与b的公约数等价于计算b-a与b的公约数。
性质3：当a=b时，a与b的公约数等于a或b。
```

```c
#include<stdio.h>
#include<stdlib.h>
int MaxCommonFactor(int a,int b);
int main()
{
    int a,b,x;
    printf("Input a,b:");
    scanf("%d,%d",&a,&b);
    x = MaxCommonFactor(a,b);
    if(x<0)
    {
        printf("Input Error!\n");
    }
    else
    {
        printf("%d\n",x);
    }
    return 0;
}
int MaxCommonFactor(int a,int b)
{
    int x;
    if(a>b){
        x = MaxCommonFactor(a-b,b);//调用自己，直到
    }
    else if(a<b){
        x = MaxCommonFactor(a,b-a);
    }
    else if(a==b){
        return a;
    }
}
```

## 第十三题：指针指定数组首尾地址

题目内容：
英文中有很多的回文词，回文词的拼法十分有趣，无论是从前往后拼读，还是从后往前拼读，他们的拼法和词义都不变。例如：dad（爸爸），mum（妈妈），noon（中午），eve（前夕），eye（眼睛），pop（流行），deed（行为），level（水平）等。简单地说，“回文”就是指顺读和倒读都一样的字符串。现在请你编程输入一个单词，判断它是否是回文。
提示：
（1）设置两个指针pStart和pEnd，让pStart指向字符串首部，让pEnd指向字符串尾部。
（2）利用循环从字符串两边对指针所指字符进行比较，当对应的两字符相等且两指针未超越对方时，使指针pStart向前移动一个字符位置（加1），使指针pEnd向后移动一个字符位置（减1），一旦发现两字符不等或两指针已互相超越（不可能是回文），则立即停止循环。
（3）根据退出循环时两指针的位置，判断字符串是否为回文。

```c
#include<stdio.h>
#include<stdlib.h>
int main()
{
    char *pStar;
    int sum=1;
    char arr[50];
    pStar = arr;
    printf("Input string:");
    gets(arr);
    char *pEnd = arr + strlen(arr)-1;//strlen()算出字符数组长度，用首地址加上
                                     //字符串长度减1（首地址自身的长度）即是数组末尾地址
    for(;pStar<=pEnd;pStar++,pEnd--){
        if(*pStar!=*pEnd){          //该地址对应字符是否一样的比较
            sum = 0;
            break;
        }

    }
    if(sum==1)
    printf("Yes!\n");
    else
        printf("No!\n");
    return 0;
}
```

## 第十四题：将10进制转换成2进制：

**转化思路：“除2求余，逆序排序”，既就是用十进制数除以2，可以得到一个商和余数；将余数保存起来，用商再去除以二，再得到一个商和余数，反复进行，直到商小于1时结束；然后将之前所得的余数逆序输出，得到的就是该十进制数的二进制写法。**

```c
#include <stdio.h>
int main()
{
    short arr[16]={0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0};
    short n;
    int i=0,j;
    printf("n=");
    scanf("%d",&n);
    do{
        arr[i] = n % 2;
        n = n / 2;
        i++;
    }while(n!=0);
    printf("the binary number is ");
    for(j=15;j>=0;j--){
        printf("%d",arr[j]);
    }

    return 0;
}
```

## 第十五题：最大值最小值，求最大公约数：

```要求
求最大数和最小数的最大公约数
从键盘输入10个正整数，求出最大数，最小数，以及他们的最大公约数。要求用数组实现。
```

```c
#include<stdio.h>
int main()
{
    int arr[10];
    int i,j,tem;
    int min,max;
    printf("Input 10 numbers:\n");
    //冒泡排序求最大值最小值
    for(i=0;i<10;i++){
        scanf("%d",&arr[i]);
    }
    for(j=0;j<9;j++){
        for(i=0;i<9-j;i++){
           if(arr[i]>arr[i+1]){
            tem = arr[i];
            arr[i] = arr[i+1];
            arr[i+1] = tem;
           }
        }
    }
    min = arr[0];
    max = arr[9];
    printf("maxNum=%d\n",arr[9]);
    printf("minNum=%d\n",arr[0]);
    //求最大公约数：
    do{
            if(max==min){
                printf("%d",max);
                break;
                }
            else if(max>min){
                    max=max-min;
                }
                else if(min>max){
                    min=min-max;
                }

    }while(min>0&&max>0);
}
```

### 求最大公约数的方法（三种）：

==(1)辗转相除法==

有两整数a和b：

① a%b得余数c

② 若c=0，则b即为两数的最大公约数

③ 若c≠0，则a=b，b=c，再回去执行①

例如求27和15的最大公约数过程为：

27÷15 余1215÷12余312÷3余0因此，3即为最大公约数

==⑵ 相减法==

有两整数a和b：

① 若a>b，则a=a-b

② 若a<b，则b=b-a

③ 若a=b，则a（或b）即为两数的最大公约数

④ 若a≠b，则再回去执行①

例如求27和15的最大公约数过程为：

27－15＝12( 15>12 ) 15－12＝3( 12>3 )

12－3＝9( 9>3 ) 9－3＝6( 6>3 )

6－3＝3( 3==3 )

因此，3即为最大公约数

==⑶穷举法==

有两整数a和b：

① i=1

② 若a，b能同时被i整除，则t＝i

③ i++

④ 若 i <= a(或b)，则再回去执行②

⑤ 若 i > a(或b)，则t即为最大公约数，结束

改进：

① i= a(或b)

② 若a，b能同时被i整除，则i即为最大公约数，

结束

③ i–，再回去执行②

有两整数a和b：

① i=1

② 若a，b能同时被i整除，则t＝i

③ i++

④ 若 i <= a(或b)，则再回去执行②

⑤ 若 i > a(或b)，则t即为最大公约数，结束

改进：

① i= a(或b)

② 若a，b能同时被i整除，则i即为最大公约数，

结束

③ i–，再回去执行②

## 第十六题：

![](C:\Users\asus\Pictures\Screenshots\QQ图片20210116115138.jpg)

#### 众数：

```c
#include<stdio.h>
#define N 40
int Midnumber(int arr[],int n);
int Average(int arr[],int n);
int Mostnumber(int arr[],int n);
int main()
{
   int arr[N],n=0;
   int Mean,Median,Mode,i;
   printf("Input the feedbacks of 40 students:\n");
   for(i=0;i<N;i++){
     scanf("%d",&arr[i]);
     n++;
   }
   //平均数：
   Mean = Average(arr,n);

   //众数：
   Mode =  Mostnumber(arr, n);
   //中位数：
   Median =  Midnumber(arr,n);
    printf("Mean value=%d\n",Mean);
    printf("Median value=%d\n",Median);
    printf("Mode value=%d\n",Mode);
}
//计算中位数：
int Midnumber(int arr[],int n)
{
    int i,j;
    int tem;
    for(j=0;j<n-1;j++){
        for(i=0;i<n-1-j;i++){
            if(arr[i]>arr[i+1]){
                tem = arr[i];
                arr[i] = arr[i+1];
                arr[i+1] = tem;
            }
        }
    }
    return (arr[19]+arr[20])/2;
}
//计算平均数：
int Average(int arr[],int n)
{
    int i,sum=0;
    for(i=0;i<n;i++){
        sum+=arr[i];
    }
    return sum/n;
}
//计算众数：
int Mostnumber(int arr[],int n)
{
    int i,j,max=0,b;
    int a[10]={0,0,0,0,0,0,0,0,0,0};
    for(i=0;i<n;i++){
        if(arr[i]==1){
            a[0]+=1;
        }
        if(arr[i]==2){
            a[1]+=1;
        }
        if(arr[i]==3){
            a[2]+=1;
        }
        if(arr[i]==4){
            a[3]+=1;
        }
        if(arr[i]==5){
            a[4]+=1;
        }
        if(arr[i]==6){
            a[5]+=1;
        }
        if(arr[i]==7){
            a[6]+=1;
        }
        if(arr[i]==8){
            a[7]+=1;
        }
        if(arr[i]==9){
            a[8]+=1;
        }
        if(arr[i]==10){
            a[9]+=1;
        }
    }
    for(j=0;j<10;j++){
        if(max<a[j]){
            max=a[j];
            b = j;
        }
    }
    return b+1;
}
```

## 第十七题：

```要求
有n个人围成一圈，顺序排号。从第一个人开始报数（从1到3报数），凡报到3的人退出圈子，问最后留下的是原来第几号的那位。
**输入格式要求："%d" 提示信息："please input the total of numbers:"
**输出格式要求："%d is left\n" 
程序运行示例如下：
please input the total of numbers:30
29 is left
```

```c
#include<stdio.h>
int main(int argc, char *argv[])
{
    int i, j = 0, k = 0, n;
    int a[30] = {0};
    printf("please input the total of numbers:");
    scanf("%d", &n);
    for (i=0; i<n; i++)
    {
        a[i] = 1;//1代表活着，0代表出局
    }
    for (i=1; i<4; i=i%3+1)//控制i的值在[0，3]
    {
        if (3==i && a[j]!=0)
        {
            a[j] = 0;
            k++;
            if (n-1 == k)
            break;
            j = (j+1)%n;
            continue;
        }
        if (0 == a[j])
        {
            j = (j+1)%n;
            i--;
            continue;
        }
        j = (j+1)%n;
    }
    for (i=0; i<n; i++)
    {
        if (1 == a[i])
        printf("%d is left\n", i+1);
    }
}

```

## 第十八题：

```c

有趣的“回文”检测(用指针实现）
英文中有很多的回文词，回文词的拼法十分有趣，无论是从前往后拼读，还是从后往前拼读，他们的拼法和词义都不变。例如：dad（爸爸），mum（妈妈），noon（中午），eve（前夕），eye（眼睛），pop（流行），deed（行为），level（水平）等。简单地说，“回文”就是指顺读和倒读都一样的字符串。现在请你编程输入一个单词，判断它是否是回文。
要求：
（1）设置两个指针pStart和pEnd，让pStart指向字符串首部，让pEnd指向字符串尾部。
（2）利用循环从字符串两边对指针所指字符进行比较，当对应的两字符相等且两指针未超越对方时，使指针pStart向前移动一个字符位置（加1），使指针pEnd向后移动一个字符位置（减1），一旦发现两字符不等或两指针已互相超越（不可能是回文），则立即停止循环。
（3）根据退出循环时两指针的位置，判断字符串是否为回文。
程序的两次运行结果如下：
第1次
Input string:ABCCBA↙
Yes!
第2次
Input string:student↙
No!
输入格式: 字符串输入用gets()函数
输出格式：
输入提示信息："Input string:"
输出信息，不是回文："No!\n"
输出信息，是回文："Yes!\n"
```

```c
#include<stdio.h>
int main(void)
{
    char str[10];
    int i,j;
    char *pStart,*pEnd;
    printf("Input string:");
    gets(str);
    pStart = str;
    pEnd = str[strlen(str)-1];//指针指向数组末尾
    i = 0;
    j = strlen(str)-1;
    while(i<=j){
        if(*pStart != *pEnd){
            break;
        }
        pStart++;
        i++;
        pEnd--;
        j--;
    }
    if(i>=j){
        printf("Yes!\n");
    }else{
        printf("No!\n");
    }
}

```

## 第十九题：

```题目
输入5个字符串，输出其中最小的字符串。
**输入格式要求："%s"
**输出格式要求："min is %s\n"
程序运行示例如下：
first        <===输入5行字符串
second
third
44444
555555
min is 44444  <===此行为输出
```

```c
#include<stdio.h>
#include<string.h>
int main(void)
{
    char arr[5][10];
    char arr1[10];
    int i=0;
    for(i=0;i<5;i++){
        scanf("%s",&arr[i]);
    }
    strcpy(arr1,arr[0]);

    for(i=0;i<5;i++){
        if(strcmp(arr1,arr[i])>0){//字符串大小比较
            strcpy(arr1,arr[i]);//字符串赋值
        }
    }
    printf("min is %s\n",arr1);
}
```

## 第二十题：考试题

```题目
将一个字符串插入至另一个源字符串的某个位置：
将一个字符串2插入到源字符串1中 第一次出现某字符的位置，并打印出形成的新串。
如果 字符串1中找不到输入的字符， 则显示“Not found!”并结束程序。
注：源字符串长度及待插入字符串长度不超过50


提示信息：
printf("Input source string 1:\n")
printf("Input inserted string 2:\n")
printf("Input a letter to locate the index:\n")

输出信息格式：
printf("The new string is:%s")
printf(“Not found!”)

测试样例1：
输入信息：
Input source string 1:
abcdecfg
Input inserted string 2:
*-*-*-*
Input the a letter to locate the index:
c
输出结果：
The new string is:ab*-*-*-*cdecfg

测试样例2：
输入信息：
Input source string 1:
abcdecfg
Input inserted string 2:
****
Input the a letter to locate the index:
h
输出结果：
Not found!
```

```c
#include<stdio.h>
#include<string.h>
int main(void)
{
    char str0[20],str1[20],str2[20];
    char arr[20],ch;
    int i=0,j=0,flag = 0;
    printf("Input source string 1:\n");
    gets(str0);
    printf("Input inserted string 2:\n");
    gets(arr);
    printf("Input a letter to locate the index:\n");
    scanf("%c",&ch);
    for(int g = 0;g<strlen(str0);g++){
        if(str0[g] == ch){
            flag = 1;
        }
    }
    if(flag == 1){
    while(str0[i]!=ch){
        str1[i]=str0[i];
        i++;
    }
    str1[i+1] = '\0';
    while(str0[i]!='\0'){
        str2[j] = str0[i];
        j++;
        i++;
    }
    str2[j+1] = '\0';
    strcat(str1,arr);
    strcat(str1,str2);
    printf("%s\n",str1);
    }
    else{
        printf("Not found!");
    }
}

```

## 第二十一题：指针数组：

```题目
写一个程序提示用户输入姓名，然后在一个保存在数组中的名字列表中查找该姓名，如果找到则显示适当的欢迎信息，否则显示“名字没有找到”。
名字列表为：{"abc", "bbc", "ccc", "Hello", "John", "Tome"};
**提示信息："请输入一行字符："
**输出格式要求："欢迎你，%s！"  "名字没有找到！"
程序运行示例1：
请输入一行字符：bbc
欢迎你，bbc！
程序运行示例2:
请输入一行字符：hell
名字没有找到！
```

```c
#include "stdio.h"
int main(){
    int flag = 0;
    char *p[6]={"abc", "bbc", "ccc", "Hello", "John", "Tome"};//指针数组存放字符串
    char str[10];
    printf("请输入一行字符：");
    scanf("%s",&str);
    for (int i = 0; i < 6; ++i) {
        if(strcmp(p[i],str)==0){
            printf("欢迎你，%s",p[i]);
            flag=1;
            break;
        }
    }
    if(flag==0){
        printf("名字没有找到！");
    }
}
```

## 第二十二题：查找子字符串数量：

```题目
用函数编程实现计算字符串中子串出现的次数
```

```c
#include <stdio.h>
#include <string.h>

int subString(char *str,char *sub)
{
    int count = 0, i, j;
    for (i = 0; i < strlen(str); i++) {
        for (j = 0; j < strlen(sub); j++) {
            if(str[i + j] != sub[j]) {//选择不同的比较起始点与子字符串比较
                break; // 出现了不同字符就退出循环
            }
        }
        if (j == strlen(sub)) {
            count++; // 退出循环后若j的值等于子串的长度，则存在子串
        }
    }
    return count;
}

int main(void)
{
    char str[100],sub[50];
    printf("请输入母串：");
    gets(str);
    printf("请输入子串：");
    gets(sub);
    printf("%d", subString(str,sub));
    return 0;
}
```

## 第二十三题：结构体初始化，字符串不考虑大小写的比较：

```c
#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
#include<string.h>
struct Candidate
{
	char name[10];
	int count;
};
int main()
{
	struct Candidate arr[3] = {
		"li",0,"zhang",0,"wang",0
	};
	int i = 0, j = 0;
	char s[10];
	int wrong = 0;
	int flag = 0;
	for (i = 0; i < 10; i++)
	{
		flag = 0;
		printf("Input vote %d:", i + 1);
		scanf("%s", s);
		for (j = 0; j < 3; j++)
		{
			if (strcasecmp(arr[j].name, s) == 0)//不考虑大小写字符串的比较
				{
				    arr[j].count++;
                    flag = 1;
				}
		}
		if (flag == 0)
		{
			wrong++;
		}
	}
	printf("Election results:\n");
	for (i = 0; i < 3; i++)
	{
		printf("%8s:%d\n", arr[i].name, arr[i].count);
	}
		printf("Wrong election:%d\n", wrong);
}
```

## 第二十四题：链表输入、寻找、插入

```c

在一个有序(按非递减顺序)的链表中插入一个元素为x的结点，使插入后的链表仍然有序（链表数据域为整型数，N为6）。
**输入提示："输入数组6个元素的值。\n"
**输入格式："%d"
**输出提示："此链表各个结点的数据域为："
**输出格式："%d "   (注：所有数据输出结束后有一个回车)
**输入提示："输入要插入的数据x:"
**输入格式："%d"
**输出提示："插入后链表各个结点的数据域为："
**输出格式："%d "  (注：所有数据输出结束后有一个回车)
   

程序运行示例如下：
输入数组6个元素的值。↙
12 23 34 45 56 67
此链表各个结点的数据域为：12 23 34 45 56 67 ↙
输入要插入的数据x:36
插入后链表各个结点的数据域为：12 23 34 36 45 56 67↙
```

```c
/*
在一个有序(按非递减顺序)的链表中插入一个元素为x的结点，
使插入后的链表仍然有序（链表数据域为整型数，初始时输入6个元素）。
程序运行示例如下：
输入数组6个元素的值。
12 23 34 45 56 67
此链表各个结点的数据域为：12 23 34 45 56 67 
输入要插入的数据x:36
插入后链表各个结点的数据域为：12 23 34 36 45 56 67 
*/

#include <stdio.h>
#include <stdlib.h>

struct num                                  //1.准备工作-结构体定义
{                                           //结构体包含：
	int a;                                  //①数据
	struct num *pNext;                      //②指针
};

#define SIZE sizeof(struct num)             //2.宏定义SIZE, 方便后续分配内存

struct num *CreatLiList(void)               //3.函数-返回结构体指针-建立链表
{
	struct num *spHead,*spPre,*spCur;       //头, 前, 现
	int n, count = 0;                      
	spPre  = (struct num *)malloc(SIZE);    //给Pre分配内存
	spHead = spPre;                         //Head指向Pre
	spHead -> pNext = NULL;                 //头结点中的②指针指向NULL
    
	do 
	{
		scanf("%d",&n);                     //输入数据
		if (count != 6)                     //结束标志
		{
            count ++;
			spCur = (struct num *)malloc(SIZE);  //给Cur分配内存

			spCur -> a = n;                      //赋予Cur①数据

			spCur -> pNext = NULL;               //Cur②指针指向NULL

			spPre -> pNext = spCur;              //Cur移到下一个
			spPre = spCur;                       //Pre移到Cur
		}
	} while (count != 6);                        //结束标志
	return spHead;                               //返回头节点, 成功创建链表
}


int AddNode(struct num *sp, int x)                   //函数-插入节点-传入头结点、插入数据
{
	struct num *spCur,*spNew;
	spCur = sp;
    int flag = 1;
	while((spCur -> pNext)->a < x)
	{
	    spCur = spCur -> pNext; 	
	}                                                //退出循环时，x 要插入Cur 与 Cur->next 之间

	spNew = (struct num *)malloc(SIZE);
	if (spNew == NULL)  return 1;
	
	spNew -> a = x;                                  //赋值
                                                     //e.g. 原来a→c，加入b后，a→b→c
    spNew -> pNext = spCur -> pNext ;                //让b→的 指向 a→的
    spCur -> pNext = spNew;  						//把a→的 改为 b
    
    return 1;
}



void TraverLiList(struct num *sp)                 //函数-遍历链表-传入头结点
{
	struct num *spCur;
	spCur = sp -> pNext;
	while (spCur != NULL)
	{
		printf("%d ", spCur->a);
		spCur = spCur -> pNext;
	}
}

int main()
{
	printf("输入数组6个元素的值。\n");
    struct num* head = CreatLiList();
    printf("此链表各个结点的数据域为：");
    TraverLiList(head); 
	printf("\n");
    int x;
    printf("输入要插入的数据x:");
    scanf("%d", &x);
    int i = AddNode(head, x);
    printf("插入后链表各个结点的数据域为：");
    TraverLiList(head); 
    return 0;
}
```

## 第二十五题：链表删除、创建

```题目
n个人围成一圈，顺序编号。从第一个人开始从1到m报数，凡报到m的人退出圈子，编程求解最后留下的人的初始编号。
程序运行示例：
6 3（两个输入数据之间有空格）
1

输入格式：scanf("%d%d",&n,&m);
输出格式：printf("%d\n",loop[dest]);
```

```c
struct Person{
    int ID;
    struct Person *next;
};
#include <malloc.h>
#include <stdio.h>

#define N sizeof(struct Person)
struct Person* Build(int n){//创建n个人
    struct Person *head,*Pt,*endPt;
    Pt = (struct Person*) malloc(N);
    Pt->ID = 1;
    head = Pt;
    endPt = Pt;
    if(n==1){
        head->next = head;
        return head;
    }
    for (int i = 2; i <= n ; ++i) {
        Pt = (struct Person*) malloc(N);
        Pt->ID = i;
        endPt->next = Pt;
        endPt = Pt;
    }
    endPt->next = head;
    return head;
}
struct Person *Delete(struct Person *h,int m){
    struct Person *head,*p,*mp;//mp做删除的目的指针
    int j;
    head = h;
    p = h;
    while (p->next!=p){
        for (int i = 2; i <= m - 1; ++i) {
            p = p->next;
        }
//        对此时所指的p的下一个结构体进行删除操作：
        mp = p->next;
        p->next = mp->next;
        free(mp);
        p = p->next;
    }
    return p;
}
int main() {
    int n,m;
    struct Person *head,*p;
    scanf("%d%d",&n,&m);
    head = Build(n);
    p = Delete(head,m);
    printf("%d\n",p->ID);
}
```
