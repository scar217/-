![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-01-08_23-47-03.png)

==Java创建的类名要与文档名一致==

___

### GitHub Brash here操作

![添加需要上传的文档](F:\Java语言学习\笔记保存的截图\v2-b388715d84dc5363b65752d5a8f09920_720w.png)

![](F:\Java语言学习\笔记保存的截图\v2-5ecf63843ec0e35ef0236ca90c94cb4e_720w.png)

- git status ：查看仓库状态
- git init：创建一个空仓库，或者重新初始化一个已有仓库
- git add：把文件添加到可提交列表（临时缓冲区）
- git commit：提交改动（增删改）至仓库
- git log：打印提交日志
- git branch：查看、添加、删除分支
- git checkout：切换分支、标签
- git merge：合并分支
- git tag：新建、查看标签

#### git commit:

补充 **git commit**常见的用法有下面三个：

- **git commit -m “message”**，-m 参数表示可以直接输入后面的 “message” ，如果不加 -m 参数，那么是不能直接输入 message的，而是会调用一个编辑器一般是 vim 来让你输入这个 message。
- **git commit -a -m “massage”**，加的 -a 参数可以将**所有**已跟踪文件中的执行修改或删除操作的文件都提交到本地仓库，即使它们没有经过 git add 添加到缓存区，注意，新加的文件（即没有被 git 系统管理的文件）是不能被提交到本地仓库的。建议一般不要使用 -a 参数，正常的提交还是使用 git add 先将要改动的文件添加到暂存区，再用 git commit 提交到本地版本库。
- **git commit --amend**，追加提交，它可以在不增加一个新的commit-id的情况下将新修改的代码追加到前一次的commit-id中

#### 常规操作：

```注释
git add .   //添加所有文件
git commit -m"评论" //推入缓存区
git push    //推送远程仓
//推送失败：git config --global http.sslVerify false
```

### MySQL命令行操作：

> ```java
> net start mysql   -------启动服务器
> mysql -u root -p  -------打开数据库，输入密码登录
> ```
>
> [MySQL密码修改：](https://blog.csdn.net/qq_35436635/article/details/80126029?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522162126455316780274138877%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=162126455316780274138877&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-1-80126029.first_rank_v2_pc_rank_v29&utm_term=mysql%E8%BF%9E%E6%8E%A5navicat2059&spm=1018.2226.3001.4449)

### 一、电脑操作：

#### 常用的DOS命令：

>cmd :打开命令窗口
>
>```知识区块
>dir 列出当前目录的文件以及文件夹
>md 创建目录
>rd 删除目录
>cd 进入指定目录
>cd.. 退回到上一级目录
>cd\ 退回到根目录
>del 删除文件
>exit 退出DOS命令行
>```
>
>![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-01-08_23-24-31.png)

1. Java严格区分字母大小写
2. Java记事本编辑后缀：  .java 用记事本打开，用cmd执行

### 二、注释（comment）：

#### 注释类型：

1. 单行注释

   ```java
   //
   ```

2. 多行注释

   ```java
   class HelloZyy{
       /*多行注释：如下的main方法是程序的入口
       main的格式是固定的*/
   	public static void main(String[] args){
           //单行注释：如下语句表示输出到控制台
   		System.out.println("Hello,World!");
   	}
   }
   ```

3. 文档注释（java特有）

   ```java
   格式：
       /**
       内容1
       ......
       .....
       */
   ```

   **注释内容可以被JDK提供的工具javadoc所解析，生成一套以网页文件形式体现的该程序的说明文档。**

4. 程序的入口是main()方法。格式是固定的

5. 在一个java源文件中可以声明多个class。但是，只能最多有一个类声明为public的

6. **输出语句**:

   ```java
   System.out.println();//先输出内容，再换行
   System.out.print();//不对内容进行换行
   System.out.printf("%.2lf",num);//保留2位小数输出
   ```

7. 编译过程：编译后，会生成一个或多个字节码文件，字节码文件的文件名与java源文件中的类名相同。

8. 标识符命名规则：

   * 由26个英文字母大小写，0-9，_或$组成
   * 数字不可用于开头
   * 不可以使用关键字和保留字，但能包含关键字和保留字
   * Java中严格区分大小写，长度无限制
   * 标识符不能包含空格

#### Java中的名称命名规范：

1. 包名：多单词组成时所用字母都小写:xxxyyyzzz
2. 类名、接口名：多单词组成时，所有单词的首字母大写：XxxYyyZzz
3. 变量名、方法名：多单词组成时，第一单词首字母小写，第二个单词首字母大写:xxxYyyZzz
4. 常量名：所有字母都大写。多单词时每个单词用下划线连接：XXX_YY_ZZZ**(相同字母为一个单词)**

==注意：==java采用unicode字符集，因此标识符可以使用汉字声明，但是不建议使用。

### 三、数据类型：

**八种数据类型**

|            |                   |                     |                                   |
| ---------- | ----------------- | :-----------------: | --------------------------------- |
|            |                   |     1.数值型：      | a.整数类型（byte,short,int,long） |
|            |                   |                     | b.浮点类型（float,double）        |
|            | 一.基本数据类型： |  2.字符型（char）   |                                   |
| 数据类型： |                   | 3.布尔型（boolean） |                                   |
|            |                   |                     |                                   |
|            |                   |    1.类（class）    |                                   |
|            | 二.引用数据类型： | 2.接口（interface） |                                   |
|            |                   |   3.数组（ [ ] ）   |                                   |
|            |                   |                     |                                   |

==注意：==

* **byte**类型的范围：-128 ~ 127

* 声明long型变量，必须**以“L”或者“l”结尾**

  ```java
  long a = 37129173L
  long b = 21312313l
  ```

* **特殊的：long类型定义时，没有在数值末尾加 l或者L,自动为int型，超出int型长度会报错**

* **float**表示数值的范围比long还大

* 定义float类型变量时，变量要**以“f”或“F”结尾**

  ```java
  float a = 32.12f
  ```

* 直接使用==Unicode(字符的编码集) 值==来表示字符型常量（类同C语言的ASII码）

  ```java
  char z = '\u0043';//0043对应的字符是c
  ```

  * Unicode:一种编码，将世界所有的字符都纳入其中，每个字符都给予一个独一无二的编码，使用Unicode 没有乱码的问题。

* **布尔型**：boolean

  * 只能取两个值： **true   或者  false**
* 常常在条件判断、循环结构中使用

#### 数据类型的转换：

```java
public class Study{
    public static void main(String[] args){
        System.out.println(1024);//这是一个整数，默认是int类型
        System.out.println(3.14);//这是一个浮点数，默认是double类型
    }
}
```

#### 基本数据类型之间的运算规则：

**前提：**这里讨论只是7种基本数据类型变量间的运算，不包含boolean类型的

1. **自动类型转换（隐式）**

   * 规则：数据范围从小到大，

   * 结论：当容量小的数据类型的变量与容量大的数据类型的变量做运算时，结果自动提升为容量大的数据类型。（byte、char、short--->int--->long--->float--->double）

   * 此时的容量大小指的是，表示数的范围的大和小。比如：float容量要大于long的容量

   * 特别的：当byte、char、short三种类型的变量做运算时，结果为 int 型

   * ```java
     public class Study{
         public static void main(String[] args){
             //左边是long类型，右边是默认的int类型，左右类型不一样
             //一个等号代表赋值，将右侧的int常量交给左侧的long变量进行存储
             //int-->long;符合数据范围从小到大的要求。
             //这一行代码发生了自动类型的转换。
             long num1 = 100;
             System.out.println(num1);//100
             //左边是double类型，右边是float类型，左右不一样
             //float-->double,符合从小到大，发生自动转换
             double num2 = 2.4F;
             System.out.println(num2);//2.4
             //long数据类型转float类型
             //满足自动转换条件
             float num3 = 392L;
             System.out.println(num3);//392.0
         }
     }
     ```

2. **强制类型转换（显式）**

   * **格式**：

     ```java
     范围小的类型   范围小的变量名  =  (范围小的类型)   原本范围大的数据;
     int num = (int) 100L;
     ```

   * 需要使用强转换符  ：(转换成什么类型)转换前变量;

   * 可能导致精度损失、数据溢出。

   * ```java
     public class HelloWorld {
         public static void main(String[] args) {
             double d1 = 12.3;
             int i = (int)d1;
             System.out.println(i);//输出i = 12
         }
     }
     ```
     
   * **byte,short,char这三种类型在运算的时候，都会被首先提升为int类型，然后进行运算**
   
     ​                                              byte+byte--->int+int--->int（结果数据类型） 
   
     ```java
     public class Study{
         public static void main(String[] args){
     		byte num1=30;
     		byte num2=49;
     		byte num3 = num1+num2;//num3应该使用int类型来进行接收
             System.out.println(num3);//发出 byte-->int 可能会有精度损失的警告
         }
     }
     ```
   
   * **boolean类型不能发生数据转换**
   
   3.**自动转换**：
   
   * ```java
     public class Study1 {
     	public static void main(String[] args){
     		char a = '0';//有运算（加减乘除），char类型转为int类型输出
     		System.out.println(a);//48
     	}
     }
     ```

#### 编码表：

1. ASCII码表：美国信息交换标准代码
2. Unicode码表：万国码，开头0-127部分和ASCII完全一样，但是从128开始包含更多字符

### 四、变量：

* 在方法体外，类体内声明的变量称==成员变量==

* 在方法体内部声明的变量称为==局部变量==

  |          |            |                                    |
  | -------- | ---------- | ---------------------------------- |
  |          |            | a.实例变量（不以static修饰）       |
  |          | 1.成员变量 | b.类变量（以static修饰）           |
  | 所有变量 |            |                                    |
  |          | 2.局部变量 | a.形参（方法、构造器中定义的变量） |
  |          |            | b.方法局部变量（在方法内定义）     |
  |          |            | c.代码块局部变量（在代码块内定义） |

* ==注意：==二者在初始化值方面的异同：

  同：都有声明周期     异：局部变量除形参外，需显示初始化。

* 变量必须先赋值再使用。

* ==作用域==：从定义变量的一行开始，一直到直接所属的大扩号结束为止。

  ```java
  {int num = 50;
  System.out.println(num);//输出是50
  }
  System.out.println(num);//显示错误，没有定义num这个变量，需要重新定义
  ```

  #### 字符串变量(String)：

  * String不是基本数据类型，是引用数据类型：

    ```java
    //数据类型 变量名称 = 数据值;
    String str1 = "Hello,world";
    ```

    * **任何数据类型和字符串进行连接的时候，结果都会变成字符串**

    * ==对字符串使用+（加法运算），即是字符串的连接==

      ```java
      //String + int ---->  String
      String str1 = "Java";//定义一个字符串
      System.out.println(str1 + 20 + 30);//输出：Java2030
      ```

#### 连接符与加法运算符：

```java
public class study {
    public static void main(String[] args){
        int num=10;
        char a = 'c';
        String str = "Hello";
        System.out.println(num+a+str);//109Hello
        System.out.println(str+num+a);//Hello10c
        System.out.println(num+str+a);//10Helloc
    }
}
```

**规律**：

==变量用+号，没有出现String类型之前（+两边没有String类型）是加法运算符，遇到String类型后，此后+号代表字符连接符==

```java
public class study {
    public static void main(String[] args){
        /*String str = 123+"";//123与一个字符串相加，即连接字符串，并赋值给str
        System.out.println(str);//输出：123
        */
        System.out.println('*'+'\t'+'*');//93
        System.out.println('*'+"\t"+'*');//*    *
        System.out.println("*"+('\t'+'*'));//*51
    }
}
```

### 五、常量：

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-01-10_12-53-58.png)

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-01-10_12-52-37.png)

#### java语言的输出：

```java
int num1 = 34,num2 = 56;
        System.out.println("num1 = " + num1 + " num2 = "+num2);// +作连接符
//输出：num1 = 34 num2 = 56
```

### 六、运算符：

#### 数学运算符的用法：

**JAVA中要想计算一个数值的平方根， 可以使用 sqrt 方法：**

> double x = 4;
> double y = Math.sqrt(x);
> System.out.println(y);

**在 Java 中，没有幂运算， 因此需要借助于 Math 类的 pow 方法。语句：**

> double y = Math.pow(x, a);

**将 y 的值设置为 x 的 a 次幂 。 pow 方法有两个 double 类型的参数， 其返回结果也为double 类型**

Math 类提供了一些常用的三角函数：

> Math,sin
> Math.cos
> Math.tan
> Math.atan
> Math.atan2

还有指数函数以及它的反函数—自然对数以及以 10 为底的对数：

> Math.exp
> Math.log
> Math.loglO

最后， Java 还提供了两个用于表示 Π 和 e 常量的近似值：

> Math.PI
> Math.E

注意

不必在数学方法名和常量名前添加前缀“ Math”， 只要在源文件的顶部加上下面
这行代码就可以了。

> import static java.1ang.Math.*;

例如：

> System.out.println("The square root of \u03C0 is " + sqrt(PI)) ;

#### 自增，自减：

**只有变量才能使用自增、自减运算符，常量不可发生改变，所以不能使用。**

```java
public class study {
    public static void main(String[] args){
        int x = 10;
        int y = 20;
        int result3 = ++x + y--;//11 + 20
        System.out.println(x);//11
        System.out.println(y);//19
        System.out.println(result3);//31
    }
}
//  30++;错误写法
```

#### 复合赋值运算符：

|  +=  | a+=1 | a=a+1 |
| :--: | :--: | :---: |
|  -=  | A-=1 | A=A-1 |
|  *=  | A*=1 | A=A*1 |
|  /=  | A/=1 | A=A/1 |
|  %=  | A%=1 | A=A%1 |

* 常量不能进行赋值，不能写在赋值运算符的左边

#### 比较符的输出：

```java
public class study {
    public static void main(String[] args){
        int x = 10;
        int y = 20;
        System.out.println(x>y);//输出：fals
    }
}
```

```java
public class study {
    public static void main(String[] args){
        System.out.println(100>=20);//输出：true
    }
}
```

#### &与&&的区别：

* &&表示与，会有==短路==现象：

  ```java
  int a = 10;
  1. if(false&&a++);
  2. if(false&a++);
  //第一个表达式输出是10，即第一个是非，不再运行后面的表达式，发生短路
  //第二个表达式输出是11，虽第一个是非，且整体为非，但是不发生短路，后面表达式依旧运行
  ```

* 如果符号左边是**true**时，则第二个表达式都会运行，==两个符号等价==

* 当符号左边是**false**时，&继续执行符号右边的运算，&&不再执行符号右边的运算。

#### |与 || 的区别：

* 相同点：当符号左边是**false**时，二者都会执行符号右边的运算；
* 不同点：当符号左边是**true**时，| 继续执行， || 不再执行符号右边的运算。

#### 左移（<<）与右移（>>）:

左移：每移动一位，在原数值上==乘以2==（一定范围内）

右移：每移动一位，在原数值上==除以2==（一定范围内，且能整除）：

> 最高位是正数，用0补最高位，最高位是负数，用1补最高位

### 七、交换两个（变量、字符）的值：

#### 方式一：（定义临时变量）可以对字符串进行交换

```java
 int temp,num1,num2;
  temp = num1;
  num1 = num2;
  num2 = temp;
```

#### 方式二：（加减交换）

```java
num1 = num1 + num2;
num2 = num1 - num2;
num1 = num1 - num2;
```

==弊端==：

* 相加操作可能超出存储范
* 有局限性：只能适用于数值类型

#### 方式三：（位运算符）

```java
num1 = num1 ^ num2;
num2 = num1 ^ num2;
num1 = num1 ^ num2;
```

### 八、获取三个数的最大值：

#### 三元运算符嵌套使用法：

```java
int num1 = 34,num2 = 56,num3 = 34;
int max = num1>num2?(num1>num3?num1:num3):(num2>num3?num2:num3);
	System.out.println("这三个数的最大值是："+max);//56
```

### 九、基本结构顺序：

#### 从键盘获取值：

需要使用==Scanner类==

**具体步骤：**

>* 导包：
>
>  ```java
>  import java.util.Scanner;
>  ```
>
>* Scanner的实例化
>
>  ```java
>  Scanner scan = new Scanner(System.in);
>  ```
>
>* 调用Scanner类的相关方法，来获取指定类型的变量
>
>  ```java
>  int num = scan.nextInt();//从键盘获取一个int类型的值
>  double num = scan.nextDouble();//获取一个double类型的值
>  String str = scan.nextLine();//获取一个字符串
>  String str = scan.next();
>  ```
>
>  * ==next与nextLine区别==：
>
>    >他们的区别在于对于==空格的处理方式==不同。
>    >
>    >**使用nextLine()方法时，不将空格看做是两个字符串的间隔，而是看作字符串的一部分，返回时，它作为String类型一并返回：**
>    >
>    >**使用next()方法时，将空格看作是两个字符串的间隔：**
>    >
>    >总结: nextLine一直读取到换行，而next以空格符作为间断符
>
>* ==注意==：对于char型的获取，Scanner没有提供相关的方法，只能获取一个字符串

#### 获取字符串中的某个字符：

```java
Scanner scan = new Scanner(System.in);//Scanner实例化
String gender = scan.next();//定义并从键盘输入一个gender字符串
//输入：zyyscar
char gen;               //定义一个字符型gen
gen = gender.charAt(0);//获取gender字符串第一位数上的字符
//格式：字符串.charAt(位置);
System.out.println(gen);
//输出：z
```

#### 字符串查找：

![](C:\Users\asus\Pictures\Screenshots\字符串的查找.jpg)

#### if-else结构：

> 同C语言基本语法一致。

#### 获取一个随机数(默认是double型)：

```java
double value = Math.random();
//产生一个 [0.0 , 1.0) 范围的一个随机double类型的值
```

==若要得到随机的整型数值，需要进行强行转换==

```java
1. double value = Math.random();
   int value1 = (int)(value);
2. int value = (int)(Math.random()*100);//随机产生一个2位数的整数型数值
```

#### swith-case

> 基本语句与C语言一致

* switch结构中的表达式，只能是如下的6种数据类型之一：**byte、 short、 char、 int、 枚举类型、 String类型**
* case后只能声明一个**常量**，**不能是范围**

#### for循环：

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-01-27_20-19-36.png)

与C语言一致:

```java
for(1;2;3){
    循环语句;
}//循环语句1只循环一次
```

* 练习：

  ```java
  public class study {
      public static void main(String[] args){
          int i = 1;
          for(System.out.println('a');i<=4;System.out.println('c'),i++){
              System.out.println('b');
          }
      }
  }
  //输出：a b c b c b c b c
  ```

#### while循环：

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-01-28_15-56-30.png)

#### do-while循环：

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-01-28_16-00-37.png)

#### break与continue关键字：

**break**:

>结束==当前==循环
>
>循环结构中

**continue**:

>结束==当次==循环
>
>循环结构中

==关键字后面不能声明执行语句==

### 十、数组：

#### 一维数组：

==数组名是第一个元素的首地址==

**数组初始化：**

1. **静态初始化**：数组的初始化和数组元素的赋值操作同时进行

   ==格式：==

   方式一：

   ```java
   元素类型[] 数组名;
   数组名 = new 元素类型[]{元素1,元素2,元素3,...};
   ```

   ```java
   int[] arr;//数组的声明
   arr = new int[]{1020,2389,2891,1004};//数组静态初始化
   ```

   方式二：

   ```java
   元素类型[] 数组名 = {元素1,元素2,元素3,元素4,....};
   ```

   方式三：

   ```java
   元素类型 数组名[] ={元素1,元素2,元素3,元素4...};
   ```

1. **动态初始化**：数组的初始化和数组元素的赋值操作分开进行

   ==格式：==

   ```java
   元素类型[] 数组名 = new 元素类型[声明数组的长度];
   ```

   ```java
   String[] name = new String[5];
   name[0] = "zyy";
   name[1] = "sda";
   name[2] = "sdf";
   ................
   ```

   ==数组大小可以用变量代替，从键盘当中输入数组的大小==

#### 获取数组的长度：

```java
String[] name = new String[5];
name[0] = "zyy";
name[1] = "sda";
name[2] = "sdf";
................
System.out.println(name.length);//获取并输出name数组的长度
```

#### 获取字符串的长度  字符串.length()：

```java
String names = "zhouyongyi";
System.out.println(names.length());
```

#### 数组的遍历：

```java
//对String类型数组的遍历输入和输出：
import java.util.Scanner;
public class study {
    public static void main(String[] args){
        Scanner scanf = new Scanner(System.in);
        String[] names = new String[5];
        int i,j;
        System.out.println("输入5名学生的名字：");
        for(i=0;i< names.length;i++){          //对数组进行遍历输入
            System.out.println("请输入第"+(i+1)+"名同学的名字：");
            names[i] = scanf.nextLine();
        }
        System.out.println("你输入的学生名单是：");
        for(j=0;j<names.length;j++){           //对数组进行遍历输出
            System.out.println(names[j]);
        }
    }
}
```

#### 数组元素的默认初始化值：

1. 数组元素是整型（int，short），默认全是 ： 0
2. 数组元素是浮点型，默认是：0.0
3. 数组元素是char型，输出为：空
4. 数组元素是boolean型，默认值：faslse
5. 数组元素是字符串型，默认是：null

#### 二维数组：

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-01-29_13-49-30.png)

**静态初始化：**

>```java
>类型[][] 数组名=new 类型[][]{{....},{....},{.....},...};
>类型[] 数组名[];
>类型 数组名[][];
>int[][] arr = new int[][]{{1,2,3},{4,5,6},{7,8,9}};
>```
>
>```java
>int[][] arr = {{1,2,3},{4,5,6},{7,8,9}};
>```

#### 获取数组的长度：

**获取外层数组的长度：**

```java
int[][] arr = new arr[4][5];        
System.out.println(arr.length);//输出：4
```

**获取内层数组的长度**：

```java
int[][] arr = new arr[4][5];
System.out.println(arr[外层元素角标].length);//输出：5
```

==数组一旦初始化，其长度就是确定的==

