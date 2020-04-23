### Java基础

#### Hello World

```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

Hello为类名，必须和文件名一样：Hello.java

main为 `main方法` ，类似C语言中的 `main函数` ，C语言中的函数在Java中称作方法

第三句和C语言中的printf函数功能一样，输出文字

public 为权限修饰符，很明显是公共的意思，具体意义之后会说到，目前只需要记住格式

class 代表类，目前只需了解即可



#### 注释

Java的注释和C语言一致

```java
//单行注释

/*
	多行注释
*/
```



#### 关键字

关键字就是 `int`、`public`、`class` 等等，和C语言一致，关键字你不能使用，你不能写成如下形式：

```java
int class = 2;
```



**关键字特点**

1. 全部是小写字母

2. 有特殊颜色



#### 标识符

- **标识符** ：程序中，我们自己定义的内容，比如类的名称、方法名、变量名等等，都是标识符

- **命名规则**
  - `26个英文字母（区分大小写）`、`0-9`、`$（美元符号）`、`_（下划线）`
  - 不能以数字开头
  - 不能是关键字

- **命名规范**
  - 类名：首字母大写，大驼峰
  - 方法名：首字母小写，小驼峰
  - 变量名：同方法名



#### 常量

在程序中不变的量

| 类型       | 示例           |
| ---------- | -------------- |
| 字符串常量 | "hello"、"123" |
| 整数常量   | 123、0、-20    |
| 浮点数常量 | 2.5、-1.2      |
| 字符常量   | 'A'、'9'       |
| 布尔常量   | true、false    |
| 空常量     | null           |



#### 基本数据类型

数据类型分为**基本数据类型**和**引用数据类型**，这里我们先只说基本数据类型，我们只要记住除了基本数据类型，其他的数据类型都是引用数据类型，如字符串、数组等等

基本数据类型包括 `整数`、`浮点数`、`字符`、`布尔`



| 类型         | 关键字  | 内存大小(字节) | 取值范围     |
| ------------ | ------- | -------------- | ------------ |
| 字节型       | byte    | 1              | -287~127     |
| 短整型       | short   | 2              | -32768~32767 |
| 整型         | int     | 4              |              |
| 长整型       | long    | 8              |              |
| 单精度浮点型 | float   | 4              |              |
| 双精度浮点型 | double  | 8              |              |
| 字符型       | char    | 2              | 0-65535      |
| 布尔类型     | boolean | 1              | true、flase  |

>Java中默认整型数字为 `int`，浮点类型为 `double`



#### 变量

程序运行期间，内容可以发生改变

```java
int a = 3;
char c = 'a';
String str = "hello";
int[] a = new int[20];
```



#### 类型转换

因为 Java 中默认整型数字为 `int`，浮点类型为 `double` ，所以给 long 和 float 变量赋值时，需要在数字后面加 `L/l`，和 `F/f` ，其中建议使用大写的 `L`  ，如你所见，小写的 `l` 容易看成数字 `1`

```java
long age = 25L;
long age = 25l;
float b = 20f;
float b = 20F;
```



**强制类型转换**

```java
 int a = (int)3.14;
```



#### 四则运算

加减乘除，自增自减，同C语言，不必多说

| 运算符 |      |
| ------ | ---- |
| +      |      |
| -      |      |
| *      |      |
| /      |      |
| %      |      |
| ++，-- |      |



#### 比较运算

同C语言

| 比较运算符 |      |
| ---------- | ---- |
| ==         |      |
| \<         |      |
| \>         |      |
| \<=        |      |
| \>=        |      |
| !=         |      |



#### 逻辑运算

同C语言

| 逻辑运算符 |      |
| ---------- | ---- |
| &&         |      |
| \|\|       |      |
| !          |      |



#### 三元运算符

三元运算符就是需要三个数据才能运算，同C语言

```java
a = (3 > 2) ? 5 : 6;
```



### 方法入门

Java中方法不是一个简单的东西，它的功能与形式类似于C语言的函数，但是方法还具有不同的修饰符，这些修饰符有不同的用法与含义，目前只需要简单的记住一些方法的模板即可，我们会慢慢解释



#### 方法的定义

方法定义在main方法外面，类里面。

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println(add(10, 20));
    }
    public static int add(int a, int b) {
        return a + b;
    }
}
```