==数组的长度一旦确定，就不可以修改==

#### 二维数组初始化值：

**规定：**二维数组分为*外层数组的元素，内层数组的元素*

```java
外层元素：arr[0],arr[1]等;
内存元素：arr[0][0],arr[1][2]等;
```

**数组元素的默认初始值**：

```java
public class suzu {
    public static void main(String[] args){
        int[][] arr = new int[3][4];
        System.out.println(arr[0]);//输出地址值：[I@15db9742
        System.out.println(arr[0][0]);//输出：0
    }
}
```

**针对于初始化方式一：**

>如：
>
>```java
>int[][] arr = new int[3][4];//对外层内层元素都声明大小
>```
>
>**外层元素的初始化值为：**==地址值==
>
>**内层元素的初始化值为**：==与一维数组初始化值情况相同==

**针对与初始化方式二**：

>如：
>
>```java
>int[][] arr = new int[4][];//只对外层元素声明大小，内层元素大小不确定
>```
>
>**外层元素的初始化值为**：==null==
>
>**内存元素的初始化值为**：==不能调用，否则报错==

#### 同维数组可直接赋值

```java
int[] arr1 = new int[]{1,2,3};
int[] arr2 = new int[4];
arr2 = arr1;
```

#### 数组常见异常：

1. 数组角标越界异常：

   ```java
   ArrayIndexOutOfBoundsExcetion;
   ```

2. 空指针异常：

   ```java
   NullPointerException;
   ```

### 十一、Arrays工具类的使用：

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-01-30_16-50-26.png)

==例如：==

**比较两个数组是否相等**:

>```java
>import java.util.Arrays;
>int[] arr1 = new int[]{1,23,43,2,31};
>        int[] arr2 = new int[]{2,31,23,123,3};
>        boolean a = Arrays.equals(arr1,arr2);
>        System.out.println(a);//输出：false
>```

**对数组进行遍历：**

>```java
>import java.util.Arrays;
>int[] arr2 = new int[]{1,23,43,2,31};
>        System.out.println(Arrays.toString(arr1));//输出：1,23,43,2,31
>```

**将指定的值填充到数组当中**：

>```java
>int[] arr2 = new int[]{1,23,43,2,31};
>        Arrays.fill(arr1,20);//将指定的值填充到数组当中
>        System.out.println(Arrays.toString(arr1));//遍历
>```

### 十二、Java面向对象学习的三条主线：

#### Java类及类的成员：

> 属性、方法、构造器、代码块、内部类

#### 面向对象的三大特征：

> 封装性、继承性、多态性、（抽象性）

#### 其他关键字：

>```java
>this super static final abstract interface package import
>```
>
>“大处着眼，小处着手”

#### 设计类就是设计类的成员：

>属性 = 成员变量 = field = 域、字段
>
>方法 =成员方法 = 函数 = method
>
>创建类的对象 = 类的实例化 = 实例化类

![Snipaste_2021-01-30_19-53-14](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-01-30_19-53-14.png)

### 十三、类：

#### 类和对象的使用：

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-01-30_20-31-32.png)

1. 创建类，设计类的成员
2. 创建类的成员
3. 通过“对象.属性”或“对象.方法”调用对象的结构

```java
import java.util.Arrays;
import java.util.Scanner;
public class study {
    public static void main(String[] args) {
       Scanner scanf = new Scanner(System.in);
               //创建Person类的对象：
               Person p1 = new Person();
               //调用属性："对象.属性"
               p1.name = "Tom";
               p1.isMale = true;
               //调用方法："对象.方法"
               p1.eat();
               p1.sleep();
               p1.talk("Chinese");

    }
}
class Person{
    //属性：
    String name;
    int age = 1;
    boolean isMale;
    //方法：
    public void eat(){
        System.out.println("人可以吃饭");//人可以吃饭
    }
    public void sleep(){
        System.out.println("人可以睡觉");//人可以睡觉
    }
    public void talk(String lauguage){
        System.out.println("人可以说话使用的是："+lauguage);//人可以说话使用的是：Chinese
    }
}
```

**如果创建了一个类的多个对象，则每个对象都独立的拥有一套类的属性。（非static的）**

意味着：如果我们修改一个对象的属性a，则不影响另外一个对象的属性a的值（每个相同类的不同对象可以直接赋值）

**将p1变量保存的对象地址值赋值给p3，导致p1和p3指向了堆空间中的一个对象实体，因此，改变p1即改变p3的对象**

#### 类中属性（成员变量）的使用：

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-01-31_13-23-11.png)

#### **属性（成员变量）VS 局部变量**

>1. 在类中声明的位置不同
>
>2. ==属性==：直接定义在类的一对{ }内
>
>   ```java
>   class Person{
>       //属性：
>       String name;
>       int age = 1;
>       boolean isMale;
>   }
>   ```
>
>3. ==局部变量==：声明在方法内、方法形参、代码块内、构造器形参、构造器内部的变量（只能先定义后使用，没有默认初始化值）
>
>   ```java
>   class User{
>       String name;//属性
>       public void talk(String language){//language是形参,也是局部变量
>           String food = "laob";//局部变量
>           System.out.println("...");
>       }
>   }
>   ```
>
>4. 权限修饰符的不同：
>
>   1. 属性：可以在声明属性时，指明其权限，使用权限修饰符
>   2. ==常见的权限修饰符==：private，public，缺省（没加权限修饰符，默认的），protected
>   3. 局部变量：不可以使用权限修饰符。
>
>5. 默认初始化值：
>
>   1. 属性：类的属性，根据其类型，都有默认初始化值
>      1. 整型（int short byte long）：0
>      2. 浮点型（float double）：0.0
>      3. 字符型（char）：0（或 " \u00 "）
>      4. boolean：false
>      5. 引用数据类型（类，数组，接口，String）：null
>   2. 局部变量：没有默认初始化值，即我们在调用局部变量之前==一定要显式赋值==
>
>6. 在内存中加载的位置不同：
>
>   1. **属性**：加载到==堆==空间中（非 static）
>   2. **局部变量**：加载到==栈==空间中（非static）

#### 类中方法的声明和使用：

**方法：**描述类应该具有的功能。

**比如：**

1. Math类：sqrt( )、random( ).....
2. Scanner类：nextXxx( )...
3. Arrays类：sort( )、binarySearch( )、toString( )、equals( )....

**方法的声明：**

```格式
权限修饰符 返回值类型 方法名(形参列表){
	方法体;
}
```

```java
public void eat(){}//没有形参，没有返回值
public void sleep(int hour){}//没有返回值，有形参
public String getName(String name){}//返回值是String，有形参
public String getNation(){}//返回值是String类型，没有形参
```

**一个类中方法对方法的调用和对属性的调用**

>```java
>class Person{
>    //属性：
>    String name;
>    int age = 1;
>    boolean isMale;
>    //方法：
>    public void eat(){
>        System.out.println("人可以吃饭"+age);//调用属性
>    }
>    public void sleep(){
>        System.out.println("人可以睡觉");//人可以睡觉
>    	eat();//方法调用方法
>    }
>}
>```
>
>==方法当中不能再定义一个方法==

#### 练习：

一：

>定义一个类Student，包含三个属性，学号number（int），年级state（int），成绩score（int）。
>
>创建20个学生对象，学号1到20，年级和成绩都由随机数确定
>
>```java
>import com.sun.org.apache.xerces.internal.util.SynchronizedSymbolTable;
>import java.util.Arrays;
>import java.util.Scanner;
>public class study {
>    public static void main(String[] args) {
>       Student[] stu = new Student[20];//声明Student类型的数组
>        for(int i = 0;i<stu.length;i++) {
>            //给数组元素赋值（构造20名同学的基本信息）：
>            stu[i] = new Student();//构造20个对象
>            //给对象的属性赋值：
>            stu[i].number=(i+1);
>            //年级：[1,6]
>            stu[i].state=(int)(Math.random()*(6-1+1)+1);
>            //成绩：[0,100]
>            stu[i].score=(int)(Math.random()*100+1);
>        }
>        //遍历学生数组：
>        for(int i=0;i<stu.length;i++){
>            System.out.println(stu[i].info());
>        }
>    }
>}
>class Student{
>    //学生三个属性：
>    int number;
>    int state;
>    int score;
>    public String info(){//方法：输出学生的基本信息
>        return "学号："+number+"，年级："+state+"，成绩："+score;
>    }
>}
>```

#### 万事万物皆对象：

1. 在JAVA语言范畴中，我们都将功能、结构等封装到类中，通过类的实例化，来调用具体的功能结构
2. 涉及到JAVA语言与前端Html、后端的数据库交互时，前后端的结构在JAVA层面交互时，都体现为、对象。

#### 内存解析的说明：

1. 引用类型的变量，只可能存储两类值：null或地址值（含变量的类型）

   ```java
   public class InstanceTest{
       public static void main(String[] args){
           Phone p = new Phone();
           p = null;//没有这语句，则输出地址值
           System.out.println(p);//输出：null
       }
   }
   class Phone{
       int num;
       String name;
   }
   ```

2. ```java
   public class study {
       public static void main(String[] args) {
                   Phone[] p1 = new Phone[10];
                   p1[0] = new Phone();
                   System.out.println(p1[0].num);//1
                   System.out.println(p1[1]);//指向空指针：null
                   System.out.println(p1[1].num);//空指针异常
               }
           }
           class Phone{
               int num=1;
               String name;
           }
   ```

   ==没有实例化（创建对象）的如：p1[1]，指向空指针，则 . 后面的都将输出错误==

#### 匿名对象：

（对象没有名，但有对象）

1. 理解：我们创建的对象，没有显式的赋给一个==变量名==，即为匿名对象
2. 匿名对象只能调用一次（因为没有变量名来命名它）
3. 使用：

```java
public class study {
    public static void main(String[] args) {
        //匿名对象：
        new Phone().sendEmail();
        new Phone().playGame();
        //调用两个不同的对象
        new Phone().price=10000;
        new Phone().showPrice();//输出：0.0即前面price的赋值与该语句无关，两个是分开的对象
    }
}
class Phone{
    double price;
    public void sendEmail(){
        System.out.println("发送邮件");
    }
    public void playGame(){
        System.out.println("可以打游戏");
    }
    public void showPrice(){
        System.out.println("手机的价格是："+price);
    }
}
```

**匿名对象的使用**：

```java
public class study {
    public static void main(String[] args) {
        PhoneMall mall = new PhoneMall();
        //匿名对象的使用：
        mall.show(new Phone());//传入一个Phone类型的变量
                                //这里传入一个匿名对象
    }//输出：发送邮件   可以打游戏
}
class PhoneMall{
    public void show(Phone phone){
        phone.sendEmail();
        phone.playGame();
    }
}
class Phone{
    double price;
    public void sendEmail(){
        System.out.println("发送邮件");
    }
    public void playGame(){
        System.out.println("可以打游戏");
    }
}
```

#### 再谈方法一：

**重载的概念**：

> 在==同一个类中==，==允许存在一个以上的同名方法==，只要它们的==参数个数或者参数
> 类型不同==即可。（两同一不同：同一类，相同方法名。参数列表参数个数参数类型不同）
>
> 不看返回值是否有，返回值返回类型是否相同；也不看权限修饰符是否相同，与方法体是否相同也无关

**重载的特征**：

>与返回值类型无关，只看参数列表，且参数列表必须不同。(参数个数或参数类
>型)。调用时，根据方法参数列表的不同来区别。

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-02-04_13-42-23.png)

==方法重载中调用的方法由传入的参数类型相关==

#### 再谈方法二：

**可变个数（0个-多个）的形参**：

> ==传入的参数必须是前面指定的类型==

**格式**：

>```java
>public class study {
>    public static void main(String[] args) {
>        Phone p = new Phone();
>        p.show("Hello","sdad");//可输入多个形参
>        p.show();//可输入0个形参
>    }//输出两个 ：可变个形参
>}
>class Phone{
>    public void show(String ... s){//定义可变个形参的方法
>        System.out.println("可变个形参");
>    }
>}
>```

1. **可变个数形参的方法与本类中方法名相同，形参不同的方法之间构成重载**

2. **可变个数形参的方法的使用与方法参数部分使用数组是一致的，换句话说，可变个形参数可当做某数据类型的数组来使用**

   ```java
   class Phone{
       public void show(String ... s){//定义可变个形参的方法
           System.out.println("可变个形参");
       }
       public void show(String[] strs){//方法形参部分使用数组
           System.out.println("部分形参数组");
       }
   }//两个方法会因为是一致的而不能使用
   ```

3. **可变个数形参在方法的形参中必须声明在末尾（如果有其他数据类型的形参）**

4. **可变个数形参在方法的形参中，最多只能声明==一个可变形参==**

#### 再谈方法三（方法参数的值传递机制）：

**关于变量的赋值**：

>1. 如果变量是基本数据类型，此时赋值的是变量所保存的==数据值==
>2. 如果变量是引用数据类型，此时赋值的是变量所保存的==数据的地址值==

```java
public class study {
    public static void main(String[] args) {
        Order q = new Order();
        System.out.println(q);//输出:地址
    }
}
class Order{
    int orderId = 0;
}
```

**方法的形参的传递机制：值传递**

> 形参：方法定义时，声明的小括号内的参数
>
> 实参：方法调用时，实际传递给形参的数据

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-02-04_21-06-33.png)

**实现两个值的交换**：

（利用引用数据类型调用需要交换的2个变量）

```java
public class study {
    int m=10,n=20;
    public static void main(String[] args) {
        study data = new study();
        System.out.println("m = "+data.m+"n = "+data.n);//m=10;n=20
        data.swap(data);
        System.out.println("m = "+data.m+"n = "+data.n);//m=20;n=10
    }
    public void swap(study data){
        int temp = data.m;
        data.m =data.n;
        data.n = temp;
    }
}
```

```java
        int[] arr = new int[]{1,2,3};
        System.out.println(arr);//输出：地址值
        char[] arr1 = new char[]{'a','b','b'};
        System.out.println(arr1); //输出：abc
```

#### 类的成员：构造器（或构造方法）：

##### 构造器的使用：

> 定义构造器的格式：
>
> ```java
> 权限修饰符 类名(形参列表){};
>     public Person(){
>         System.out.println("person()....");
>     }
> ```
>
> 

##### 构造器的作用：

> 创建对象。
>
> ```java
> 格式：
>     new + 构造器;
> ```
>
> ```java
> public class study{
>     public static void main(String[] args){
>         //创建类的对象：
>         Person p = new Person();
>     }
> }
> class Person{
>     //构造器：
>     public Person(){
>         System.out.println("person()....");
>     }
> }
> //输出：person()....
> ```
>
> 给对象进行初始化。
>
> ```java
> public class study{
>     public static void main(String[] args){
>         //创建类的对象：
>         Person p = new Person("Tom");
>         System.out.println(p.name);
>     }
> }
> class Person{
>     String name;
>     //构造器：
>     public Person(String name){
>         this.name = name;
>     }
> }
> //输出：Tom
> ```
>
> 理解：
>
> ![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-02-17_12-57-56.png)
>
> 

##### 说明：

> 1. 如果没有显式的定义类的构造器的话，则系统默认提供一个空参的构造器，一旦我们==显式的定义了类的构造器==之后，系统就==不再提供默认的空参构造器。==
> 2. 一个类中定义的多个构造器彼此==构成重载==（同名不同形参数）。
> 3. 一个类中，至少会有一个构造器。
> 4. ==默认构造器的修饰符==与==所属类的修饰符一致==
> 5.  ==父类的构造器不可被子类继承==

#### 总结：

##### 属性赋值的先后顺序：

>1. 默认初始化
>2. 显式初始化
>3. 构造器中赋值
>4. 通过“对象.方法"或”对象.属性“的方式赋值
>
>以上操作的先后顺序：
>
>1 -->  2 --> 3 --> 4

### 十四、面向对象特征之一：封装与隐藏：

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-02-09_21-22-07.png)

#### 一、问题的引入：

> **当创建一个类的对象以后，可以通过“对象.属性”的方式，对对象的属性进行赋值，这里，赋值操作受到属性的数据类型和存储范围的制约，除此之外，没有其他制约条件。实际问题中，我们往往需要给属性赋值加入额外的限制条件，这个条件就不能在属性声明时体现，只能通过方法限制条件的添加。同时，需要避免用户再使用“对象.属性”的方式对属性进行赋值，则需要将属性声明为私有的(private)----->此时，针对于属性就体现了封装性**

#### 二、封装性的体现：

>将类的属性私有化（private），同时，提供公共（public）的方法来获取(get)和设置(set)(例如：对下面age来赋值，通过调用方法再对legs进行赋值)
>
>```java
>public class study{
>    public static void main(String[] args){
>        Animal a = new Animal();
>        a.name = "周泳屹";
>        a.age = 20;
>        a.setLegs(10);//对封装的legs进行赋值
>        System.out.println(a.getLegs);//获取legs的值
>    }
>}
>class Animal{
>    String name;
>    int age;
>    private int legs;//对该属性私有化
>    public int getLegs(){//获取
>        return legs;
>    }
>    public void setLegs(int a){//设置
>        lega = a;
>    }
>}//获取和设置不能合为一个方法
>```

#### 三、封装性的体现需要权限修饰符来配合:

>Java规定的4种权限（从大到小）：private、缺省、proteced、public
>
>![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-02-11_18-39-25.png)
>
>==对于class（类）的权限修饰只可以用public和default(缺省)。==
>
>* public类可以在任意地方被访问。
>* default类只可以被同一个包内部的类访问。
>
>具体的：
>
>4种权限都可以用来修饰类的内部结构：属性、方法、构造器、内部类

### 拓展知识：

#### 一、JavaBean

JavaBean是一种Java语言写成的可重用组件

所谓javaBean，是指符合如下标准的java类：

> 1. 类是公共的
> 2. 有一个无参的公共的构造器
> 3. 有属性，且有对应的get、set方法

#### 二、UML类图：

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-02-17_14-19-16.png)

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-02-17_14-19-25.png)

### 十五、关键字:

#### this关键字的使用：

1. this可以用来修饰：属性、方法、构造器

2. ==this是自身的一个对象，代表对象本身，可以理解为：指向对象本身的一个指针。==

3. **this修饰属性和方法：**

   1. this理解为当前对象或当前正在创建的对象

   2. 在类的方法中，可以使用“this.属性”和“this.方法”的方式，调用当前对象属性和方法，但一般都选择省略“this.”，==方法形参和类的属性同名==，==必须显示使用“this.变量”的方式==，表明此变量是属性，而非形参

   3. ```java
      public class study{
          public static void main(String args[]){
              Person p = new Person();
              p.setName("周泳屹");
              System.out.println(p.getName());
          }
      }
      class Person{
          private String name;
          private int age;
          public void setName(String name){
              this.name = name;//this.name表示Person类的属性
          }
          public String getName(){
              return name;
          }
      }
      ```

4. **this调用构造器：**

   1. 在类的构造器中，可以显式的使用“this(形参列表)”方式，调用本类中指定的其他构造器

   2. 构造器中==不能通过“this(形参列表)”方式调用自己==(调用多个构造器，但只是造了一个对象)

   3. ```java
      public class study{
          public static void main(String args[]){
              Person p = new Person();
          }
      }
      class Person{
          private String name;
          private int age;
          public Person(String name,int age){
              this.name = name;
              this.age = age;
          }
          public Person(){
              this("周泳屹",20);//用this(形参列表)调用上面的构造器
          }
      }
      ```

   4. 如果一个类中有n个构造器，则最多有(n-1)个构造器中使用了“this(形参列表)”，==即构造器不能互相调用==

   5. ==规定：“this(形参列表)”必须声明在当前构造器的首行==

   6. ```java
      class Person{
          private String name;
          private int age;
          private int height;
          public Person(String name,int age){
              this(173);//this(形参)声明在当前构造器的首行
              this.name = name;
              this.age = age;
          }
          public Person(int height){
              this.height = height;
          }
      ```

   7. ==规定：构造器内部最多只能声明一个“this(形参列表)”，用来调用其他构造器==

   8. ```java
      class Person{
          private String name;
          private int age;
          private int height;
          public Person(String name,int age){
              this(173);//该构造器调用下面的构造器
              this.name = name;
              this.age = age;
          }
          public Person(int height){
              this.height = height;
          }
          public Person(){
              this("Zhouyongyi",20);//该方法可以实现多个构造器的调用
          }
      ```

#### package关键字的使用：

1. 为了更好的实现项目中类的管理，提供包的概念
2. 使用package声明类或接口所属的包，声明在源文件的首行
3. 包属于标识符，需要遵循标识符的命名规则和规范、“见名知意”。
4. 每“ . ”一次，代表一层文件目录
5. 同一个包下，不可以命名同名的接口、类，不同的包下可以命名同名的接口、类。

#### import关键字的使用：

1. import:导入
2. 在源文件中，显式的使用import结构导入指定包下的类、接口
3. 声明在包的声明和类的声明之间
4. 如果需要导入多个结构，则并列写出即可。
5. 可以使用“ XXX.* ”的方式表示可以导入XXX包下的所有结构
6. 如果使用的类或接口是在java.lang包下定义的，则可以省略import结构
7. 如果使用的类或接口是本包下定义的，则可以省略import结构
8. 如果在源文件中，使用了不同包下的同名类，则必须至少有一个类需要以全类名的方式显示
9. 使用“XXX.”方式表明可以调用XXX包下的所有结构，但是如果使用的是XXX子包下的结构，则仍需要显式导入
10. import static：导入指定类或接口中的静态结构

#### super关键字：

##### 作用：

>1. super理解为：父类的
>2. ==super可以理解为父类对象==
>3. super可以用来调用：属性、方法、构造器

##### 使用：

>1. super和this的用法相像，this代表本类对象的引用，super代表父类的内存
>    空间的标识
>
>2. 可以在子类的方法或构造器中，使用“super.属性”或者“super.方法”的方式，显式调用父类中声明的属性或方法。但是一般习惯省略“super”。
>
>3. **调用属性**：
>
>  ```java
>  public class Person{
>      int id;//身份证号
>      String name;
>  }
>  class Student extends Person{
>      int id;//学号
>      String gender;//性别
>      public void show(){
>          system.out.println("学号是："+this.id+"身份证号是："+super.id);
>      }//前面第一个id是调用Student类中的id，后面一个是调用父类Person类中的id
>  }
>  class PersonTest {
>      public static void main(String[] args) {
>          Student s = new Student();
>          s.show();
>      }
>  }
>  ```
>
>4. **调用方法：**
>
>  1. ==特殊的：==当子类重写了父类中的方法以后，我们想在子类的方法中调用父类中被重写的方法时，必须显式的使用“super.方法”的方式，表明调用的是父类中声明的方法。如下：
>
>  ```java
>  public class Person{
>      int id;//身份证号
>      String name;
>      public void eat(){
>          System.out.println("人吃饭")
>      }
>  }
>  class Student extends Person{
>      int id;//学号
>      String gender;//性别
>      public void eat(){
>          super.eat();//调用父类中的eat方法
>      }
>  }
>  class PersonTest {
>      public static void main(String[] args) {
>          Student s = new Student();
>          s.show();
>      }
>  }
>  ```
>
>5. **调用构造器**：
>
>   调用父类的构造器：
>
>   1. 可以在子类的构造器中显式的使用“super(形参列表)”的方式，==调用父类中声明的指定的构造器==（特别在父类属性权限为private情况下）
>   2. “super(形参列表)”的使用，必须声明在==子类构造器的首行==
>   3. 在类的构造器中，==针对于“this(形参)”或者“super(形参列表)”==只能二选一，==不能同时出现==
>   4. 在构造器的首行，**没有显式的声明“this(形参)”或者“super(形参列表)”，则默认调用父类中空参的构造器：super( )**。==即==：如果子类构造器中既未显式调用父类或本类的构造器，且父类中又
>      没有无参的构造器，则**编译出错**
>   5. 在类的==多个构造器中==，==至少有一个类的构造器中使用了“super(形参列表)”==，调用父类中的构造器
>
>6. 例子：
>
>   ```java
>   public class Person {
>   private String name;
>   private int age;
>   private Date birthDate;
>   public Person(String name, int age, Date d) {
>   this.name = name;
>   this.age = age;
>   this.birthDate = d;
>   }
>   public Person(String name, int age) {
>   this(name, age, null);
>   }
>   public Person(String name, Date d) {
>   this(name, 30, d);
>   }
>   public Person(String name) {
>   this(name, 30);
>   }
>   }
>   5.4 关键字—super
>   调用父类构造 器 举例
>   public class Student extends Person {
>   private String school;
>   public Student(String name, int age, String s) {
>   super(name, age);
>   school = s;
>   }
>   public Student(String name, String s) {
>   super(name);
>   school = s;
>   }
>   // 编译出错: no super(),系统将调用父类无参数的构造器。
>   public Student(String s) {
>   school = s;
>   }
>   }
>   ```

### 十六、继承性：

#### 实例：

```java
public class Student {
    String name ="周泳屹";
    int age = 20;
    String major = "Computer";
    public Student(){

    }
    public Student(String name,int age,String major){
        this.age = age;
        this.name = name;
        this.major = major;
    }
    public void eat(){
        System.out.println("可以吃饭");
    }
    public void sleep(){
        System.out.println("可以睡觉");
    }
}
class Zyy extends Student{
    String Number = "2020211634";//学号
}
//Zyy这个类继承了Student这个类，Zyy不再声明name,age等成员，也拥有该成员（即可在main方法中从Zyy类中调用
//这些成员和方法）
```

#### 继承性的好处：

>1.  继承的出现==减少了代码冗余==，提高了代码的复用性。
>2. 继承的出现，更==有利于功能的扩展==。（将子类都拥有的功能都提取放入父类中）
>3.  继承的出现让类与类之间产生了关系，==提供了多态的前提==。

#### 继承性的格式：

```java
class A extends B{}
/*
A:子类、派生类、subclass
B:父类、超类、基类、superclass
*/
```

##### 体现： 

1. 子类继承了父类，就==继承了父类的所有的方法和属性==；在子类中，==可以使用父类中定义的方法和属性==，也==可以创建新的数据和方法==。
2. 在Java 中，继承的关键字用的是“extends”，即子类不是父类的子集，而是对父类的“扩展” 。
3. ==特别的：==父类中声明的为private的属性或方法，子类继承父类以后，仍然认为获取了父类中私有的结构，只有因为封装性的影响，使得子类不能直接调用父类的结构而已
4. 子类继承父类以后，还可以声明自己持有的属性和方法，实现功能的拓展

#### 继承性的规定：

1. Java中==类的单继承性==一个类只能有一个父类；
2. 一个父类可以派生出多个子类；
3. 类可以多重继承；
4. 子类直接继承的父类称为：直接父类；间接继承的父类称为：间接父类
5. 子类继承父类后，就获取了直接父类以及所有间接父类中声明的属性和方法
6. 如果没有显式的声明一个类的父类，则此类继承与java.lang.Object类。意味着：所有java类具有java.lang.Object类的方法和属性

#### 子类对象实例化的全过程：

1. **结果上：**
   1. 子类继承父类以后，就获取了父类中声明的属性和方法
   2. 创建子类的对象在堆空间中就会加载所有父类中声明的属性
2. **过程上：**
   1. 当我们通过子类的构造器创建子类对象时，我们一定会直接或间接的调用其父类的构造器，进而调用父类的父类的构造器，直到调用java.lang.Object类中空参的构造器，所以才可以看到内存中有父类的结构，子类对象才可以考虑进行调用
   2. 明确：虽然创建子类对象时，调用了父类的构造器，但是自始至终就创建过一个对象，即为new的子类对象。

### 十七、方法的重写(override/overwrite)：

#### 定义：

> 在子类中可以根据需要==对从父类中继承来的方法==进行改造，也称为==方法的重置、覆盖==。在程序执行时，==子类的方法将覆盖父类的方法==。

> 1. **重写**：子类继承父类以后，可以对父类中同名同参数的方法，进行覆盖
> 2. **应用**：重写以后，==当创建子类对象==以后，通过子类对象调用子父类中的同名同参数的方法时，实际执行的是子类重写父类的方法（子类自己定义的方法）
> 3. **重写的规定：**
>    1. 子类中的叫重写方法，父类中叫被重写的方法

#### 要求：

1. 子类重写的方法必须和父类被重写的方法**具有相同的方法名称、参数列表**
2. 子类重写的方法的==返回值类型不能大于父类==被重写的方法的返回值类型
   1. 父类被重写的方法的返回值类型是void，则子类重写的方法的返回值类型只能是void
   2. 父类被重写的方法的返回值类型是A类型，则子类重写的方法的返回值类型可以是A类或A类的子类（如：父类被重写的方法返回值类型是Object，则子类可以是String，也可以是Object）
   3. 父类被重写的方法的返回值类型是基本数据类型（比如：double），则子类重写的方法的返回值类型必须是相同的基本数据类型（double）
3. 子类重写的方法使用的==访问权限不能小于父类==被重写的方法的访问权限
4. **特殊情况**：==子类不能重写父类中声明为private权限的方法==
5. 子类方法==抛出的异常不能大于父类==被重写方法的异常

**子类与父类中同名同参数的方法必须同时声明为非static的(即为重写)，或者同时声明为
static的（不是重写）。因为static方法是属于类的 ，子类无法覆盖父类的方法。**

### 十八、面向对象特征之三：多态性

#### 理解：

> 一个事物的多种形态
>
> ```注释
>      对象的多态性：父类的引用指向子类的对象（或者子类的对象赋给父类的引用）
> ```

#### 多态的使用：

> ```java
> 父类类名 自定义名 = new 子类类名();//多态应用格式
> //编译看左边的类，执行（运行）看右边的类
> ```
>
> 当==调用子父类同名同参数的方法时==，实际==执行的是子类重写父类的方法==-------虚拟方法调用（子类中没有重写父类的方法，则执行父类中的方法）
>
> 有了对象的多态性以后，我们在编译器，只能调用父类中声明的方法，但在运行期，我们实际执行的是子类重写父类的方法。==总结：==编译看左边（父类），执行看右边（子类）  （不适用于属性）**（子类中没有重写父类的方法，则执行父类中的方法）**【可以调用子类中没有的方法（实际调用父类），不能调用父类中没有定义或声明的方法】
>
> **实例：**
>
> ```java
> public class PersonTest {
>     public static void main(String[] args){
>         PersonTest p = new PersonTest();
>         p.Fun(new Woman());//多态的使用：可以用子类的对象调用
>     }
>     public void Fun(Person person){//形参列表是Person类引用数据类型
>         person.eat();
>         person.walk();
>     }
> }
> class Person {
>     String name;
>     int age;
>     public void eat(){
>         System.out.println("人，吃饭");
>     }
>     public void walk(){
>         System.out.println("人，走路");
>     }
> }
> class Woman extends Person{
>     boolean isBeauty;
>     public void goShopping(){
>         System.out.println("女人喜欢购物");
>     }
>     public void eat(){
>         System.out.println("女人少吃");
>     }
>     public void walk(){
>         System.out.println("女人窈窕的走路");
>     }
> }
> ```
>
> 

#### 多态性的使用前提：

> 1. 类的继承关系
> 2. 要有方法的重写（子类重写父类的方法）
> 3. ==多态性是运行时行为==

#### 虚拟方法的调用：

> 子类中定义了与父类同名同参数的方法，在多态情况下，将此时父类的方法称为虚拟方法，父
> 类根据赋给它的不同子类对象，动态调用属于子类的该方法。这样的方法调用在编译期是无法
> 确定的。
>
> ```java
> Person e = new Student();
> e.getInfo(); // 调用Student 类的getInfo()
> ```
>
> 编译时e 为Person 类型，而方法的调用是在运行时确定的，所以调用的是Student类的getInfo() 方法。——**动态绑定**

#### 总结：

> ![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-03-05_16-29-45.png)
>
> **有了对象的多态以后，内存中实际上是加载了子类持有的属性和方法的，但是由于变量声明为父类类型，导致编译时，只能调用父类中声明的属性和方法，子类持有的属性和方法不能调用。**

#### 多态定义时，要调用子类中的方法和属性：

##### instanceof操作符：

>  **多态情况下：如何调用子类持有的属性和方法？**
>
>  ```java
>  //Person是父类，Man是子类,Woman是子类
>  Person p1 = new Man();
>  //为能调用Man子类中的属性和特有方法，对p1强行转换：
>  Man m = (Man)p1;
>  //子类之间不能转换：
>  Woman m1 = (Woman)p1;
>  ```
>
>  使用强制类型转换(可能会出现ClassCastException的异常)；
>
>  ![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-03-05_16-49-51.png)
>
>  1. **为了避免出现转换异常，可以在向下转换之前，先进行 instanceof 的判断。一旦返回true，就进行向下转型，如果返回 false，不进行向下转型。**
>
>    ```java
>            Person p1 = new Man();
>            if(p1 instanceof Man){
>                p1.walk();
>                System.out.println("Yes");
>            }else{
>                System.out.println("No");
>            }
>    ```
>
>  2. instanceof格式：
>
>       ```java
>       //instanceof是Java的一个保留关键字
>       a instanceof A
>       //左边是对象，右边是类，返回类型是Boolean类型
>           //它的具体作用是 测试左边的对象 是否 是右边类或者该类的子类创建的实例对象 ，是，则返回true，否则返回false。
>       ```
>
>  3. 如果  a instanceof A返回 true，则 a instanceof B也返回 true，其中，B是A的父类，即对象a与instanceof自己所在类，所在类的父类，返回值都是instanceof
>
>  4. ==多态定义时，调用子类中的方法和属性:==
>
>       ```java
>       //Person类是Man的父类：
>       Person p = new Man();
>       p1.Name;//只能调用父类中的或者子类重写父类的方法
>       ((Man) p1).walk();//先强制转换后，再调用子类Man的方法
>       ```
>
>       
>
>  5. ```java
>       //Person 是Man和Woman的父类：
>       ```
>
>    ```java
>    //编译时通过，运行时不通过：
>    Person p3 = new Woman();
>    Man m3 = (Man)p3;
>    //编译时通过，运行时也通过：
>    Object obj = new Woman();
>    Person p = (Person)obj;
>    ```

#### "=="引用数据类型：

> 对于引用数据类型来讲，比较的是两个==引用数据类型变量的地址值==是否相同（赋值赋地址值）

#### ==与equals( )区别：

##### **==**:

> 1. 可以使用在基本数据类型变量和引用数据类型变量中
> 2. 如果比较的是基本数据类型变量：比较两个变量==保存的数据是否相等==（不一定类型要相同，如：int 10和double 10.0）;如果比较的是引用数据类型变量：比较==两个对象的地址值是否相同==，即两个引用是否指向同一个对象实体

##### equals( )方法的使用：

> 1. 一个方法，非运算符
>
> 2. 只能适用于引用数据类型
>
> 3. Object类中equals( )的定义：
>
>    ```java
>    public boolean equals(Object obj){
>        return (this == obj);
>    }
>    //得知：Object类中定义的equals方法和 == 的作用相同（比较两个对象的地址值是否相等）
>    ```
>
> 4. 像String、Date、File、包装类==等都重写了Object类中的equals( )方法==。重写以后，比较的不是两个引用的地址是否相同，而是比较两个对象的“实体内容”是否相同。
>
> 5. 为了能够使自定义的类中equals( )比较的是“实体内容”，则需要重写Object中类的equals( )方法（和String类中的equals方法一样）==涉及getClass( )方法：返回一个对象所属的类==
>
> 6. ==equals( )方法的重写快捷（idea): ctrl+insert==

##### 总结：

> ![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-03-06_20-42-26.png)

#### 重写equals方法：

==用于比较两个对象是否相等==

> ```java
> public class Employee{
>         //........
>     public boolean equals(Object otherObject){
>         if(this==otherObject)//如果地址值都相等，则两个对象必等
>             return true;
>         if(otherObject==null)//如果该对象为null,则没有内容可比较
>             return false;
>         if(this.getClass()!=otherObject.getClass())
> //      getClass返回一个对象所属类，只有在两个对象属于同一个类时，才有可能相等
>             return false;
> //      都满足，则对其进行强转：
>         Employee other = (Employee) otherObject;
>         //后续对属性进行分别比较，等则返回true不等则返回false
>     }
> }
> ```

#### 重写方法特殊：

```java
public class Base1Test{
    public void main(String[] args){
        
    }
}
class Base1{
    public void arr(int a,int...b){
        System.out.println("base1");
    }
}
class Sub1 extends Base1{
    public void arr(int a,int[] b){
        System.out.println("sub_1");
    }
    public void arr(int a,int b,int c){
        System.out.println("sbu_2");
    }
}
//输出结果：sub_1
//解释：
/*父类与子类同方法名，若父类形参列表形如：(int a,int...b)与子类形参列表(int a,int[] b)似为子类重写了父类中的方法，多态性则输出：子类中的方法体，且与子类中另一个方法无关*/
```

### 十九、Object类的使用：

java.lang.Object类

1. **Object类只声明了一个空参构造器**

2. **数组也可以理解是Object类的子类**，可以调用Object类中的方法

3. Object类是所有Java类的根父类

4. 如果在类的声明中未使用extends关键字指明父类，则默认父类为java.lang.Object类

5. Object类中的功能（属性、方法）就具有通用性

6. Object类中的部分方法：

   1. clone( )，克隆对象：

      ```java
      Person a1 = new Man();
      Man a2 = (Man)a1.clone();//将a1的克隆体强制类型转换成a2而不影响a1本体，此时a1,a2无关系
      ```

#### 字符串常量池：

> 1. ![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-03-06_21-08-32.png)
>
>    
>
> 2. 当我们==使用双引号创建一个字符串==（字面量创建）时，**首先在字符串常量池中查找是否有相同值的字符串，如果发现则返回其引用（地址值）**，否则它会在池中创建一个新的字符串，然后返回新字符串的引用（即：str = "zyy";
>
>    str2 = "zyy"; 输出：str == str2 为 true
>
> 3. 如果==使用new运算符创建字符串==，则会**强制String类在堆空间中创建一个新的String对象,而且若常量池中没有该字符串，则同时会在字符串常量池中创建一个该字符串**。我们可以使用intern()方法将其放入字符串常量池或从字符串常量池中查找具有相同的值字符串对象并返回其引用
>
> 4. # 有时在java面试中，你会被问到有关字符串常量池的问题。例如，在下面的语句中创建了多少个字符串对象：
>
>    ```java
>    String str = new String("Cat");  
>    ```
>
>    **在上面的语句中，可能创建1或2个字符串对象。如果池中已经有一个字符串*“Cat”*，那么只在堆空间new一个"Cat"对象，然后直接使用池子已有的"Cat"。如果池中没有字符串字面量*“Cat”*，那么它将首先在池中创建（char[ ]常量池中的数据），然后在堆空间中创建，因此将创建总共2个字符串对象。**
>
> 5. **可以调用intern( )方法查看字符串常量池中的字符串**
>
>    ```java
>            String str1 = new String("zuu");
>            System.out.println(str1.intern());//输出：zuu
>    ```

#### toString( )方法：

> 1.  ==Object中的toString方法返回：类名@java对象的内存地址经过哈希算法得出的int类型值再转换成十六进制
>  这个输出结果可以等同看做java对象在堆中的内存地址==
>    
> 2. 当我们输出一个对象的引用时，实际上就是调用当前对象的 toString( )
>
>    ```java
>    //定义了一个class Person
>    Person p = new Person();
>    System.out.println(p);
>    ```
>
> 3. Object类中toString( )的定义（没有被重写的toString( )方法）：
>
>    ```java
>    public String toString(){
>        return getClass.getName+"@"+Integer.toHexString(hashCode());
>    }
>    ```
>
> 4. 像String、Date、File、包类等都重写了Object类中的toString( )方法
>
> 5. 自定义 重写  toString( ) 方法：

#### Arrays.toString():

> ==调用方法，可以直接输出一个数组:==
>
> ```java
>         int[] str = {19, 232, 390, 3421};
>         System.out.println(Arrays.toString(str));
> //输出：[19, 232, 390, 3421]
> ```

### 二十、包装类的使用：

> java提供了8种基本数据类型对应的包装类，使得基本数据类型的变量具有类的特征
>
> 针对八种基本数据类型定义相应的引用类型—包装类（封装类）
>
> 有了类的特点，就可以调用类中的方法，Java才是真正的面向对象
>
> ![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-03-07_17-10-03.png)
>
> ![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-03-07_17-08-39.png)

#### 单元测试的注意事项：

> 方法的权限是public,没有返回值，没形参

#### 为什么要有包装类？

为了使基本数据类型的变量具有类的特征，引入包装类

#### 基本数据类型 ---->  包装类：

==调用包装类的构造器==

* 如：想要让纯数字的字符串转换为int、double、float等数据类型，则可以使用：

  ```java
  //String –> Integer –> int
  public class WrapperTest {
      public static void main(String[] args) {
          String num1 = "345";
          Integer num2 = new Integer(num1);//将String --> Integer
          System.out.println(num1+100);//输出：345100 即num1是 字符串 345
          System.out.println(num2+100);//输出：445 即num2是 数字345
          int num3 = num2.intValue();//将Integer --> int
          System.out.println(num3+100);//输出：445 即num3是 基本数据类型345
      }
  }
  ```

#### 包装类 ---> 基本数据类型：

==调用包装类Xxx的xxxValue( )方法==

```java
//由上面 String ---> int 类型的案例：
int num3 = num2.intValue();//将Integer --> int
```

#### 自动装箱、自动拆箱：

```java
//自动装箱：基本数据类型 --> 包装类
int num = 10;
Integer num1 = num;//基本数据类型直接赋值给Integer类类型，不用再另外将num变为包装类再赋值给num1
```

```java
//自动拆箱：包装类 --> 基本数据类型
public class WrapperTest {
    public static void main(String[] args) {
        Integer num1 = 20;
        int num2 = num1;//Integer类型直接赋值给int类型
        System.out.println(num2);//输出：20
    }
}
```

#### 基本数据类型、包装类-->String类型：

* 方式一：基本数据类型 + String类型 = String类型

  ```java
  int num1 = 10;
  String str1 = num1 + "";
  ```

* 方式二：调用String重载的valueOf( )

  ```java
  public class WrapperTest {
      public static void main(String[] args) {
          int num1 = 10;
          String num2 = String.valueOf(num1);
          System.out.println(num1+10);//输出：20
          System.out.println(num2+10);//输出：1010
      }
  }
  ```

#### String类型 --->  基本数据类型、包装类：

==调用包装类的parseXxx( )==

```java
public class WrapperTest {
    public static void main(String[] args) {
        String num1 = "10";
        int num2 = Integer.parseInt(num1);
        System.out.println(num1+10);
        System.out.println(num2+10);
    }
}
```

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-03-07_17-10-03.png)

#### 总结：

1. 包装类-->String，在String中找方法
2. String--->包装类，在包装类找方法
3. ==**parse…()返回值都为基本类型**==
4. ==**valueOf返回值都为对应的对象类型，且valueOf会调用parse…()**==

#### 面试题1：

```java
public class WrapperTest {
    public static void main(String[] args) {
        Object o1 = true ? new Integer(1):new Double(10);//Integer提升为Double统一后再进行比较该输出
        System.out.println(o1);//输出：1.0
    }
}
```

#### 面试题2：

```java
import javax.annotation.Generated;

public class WrapperTest {
    public static void main(String[] args) {
//  num1和num2是new的对象，对于对象的比较（==），直接比较地址
        Integer num1 = new Integer(20);
        Integer num2 = new Integer(20);
        System.out.println(num1==num2);//false
        
        Integer i = 100;
        Integer j = 100;
        System.out.println(i==j);//true
//  Integer包装类有一定数目大小的缓存区范围：[-128,127]，即该范围内，只要内容相同，则地址值相同，即==
        Integer m = 128;//相当于new了一个Integer对象
        Integer n = 128;
        System.out.println(n==m);//false
    }
}
```