`public static` 暂时就这样固定的写，这两个修饰符的大致意义是：`public` 表示方法是公共的， `static` 可以在mian方法中用方法名直接调用，不行你把static去了看看还能不能再main方法中直接调用。具体原理之后细说，再次小伙伴们只需要记住格式就可以了

`int` 为方法返回值类型，同C语言

参数列表同C语言



#### 注意事项

1. 方法定义的先后顺序无所谓
2. 方法的定义不能产生嵌套包含关系

方法目前只介绍这么多，本章节只是方法的入门教程



### 输入输出

到了这里，你可能还不清楚 Java 怎么进行输入输出，C语言刚学的时候我们知道用 `printf` 和 `scanf` 进行输出和输入，前面我们也见过 ` System.out.println` ，它表示：向屏幕中输出数据并换行。

我们这里简单介绍一下java的输入输出，为什么是简单的介绍，因为java的输入并不简单，希望大家和之前的方法入门一样，只需要记住就可以了，就像我们学习 `printf` 和 `scanf` 时，一开始只掌握它们的使用，对它们的理解会随着学习的深入越来越清楚。



##### 输出

前面我们认识了 ` System.out.println()` ，它表示向控制台输出一个**字符串**，并换行

```java
System.out.println("Hello World!");
```



可以通过 `+` 把两个字符串连接起来， `+` 被称为**字符串连接符**

```java
System.out.println("Hello " + "World!");
```



可以直接输出参数，也可以使用字符串连接符与其他字符串连接起来

```java
int age = 18;
System.out.println(age);
System.out.println("我今年" + age + "岁了");
```



`System.out.print()` 表示向控制台输出一个**字符串**，不换行

```java
System.out.print("Hello World!");
```



可以使用格式控制符 `\n` 、`\t` 等等

```java
System.out.print("Hello World!\n");
```



##### 输入

使用 `Scanner` 进行输入，先看例子：

```java
import java.util.Scanner;

public class HelloWorld {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int a = scanner.nextInt();
        System.out.println(a);
    }
}
```

我们发现第一行多了一句 `import java.util.Scanner;` ，这是**导包**，和C语言的头文件一样，我们要使用 `Scanner` 就要先导包

导包之后还不能直接用，`Scanner scanner = new Scanner(System.in);` 表示创建一个 `Scanner` 对象，小写的 `scanner` 为对象名，可以随意取名，但一般取名为 `scanner` 。关于对象是什么，为什么要创建对象的问题，大家先不用管，就这样写，随着之后的学习，大家就慢慢清楚了

创建对象之后，使用 `scanner.nextInt()` 来获取键盘上输入的 `int` 型数据赋值给 a ， `scanner` 为对象名，`nextInt()` 是一个方法，这种**点**的操作有点像结构体，确实Java中的对象的操作就类似C语言中的结构体，但是Java的对象可以调用方法，我们看到的 `nextInt()` 就是 `Scanner` 对象的一个方法

`nextInt()` 是输入 `int` 型数据，同理 `nextDouble()` 就是输入 `double` 型数据，你要输入什么类型的数据，就在next后面加上类型名称，首字母大写就行了

如果是 `nextInt()` ，但是你输入了不是 `int` 型的数据，那程序就会**抛异常**，你可以理解为程序运行中发生了异常，此时程序终止运行，并把异常抛出来，关于**异常**的知识我们之后会讲解，暂时只需要认为程序因为发生了错误而终止



### 流程控制

#### if/else

同C语言，看一下例子就清楚了

```java
public static void main(String[] args) {
    int year = 2020;
    if (year % 400 == 0) {
        System.out.println(year + "为闰年");
    } else if (year % 4 == 0 && year % 100 != 0) {
        System.out.println(year + "为闰年");
    } else {
        System.out.println(year + "不是闰年");
    }
}
```