##### Integer包装类缓存区详细解释：

```解释
Integer 内部定义了IntegerCache结构，IntegerCache中定义了Integer[],保存了从-128~127的整数，如果使用自动自动装箱的方式，给Integer赋值的范围在-128~127范围内时，可以直接使用数组中的元素，不用再去new了（地址值一样），提高效率
```

### ==常用内存区域：==

**例图：**

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-03-09_21-34-27.png)

#### 栈内存空间：

> 保存所有的==对象名称==（准确说是保存引用的堆内存空间的地址）（局部变量）

#### 堆内存空间：

> 保存每个对象的具体属性内容（new出来的结构：对象，数组.....）

#### 全局数据区：

> 保存 static类型 的属性

#### 全局代码区：

> 保存所有的方法定义

#### 方法区：

> 类的加载信息、静态域、常量池

### 二十一、关键字static：

> 1. static：静态的
> 2. static可以用来修饰：属性、方法、代码块、内部类
> 3. ![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-03-09_12-10-29.png)

##### 用static修饰属性：（静态变量或类变量）

> 修饰后的属性叫：**静态变量**
>
> 按照是否使用static修饰，分为==静态属性==和==非静态属性==

**静态属性**VS**非静态属性（实例变量）**

> 1. ==实例变量==：我们创建了类的多个对象，每个对象都独立的拥有一套类中的非静态属性，当修改其中一个对象中的非静态属性时，不会导致其他对象中同样的属性值的修改
>
> 2. ==静态变量（属性）==：我们创建了类的多个对象，多个对象共享同一个静态变量，意味着：当通过某一个对象修改静态变量时，会导致其他对象调用此静态变量时，是修改过了的。
>
>    ```java
>    import java.util.Scanner;
>    import java.util.Vector;
>    public class Study {
>    
>        public static void main(String[] args) {
>            Scanner scan = new Scanner(System.in);
>            Chinese c1 = new Chinese();
>            c1.name = "zyy";
>            c1.age = 20;
>            c1.nation = "CN";
>            Chinese c2 = new Chinese();
>            c2.name = "马龙";
>            c2.age = 30;
>            c2.nation = "CHINA";//修改了nation静态变量，c1调用的静态变量也会跟着被修改
>            System.out.println(c2.nation);//输出：CHINA
>            System.out.println(c1.nation);//输出：CHINA
>        }
>    }
>    class Chinese{
>        String name;
>        in t age;
>        static String nation;
>    }
>    ```
>
>    ![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-03-09_21-34-27.png)
>
> 3. static修饰属性的其他说明：
>
>    1. 静态变量随着类的加载而加载，
>
>    2. 静态变量的加载早于对象的创建（比如在上面代码中，可以在new一个对象前就可以根据：Chiness.nation调用静态变量nation）可以通过“类.静态变量”的方式调用
>
>    3. 由于类只会加载一次，则静态变量在内存中==也只会存在一次==（存在方法区的静态域中）
>
>    4. | （调用范围） | 类变量（静态变量） | 实例变量 |
>       | ------------ | :----------------: | -------- |
>       | 类           |        yes         | No       |
>       | 对象         |        yes         | yes      |
>
>    5. ==调用静态的属性，可以不用声明对象直接用类名调用，非静态的属性则需要声明类的对象再调用==

##### 用static修饰方法(静态方法)：

> 1. 随着类的加载而加载，可以通过“类名.静态方法”进行调用
>
> 2. |      | 静态方法 | 非静态方法 |
>    | ---- | -------- | ---------- |
>    | 类   | yes      | no         |
>    | 对象 | yes      | yes        |
>
> 3. ==静态方法中只能调用静态方法和属性，非静态方法中，既可以调用静态方法和属性，也可以调用非静态的方法和属性==（声明周期不同，静态属性方法优先加载，调用输出时优先输出静态方法体）
>
> 4. ==在静态的方法内，不能使用this、super关键字==

#### 如何确定一个属性是否需要声明为static？

> 属性是可以被多个对象所共享的，不会随着对象的不同而不同。

#### 如何确定一个方法是否需要声明为static？

> 操作静态属性的方法，通常设置为static
>
> 工具类中的方法（直接“类.方法”调用工具类，不用声明对象），习惯上声明为static(比如Math、Arrays、Collections)
>
> ```java
> public class Study {
>     public static void main(String[] args) {
>         Tool.tool();//直接“类.方法”调用工具类
>     }
> }
> class Tool{
>       public static void tool(){
>           System.out.println("工具方法");
>       }
> }
> ```

#### 单例设计模式（在本类中new对象）（饿汉式）：

> 所谓单例设计模式，就是采取一定的方法保证在整个的软件系统中，对某个类只能存在一个对象实例（==直接提前造好对象，什么时候用，什么时候拿==）坏处：对象加载时间过长；好处：线程安全
>
> **实例**：
>
> ```java
> public class Study {
>     public static void main(String[] args) {
>         tool a1 = tool.getInstance();
>         tool a2 = tool.getInstance();
>         System.out.println(a1==a2);//a1,a2赋的是同一个对象，地址值相同，输出：true
>     }
> }
> class tool{
> //私有化类的构造器:
>     private tool() {
>     }
> //内部创建类的对象:（只要静态属性才能被静态方法调用）
>     private static tool instance = new tool();
> //提供公共方法，返回类的对象：（只要静态方法才可以直接被类调用）
>     public static tool getInstance(){
>         return instance;
>     }
> }
> ```

#### 单例设计模式（懒汉式）：

> 与饿汉式类似（特点：==啥时候用，啥时候造对象==）好处：延迟对象创建；坏处：**目前写法**线程不安全
>
> ```java
> public class Study {
>  public static void main(String[] args) {
>      Scanner scan = new Scanner(System.in);
>      tool t1 = tool.getInstance();
>      tool t2 = tool.getInstance();
>      System.out.println(t1==t2);
>  }
> }
> class tool{
> //    私有化类的构造器
>  private tool() {
>  }
> //    声明当前类的对象，没有初始化：
> //    此对象也声明为static的
>  private static tool instance = null;
> //    声明public、static的返回当前类对象的方法
>  public static tool getInstance(){
>      if(instance==null){//避免出现构造多个对象的现象
>          instance = new tool();
>      }
>      return instance;
>  }
> }
> ```
>
> ==懒汉式的多线程==
>
> ```java
> class tool{
> //    私有化类的构造器
>  private tool() {
>  }
> //    声明当前类的对象，没有初始化：
> //    此对象也声明为static的
>  private static tool instance = null;
> //    声明public、static的返回当前类对象的方法
>  private static synchronized tool getInstance(){
>      if(instance == null){
>      if(instance==null){//避免出现构造多个对象的现象
>          instance = new tool();
>      }
>      }
>      return instance;
>  }
> }
> ```
>
> 

#### main( )方法：

> 1. 由于Java虚拟机需要调用类的main()方法，所以该方法的访问权限必须是
>    public，又因为Java虚拟机在执行main()方法时不必创建对象，所以该方法必须
>    是static的，该方法接收一个String类型的数组参数，该数组中保存执行Java命令
>    时传递给所运行的类的参数。
> 2. 又因为main() 方法是静态的，我们不能直接访问该类中的非静态成员，必须创
>    建该类的一个实例对象后，才能通过这个对象去访问类中的非静态成员，这种情
>    况，我们在之前的例子中多次碰到

### 二十二、类的成员之四：代码块（初始化块）：

> 1. ==代码块的作用：用来初始化类、对象==
>
> 2. 代码块如果修饰的话，只能使用static
>
> 3. 分类：**静态代码块、非静态代码块**
>
> 4. **静态（static）代码块：**
>
>    1. ```java
>       static{
>           内容;
>           .....
>       }
>       ```
>
>    2. 内部可以有输出语句
>
>    3. 随着类的加载而执行（==只会执行一次==）
>
>    4. 作用：初始化类的信息
>
>    5. 如果一个类中定义了多个静态代码块，则按照声明的先后顺序执行
>
>    6. 静态代码块比非静态代码块优先执行（类的声明先与对象的创建）
>
>    7. 静态代码块类，只能调用静态的方法和属性，不能调用非静态
>
>    8. ==static 代码块化 通常用于初始化static==
>
>    9. ```java
>       class Person {
>       public static int total;
>       static {
>       total = 100;// 为total 赋初值
>       }
>       …… //其它属性或方法声明
>       }
>       ```
>
> 5. **非静态代码块**：
>
>    1. 内部可以有输出语句
>    2. 随着对象的创建而执行（==每创建一个对象，就执行一次非静态代码块==）
>    3. 作用：可以在创建对象时，对对象的属性等进行初始化
>    4. 非静态代码块类，可以调用静态的方法和属性，也可以调用非静态
>
> 6. **成员变量赋值顺序总结：**
>
>    ![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-03-12_13-01-29.png)
>
>    ==由父及子，静态先行==：父类中有子类想继承的属性或方法，调用子类时，需要先“激活”父类
>
>    ```java
>    public class Something {//父类
>        public static String name;
>        int Id=1;
>        private int age;
>        static{
>            System.out.println("Father111");
>        }
>        {
>            System.out.println("Father222");
>        }
>    }
>    class son extends Something{//子类
>        static {
>            System.out.println("son111");
>        }
>        {
>            System.out.println("son222");
>        }
>    //入口main调用时，会“激活”所在的类son，且static类型同时激活，再根据由父及子，静态先行：
>        public static void main(String[] args) {
>            System.out.println("main111");
>            new son();
>        }
>    }
>    输出：
>    Father111
>    son111
>    main111
>    Father222
>    son222
>    ```

### 二十三、final修饰类和方法：

> ==final:最终的==
>
> ==用在权限修饰符后==
>
> 1. final可以用来修饰的结构：==**类、方法、变量**==
>
> 2. final修饰==引用数据类型==，该类型变量的地址确定不再改变，内容可进行改变
>
> 3. final 用来修饰一个类：
>
>    1. ==此类不能被其他类所继承==（比如：String类、System类）
>
>    2. 提高安全性，提高程序的可读性
>
>    3. ```java
>       final class A{
>       }
>       class B extends A{ //错误，不能被继承。
>       }
>       ```
>
> 4. final用来修饰一个方法：
>
>    1. ==表明此方法不能被重写==
>
>    2. 比如：Object类中的getClass()。
>
>    3. ```java
>       class A {
>       public final void print() {
>       System.out.println("A");
>       }
>       }
>       class B extends A {
>       public void print() { // 错误，不能被重写。
>       System.out.println("尚硅谷");
>       }
>       }
>       ```
>
> 5. final用来修饰一个变量：
>
>    1. 此时的”变量“称为一个==常量==：不能被修改的“变量”
>
> 6. final用来修饰属性：
>
>    1. 可以用显式赋值、构造器、代码块对final修饰的属性进行初始化
>
> 7. final修饰局部变量（相当局部常量）：
>
>    1. 尤其是使用final修饰形参时，表明此时形参是一个常量，当我们调用此方法时，给常量赋一个实参，一旦赋值以后，就只能在方法体内使用形参，但不能再修改形参的值
>
> 8. static final 用来修饰属性：全局变量

### 二十四、抽象类与抽象方法：

#### 抽象类的产生：

> 随着继承层次中一个个新子类的定义，类变得越来越具体，而父类则更一
> 般，更通用。类的设计应该保证父类和子类能够共享特征。有时将一个父
> 类设计得非常抽象，以至于它没有具体的实例，这样的类叫做抽象类

#### abstract关键字的使用：

> 1. abstract：抽象的
> 2. abstract可以用来修饰的结构：类（抽象类）、方法（抽象方法）
> 3. ==一旦类抽象了，就不可以实例化==
> 4. ==包含抽象方法的类，一定是一个抽象类==，**抽象类中可以没有抽象方法**

##### abstract修饰类：抽象类：

> 1. ==此类不能进行实例化==
>
> 2. 抽象类中一定有构造器，便于子类对象实例化的时候调用
>
> 3. 开发中，都会提供抽象类的子类，让子类实例化，完成相关操作
>
>    ```java
>    public class Test{
>        public void main(String[] args){
>            //利用多态性让子类帮助父类实例化：
>            Person p = new Student();
>            //则子类可以调用重写父类的抽象方法了
>        }
>    }
>    abstract class Person {
>        public Person(){
>        }
>        public Person(String name,int age){
>            this.name = name;
>            this.age = age;
>        }
>        public abstract void eat();
>    }
>    class Student extends Person{
>        public void eat(){
>            System.out.println("学生吃饭");
>        }
>    }
>    ```
>
>    

##### abstract修饰方法：抽象方法：

> 1. 抽象方法：==只有方法的声明，没有方法体==
> 2. 若子类重写了父类中的==所有的抽象方法后，此子类方可实例化==，否者子类也是一个抽象类，需要用abstract修饰

#### 使用时的注意事项：

> 1. abstract不能用来修饰：属性、构造器等
> 2. abstract不能用来修饰==私有方法==（无法重写父类中的私有方法）、静态方法（static）（子类重写父类的静态方法只是隐藏，多态时使用子类的方法，但父类的方法没有被覆盖）、final的方法、final的类。

#### 抽象类的匿名子类：

==边实例化边重写抽象类中的抽象方法==

> ```java
> public class PersonTest {
>     public static void main(String[] args){
> //        创建了一个匿名类的对象：p
>         Person p = new Person() {
>             @Override//重写父类中的抽象方法：
>             public void eat() {
>                 System.out.println("吃好饭");
>             }
>         };
>         p.eat();//输出：吃好饭
>     }
> }
> abstract class Person {
>     public Person(){
> 
>     }
>     public Person(String name,int age){
>         this.name = name;
>         this.age = age;
>     }
>     public abstract void eat();
> }
> class Student extends Person{
>     public void eat(){
>         System.out.println("学生吃饭");
>     }
> }
> ```
>
> ==此时可以不用创建子类（Student）来重写抽象类中的抽象方法==
>
> **还可以创建匿名对象的匿名子类**

### 二十五、接口：

#### 概述：

> * 一方面，有时**必须从几个类中派生出一个子类，继承它们所有的属性和方
>   法。**但是，Java不支持多重继承。有了接口，就可以得到多重继承的效果。
> * 另一方面，有时必须**从几个类中抽取出一些共同的行为特征**，而它们之间又
>   没有is-a的关系，仅仅是具有相同的行为特征而已。例如：鼠标、键盘、打
>   印机、扫描仪、摄像头、充电器、MP3机、手机、数码相机、移动硬盘等都
>   支持USB连接。
> * ==接口就是规范，定义的是一组规则，体现了现实世界中“如果你是/要...则
>   必须能...”的思想==。继承是一个"是不是"的关系，而接口实现则是 "能不能"
>   的关系。
> * **接口的本质是契约，标准，规范，就像我们的法律一样。制定好后大家都
>   要遵守**

#### 接口的使用：

> * 使用==interface来定义==
> * Java中，==接口和类是并列的两个结构==

#### 如何定义接口：

##### 定义接口中的成员：

> JDK8：
>
> * 可以定义==全局常量==、==抽象方法==、==静态方法==、==默认方法==
>
> * ==接口中定义全局常量时，可以省略 static final==，默认是常量，==抽象方法也可以省略关键字==：
>
>   ```java
>   interface Flyable{
>   //    写法一：
>       public static int MAX_SPEED = 7900;
>   //    写法二：默认为常量
>       int MIN_SPEED = 1;
>   //    写法一：
>       public abstract void fly();
>   //    写法二：默认为抽象方法
>       void stop();
>   }
>   ```
>
> * ==接口中不能定义构造器（接口不可以实例化）==
>
> * Java开发中，接口都==通过让类去实现（implements）的方式来使用==
>
>   ```java
>   class Plane implements Flyable{
>       public void fly(){
>           System.out.println("通过引擎");
>       }
>       public void stop(){
>           System.out.println("驾驶员减速停止");
>       }
>   }
>   ```
>
>   1. ==实现类可以理解为接口的子类==，但不能调用“父类”接口的方法（没有内容），实际调用“子类”中的方法，==类同于多态==
>   2. 如果实现类覆盖了（重写）接口中的所有抽象方法，则此实现类就可以实例化
>   3. 如果实现类没有覆盖接口中所有的抽象方法，则此实现类任为一个抽象类（需要加abstract才不会报错）
>
> * Java类可以实现多个接口 -----> 弥补了Java单继承性的局限（接口采用多继承机制）
>
> * ==多个接口，一个继承同时实现：==
>
>   * 格式：
>
>   * ```java
>     class AA extends BB implements CC,DD,EE{
>     }
>     ```
>
> * ==接口与接口之间可以继承，且可以多继承==
>
> * ```java
>   interface AA{
>       void method1();
>   }
>   interface BB{
>       void method2();
>   }
>   interface CC extends AA,BB{
>       void method3();
>   }
>   ```
>
> * 接口和类是并列关系，或者可以理解为一种特殊的类。从本质上讲，
>   接口是一种特殊的抽象类，这种抽象类中只包含常量和抽象方法的定义
>   (JDK7.0及之前,以后的版本有可以定义**静态方法、默认方法**)，而没有变量和方法的实现。
>
> * ==接口使用时需要动态的方式使用：==声明一个接口，用实例类来对其进行实例化并使用

##### 接口实现类的定义：

> ```java
> //Flash,Printer都是接口USB的实现类
> Computer com = new Computer;//Computer是一个类
> //创建了接口的非匿名实现类的非匿名对象
> Flash flash = new Flash();
> com.tranfer(flash);
> //创建了接口的非匿名实现类的匿名对象
> com.tranfer(new Printer());
> //创建了接口的匿名实现类的匿名对象
> USB phone = new USB(){
>   重写接口中的方法;  
> };
> ```

##### 接口中定义静态方法、默认方法：

> * ```java
>   //JDK8除了定义全局常量和抽象方法外，还可以定义静态方法、默认方法
>   public interface Interface_java8 {
>   //    静态方法：可以直接调用
>       public static void method1(){
>           System.out.println("1");
>       }
>   //    默认方法
>       public default void method2(){
>           System.out.println("2");
>       }
>       default void method3(){
>           System.out.println("3");
>       }
>   }
>                                                         
>   ```
>
> * ==默认方法使用 default 关键字修饰==。可以**通过实现类对象来调用**
>
> * 如果**实现类重写了接口中的默认方法**，调用时，仍然**调用的是重写以后的方法**
>
> * 接口中定义的**静态方法**，只能==通过“接口.静态方法”==来调用
>
> * 如果子类（实现类）继承的父类和实现的接口中，声明了同名同参数的方法，则子类在没有重写此方法的情况下，则默认调用的是==父类中的方法，类优先原则==
>
> * 如果在实现类***实现了多个接口**，而这些接口中定义了同名同参数的默认方法，那么在==实现类没有重写此方法的情况下==，==报错==------>接口冲突。则需要必须在实现类重写此方法

##### 如何在子类（接口类）的方法中调用父类、接口中被重写的方法：

> * ```java
>   class Study1 extends Study3 implements Interface_java8,Compare {
>   //重写父类和接口中的方法：
>       public void method3(){
>           System.out.println("Study1");
>       }
>       public void myMethod3(){
>   //        调用自己定义的重写的方法
>           method3();
>   //        调用父类中声明的方法：
>           super.method3();
>   //        调用接口中的默认方法：
>           Compare.super.method3();
>           Interface_java8.super.method3();
>   //        调用接口中的属性：
>           Compare.name;
>       }
>   }
>   class Study3 {
>       public void method3(){
>           System.out.println("父类3");
>       }
>   }
>   //定义的2个接口：
>   interface Interface_java8 {
>   //    默认方法
>       default void method3(){
>           System.out.println("3");
>       }
>   }
>   interface Compare{
>       String name = "Compare";
>       default void method3(){
>           System.out.println("Compare3");
>       }
>   }
>   ```

#### 排错：

> ```java
> interface A {
>     int x = 0;//全局常数
> }
> class B {
>     int x = 1;
> }
> class C extends B implements A {
>     public void pX() {
>         System.out.println(x);//如果能运行，就近原则：取父类中的x
>         //实际上编译不通过，接口与父类属性同名了
>     }
>     public static void main(String[] args) {
>         new C().pX();
>     }
> }
> ```

##### （同名时）如何分别调用着2个位置的变量（常量）：

> ```java
> interface A {
>     int x = 0;//全局常数
> }
> class B {
>     int x = 1;
> }
> class C extends B implements A {
>     public void pX() {
>         System.out.println(super.x);//1
>         System.out.println(A.x);//0
> //A中x的定义的完整模式：public static int x = 0;可以用实例化，直接"类.属性"调用
>     }
>     public static void main(String[] args) {
>         new C().pX();
>     }
> }
> ```

### 二十六、类的内部成员之五：内部类：

> * 在Java中，允许一个类的定义位于另一个类的内部，==前者称为内部类，后者
>   称为外部类==

#### 内部类的分类：

##### 成员内部类和局部内部内：

> * **局部内部类：方法内、代码块内、构造器内：**
>
> * ```java
>   class person{
>       public void method(){
>   //        局部内部类（方法内）：
>           class AA{
>                                                                     
>           }
>       }
>       {
>   //        局部内部类（代码块内）
>           class BB{
>                                                                     
>           }
>       }
>   //    局部内部类（构造器内）：
>       public person(){
>           class CC{
>                                                                     
>           }
>       }
>   }
>   ```
>
> * **成员内部类：静态成员内部类、非静态成员内部类：**
>
> * ```java
>   class person{
>   //静态成员内部类：
>       static class Dog{
>                                                                 
>   }
>   //非静态成员内部类：
>       class Bird{
>                                                                 
>       }
>   }
>   ```

##### 成员内部类：

> 1. **作为外部类的成员：**
>    1. 和外部类不同，==Inner class==还可以声明为 private 或 protected；
>    2. 可以调用外部类的结构
>    3. Inner class 可以声明为static的，但此时就不能再使用外层类的非 static的成员
>       变量；
>    4. 可以被4种不同的权限修饰
> 2. **作为一个类：**
>    1. 可以**在内部定义属性、方法、构造器等结构**
>    2. 可以声明为 abstract 类 ，因此==可以被其它的内部类继承==
>    3. 可以声明为 final ，不能被继承
>    4. 编译以后生成 OuterClass$InnerClass.class 字节码文件（也适用于局部内部类）
> 3. **注意：**
>    1. 非static的成员内部类中的成员不能声明为static的，只有在外部类或static的成员
>       内部类中才可声明static成员。
>    2. 外部类访问成员内部类的成员，需要 “内部类.成员” 或 “内部类对象.成员” 的方式
>    3. ==成员内部类可以直接使用外部类的所有成员，包括私有的数据==
>    4. 当想要在外部类的静态成员部分使用内部类时，可以考虑内部类声明为静态的

#### 如何实例化成员内部类的对象？：

> ```java
> public class Study {
>     public static void main(String args[]) {
> //        创建一个Dog的实例（静态成员内部类）：
>         Person.Dog dog = new Person.Dog();
>         dog.show();
> //        创建Bird实例（非静态的成员内部类）：
>         Person p = new Person();
>         Person.Bird bird = p.new Bird();//用实例化对象p调用Person类里面的内部类结构
>         bird.sing();
>     }
> }
> ```

#### 如何在成员内部类中区分调用外部类的结构？：

>==如果定义的内部类与外部类中的属性没有重名，则直接调用==；
>
>如果重名了：
>
>```java
>public class Outer {
>private int s = 111;
>public class Inner {
>private int s = 222;
>public void mb(int s) {
>System.out.println(s); // 局部变量s
>System.out.println(this.s); // 内部类对象的属性s
>System.out.println(Outer.this.s); // 外部类对象属性s
>}
>}
>public static void main(String args[]) {
>Outer a = new Outer();
>Outer.Inner b = a.new Inner();
>b.mb(333);
>}
>}
>```

### 二十七、Java异常处理的方式：

#### throw·与throws区别：

throw：生成一个异常对象并抛出，使用在方法内部<--------------->自动抛出异常对象

throws：处理异常的方式，使用在方法声明处的末尾<--------------->try-catch-finally

上有排污（throw），下有治污（throws）

#### 方式一：try-catch-finally：

##### 过程一：

> 程序在正常执行的过程中，一旦出现异常，就会在异常代码处生成一个对应异常类的对象，并将此对象抛出
>
> 一旦抛出对象后，其后的代码就不再执行

##### 过程二：

> 可以理解为异常的处理方式：1.try-catch-finally 2.throws

##### try-catch-finally的使用

> ==try==:捕获异常的第一步是用try{…}语句块选定捕获异常的范围，将可能出现
> 异常的代码放在try语句块中
>
> ==catch==:在catch语句块中是对异常对象进行处理的代码。每个try语句块可以伴随
> 一个或多个catch语句，用于处理可能产生的不同类型的异常对象。

方式二：而throws + 异常类型：

### 二十八、多线程

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-03-23_09-08-20.png)

#### 并行与并发：

> 并行与并发:
>
> * 并行：多个CPU同时执行多个任务。比如：多个人同时做不同的事。
> * 并发：一个CPU(采用时间片)同时执行多个任务。比如：秒杀、多个人做同一件事。

#### 何时需要多线程：

> * 程序需要同时执行两个或多个任务。
> * 程序需要实现一些需要等待的任务时，如用户输入、文件读写。
> * 操作、网络操作、搜索等。
> * 需要一些后台运行的程序时 。

#### 线程的创建和使用：

* Java语言的JVM允许程序运行多个线程，它通过==java.lang.Thread
  类==来体现。
* Thread类的特性：
  * 每个线程都是**通过某个特定Thread对象的run()方法来完成操作的**，经常
    把run()方法的主体称为==线程体==
  * **通过该Thread对象的start()方法来启动这个线程，而非直接调用run()**

#### 多线程定义方式一：

##### 步骤：

```注释
多线程的创建：
* 方式一：继承与Thread类
* 1.创建一个继承于Thread类的子类
* 2.重写Thread类的run()方法---->将此线程执行的操作声明在run()中
* 3.创建Thread类的子类的对象（每创建一个线程，就声明一个对象）
* 4.通过此对象调用start()
```

##### 实例：

```java
public class ThreadTest {
    public static void main(String[] args) {
//    创建Thread子类的对象：
        MyThread t1 = new MyThread();
        MyThread t2 = new MyThread();
//        调用此对象的start()：①启动当前线程②调用当前线程的run()
        t1.start();//自动调用run方法,多线程原因：输出结果会与下面的输出交替输出
//        t1.run();//直接调用run方法，不会执行多线程：会进行正常的先后执行
//        如下操作仍是在main线程中执行的：
        for(int i = 0;i<100;i++){
            if(i%2==0){
                System.out.println(i+"********");
            }
        }
    }
}
class MyThread extends Thread{
//    重写run()方法：
    @Override
    public void run() {
        for(int i = 0;i<100;i++){
            if(i%2==0){
                //currentThread():返回当前线程：（主函数调用Thread.currentThread()返回主线程）
                System.out.println(i+Thread.currentThread().getName());
            }
        }
    }
}
```

==创建Thread的一个匿名子类并进行多线程调用==:

```java
//        创建Thread的一个匿名子类并进行多线程调用：
        new Thread(){
            @Override
            public void run() {
                for(int i=0;i<100;i++){
                    if(i%2==0){
                        System.out.println(i);
                    }
                }
            }
        }.start();
```

**问题：**

> 1. 我们不能通过直接调用run( )的方式启动多线程
> 2. 再启动一个线程（实现100以内的偶数），不可以还让已经start( )的线程去执行。（会报错）
>    * ==此时可以再new一个Thread的子类对象，继续调用start( )==

###### 测试Thread类中的常用方法：

```注释
测试Thread类中的常用方法：
* 1.start()方法：启动当前线程，调用当前线程的run()
* 2.run():通常需要重写Thread类中的此方法，将创建的线程要执行的操作声明在此方法中
* 3.currentThread():静态方法，返回执行当前代码的线程
* 4.getName():获取当前线程的名字
* 5.setName():设置当前线程的名字
```

* yield(): 释放当前cup的执行权（执行线程1遇到时，退出线程1的执行，执行其他线程）：

  * ```java
    public void run() {
            for (int i = 0; i < 100; i++) {
                if (i % 2 == 0) {
                    this.yield();
                    System.out.println(i + Thread.currentThread().getName());
                }
            }
        }
    ```

* join(): 在线程A中调用线程B的join( )，此时线程A就进入阻塞状态，直到线程B完全执行完以后，线程A才结束阻塞状态(==谁调用，谁阻塞==)

  * ```java
    public class ThreadTest {
        public static void main(String[] args) {
    //    创建Thread子类的对象：
            MyThread t1 = new MyThread();
            t1.setName("线程一");
            t1.start();
            for(int i = 0;i<100;i++){
                if(i%2==0){
                    System.out.println(i+"**主线程");
                }else if(i==11) {
                    try {
                        t1.join();//调用Thread子类中的join()，
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                }
            }
        }
    }
    ```

  * 执行效果：

    ![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-03-22_18-01-28.png)

* sleep(long 毫秒数)：让当前线程“睡眠”指定的毫秒，当前线程是阻塞状态，属于静态方法，用Thread类直接调用：

  ```java
  class MThread implements Runnable{
  //2.实现类去实现Runnable中的抽象方法：run()
      @Override
      public void run() {
          for (int i = 0; i < 100; i++) {
              if(i%2==0){
                  try {
                      Thread.sleep(1000);//通过Thread类直接调用
                  } catch (InterruptedException e) {
                      e.printStackTrace();
                  }
                  System.out.println(i+Thread.currentThread().getName());
              }
          }
      }
  }
  ```

  

* isAlive( ):判断当前线程是否存活

#### 线程的调度：

#####  线程的优先级等级：

* MAX_PRIORITY ：10
* MIN _PRIORITY ：1
* NORM_PRIORITY ：5

##### 涉及的方法：

* getPriority() ： ：获取返回线程优先值
* setPriority(int newPriority) ： ：改变线程的优先级

##### 说明：

* 线程创建时继承父线程的优先级
* ==低优先级只是获得调度的概率低，并非一定是在高优先级线程之后才被调用== 

==高优先级线程要抢占低优先级线程cpu的执行权，但是只是从概率上讲，高优先级比低优先级优先执行，也可能会有低优先级比高优先级先执行==

##### 例子：

100张高铁票，2个不同的窗口卖票，创建多线程：

```java
package newStudy;
//存在线程安全问题：
public class ThreadDemo {
    public static void main(String[] args) {
        window w1 = new window();
        window w2 = new window();
        w1.setName("窗口1");
        w2.setName("窗口2");
        w1.start();
        w2.start();
    }
}
class window extends Thread{
    static private int ticket = 100;//总票100张，不能同时出现2张相同号的票，所以声明静态变量
    public void run(){
        while (true){
            if(ticket>0){
                System.out.println(this.getName()+"卖票，票号为："+ticket);
            }else {
                break;
            }
            ticket=ticket-1;
        }
    }
}
```

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-03-22_19-43-07.png)

#### 多线程定义方式二：

##### 步骤：

==创建多线程方式二：实现Runnable接口==

```注释
* 创建多线程方式二：实现Runnable接口
* 1.创建一个实现了Runnable接口的类
* 2.实现类去实现Runnable中的抽象方法：run()
* 3.创建实现类的对象
* 4.将此对象作为参数传递到Thread类的构造器中，创建Thread类的对象
* 5.通过Thread类的对象调用start()
```

##### 实例：

```java
public class ThreadTest1 {
    public static void main(String[] args) {
//        3.创建实现类的对象
        MThread mThread = new MThread();//实现类只进行一次对象创建，后面传入Thread的都是一个对象
//        4.将此对象作为参数传递到Thread类的构造器中，创建Thread类的对象
        Thread t1 = new Thread(mThread);
//        5.通过Thread类的对象调用start():①启动线程②调用当前线程的run()-->调用了Runnable类型的target()(mThread)的run()
        t1.setName("副线程1");//对线程修改名字
        t1.start();//调用了Runnable类型的target()(mThread)的run()
        Thread t2 = new Thread(mThread);//传入对象的目的：返回run()函数，达到调用的效果
        t2.setName("副线程2");
        t2.start();
    }

}
//1.创建一个实现了Runnable接口的类
class MThread implements Runnable{
//2.实现类去实现Runnable中的抽象方法：run()
    @Override
    public void run() {
        for (int i = 0; i < 100; i++) {
            if(i%2==0){
                System.out.println(i+Thread.currentThread().getName());
            }
        }
    }
}
```

#### 两种方式的比较：

> 1. 开发中首选：==实现Runnable接口的方式==
> 2. 原因：
>    * 实现的方式没有类的单继承性的局限性
>    * 实现的方式==更适合来处理多个线程有共享数据的情况==（不用在子类中static属性来实现共享数据）
> 3. 联系：
>    * ==Thread类本身也实现了Runnable接口==
>    * 即：方式一通过继承Thread获取run( )方法，方式二通过直接实现Runnable接口获取run( )方法
>    * 两种方法都需要重写run( )，将线程要执行的逻辑声明在run( )中，都需要使用 Thread 类

#### 线程的生命周期：

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-03-23_10-50-34.png)

#### 线程安全问题：

> **问题**：买票过程中，出现了重票、错票
>
> **问题出现的原因**：当某个线程操作车票的过程中，尚未操作完成时，其他线程参与进来，也操作车票
>
> **如何解决：**当一个线程a在操作ticket的时候，其他线程不能参与进来，直到线程a操作完ticket时，线程才可以开始操作ticket，这种情况即使线程a出现了阻塞，也不能被改变

在Java中，通过同步机制，来解决线程的安全问题：

##### 方式一：同步代码块

```java
// 方式一：
 synchronized(同步监视器){
     //需要被同步的代码（操作共享数据的代码）
     //共享数据：多个线程操作的变量
 }
//1.共享数据：多个线程操作的变量
//2.同步监视器：俗称：锁。任何一个对象都可以充当锁
//3.锁的要求：多个线程，都必须共用同一把锁（如：Object对象、方式二定义下可以使用this(本类)、方式二下定义的不能使用this可以使用：自己类名.class（只会加载一次），如果另声明一个类（锁）时用static修饰
```

```java
class window implements Runnable{
    private int ticket = 100;
    Object obj = new Object();//锁只要满足线程共用（共享一个对象的数据）
    public void run(){
//        obj锁不能声明在run类，每一线程调用一次，这样一个线程一把锁，不满足共用一把锁的情况
        synchronized (obj) {
        while (true) {
                if (ticket > 0) {
                    System.out.println(Thread.currentThread().getName() + "卖票，票号为：" + ticket);
                    ticket--;
                } else {
                    break;
                }
            }
        }
    }
}
```

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-03-25_23-10-29.png)

==方式一的评价：==解决了线程的安全问题，操作同步代码的同时，只能有一个线程参与，其他线程等待，相当于是一个单线程，效率低。

==说明：==在继承Thread类创建多线程的方式中，慎用this充当同步监视器，考虑使用当前类充当同步监视器（在子类中创建一个static对象作为锁，保证同步监视器唯一即可）

##### 方式二：同步方法

==直接在子类（实例化类）中创建一个私有 synchronized  修饰的方法执行run方法中需要执行的功能代码==

* ==适用于接口实现类的方式定义的多线程==
* （非静态）同步方法，默认同步监视器是：**this**

```java
package newStudy;

import sun.awt.windows.ThemeReader;

public class ThreadDemo {
    public static void main(String[] args) {
        window window = new window();
        Thread w1 = new Thread(window);
        Thread w2 = new Thread(window);
        w1.setName("窗口1");
        w2.setName("窗口2");
        w1.start();
        w2.start();
    }
}
class window implements Runnable {
    private int ticket = 100;
    public void run() {
        while (true) {
            show();
            if(ticket<=0){
                break;
            }
        }
    }
//直接创建一个synchronized修饰的功能方法：（默认同步监视器是this）
    private synchronized void show(){
//        synchronized (this) {
                if (ticket > 0) {
                    System.out.println(Thread.currentThread().getName() + "卖票，票号为：" + ticket);
                    ticket--;
                }
            }
//        }
}
```

* ==适用于继承Thread类的方式定义多线程==
* 由于每一次创建一个线程，则创建一个类，此时synchronized修饰的方法不共享，同步监视器（默认的this）也不共享，于是声明为static形式。
* （静态同步方法）此时该方式的默认同步监视器是：**当前类本身.class**

```java
public class ThreadTest {
    public static void main(String[] args) {
//    创建Thread子类的对象：
        MyThread t1 = new MyThread();
        MyThread t2 = new MyThread();
//        调用此对象的start()：①启动当前线程②调用当前线程的run()
        t2.setName("副线程2");
        t1.setName("副线程1");
        t1.start();
        t2.start();
            }
        }
class MyThread extends Thread {
    //    重写run()方法：
    static int ticket = 100;
    @Override
    public void run() {
        while (true){
            show();
            if(ticket<=0){
                break;
            }
        }
    }
    private static synchronized void show(){//所有声明的对象都共用这一个方法，保证同步监视器的唯一
        if (ticket > 0) {
            System.out.println(Thread.currentThread().getName() + "卖票，票号为：" + ticket);
            ticket--;
        }
    }
}
```

#### 线程的死锁问题：

* 不同的线程分别占用对方需要的同步资源不放弃，都在等待对方放弃
  自己需要的同步资源，就形成了线程的死锁

* 出现死锁后，不会出现异常，不会出现提示，只是所有的线程都处于
  阻塞状态，无法继续

* ```java
  public class DeadLockTest {
  public static void main(String[] args) {
  final StringBuffer s1 = new StringBuffer();
  final StringBuffer s2 = new StringBuffer();
  new Thread() {
  public void run() {
  synchronized (s1) {//一个线程需要先拿s1锁才能进入，另一个线程需要拿到s2锁，此时进入下个阶段时，各自需要的锁都被互相占用，不能继续向下执行
  s2.append("A");
  synchronized (s2) {
  s2.append("B");
  System.out.print(s1);
  System.out.print(s2);
  }
  }
  }
  }.start();
      new Thread() {
  public void run() {
  synchronized (s2) {//需要先拿s2锁
  s2.append("C");
  synchronized (s1) {
  s1.append("D");
  System.out.print(s2);
  System.out.print(s1);
  }
  }
  }
  }.start();
  }
  }
  ```

#### 解决线程安全问题的方式三：Lock锁

JDK:5.0

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-03-31_12-41-00.png)

```java
class MThread implements Runnable{
//2.实现类去实现Runnable中的抽象方法：run()
    static private int ticket = 100;
//    1.实例化ReentrantLock
    private final ReentrantLock lock = new ReentrantLock();
//用final修饰对象，该对象的地址不再改变，内容可变
    @Override
    public void run() {
        try {
//     2.启动同步锁
            lock.lock();
            while (true) {
                if (ticket > 0) {
                    System.out.println(Thread.currentThread().getName() + ":售票，票号为：" + ticket);
                    ticket--;
                } else {
                    break;
                }
            }
        }finally {
//       3.调用解锁的方法：
            lock.unlock();
        }
    }
}
```

```java
//调用ReentrantLock对象的lock()方法获取锁，调用unlock()方法释放锁
private Lock ticklock=new ReentrantLock();
```

```java
public class MyThread{
    private Lock lock=new ReentrantLock();
    public void TestMethod(){
        lock.lock();         //得到对象锁
        for(int i=0;i<5;i++){
            System.out.println(Thread.currentThread().getName()+i);
        } 
        lock.unlock();        //释放对象锁.不调用释放锁，则一直执行该线程到结束，后面线程也无法拿到锁
    }
}
```

#### 涉及到线程通信的方法：

* ==使用前提==：

  1. 只能是在同步代码块或者同步方法（锁）当中（lock中还不能使用）

                       2. 这三个方法的调用者必须是同步代码块或同步方法中的同步监视器（锁）
     
     3. 三个方法定义在Object类里面

> * wait( ):一旦执行此方法，当前线程就进入阻塞状态，并释放同步监视器（锁）
> * notify( ): 一旦执行此方法，则就会唤醒被wait的一个线程，如果多个线程被wait，就唤醒优先级高的（只能唤醒一个被阻塞的线程）
> * notifyall( ):一旦执行唤醒所以被阻塞的线程

#### sleep( )与wait( )方法的异同：

> 相同点：一旦执行方法，都可以使得当前的线程进入阻塞状态
>
> 不同点：
>
> 1. 两个方法声明的位置不同：Thread类中声明sleep( )，Object类中声明wait( )
> 2. 调用的范围不同：sleep可以在任何需要的场景下调用，wait( )方法需要在同步代码块或者同步方法中
> 3. 关于是否释放同步监视器：如果两个方法都使用在同步代码块或同步方法中，sleep( )不会释放同步监视器（拿着锁不放，使后面的线程在该线程等待时也在等待）。wait( )则释放锁

##### synchronized与Lock的异同？

![](C:\Users\asus\Pictures\Screenshots\Snipaste_2021-03-31_12-40-34.png)

> 相同：都可以解决线程安全问题
>
> 不同点：
>
> * synchronized机制在执行完相应代码后，自动的释放同步监视器
> * Lock需要手动的启动同步（Lock( )），同时结束同步也需要手动的实现（unlock()）

#### 创建线程新方式：

##### 方式一实现Callable接口:

**与使用Runnable相比， Callable功能更强大些**

* 相比run()方法，可以有返回值
* 方法可以抛出异常
* 支持泛型的返回值
* 需要借助FutureTask类，比如获取返回结果 

 **Future接口**：

* ==可以对具体Runnable、Callable任务的执行结果进行取消、查询是
  否完成、获取结果等。==
* ==FutrueTask是Futrue接口的唯一的实现类==
* FutureTask 同时实现了Runnable, Future接口。它既可以作为
  Runnable被线程执行，又可以作为Future得到Callable的返回值

##### 创建线程的步骤：

（求100以内的所有偶数的和）

1. 创建一个==实现Callable接口的实现类==
2. 实现call( )方法，将此线程需要执行的操作声明在call( )方法中【call( )有返回值，可选择要或者不要】
3. 创建Callable接口实现类的对象
4. 将此Callable实现类的对象作为参数传入到FutureTask构造器中，创建FutureTask的对象
5. 将FutureTask的对象作为参数传递到Thread类的构造器中，创建Thread对象，并调用start( )启动线程
6. 获取Callable中的call( )方法的返回值【如果只是执行call( )方法的内容，不需要返回值，可以省略6步骤，返回值写：==return null==】

```java
package newStudy;

import java.util.concurrent.Callable;
import java.util.concurrent.ExecutionException;
import java.util.concurrent.Future;
import java.util.concurrent.FutureTask;
//1.创建一个实现Callable接口的实现类
class NumThread implements Callable{
//    重写一个call的方法,将需要被多线程执行的代码放入call()方法中
    @Override
//2.实现call( )方法，将此线程需要执行的操作声明在call( )方法中
    public Object call() throws Exception {//返回值属于Object引用数据类型
        int sum = 0;
        for (int i = 1; i <= 100; i++) {
            if(i%2==0){
                System.out.println(i);
                sum += i;
            }
        }
        return sum;//自动装箱，转化为integer
    }
}
public class ThreadNew {
    public static void main(String[] args) {
//3.创建Callable接口实现类的对象
        NumThread n1 = new NumThread();
//4.将此Callable实现类的对象作为参数传入到FutureTask构造器中，创建FutureTask的对象
        FutureTask futureTask = new FutureTask(n1);
//5.将FutureTask的对象作为参数传递到Thread类的构造器中，创建Thread对象，并调用start( )启动线程
        new Thread(futureTask).start();
        try {
//6.get方法的返回值即为FutureTask构造器参数Callable实现类重写的 call()方法 的返回值
//            如果不需要看call()方法的返回值，则可以不用调用get()方法
            Object sum = futureTask.get();
            System.out.println(sum);
        } catch (InterruptedException e) {
            e.printStackTrace();
        } catch (ExecutionException e) {
            e.printStackTrace();
        }
    }
}
```