输出结果

```java
2020为闰年
```



#### switch

用法和功能和C语言一样

```java
Scanner scanner = new Scanner(System.in);
int par = scanner.nextInt();
switch (par){
    case 1:
        System.out.println("Hello");
        break;
    case 2:
        System.out.println("World");
        break;
    default:
        System.out.println("Java");
        break;
}
```



### 循环结构

Java的循环结构和C语言一致，`continue` 和 `break` 也一致

#### for循环

同C语言

```java
for (int i = 0; i < 10; i++) {
    System.out.println(i);
}
```



#### while循环

同C语言

```java
while (true){
    System.out.println("666");
}
```



#### do-while循环

同C语言

```java
do {
    System.out.println("66");
}while (true);
```



### 方法的重载

同C语言的函数重载

1. 参数个数不同 
2. 参数类型不同
3. 多类型的顺序不同
4. 与返回值无关
5. 与参数名称无关



```java
public static void main(String[] args) {
    System.out.println(add(2, 3));
    System.out.println(add(2.5, 3));
    System.out.println(add(2, 3.5));
    System.out.println(add(2, 3, 4));
}
public static double add(int a, int b) {
    return a + b;
}
public static double add(double a, int b) {
    return a + b;
}
public static double add(int a, double b) {
    return a + b;
}
public static double add(int a, int b, int c) {
    return a + b + c;
}
```



### 数组

数组的功能和C语言一样，但是定义形式不同，在Java中，数组是一种引用类型

#### 数组的特点

1. 数组是一种引用类型
2. 数组的长度在程序运行期间不可改变



#### 数组的定义

Java中数组的定义和C语言不同，C语言是 `int a[10];` ，但Java是如下的形式

`数据类型[] 数组名称 = new 数据类型[20];`

```java
int[] array = new int[20];
double[] arr = new double[20];
```



#### 数组的初始化

同C语言的 `int a[] = {2,3,4,5};`

以下两种都可以

```java
int[] array = new int[] {2,3,4,5};
int[] arr = {2,3,4,5};
```



#### 数组的使用

##### 访问和赋值

数组元素的访问和赋值和C语言一致，通过 `array[i]` 操作就可以了下标从0开始，一直到数组长度-1

获取数组长度的方法：通过 `数组名.length` 获得数组的长度，比C语言要方便

简单的示例

```java
int[] arr = new int[10];
System.out.println(arr.length);
for (int i = 0; i < arr.length; i++) {
    arr[i] = i+1;
}
for (int i = 0; i < arr.length; i++) {
    System.out.println(arr[i]);
}
```



直接打印数组名会输出数组的**哈希值**，这个哈希值就类似C语言的地址，C语言可以通过指针操作地址，但在Java中没有指针，不允许操作地址

```java
int[] arr = new int[10];
System.out.println(arr);
```

输出结果

```jav
[I@10f87f48
```



##### 数组默认值

在数组定义的时候没有初始化，这时候数组中的元素会有一个默认值

| 数据类型 | 默认值   |
| -------- | -------- |
| 整型类型 | 0        |
| 浮点型   | 0.0      |
| 字符类型 | '\u0000' |
| 布尔类型 | false    |
| 引用类型 | null     |

> 字符类型的默认值为  '\u0000' ，\u 代表Unicode，0000代表十六进制数，这是一个不可见字符



### Java的内存划分

![](https://raw.githubusercontent.com/lijiangdong/study-notes/master/JVMNotes/imgs/03-01.png)





### 字符串基础

该节讲一讲字符串的基本操作，方便大家对 Java 的基础语法有个快速的了解，在这一节大家只需要掌握如何定义和使用字符串即可



#### 字符串的定义

字符串的定义可以通过对象的形式定义，就像之前的 `Scanner`，也可以像 `int` 一样定义

```java
//对象形式
String string = new String("hello");
System.out.println(string);

//简略形式
String str = "hello";
System.out.println(str);
```



