##### 如何理解实现Callable接口的方式创建多线程比实现Runnable接口创建多线程方式强大？

* call( )方法可以有返回值
* call( )方法可以抛出异常，被外面的操作捕获，获取异常的信息
* Callable是==支持泛型==

##### 方式二使用线程池：

==线程池：==提前创建好多个线程，放入线程池中，使用时直接获取，使用完放回池中。可以避免频繁创建销毁、实现重复利用。类似生活中的公共交通工具。

==定义多线程后扔进线程池，启动线程==

##### 好处：

* 提高响应速度（减少了创建新线程的时间）
*  降低资源消耗（重复利用线程池中线程，不需要每次都创建）
* 便于线程管理 ：
  *  corePoolSize：核心池的大小
  *  maximumPoolSize：最大线程数
  * keepAliveTime：线程没有任务时最多保持多长时间后会终止

```注释
 * 创建线程的方式四：使用线程池：
 * 1. 提供指定线程数量的线程池
 * 2. 执行指定的线程的操作，需要提供实现Runnable接口或Callable接口实现类的对象
 *        service.execute(); 适合用于Runnable
 *        service.submit();  适合用于Callable
 * 3. 关闭连接池：service.
```

```java
// 2.用实现Runnable接口的方法定义2个多线程
class NumberThread implements Runnable{
    @Override
    public void run() {
        for (int i = 0; i <= 100; i++) {
            if(i%2==0){
                System.out.println(i);
                System.out.println(Thread.currentThread().getName());
            }
        }
    }
}
class NumberThread1 implements Runnable{
    @Override
    public void run() {
        for (int i = 0; i <= 100; i++) {
            if(!(i%2==0)){
                System.out.println(Thread.currentThread().getName());
                System.out.println(i);
            }
        }
    }
}
public class ThreadPool {
    public static void main(String[] args) {
        // 1.创造一个10个线程数的线程池：
        ExecutorService service = Executors.newFixedThreadPool(10);
//        5.设置线程池的属性:(理论是利用线程池的对象进行方法的调用，由于线程池是接口，则调用实现类，再调用其方法）
//        4.查看线程池接口实现类：
//        System.out.println(service.getClass());//输出：class java.util.concurrent.ThreadPoolExecutor
//        6.对 ExecutorService的对象进行强转：
        ThreadPoolExecutor service1 = (ThreadPoolExecutor) service;
        service1.setCorePoolSize(18);//设置核心池的大小
//        service.execute(); 适合用于Runnable
//        service.submit();  适合用于Callable
//      3.利用接口Runnable定义的多线程传入实现类的对象:
        service.execute(new NumberThread());
        service.execute(new NumberThread1());
        service.shutdown();// 4.关闭线程池
    }
}
```

### 二十九、常用类：

#### 字符串相关的类：

#####  String类： 

* String类 ： 代表字符串。Java 程序中的所有字符串字面值（如 "abc" ）都作
  为此类的实例实现。
* String是一个final类，代表不可变的字符序列（不可变性）,不可被继承。
  * 体现：
  * 当对字符串重新赋值时，需要重写指定内存区域赋值，不能使用原有的value进行赋值
  * 当对现有的字符串进行连接操作时，也需要重新指定内存区域赋值，不能使用原有的value直接赋值
  * 当调用String的replace修改方法时，修改内部指定的字符，也需要重新指定内存区域

* String
  * 实现了Serializable实现接口：表示字符串是支持序列化的
  * 实现了Comparable接口：表示String可以比较大小
* 字符串是常量，用双引号引起来表示。它们的值在==创建之后不能更改==。
* String对象的字符内容是存储在一个字符数组value[ ]中的
* 通过字面量的方式（区别于new）给一个字符串赋值，此时的字符串值声明在字符串常量池中
* 字符串常量池中是不会存储相同内容的字符串的

##### String两种实例化方式：

```java
/**
 * String的实例化方式：
 * 方式一：通过字面量定义的方式
 * 方式二：通过new + 构造器的方式
 *
 * */

@Test
public void test1(){
    //此时的s1s2声明在字符串常量池中：
    String s1 = "javaEE";
    String s2 = "javaEE";
    //通过new的方式，此时s3s4保存的地址值，是数据在堆空间中开辟空间以后对
    String s3 = new String("javaEE");
    String s4 = new String("javaEE");

    System.out.println(s1 == s2);//true
    System.out.println(s3 == s4);//false(两个不同地址的新对象)
    System.out.println(s3 == s1);//false
    System.out.println(s1.equals(s3));//true
    System.out.println(s3.equals(s4));//true
}
```

**这两个方式的区别：**

[java中String new和直接赋值的区别]: https://blog.csdn.net/u014082714/article/details/50087563?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522161832235116780271519245%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&amp;request_id=161832235116780271519245&amp;biz_id=0&amp;utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-2-50087563.first_rank_v2_pc_rank_v29&amp;utm_term=java+string+new+string	"java中String new和直接赋值的区别"

```java
@Test
public void test2(){
    String s1 = "javaEE";
    String s2 = "hadoop";

    String s3 = "javaEEhadoop";
    String s4 = "javaEE" + "hadoop";

    String s5 = s1 + "hadoop";
    String s6 = "javaEE" + s2;
    String s7 = s1 + s2;

    System.out.println(s3 == s4);//true
    System.out.println(s3 == s5);//false
    System.out.println(s3 == s6);//false
    System.out.println(s3 == s7);//false
    System.out.println(s5 == s7);//false

    String s8 = s5.intern();//返回值得到的s8是在常量池中已经存在的"javaEEhadoop"
    System.out.println(s3 == s8);//true
}
```

==结论：==

1. ==常量与常量的拼接==结果==在常量池==。且常量池中不会存在相同内容的常量。**（final修饰的变量为常量）**
2. 只要其中有一个是变量，结果就在堆中
3. 如果拼接的结果调用intern()方法，返回值就在常量池中

```java
public class StringTest {
String str = new String("good");
char[] ch = { 't', 'e', 's', 't' };
public void change(String str, char ch[]) {
str = "test ok";
ch[0] = 'b';
}
public static void main(String[] args) {
StringTest ex = new StringTest();
ex.change(ex.str, ex.ch);
System.out.print(ex.str + " and ");//good and
System.out.println(ex.ch);//best
	}
}
//若change方法的形参str改变成除了str外的一个明，又或者方法体中：改为this.str = "test ok",则输出结果变成test ok and best
/*s1 = s1 + "b";
说明：实际上原来的“a”字符串对象已经丢弃了，现在在堆空间中产生了一个字符
串s1+"b"（也就是"ab")。如果多次执行这些改变串内容的操作，会导致大量副本
字符串对象存留在内存中，降低效率。如果这样的操作放到循环中，会极大影响
程序的性能*/
```

##### String类的常用方法1：

```java
int length();// ：返回字符串的长度： return value.length
char charAt(int index);// ： 返回某索引处的字符return value[index]
boolean isEmpty();// ：判断是否是空字符串：return value.length == 0
String toLowerCase();// ：使用默认语言环境，将 String 中的所有字符转换为小写
String toUpperCase();// ：使用默认语言环境，将 String 中的所有字符转换为大写
String trim();//：返回字符串的副本，去除前导空白和尾部空白
boolean equals(Object obj);// ：比较字符串的内容是否相同
boolean equalsIgnoreCase(String anotherString);// ：与equals方法类似，忽略大小写
String concat(String str);// ：将指定字符串连接到此字符串的结尾。 等价于用“+”
int compareTo(String anotherString);// ：比较两个字符串的大小，大于0前面大，小于0反之（比较相差ASCII码）
String substring(int beginIndex);//：返回一个新的字符串，它是此字符串的从 beginIndex开始 截取到 最后的一个子字符串。
String substring(int beginIndex, int endIndex);//：返回一个新字符串，它是此字符串从beginIndex开始截取到endIndex(不包含)的一个子字符串。与python范围取值方法类似含右不含左
```

##### String类的常用方法2：

```java
boolean endsWith(String suffix);// ：测试此字符串是否以指定的后缀结束
boolean startsWith(String prefix);// ：测试此字符串是否以指定的前缀开始
boolean startsWith(String prefix, int toffset);// ：测试此字符串从指定索引开始的子字符串是否以指定前缀开始
```

```java
boolean contains(CharSequence s);// ：当且仅当此字符串包含指定的 char 值序列时，返回 true
int indexOf(String str);// ：返回指定子字符串在此字符串中第一次出现处的索引
int indexOf(String str, int fromIndex);// ：返回指定子字符串在此字符串中第一次出现处的索引，从指定的索引开始(可以用来统计字符串出现的次数)
int lastIndexOf(String str);// ：返回指定子字符串在此字符串中最右边出现处的索引
int lastIndexOf(String str, int fromIndex);// ：返回指定子字符串在此字符串中最后一次出现处的索引，从指定的索引开始 反向搜索
//注：indexOf和lastIndexOf方法如果未找到都是返回-1
```

##### String类的常用方法3：

```java
String replace(char oldChar, char newChar);// ：返回一个新的字符串，它是通过用 newChar 替换此字符串中出现的 所有 oldChar 得到的。
String replace(CharSequence target, CharSequence replacement);// ：使用指定的字面值替换序列替换此字符串 所有匹配字面值 目标序列的子字符串。
String replaceAll(String regex, String replacement);// ： 使用给定的replacement 替换此字符串所有匹配给定的正则表达式的子字符串。
String replaceFirst(String regex, String replacement);// ： 使用给定的replacement 替换此字符串 匹配 给定的正则表达式的 第一个子字符串。
```

[replace与replaceAll](https://blog.csdn.net/weixin_44782075/article/details/88699932?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522161833023716780262510861%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&amp;request_id=161833023716780262510861&amp;biz_id=0&amp;utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-1-88699932.first_rank_v2_pc_rank_v29&amp;utm_term=replace%E4%B8%8Ereplaceall%E7%9A%84%E5%8C%BA%E5%88%AB)

```java
boolean matches(String regex);// ：告知此字符串是否匹配给定的正则表达式。
```



```java
String str = "12345";
String str1 = "023-2321232";
boolean m = str.matches("\\d+");//判断str字符串是不是全是数字
boolean m1 = str.matches("023-\\d{7,8}");//判断是不是023-开头且后面数字是否为7-8位，都满足则返回true，否则返回false
```

```java
String[] split(String regex);// ：根据给定正则表达式的匹配拆分此字符串。
String[] split(String regex, int limit);// ：根据匹配给定的正则表达式来拆分此字符串，最多不超过limit个，如果超过了，剩下的全部都放到最后一个元素中。
```

```java
String str = "Hello|world|dsa";
str.split("\\|");//以|作为切割线
```

##### 字符串的最大相同子串查找：

获取两个字符串中最大相同子串。比如：
str1 = "abcwerthelloyuiodef“;str2 = "cvhellobnm"

提示：将短的那个串进行长度依次递减的子串与较长的串比较。

```java
public String Function(String str1,String str2){
        if(str1 != null && str2 != null){
            String strMax = (str1.length() >= str2.length()) ? str1 : str2;
            String strMin = (str1.length() < str2.length()) ? str1 : str2;
//从可能出现的最长的相同子字符串（整个短的字符串）开始比较
            for(int i = 0;i < strMin.length();i++){//需要比较的子字符串数
                for(int a = 0,j = strMin.length()-i;j <= strMin.length();j++,a++){
                    String str3 = strMin.substring(a,j);//对短的字符串进行取子字符串判断是否在长字符串中
                    if(strMax.contains(str3)){
                        return str3;
                    }
                }
            }
        }
        return null;
    }
```

##### \ \ d+与^,$符：

```java
String str1 = "123China343Hello009";
String str2 = str1.replaceAll("\\d",",");// \\d 匹配一个数字，将出现的数字用","替换，一个数字替换成一个","
//输出：str2: ,,,China,,,Hello,,,
String str4 = str1.replaceAll("\\d+",",");//  \\d+ 匹配一连续的数字，将某一次出现一连续的数字替换成一个","
//输出：str4: ,China,Hello,
```

```java
String str1 = ",China,Hello,";
String str2 = str1.replaceAll("^,|,$","");
//释义：^，$分别表示字符串开头和结尾，^,|,$表示如果开头或者结尾有","则去掉
```

![]()![Snipaste_2021-04-14_19-28-08](F:\Java语言学习\笔记保存的截图\Snipaste_2021-04-14_19-28-08.png)

![](F:\Java语言学习\笔记保存的截图\Snipaste_2021-04-14_19-29-44.png)

##### String--->char[ ]:

==调用String的toCharArray( )==

```java
String str = "abc123";
char[] charArray = str.toCharArray();
for(int i = 0;i<charArray.length;i++){
    System.out.println(charArray[i]);//a b c d 1 2 3
}
```

##### char[ ]--->String:

==将char[]类型扔在String构造器中：==

```java
char[] arr = {'a','b','c','d'};
String str = new String(arr);
System.out.println(str);//abcd
```

#### String与byte[]字节数组：

##### 编码：String--->byte[]:

==调用String的getBytes( )==

getBytes( )方法可以指定编码器（有ASCII的字符，编码出来的数字都是ASCII值且相同）

```java
public byte[] getBytes();// ：使用平台的默认字符集将此 String 编码为byte 序列，并将结果存储到一个新的 byte 数组中。
public byte[] getBytes(String charsetName);// ：使用指定的字符集将此 String 编码到 byte 序列，并将结果存储到新的 byte 数组。
```

==使用的字符集不同，编码出的个数也不同==

```java
String str1 = "abc123";
byte[] s = str1.getBytes();//将字符串每个字符转化为对应的ASCII码值
//调用Arrays.toString()直接输出数组
System.out.println(Arrays.toString(s));
//输出：[97,98,99,49,50,51]
```

##### 解码：byte[]--->String:

```java
String(byte[]);//：通过使用平台的默认字符集解码指定的 byte 数组，构造一个新的 String。
String(byte[] ，int offset ，int length);// ：用指定的字节数组的一部分，即从数组起始位置offset开始取length个字节构造一个字符串对象。
```

==用哪种字符集编码，就用哪种字符集解码，否则可能出现乱码的情况==

#### StringBuffer、StringBuilder:

##### String、StringBuffer、StringBuilder三者异同：

> String：不可变的字符序列；底层使用 char[]储存
>
> StringBuffer：可变的字符序列，**线程安全**（方法皆是同步方法），效率偏低，底层使用 char[]储存
>
> StringBuilder：可变的字符序列：**线程不安全**，效率高，底层使用 char[]储存
>
> 1. 如果有现成问题，推荐使用StringBuffer，否则使用StringBuilder
>
> 2. ==可变字符序列与不可变字符序列的体现：==
>
>    1. StringBuffer、StringBuilder中底层字符数组 value 没有 final 声明,value可以不断扩容（数组大小可以改变）
>
>    2. ```java
>       //试图改变一个StringBuffer声明的字符串时，不会重新造一个再改变，而是在原有的字符串直接进行改变
>       StringBuffer str = new StringBuffer("abc");
>       StringBuffer str2 = str.replace(0,2,"周泳屹");
>       System.out.println(str);//周泳屹c
>       System.out.println(str2);//周泳屹c
>       ```
>
> 3. ```java
>    String str = new String();//new char[0]
>    String str1 = new String("abc");//char[] value = new char[]{'a','b','c'};
>    StringBuffer sb1 = new StringBuffer();//char[] value = new char[16];底层创建了一个长度为16的字符数组
>    sb1.append('a');//value[0] = 'a';
>    sb1.append('b');//value[1] = 'b';
>                                                                                 
>    StringBuffer sb2 = new StringBuffer("abc");//char[] value =new char{"abc".length() + 16}; value.append("abc");
>    /* 问题1：扩容问题：如果要添加的数据底层数组盛不下了，那就要扩容底层的数组
>          默认情况下，扩容为原来容量的2倍+2，同时将原有的数组中的元素复制到新的数组中
>          指导意义：开发中建议使用：StringBuffer(int capacity)或者StringBuilder(int capacity)直接自定义一个capacity大小的数组*/
>    ```

##### StringBuffer类和StringBuilder类：

![](F:\Java语言学习\笔记保存的截图\Snipaste_2021-04-15_22-50-04.png)

**StringBuffer和StringBuilder常用方法：**

```java
StringBuffer append(xxx);//：提供了很多的append()方法，用于进行字符串拼接(如同字符串使用+)
//str.append(1);str.append("1");效果一致
StringBuffer delete(int start,int end);//：删除指定位置的内容
StringBuffer replace(int start, int end, String str);//：把[start,end)位置替换为str
StringBuffer insert(int offset, xxx);//：在指定位置插入xxx
StringBuffer reverse();// ：把当前字符序列逆转
```

==当append和insert时，如果原来value数组长度不够，可扩容==

```java
public int indexOf(String str);
public String substring(int start,int end);
public int length();
public char charAt(int n );
public void setCharAt(int n ,char ch);
```

##### 对比3者之间的效率：

StingBuilder > StringBuffer > String

#### StringBuffer类的面试题：

```java
    public void test1(){
        String str = null;
        StringBuffer sb = new StringBuffer();
        sb.append(str);
        System.out.println(sb.length());//4
        System.out.println(sb);//"null"
        StringBuffer sb1 = new StringBuffer(str);//抛异常
//        System.out.println(sb1.length());
//        System.out.println(sb1);
    }
```

==原因：==

如果添加的到StringBuff类型字符串的值为空（null）则执行以下方法：

![](F:\Java语言学习\笔记保存的截图\Snipaste_2021-04-17_15-10-55.png)

#### JDK8之前日期和时间的API：

![](F:\Java语言学习\笔记保存的截图\Snipaste_2021-04-16_20-30-52.png)

**System类提供的public static long currentTimeMillis()用来返回当前时
间与1970年1月1日0时0分0秒之间以毫秒为单位的时间差。**

```java
//返回当前时间与1970年1月1日0时0分0秒之间以毫秒为单位的时间差
//陈为时间戳
long time = System.currentTimeMillis();
System.out.println(time);
```

##### java.util.Date:

```java
/* java.util.Date类
 1.两个构造器的使用
 构造器一：Date():创建一个对应当前时间的Date对象
 构造器二：创建指定的毫秒数(时间戳)的Date对象，生成对应的时间(年月日....)*/
         Date date4 = new Date(1618577702768l);
         System.out.println(date4.toString());//Fri Apr 16 20:55:02 CST 2021
/* 2.两个方法的使用
 ---->toString显示当前年、月、日、时、分、秒
 ---->getTime获取当前Date对象对应的毫秒数(时间戳)*/
```

##### java.sql.Date:

```java
// java.sql.Date类 是对应数据库中的日期类型变量(一般用于数据库的交互)
// 1.如何实例化：(只有参数型型构造器)
         java.sql.Date date = new java.sql.Date(1618577702768l);//传入时间戳
         System.out.println(date);//2021-04-16
         System.out.println(date.toString());//2021-04-16
// 2.如何把java.util.Date对象转化为java.sql.Date对象：
      情况一：
      util---->sql
      Date date4 = new java.sql.Date(时间戳);//使用多态
      java.sql.Date date5 = (java.sql.Date) date4;
      情况二：
      sql---->util
      java.sql.Date date = new java.sql.Date();
      java.util.Date d = new java.util.Date (date.getTime());
```

##### SimpleDateFormat的使用：

```注解
* SimpleDateFormat的使用：SimpleDateFormat对日期Date类的格式化和解析：
* 1.两个操作：
* 1.1格式化：日期--->字符串
* 1.2解析：格式化的逆过程：字符串--->日期
* 2.SimpleDateFormat的实例化：
* 2.1：使用默认的构造器
* 2.2：有参构造器规定字符串解析格式
```

```java
//        SimpleDateFormat的实例化:使用默认的构造器
        SimpleDateFormat sdf = new SimpleDateFormat();

//        格式化：日期--->字符串
        Date date = new Date();
        System.out.println(date);//Sat Apr 17 15:27:05 CST 2021
        String str = sdf.format(date);//格式化
        System.out.println(str);//21-4-17 下午3:27

//        解析：格式化的逆过程：字符串--->日期
        String str1 = "21-4-17 上午3:23";//字符串转日期时的格式
        Date date1 = sdf.parse(str1);//解析
        System.out.println(date1);//Sat Apr 17 03:23:00 CST 2021
```

```java
//  *************************按照指定的方式进行格式化和解析*******************************

//        SimpleDateFormat的实例化(有参构造器规定字符串解析格式):
        Date date1 = "Sat Apr 17 03:23:00 CST 2021";
        SimpleDateFormat sdf1 = new SimpleDateFormat("yyyy-MM-dd hh:mm:ss");//指定方式格式化
        String format1 = sdf1.format(date1);
        System.out.println(format1);//2021-04-17 03:23:00
//        解析：
        Date date2 = sdf1.parse("2021-04-17 03:23:00");//格式需要和构造器声明的格式一致，否则报错
        System.out.println(date2);
```

##### java.util.Calendar( 日历)类：

**Calendar是一个抽象基类，主用用于完成日期字段之间相互操作的功能。**

```java
     * Calendar日历类（抽象类）的使用：
     * 1.实例化：
     * 方式一：创建子类(GregorianCalendar)
     * 方式二：调用其静态方法getInstance,
     * 2.常用方法：
     * get():
     *         int i = calendar.get(Calendar.DAY_OF_MONTH);//这个月的第几天
     *         int j = calendar.get(Calendar.DAY_OF_WEEK);//这周的第几周
     *         int e = calendar.get(Calendar.DAY_OF_YEAR);//这年的第几天
     * set()：
     *         int i = calendar.set(Calendar.DAY_OF_MONTH,22);//将这个月的第几天修改成22
     * add():
     *         int i = calendar.add(Calendar.DAY_OF_MONTH,3);//将这个月的第几天加上3天
     *         int i = calendar.add(Calendar.DAY_OF_MONTH,-3);//将这个月的第几天减上3天
     * getTime():
     *         日历类 ----> Date
     *         Date date = calendar.getTime();
     *         System.out.println(date.toString());
     * setTime()；
     *         Date -----> 日历类
     *         Date date1 = new Date();
     *         calendar.setTime(date1);
     *         days = calendar.get(Calendar.DAY_OF_MONTH)
```

```java
//        方式二：创建子类(GregorianCalendar)
        GregorianCalendar cal = new GregorianCalendar();
//        方式二：调用其静态方法getInstance获得Calendar内部定义的对象
        Calendar calendar = Calendar.getInstance();
```

==注意：== 

* 获取月份时：一月是0，二月是1，以此类推，12月是11
* 获取星期时：周日是1，周二是2 ， 。。。。周六是7 

#### JDK8中新日期时间API：

##### 新的API出现的背景：

1. 可变性：像日期和时间这样的类应该是不可变的。

   * Calendar可以调用set()函数进行修改

2. 偏移性：Date中的年份是从1900开始的，而月份都从0开始。

   * ```
     Date date = new Date(2021,4,19);
     System.out.println(date);//Thu May 19 00:00:00 CST 3921
     //输出的值与实际值有差别，年份是指1990年增加2021年后的时间
     ```

3. 格式化：格式化只对Date有用，Calendar则不行。

4. 此外，它们也不是线程安全的；不能处理闰秒等。

##### 新API的实例化：LocalDateTime

![](F:\Java语言学习\笔记保存的截图\Snipaste_2021-04-20_23-02-41.png)

![](F:\Java语言学习\笔记保存的截图\Snipaste_2021-04-20_23-02-56.png)

##### 实例化此类(LocalDateTime)：

```java
//        通过now()方法调用获取 当前 时间、日期、日期和时间
        LocalDate localDate = LocalDate.now();
        LocalTime localTime = LocalTime.now();
        LocalDateTime localDateTime = LocalDateTime.now();
        System.out.println(localDateTime);//获取时间+日期
        System.out.println(localDate);//获取日期
        System.out.println(localTime);//获取时间
//        通过of()获取 指定 的年月天时分秒且没有偏移量：
        LocalTime of1 = LocalTime.of(23, 4, 5);
        System.out.println(of1);//23:04:05
        LocalDateTime of2 = LocalDateTime.of(2021,4,20,9,33);
        System.out.println(of2);//2021-04-20T09:33
```

LocalDateTime的方法：

```java
//        getXxx():非静态方法，需要用对象调用方法：
        System.out.println(localDate.getDayOfMonth());//获取这个月的第几天
//        withXxx();设置时间，具有不可变性
        LocalDate localDate1 = localDate.withMonth(10);
        System.out.println(localDate1);//2021-10-20
        System.out.println(localDate);//2021-04-20
//        加上几天（几月）：plusXxx();
//        减去几天（几月）：minusDay();
```

##### Instant的使用：

```java
//        实例化 Instant.now() ：获取本初子午线对应的标准时间
        Instant now1 = Instant.now();
        System.out.println(now1);//输出的是本初子午线的时间
//        添加时间的偏移量：
        OffsetDateTime offsetDateTime1 = now1.atOffset(ZoneOffset.ofHours(8));//修改成东八区（北京时间）时间
        System.out.println(offsetDateTime1);
//        获取瞬时点 自时间1970年01月01日00时00分00秒 毫秒数
        long l = now1.toEpochMilli();
        System.out.println(l);
//      ofEpochMilli():通过给定的毫秒数，获取Instant实例
        Instant instant1 = Instant.ofEpochMilli(3242124343L);
        System.out.println(instant1);//1970-02-07T12:35:24.343Z
```

##### DateTimeFormatter：格式化或解析时间、日期：

==类似于SimpleDateFormate==

```java
//        ***********************************************************
//        方式一：预定义的标准格式:ISO_LOCAL_DATE_TIME;ISO_LOCAL_DATE;ISO_LOCAL_TIME
        DateTimeFormatter formatter = DateTimeFormatter.ISO_LOCAL_DATE_TIME;
        //格式化：日期--->字符串
        LocalDateTime localDateTime = LocalDateTime.now();
        String str1 = formatter.format(localDateTime);
        System.out.println(localDateTime);//2021-04-20T23:49:59.142
        System.out.println(str1);//2021-04-20T23:49:59.142
        //解析：字符串--->日期
        TemporalAccessor parse = formatter.parse("2021-04-20T23:49:59.142");
        System.out.println(parse);//{},ISO resolved to 2021-04-20T23:49:59.142
//        ***********************************************************
//        方式二：本地化相关的格式 如：ofLocalizedDateTime(FormatStyle.LONG)
//        FormatStyle.LONG/FormatStyle.MEDIUM/FormatStyle.SHORT适用于LocalDateTime
        DateTimeFormatter formatter1 = DateTimeFormatter.ofLocalizedDateTime(FormatStyle.SHORT);
        //格式化：
        String str2 = formatter1.format(localDateTime);
        System.out.println(str2);//21-4-20 下午11:57
//        本地化相关的格式:ofLocalizedDate()
//        FormatStyle.Full/FormatStyle.LONG()/FormatStyle.MEDIUM/FormatStyle.SHORT:适用于LocalDate
        DateTimeFormatter formatter2 = DateTimeFormatter.ofLocalizedDate(FormatStyle.FULL);
        String str3 = formatter2.format(LocalDate.now());
        System.out.println(str3);//2021年4月21日 星期三
//        ***********************************************************
//        重点：：方式三：自定义格式，如：ofPattern("yyyy-mm-dd hh:mm:ss")
        DateTimeFormatter formatter3 = DateTimeFormatter.ofPattern("yyyy-MM-dd hh:mm:ss");
//        格式化：
        String format = formatter3.format(LocalDateTime.now());
        System.out.println(format);//2021-04-21 10:29:01

//       解析：日期---->字符串
        TemporalAccessor parse1 = formatter3.parse("2021-04-21 10:29:01");
        System.out.println(parse1);
```

#### Java比较器：

##### 出现背景：

一、Java中的对象，正常情况下，只能进行比较：==或!=不能使用 > 或 <

当需要对多个对象进行排序时：如何实现？

 ==Java实现对象排序的方式有两种：==

> * 自然排序：java.lang.Comparable
> * 定制排序：java.util.Comparator

##### Comparable接口（自然排序）的使用：

==Comparable接口强行对实现它的每个类的对象进行整体排序。这种排序被称
为类的自然排序==

```注释
1.向String、包装类等实现了Comparable接口：重写了compareTo()方法，给出了比较两个对象大小的方法
2.像String、包装类重写CompareTo()方法以后，进行了从小到大的排列
3.实现Comparable接口的对象列表（和数组）可以通过 Collections.sort 或 Arrays.sort 进行自动排序。实现此接口的对象可以用作有序映射中的键或有序集合中的元素，无需指定比较器。
4.重写CompareTo(obj)的规则：
	如果当前对象this 大于 形参对象obj，则返回 正整数，
	如果当前对象this 小于 形参对象obj，则返回 负整数，
	如果当前对象this 等于 形参对象obj，则返回 零。
```

![](F:\Java语言学习\笔记保存的截图\Snipaste_2021-04-22_23-48-12.png)

___

* 对于自定义类来说，如果==指定某种属性来进行对象的排序==，我们可以让自定义类实现Comparable接口，重写CompareTo(obj)的方法

* CompareTo()方法的重写规则按照 CompareTo(obj)原始规则（见自然排序第4点）且默认从小到大排列

```java
class Goods implements Comparable{//需要比较的对象需要实现接口Comparable
    private String name;
    private double price;

    public Goods(String name, double price) {
        this.name = name;
        this.price = price;
    }

    @Override
    public String toString() {
        return "Goods{" +
                "name='" + name + '\'' +
                ", price=" + price +
                '}';
    }

    //指明商品比较大小的方式：(按照 价格 从低到高)
    //如果按照商品名排序，直接调用String里面已经写好的CompareTo()方法
    @Override
    public int compareTo(Object o) {
        if(this.getClass()==o.getClass()){
            Goods goods = (Goods) o;
            if(this.price>goods.price){
                return -1;
            }else if(this.price< goods.price){
                return 1;
            }else {
                return 0;
//                return
            }
        }
//      方式二：    Double.compare();
        throw new RuntimeException("传入的数据不一致！");
    }
}
```

```java
class Goods implements Comparable {
	private String name;
	private double price;
//按照价格，比较商品的大小
@Override
public int compareTo(Object o) {
	if(o instanceof Goods) {
		Goods other = (Goods) o;
	if (this.price > other.price) {
		return 1;
	} else if (this.price < other.price) {
		return -1;
	}
	return 0;
	}
	throw new RuntimeException("输入的数据类型不一致");
}
//构造器、getter、setter、toString()方法略
}
public class ComparableTest{
	public static void main(String[] args) {
		Goods[] all = new Goods[4];
		all[0] = new Goods("《红楼梦》", 100);
		all[1] = new Goods("《西游记》", 80);
		all[2] = new Goods("《三国演义》", 140);
		all[3] = new Goods("《水浒传》", 120);
		Arrays.sort(all);
		System.out.println(Arrays.toString(all));
	}
}
```



##### Comparator接口的使用（定制排序）：

使用背景：

> 当元素的类型==没有实现java.lang.Comparable 接口==而又不方便修改代码了 或者 实现了java.lang.Comparable 接口的==排序规则不适合当前的操作==，那用么可以考虑使用Comparator的对象来排序

```java
    public void test1(){
        Goods[] arr = new Goods[4];
        arr[0] = new Goods("Lenovo",34);
        arr[1] = new Goods("dell",43);
        arr[2] = new Goods("xiaomi",12);
        arr[3] = new Goods("Huawei",65);
        Comparator comparator = new Comparator() {

            @Override
            public int compare(Object o1, Object o2) {
                if(o1 instanceof Goods && o2 instanceof Goods){
                    Goods goods1 = (Goods) o1;
                    Goods goods2 = (Goods) o2;
//                    比较对象里面的某个属性
//                    按照名字进行排列，如果名字相同，则对比价格：
                    if(goods1.getName().equals(goods2.getName())){
//                        从低到高的价格排列：
                        return -Double.compare(goods1.getPrice(),goods2.getPrice());
                    }else {
                     return goods1.getName().compareTo(goods2.getName());
                    }
                }
                throw new RuntimeException("输入的数据有误！");
            }
        };
        Arrays.sort(arr,comparator);//传入需要排序的（数组），传入实现Comparator接口类的对象
        System.out.println(Arrays.toString(arr));
    }
}
```

##### 自然排序和定制排序的异同点：

自然排序：需要进行排序的类实现Comparable接口，并且==重写compareTo方法==，compareTo方法只有一个参数，。
定制排序：需要在需要排序的类之外再定义一个类实现Comparator接口，并且==重写compare方法==，compare方法有两个参数。

Comparable接口的方式一旦一定，保证Comparable接口实现类的对象在仍何位置都可以比较大小，Comparator接口属于临时性的比较

相同点：compareTo和compare方法返回值都是int类型，并且方法内部比较的两个对象，大于返回正数，小于则返回负数，如果相等则返回0.

#### System类：

* System类代表系统，系统级的很多属性和控制方法都放置在该类的内部。
* 该类位于java.lang包。由于该类的构造器是private的，所以无法创建该类的对象，也就是无法实例化该类。
* 其内部的成员变量和成员方法都是static的，所以也可以很方便的进行调用。

##### 成员变量：

 System类内部包含in、out和err三个成员变量，分别代表标准输入流
(键盘输入)，标准输出流(显示器)和标准错误输出流(显示器)。

##### 成员方法：

* native long currentTimeMillis()： ：
  该方法的作用是返回当前的计算机时间，时间的表达格式为当前计算机时
  间和GMT时间(格林威治时间)1970年1月1号0时0分0秒所差的毫秒数。
* void exit(int status)： ：
  该方法的作用是退出程序。其中status的值为0代表正常退出，非零代表
  异常退出。 使用该方法可以在图形界面编程中实现程序的退出功能等
* void gc()： ：
  该方法的作用是请求系统进行垃圾回收。至于系统是否立刻回收，则
  取决于系统中垃圾回收算法的实现以及系统执行时的情况。
* String getProperty(String key)： ：
  该方法的作用是获得系统中属性名为key的属性对应的值。系统中常见
  的属性名以及属性的作用如下表所示：![](F:\Java语言学习\笔记保存的截图\Snipaste_2021-04-24_20-29-46.png)

```java
public void test6(){
    String javaVersion = System.getProperty("java.version");
    System.out.println("java的version:" + javaVersion);
    String javaHome = System.getProperty("java.home");
    System.out.println("java的home:" + javaHome);
    String osName = System.getProperty("os.name");
    System.out.println("os的name:" + osName);
    String osVersion = System.getProperty("os.version");
    System.out.println("os的version:" + osVersion);
    String userName = System.getProperty("user.name");
    System.out.println("user的name:" + userName);
    String userHome = System.getProperty("user.home");
    System.out.println("user的home:" + userHome);
    String userDir = System.getProperty("user.dir");
    System.out.println("user的dir:" + userDir);
}
```

#### BigInteger类:

当整数型超过long型，可以使用该类：

java.math包的BigInteger 可以表示不可变的任意精度的整数。BigInteger 提供
所有 Java 的基本整数操作符的对应物，并提供 java.lang.Math 的所有相关方法。
另外，BigInteger 还提供以下运算：模算术、GCD 计算、质数测试、素数生成、
位操作以及一些其他操作

##### 构造器：

 BigInteger(String val)：根据字符串构建BigInteger对象

```java
public BigInteger abs();//：返回此 BigInteger 的绝对值的 BigInteger。
BigInteger add(BigInteger val);// ：返回其值为 (this + val) 的 BigInteger
BigInteger subtract(BigInteger val)// ：返回其值为 (this - val) 的 BigInteger
BigInteger multiply(BigInteger val)// ：返回其值为 (this * val) 的 BigInteger
BigInteger divide(BigInteger val)// ：返回其值为 (this / val) 的 BigInteger。整数
相除只保留整数部分。
BigInteger remainder(BigInteger val)// ：返回其值为 (this % val) 的 BigInteger。
BigInteger[] divideAndRemainder(BigInteger val)：//返回包含 (this / val) 后跟
(this % val) 的两个 BigInteger 的数组。
BigInteger pow(int exponent) //：返回其值为 (this exponent ) 的 BigInteger
```

BigDecimal类：

一般的Float类和Double类可以用来做科学计算或工程计算，但在 商业计算中，
到 要求数字精度比较高，故用到java.math.BigDecimal类 类 。
 BigDecimal类支持不可变的、任意精度的有符号十进制定点数。

##### 构造器：

 public BigDecimal(double val)
 public BigDecimal(String val)

##### 常用方法：

 public BigDecimal add(BigDecimal augend)
 public BigDecimal subtract(BigDecimal subtrahend)
 public BigDecimal multiply(BigDecimal multiplicand)
 public BigDecimal divide(BigDecimal divisor, int scale, int roundingMode)   // scale表示指定精度

#### 举例：

```java
public void testBigInteger() {
BigInteger bi = new BigInteger("12433241123");
BigDecimal bd = new BigDecimal("12435.351");
BigDecimal bd2 = new BigDecimal("11");
System.out.println(bi);
// System.out.println(bd.divide(bd2));
System.out.println(bd.divide(bd2, BigDecimal.ROUND_HALF_UP));
System.out.println(bd.divide(bd2, 15, BigDecimal.ROUND_HALF_UP));
}
```

### 三十、枚举类和注解：

![](F:\Java语言学习\笔记保存的截图\Snipaste_2021-04-25_13-56-01.png)

#### 枚举类的属性：

* 枚举动 类对象的属性不应允许被改动, 所以应该使用 private final 修饰
* 枚举类的使用 private final 修饰的属性应该在构造器中为其赋值
* 若枚举类显式的定义了带参数的构造器, 则在列出枚举值时也必须对应的
  传入参数

#### 如何自定义枚举类：

##### 方式一：JDK5.0之前，自定义枚举类

1. 私有化类的构造器，保证不能在类的外部创建其对象
2. 在类的内部创建枚举类的实例。声明为：public static final
3. 对象如果有实例变量，应该声明为private final，并在构造器中初始化

```java
public class SeasonTest {
    public static void main(String[] args) {
        Season autumn = Season.AUTUMN;
        System.out.println(autumn.toString());//Season{seasonName='秋天', seasonDesc='秋高气爽'}
        System.out.println(autumn.getSeasonName());//秋天
        System.out.println(autumn.getSeasonDesc());//秋高气爽
    }
}
class Season{
    //1.声明Season对象的属性：private final修饰(final修饰可在构造器赋值，显式赋值，代码块赋值)
    private final String seasonName;
    private final String seasonDesc;
    //2.私有化类的构造器（如果构造器不私有化，则不知道会有几个类的对象）,并给对象属性赋值
    private Season(String seasonName,String seasonDesc){
        this.seasonDesc = seasonDesc;
        this.seasonName = seasonName;
    }
//    3.提供枚举类的多个对象：
    public static final Season SPRING = new Season("春天","春暖花开");
    public static final Season SUMMER = new Season("夏天","夏日炎炎");
    public static final Season AUTUMN = new Season("秋天","秋高气爽");
    public static final Season WINTER = new Season("冬天","冰天雪地");
//    其他需求：获取枚举类对象的属性：

    public String getSeasonName() {
        return seasonName;
    }

    public String getSeasonDesc() {
        return seasonDesc;
    }
//重写toString,否则调用toString输出的是地址
    @Override
    public String toString() {
        return "Season{" +
                "seasonName='" + seasonName + '\'' +
                ", seasonDesc='" + seasonDesc + '\'' +
                '}';
    }
}
```

##### 方式二：之后调用enum关键字定义枚举类：

> 该方式定义的枚举类默认继承与：java.lang.Enum类
>
> 该方法toString不重写，则默认打印对象名

* 使用 enum 定义的枚举类默认继承了 java.lang.Enum类，因此不能再
  继承其他类
* 枚举类的构造器只能使用 private 权限修饰符
* 枚举类的所有实例必须在枚举类中显式列出(, 分隔 ; 结尾)。列出的
  实例系统会自动添加 public static final 修饰
* 必须在枚举类的第一行声明枚举类对象

```java
public class SeasonTest {
    public static void main(String[] args) {
        Season summer = Season.SUMMER;
        System.out.println(summer.toString());
        System.out.println(summer.getSeasonName());
        System.out.println(summer.getClass().getSuperclass());
    }
}
enum Season{
    //    1.提供当前枚举类的对象，要求多个枚举类之间用“,”隔开，最后一个对象用”;“号
    SPRING("春天","春暖花开"),
    SUMMER("夏天","夏日炎炎"),
    AUTUMN("秋天","秋高气爽"),
    WINTER("冬天","冰天雪地");
    //2.声明Season对象的属性：private final修饰(final修饰可在构造器赋值，显式赋值，代码块赋值)
    private final String seasonName;
    private final String seasonDesc;
    //3.私有化类的构造器（如果构造器不私有化，则不知道会有几个类的对象）,并给对象属性赋值
    private Season(String seasonName,String seasonDesc){
        this.seasonDesc = seasonDesc;
        this.seasonName = seasonName;
    }

//    获取枚举类对象的属性：

    public String getSeasonName() {
        return seasonName;
    }

    public String getSeasonDesc() {
        return seasonDesc;
    }
    //此时可以不用重写toString:
//重写toString,否则调用toString输出的是地址
//    @Override
//    public String toString() {
//        return "Season{" +
//                "seasonName='" + seasonName + '\'' +
//                ", seasonDesc='" + seasonDesc + '\'' +
//                '}';
//    }
}
```

#### 如何使用关键字enum定义枚举类：

#### Enum类的主要方法：

* values() 方法：返回枚举类型的对象数组。该方法可以很方便地遍历所有的
  枚举值。

  * ```java
    Season[] values = Season.values();
    for (int i = 0; i < values.length; i++) {
        System.out.print(values[i]+" ");//SPRING SUMMER AUTUMN WINTER
    }
    ```

* valueOf(String str)：可以把一个字符串转为对应的枚举类对象。要求字符串必须是枚举类对象的“名字”。如不是，会有运行时异常：
  IllegalArgumentException。

  * ```java
    Season spring = Season.valueOf("SPRING");
    System.out.println(spring);//SPRING
    ```

* toString()：返回当前枚举类对象常量的名称 

#### 实现接口的枚举类：

**和普通 Java 类一样，枚举类可以实现一个或多个接口**

##### 情况一：每个枚举值在调用实现的接口方法呈现相同的行为方式

若每个枚举值在调用实现的接口方法呈现相同的行为方式，则只
要统一实现该方法即可

```java
enum Season implements info{
    //    1.提供当前枚举类的对象，要求多个枚举类之间用“,”隔开，最后一个对象用”;“号
    SPRING("春天","春暖花开"),
    SUMMER("夏天","夏日炎炎"),
    AUTUMN("秋天","秋高气爽"),
    WINTER("冬天","冰天雪地");
    //1.声明Season对象的属性：private final修饰(final修饰可在构造器赋值，显式赋值，代码块赋值)
    private final String seasonName;
    private final String seasonDesc;
    //2.私有化类的构造器（如果构造器不私有化，则不知道会有几个类的对象）,并给对象属性赋值
    private Season(String seasonName,String seasonDesc){
        this.seasonDesc = seasonDesc;
        this.seasonName = seasonName;
    }

//    获取枚举类对象的属性：

    public String getSeasonName() {
        return seasonName;
    }

    public String getSeasonDesc() {
        return seasonDesc;
    }

    @Override
    public void show() {
        System.out.println("这是一个季节");
    }
}
interface info{
    void show();
}
```

##### 情况二：每个枚举值在调用实现的接口方法呈现出不同的行为方式

若需要每个枚举值在调用实现的接口方法呈现出不同的行为方式,
则可以让每个枚举值分别来实现该方法：==需要每个枚举对象都重写接口的方法==

```java
enum Season implements info{
    //    1.提供当前枚举类的对象，要求多个枚举类之间用“,”隔开，最后一个对象用”;“号
    SPRING("春天","春暖花开"){
        @Override
        public void show() {
            System.out.println("春天来了");
        }
    },
    SUMMER("夏天","夏日炎炎"){
        @Override
        public void show() {
            System.out.println("夏天来了");
        }
    },
    AUTUMN("秋天","秋高气爽"){
        @Override
        public void show() {
            System.out.println("秋天来了");
        }
    },
    WINTER("冬天","冰天雪地"){
        @Override
        public void show() {
            System.out.println("冬天来了");
        }
    };
    //1.声明Season对象的属性：private final修饰(final修饰可在构造器赋值，显式赋值，代码块赋值)
    private final String seasonName;
    private final String seasonDesc;
    //2.私有化类的构造器（如果构造器不私有化，则不知道会有几个类的对象）,并给对象属性赋值
    private Season(String seasonName,String seasonDesc){
        this.seasonDesc = seasonDesc;
        this.seasonName = seasonName;
    }

//    获取枚举类对象的属性：

    public String getSeasonName() {
        return seasonName;
    }

    public String getSeasonDesc() {
        return seasonDesc;
    }
}
interface info{
    void show();
}
```

#### 注解：

##### 注解的概念：

* Annotation 其实就是代码里的 特殊标记, 这些标记可以在编译, 类加
  载, 运行时被读取, 并执行相应的处理。通过使用Annotation, 程序员
  可以在不改变原有逻辑的情况下, 在源文件中嵌入一些补充信息。代
  码分析工具、开发工具和部署工具可以通过这些补充信息进行验证
  或者进行部署。
* Annotation 可以像修饰符一样被使用, 可用于 修饰包, 类, 构造器, 方 方
  法 法, 成员变量, 参数, 局部变量的声明, 这些信息被保存在 Annotation
  的 “name=value” 对中。

##### 示例一：

![](F:\Java语言学习\笔记保存的截图\Snipaste_2021-04-26_09-09-36.png)

##### 如何自定义注解：

1. 参照SupperessWarinings定义。
2. 注解声明为@interface
3. 自定义注解自动继承了java.lang.annotation.Annotation 接口
4. 内部定义成语通常使用value表示
5. 可以指定成员的默认值，使用default定义
6. 如果自定义注解没有成员，表明是一个标识

==如果注解有成员，在使用注解时，需要指明成员的值==

##### 元注解：

JDK 的元 Annotation 用于修饰其他 Annotation 定义

![](F:\Java语言学习\笔记保存的截图\Snipaste_2021-04-26_22-51-42.png)

![](F:\Java语言学习\笔记保存的截图\Snipaste_2021-04-26_22-51-31.png)

==只有声明为RUNTIME生命周期的注解，才能通过反射获取==

![](F:\Java语言学习\笔记保存的截图\Snipaste_2021-04-26_23-02-01.png)

##### 可重复注解：

> 1. 在MyAnnotation上声明@Repeatable,成员值为MyAnnotation.class
> 2. MyAnnotation的Target和Retention等元注解与MyAnnotations相同

##### 类型注解：

> 

### 三十一、Java集合：

#### 集合框架的概述：

* 集合、数组都是对多个数据进行存储操作的结构，简称Java容器
* **说明**：此时的存储，主要指的是内存层面的存储，不涉及到持久的存储（.txt、.jpg、.avi、数据库中）

##### 数组在存储多个数据方面的特点、缺点：

特点：

> * 一旦定义成功，其长度就确定了
> * 数组一旦定义好，其元素的类型也就确定了，我们也就只能操作指定类型的数据

缺点：

> * 一旦初始化，长度就不可以修改
> * 数组提供的方法有限，对于添加、删除、插入数据等操作不方便
> * 获取数组中实际元素的个数的需求，数组没有现成的属性和方法可用
> * 数组存储数据特点：有序、可重复，对于无序、不可重复的需求不能满足

##### Collection、Map两种体系：

![](F:\Java语言学习\笔记保存的截图\Snipaste_2021-04-27_09-53-44.png)

> List      ---------->    “动态数组”
>
> * 提供常用实现类：ArrayList、Linkedlist、Vector
>
> Set      ---------->     “高中数学中的集合”
>
> * 提供常用实现类：HashSet、LinkedHashSet、TreeSet
>
> Map     ------------>    “python中的字典”
>
> * 提供常用实现类：HashMap、LinkedHashMap、ThreeMap、Hashtable、Properties

![](F:\Java语言学习\笔记保存的截图\Snipaste_2021-04-27_09-54-49.png)

#### Collection接口中的方法的使用：

**方法一：**

add()、size()、addAll()、clear()、isEmpty()

```java
//        使用Collection接口的某个实现类：ArrayList：
        Collection coll = new ArrayList();
//        add(Object e);将元素e添加到集合coll中
        coll.add("AA");
        coll.add(123);//自动装箱Integer
        coll.add(new Date());

//        size();获取添加元素的个数
        System.out.println(coll.size());

//      addAll(Collection coll);将coll1中的元素添加到coll中
        Collection coll1 = new ArrayList();
        coll1.add(345);
        coll1.add("cc");
        coll.addAll(coll1);
        System.out.println(coll.toString());
        
//        clear();清空集合中的元素
        
//        isEmpty();判断当前集合是否为空，返回 布尔值
```

**方法二：**

contains()、containsAll()

==在向Collection接口实现类中添加数据obj时，要求obj所在类要重写equal()方法，为后面contains()方法调用==

```java
Collection coll = new ArrayList();
        coll.add(123);
        coll.add("zyy");
        coll.add(new String("周泳屹"));
        coll.add(new Person("周泳屹",20));
        Collection coll1 = new ArrayList();
        coll1.add(new Person("周泳屹",20));
//        contains(Object obj);判断当前集合中是否包含obj，返回布尔类型
//        在判断时，会调用obj对象所在类的equal，将形参contains方法对集合逐个对比，直到输出true或者对比完所有集合对象输出false
        System.out.println(coll.contains("周泳屹"));//true
        System.out.println(coll.contains(new String("周泳屹")));//true
        System.out.println(coll.contains(new String("zyy")));//true
        System.out.println(coll.contains(new Person("周泳屹", 20)));
//        即：contain判断的是调用类中的  equal() 方法，如过方法重写则比较对象中的值，没有重写则比较对象的地址

//        containsAll(Collection coll1);判断形参coll1中的所有元素，是否都存在于当前集合中，返回布尔类型，比较原理与contains一样
        System.out.println(coll.containsAll(coll1));//true
```

**方法三**：

```java
//        1.remove(Object obj);从当前集合中移除obj元素，（先调用equals方法判断是否存在）存在则删除并返回true，不存在则返回false
        
//        2.removeAll(Collection coll1);差集：从当前集合中移除coll1中共有的元素
        
//        3.retainAll(Collection coll1);交集：获取当前集合与coll1的交集并返回给当前集合中
        
//        4.equals(Object obj);若返回true，各个集合中的元素相同（list）中考虑顺序要相同，否则为false

//		5.hashCode():返回当前对象的哈希值
```

**方法四**：

#### 集合数组之间的转换：

```java
//        集合 -------------> 数组：toArray()
        Object[] objects = coll.toArray();
        System.out.println(Arrays.toString(objects));
//        数组 -------------> 集合：Arrays.list();
        List list = Arrays.asList(c);
        System.out.println(list.isEmpty());
        System.out.println(list);
```

#### Iterator迭代器接口

* Collection接口继承了java.lang.Iterable接口，==该接口有一个iterator()方法==，那么所
  有实现了Collection接口的集合类都有一个iterator()方法，用以返回一个实现了
  Iterator接口的对象。

*  Iterator 仅用于遍历集合，Iterator 本身并不提供承装对象的能力。==如果需要创建
  Iterator 对象，则必须有一个被迭代的集合。==
*  集合对象==每次调用iterator()方法都得到一个全新的迭代器对象==，默认游标都在集合
  的第一个元素之前

##### 使用 Iterator 接口遍历集合元素：

```java
    public void test3(){
        int[] c = new int[]{1,23,4,5,5};
        Collection coll = new ArrayList();
        coll.add(123);
        coll.add("zyy");
        coll.add(new String("zyt"));
        coll.add(new String("周泳屹"));
        coll.add(new Person("周泳屹",20));

        Iterator iterator = coll.iterator();
//      方式一：
//        System.out.println(iterator.next());//123
//        System.out.println(iterator.next());//zyy
        //............
//        方式二：
//        for (int i = 0; i < coll.size(); i++) {
//            System.out.println(iterator.next());
//        }
//        方式三：推荐：hasNext()方法判断下一个遍历是还有没有元素
        while(iterator.hasNext()){
            //next():①指针下移 ②将下移以后集合位置上的元素返回
            System.out.println(iterator.next());
        }
```

![](F:\Java语言学习\笔记保存的截图\Snipaste_2021-04-28_22-30-50.png)

==错误写法：==

```java
Iterator iterator = coll.iterator;
//一个循环，调用两次next，指向地址的光标移动两个位置
while((iterator.next())!=null){
    System.out.println(iterator.next());
}
```

```java
//每循环一次，就重新生成iterator对象，指针重新从第一个元素开始指
while(coll.iterator().hasNext()){
       System.out.println(coll.iterator().next());//不断输出第一个元素
}
```

##### 使用iterator迭代器的方法remove()：

```java
        Collection coll1 = new ArrayList();
        coll1.add(123);
        coll1.add("zyy");
        coll1.add(new String("zyt"));
        coll1.add(new String("周泳屹"));
        coll1.add(new Person("周泳屹",20));

        Iterator iterator = coll1.iterator();

//        删除集合中"zyt"
        while(iterator.hasNext()){
            if("zyt".equals(iterator.next())){
                iterator.remove();
            }
        }
        System.out.println(coll1);//已经删除zyt
    }
```

==如果还未调用next()或在上一次调用 next 方法之后已经调用了 remove 方法，再调用remove都会报IllegalStateException==（此时指针还在上一级，或所指的元素已经被移除）

#### foreach循环（遍历集合、数组）：

 遍历操作不需获取Collection或数组的长度，无需使用索引访问元素。

**格式：**

```java
//内部任然使用了迭代器：
for(集合中元素的类型 局部变量 : 集合对象){
    System.out.println(obj);
}
for(数组中元素的类型 局部变量 : 数组对象){
    System.out.println(obj);
}
```

![](F:\Java语言学习\笔记保存的截图\Snipaste_2021-04-29_15-36-17.png)

==注意：==用 foreach 遍历出的数组 重新赋值后 **不改变原数组的元素**

```java
int[] arr = new int[]{1,3,5,6,8};
for(int obj:arr){
    obj = 8;//对arr数组里面的元素重新赋值
}
for (int str:
     arr) {
     //原素组里面的值不发生改变
    System.out.println(str);//1,3,5,6,8
}
```

#### Collection子接口之一：List接口

>  Collection接口：单列集合，用来存储一个一个的对象
>
> List接口：存储有序的可重复的数据-----“动态”数组，替换原有的数组
>
> * ArrayList：
> * LinkedList：
> * Vector：

##### ArrayList、LinkedList和Vector的异同：

同：

> * 元素有序、且可重复，集合中的每个元素都有其对应的顺序索引。
> * List容器中的元素都对应一个整数型的序号记载其在容器中的位置，可以根据
>   序号存取容器中的元素。

> ArrayList:作为List接口主要实现类，==线程不安全，效率高==底层使用 Object[] elementData存储
>
> LinkedList:对于==频繁的插入和删除操作==，使用==此类操作比ArrayList效率高==；底层使用双向链表存储
>
> Vector:作为List接口古老实现类，==线程安全，效率低==底层使用 Object[] elementData存储

##### ArrayList源码分析：

```java
//        JDK7中：
        ArrayList list = new ArrayList();//创建了长度是10的Object[]数组elementData
        list.add(123);//elementData[0] = new Integer(123)
        System.out.println(list);
//        ...........
        list.add(224);//如果此次添加导致底层数组容量不够，则扩容
//        默认情况下：扩容为原来容量的1.5倍，同时需要将原来数组中的数据复制到新数组中
//        结论：建议开发中使用带参的构造器
//        JDK8中：
        ArrayList list1 = new ArrayList();//底层Object[] elementData初始化为：{} 并没有创建一个长度为10的数组
        list1.add(123);//第一次调用add()时，底层才创建了长度为10的数组，并将数据添加到底层数组中
//        后面 添加与扩容 操作与JDK7一致
```

==小结==：JDK7中的ArrayList对象的创建类似于单例的饿汉式，JDK8当中的ArrayList对象的创建类似于单例的懒汉式，延迟数组的创建，节省内存

##### LinkedList源码分析：

```java
LinkedList linkedList = new LinkedList();//内部声明了Node类型的first和last属性，默认值为null
linkedList.add(123);//将123封装到Node中，创建了Node对象
```

双向链表不讨论扩容问题

##### Vector的源码分析：

jdk7,8中通过Vector()构造器创建对象时，底层都创建了为10的数组

扩容默认为原来数组的2倍

![](F:\Java语言学习\笔记保存的截图\Snipaste_2021-05-07_22-51-47.png)

##### List接口方法：

增、删、改、查：

```java
        ArrayList list = new ArrayList();
        list.add(123);
        list.add(456);
        list.add("AA");
        list.add(new Person("周泳屹",20));
        list.add(456);
        List list1 = Arrays.asList(1,2,3);//将数组（1,2,3）转化为列表
        System.out.println(list);
//        void add(int index, Object ele): 在 index 位置插入 ele 元素
        list.add(1,"zyt");

//
//        boolean addAll(int index, Collection eles):从 index 位置开始将 eles 中的所有元素添加进来
        list.addAll(1,list1);

//        Object get(int index): 获取指定index
        
//        int indexOf(Object obj): 返回obj,如果不存在，返回-1
        
//        int lastIndexOf(Object obj): 返回obj，如果不存在，返回-1
        
//        Object remove(int index): 移除指定index 位置的元素，并返回此元素
        System.out.println(list.remove(3));
//        Object set(int index, Object ele): 设置指定index 位置的元素为ele
        
//        List subList(int fromIndex, int toIndex): 返回从fromIndex 到toIndex位置的子集合
        
```

```java
public void testListRemove() {
    List list = new ArrayList();
    list.add(1);
    list.add(2);
    list.add(3);
    updateList(list);
    System.out.println(list);//1,2
}
private static void updateList(List list) {
    list.remove(2);//删除的是元素位置，要删除元素，需要传入元素的对象（装箱）
    //list.remove(new Integer(2));
}
```

#### Collection子接口之二：Set接口

==存储无序的，不可重复的数据==

> Set接口是Collection的子接口，set接口没有提供额外的方法
>
> 1. 无序性：
>    1. （添加的时候不按照顺序添加）不等于随机性，储存的数据在底层数组存贮中并非按照数组索引的顺序添加，而是根据数据的哈希值决定
> 2. 不可重复性：
>    1. 保证添加的元素按照equals()（重写equals()，否则比较的是地址）判断时，不能返回true，即相同的元素只能添加一个

##### HashSet实现类:

==作为Set接口的主要实现类，线程不安全，可以存储null==

**以HashSet为例：**

> 向HashSet中添加元素a，首先调用元素a所在类的hashCode()方法，计算a的哈希值
>
> 此哈希值通过某种算法，计算出在HashSet底层数组中的存放位置（索引），==判断数组此位置上是否已经有元素==：
>
> * 此位置上没有元素，则a直接添加成功-------情况一
> * 此位置上有元素b（或以链表形式存在的多个元素），==则比较元素a和元素b的hash值==：
>   * hash值不相同，则元素a添加成功--------情况二
>   * hash值相同，进而调用a所在类的equals()方法：
>     * equals()返回true，则函数添加失败
>     * equals()返回false，则函数添加成功--------情况三
>
> * 对于添加成功的情况2和3而言：元素a与已经存在指定索引位置上的数据以链表的形式存储：
>   * jdk7：新元素（a）放在数组中，指向旧元素（b）【从上顶替添加存储】
>   * jdk8：旧元素（b）放在数组中，指向新元素（a）【从下继续添加存储】
>   * 总结：七上八下
>   * ![](F:\Java语言学习\笔记保存的截图\图片.png)
> * ==HashSet底层是：数组+链表的结构==
> * ==要求：==
>   * 向Set中添加的数据，其所在类一定要要重写hashCode()、equals()方法
>   * 重写的hashCode()、equals()方法尽可能保持一致性：相等的对象必须具有相等的散列码（哈希值）

**HashSet实现类的子类：LinkedHashSet：**

> * 作为HashSet的子类：遍历其内部数据时，可以按照添加的顺序遍历
> * LinkedHashSet 根据元素的 hashCode 值来决定元素的存储位置，但它同时使用双向链表维护元素的次序，这使得元素看起来是以插入顺序保存的。
> * LinkedHashSet 不允许集合元素重复
> * ![](F:\Java语言学习\笔记保存的截图\Snipaste_2021-05-09_15-19-32.png)
> * 再添加数据的同时，每个数据还维护了 两个引用，记录此数据前一个和后一个的数据
>   * 优点：对于频繁的遍历操作，效率高于HashSet

##### TreeSet实现类：

==可以按照添加对象的指定属性，进行排序==

> * 向TreeSet中添加的数据，要求是相同类的对象，自动（从小到大的顺序）排序，自定义的类需要重写CompareTo才能实现排序
>
> * 两种排序的方式：自然排序、定制排序。
>
> * 自然排序：比较两个对象相等的标准：CompareTo()返回0，不在是equals()
>
> * 定制排序：比较两个对象相等的标准：Compare()返回0，不在是equals()
>
> *  **自然排序**：TreeSet 会调用集合元素的 compareTo(Object obj) 方法来比较元素之间的大小关系，然后将集合元素按升序(默认情况)排列
>
> * **定制排序：**重写compare()方法，利用int compare(T o1,T o2)方法，比较o1和o2的大小：如果方法返回正整数，则表
>   示o1大于o2；如果返回0，表示相等；返回负整数，表示o1小于o2。
>
>   ****
>
> * 要实现定制排序，需要将实现Comparator接口的实例作为形参传递给TreeSet的构
>   造器。
>
>   * 
>
>   ```java
>   TreeSet set = new TreeSet()//构造器传入定制排序对象，则按照定制排序来进行排序，
>       //构造器传入空参，则按照自然排序
>   ```
>
> * TreeSet的存储结构图：（比上一个数大的放右边，小的放左边）
>
>   ![](F:\Java语言学习\笔记保存的截图\图片1.png)

#### 三个实现类需要自定义类重写的方法：

> 1. List：equals()：用于删除查找
>
> 2. Set：equals()、hashCode()：用于存储不同值
>
> 3. TreeSet：Comparable：CompareTo(Object obj)
>
>    ​				 Comparator：Compare(Object obj1,Object obj2)：用于值的存储
>    
>    [JavaMap笔记](https://blog.csdn.net/qq_29373285/article/details/81487594?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522162069643816780264030617%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=162069643816780264030617&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-1-81487594.first_rank_v2_pc_rank_v29&utm_term=java+map%E4%BD%BF%E7%94%A8)

#### Set转化---------> List:

**问题的引出：**做一个功能的时候 需要将已得到的map的键值放入一个List中做他用，我就很stupid的 逐个遍历、add到list中，真的很低级，简单回顾下其他简便方法吧。

```java
        //构造Map数据
    	Map<String, String> map = new HashMap<String, String>();
    	map.put("ele1", "小樱");
    	map.put("ele2", "若曦");
    	map.put("ele3", "晴川");
    	Set<String> set = map.keySet();
    	
    	//Set转List,方法一 ： ArrayList(Collection<?> c) 
    	List<String> list1 = new ArrayList<String>(set);
    	for(int i = 0; i < list1.size(); i++){
    		System.out.println("list1(" + i + ") --> " + list1.get(i));
    	}
    	
    	//Set转List,方法二：List实现类（ArrayList/LinkedList）的方法  -- addAll(Collection<?> c) 
    	List<String> list2 = new ArrayList<String> ();
    	list2.addAll(set);
    	for(String elem : list2){
    		System.out.println(elem);
    	}
```

#### 思考题：

**一、练习：在List内去除重复数字值，要求尽量简单**

```java
public static List duplicateList(List list) {
	HashSet set = new HashSet();
	set.addAll(list);
	return new ArrayList(set);//返回值的同时将Set集合强转为List列表
}
public static void main(String[] args) {
	List list = new ArrayList();
	list.add(new Integer(1));
	list.add(new Integer(2));
	list.add(new Integer(2));
	list.add(new Integer(4));
	list.add(new Integer(4));
	List list2 = duplicateList(list);
	for (Object integer : list2) {
		System.out.println(integer);
	}
}
```

**二、面试题**

```java
HashSet set = new HashSet();
        Person p1 = new Person(1001,"AA");
        Person p2 = new Person(1002,"BB");
        set.add(p1);
        set.add(p2);
        p1.name = "CC";
        set.remove(p1);
//CC替换AA HashCode所在的位置，实际上(1001,CC)的大概率不在(1001,AA)位置上，因此对P1 hashCode计算出的位置不是(1001,CC)的实际位置，而是真实位置(真实位置实际上是空位置)，即：该方法出去了一个位置上的空元素
        System.out.println(set);//(1002,BB),(1001,CC)
 
        set.add(new Person(1001,"CC"));
//(1001,CC)添加到了实际位置上，与前面(1001,CC)的位置不冲突
        System.out.println(set);//(1002,BB),(1001,CC),(1001,CC)
//根据HashCode值计算出的位置则是第一个(1001,CC)的位置，但由于(1001,CC),(1001,AA)值不同，则也会进行添加成功
        set.add(new Person(1001,"AA"));
        System.out.println(set);//(1002,BB),(1001,CC),(1001,AA)(1001,CC)
```

*其中Person 类中重写了hashCode() 和equal()*

