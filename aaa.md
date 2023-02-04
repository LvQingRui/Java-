 

# 类型转换

## 强制类型转换

### 基础

自动类型转换的逆过程，将容量大的数据类型转换为容量小的数据类型。使用时要加上强制转换符（），但可能造成精度降低或溢出,格外要注意。

### 细节

1. 当进行数据的大小从 大 到 小的时候， 就需要使用到强制类型转换
2. 强转符号只针对于最近的操作数有效，往往会使用小括号提升优先级

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230105173117.png)

3. char类型可以保存int的常量值，但是不能保存int的变量值，需要强转

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230105173151.png)

4. byte和short， char 类型在进行运算时，当做int类型处理

###  基础数据类型转换题

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230105173547.png)

## 基本数据类型和String类型的转换

### 基本数据类型转String类型

语法就是：将基本类型的值 + “” 即可

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230105173837.png)

### String类型转基本数据类型

语法就是：通过基本类型的包装类调用ParseXX方法就可以

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230105174149.png)

### String类型的变量取字符

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230105174431.png)

### 注意事项

1. 在将String 类型转成 基本数据类型时，要确保String类型能够转成有效的数据，比如 我们可以把“123”，转成一个整数，但是不能把“hello”转成一个整数

2. 如果格式不正确，就会抛出异常，程序就会终止，这个问题在异常处理章节中，会处理的。

# 运算符

## 算术运算符

### 算术运算符一览：

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230111205519.png)

==在%的本质，其实就是一个公式：a % b = a - a / b * b==

####  面试题1：

```java
/*
* 使用临时变量
* 解释：
* temp = i; i = i + 1; i = temp;
**/
int i = 1;
i = i ++;
System.out.println(i); 
```

 

##### 面试题2：

```java
/*
* 使用临时变量
* 解释：
* i = i + 1; temp = i; i = temp;
**/ 
int i = 1;
i = ++i;
System.out.println(i);  // 2
```

## 关系运算符

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230111213929.png)

## 逻辑运算符

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230111214705.png)



#### 短路与( && )和逻辑与( & )

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230111215200.png)

 

#### 短路或( || )和逻辑与( | )

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230111220813.png)

#### 取反( ! ) 和 逻辑异或( ^ )

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230111221011.png)

##  赋值运算符

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230111225145.png)



### 细节：主要注意第四点

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230111225328.png)

 ```java
// 复合赋值运算符会进行类型转换
byte b = 3;
b += 2; // b = (byte)(b + 2)
b = b + 2; // 就会报错int 转 byte  会损失
b ++; // b = （byte)(b + 1)
b = b + 1; // 就会报错int 转 byte  会损失
 ```

## 三元运算符

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230111230540.png)

==上述案例的答案是 result 输出是 99==  

### 细节

1.

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230111232625.png)

2. 三元运算符可以转换成if -- else语句

## 运算符的优先级

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230111234944.png)

# 标识符的命名规则和规范

## 规则

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114123411.png)

## 规范

 ![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114124749.png)

# 关键字和保留字

## 关键字

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114125528.png)

  ![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114125555.png) 

## 保留字

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114125705.png)

# 键盘输入语句

这里比较简单 简单笔记

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114130918.png)

# 进制

## 进制介绍

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114131026.png)

## 进制转换(基本功)

### 其他进制转十进制

#### 二进制转十进制

规则：

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114163342.png)





#### 八进制转十进制

规则：

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114163624.png)







#### 十六进制转十进制

规则：

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114163714.png)





### 十进制转其他进制

注意： 要短除到商0为止，从下往上倒着写

#### 十进制转二进制

规则：

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114163832.png)



#### 十进制转八进制

规则：

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114164032.png)



#### 十进制转十六进制

规则： 

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114164131.png)



### 其他进制的互相转换

#### 二进制转八进制 、二进制转十六进制、十六进制转二进制、八进制 转二进制

规则：其实有其他方法，但是 我觉得 还是以十进制 为 中间介质 进行计算  比较好理解：

我们以第一种转化为例子：二进制转八进制，只需要先将二进制转成十进制，再将转化过后的十进制转化为八进制即可。

# 原码、反码、补码（重点、难点）

## 总体概括（非常重要！！！！）

 ![   ](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114165728.png)

## 位运算符

（按位与&,按位或|,按位异或^,按位取反~,算术左移<<,算术右移>>,逻辑右移（无符号右移）>>> ）

### 运算规则

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114170826.png)

 左乘右乘  2

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114172155.png)



### 运算案例：

1. 2&3   

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114170717.png)

2. ~-2

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114171312.png)

3. ~2

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114171611.png)

4. 1 >> 2      1 << 2

 ![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114172516.png)



# 条件分支

## 单分支

### 单分支基本语法和说明

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114185938.png) 

### 单分支的流程图

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114191145.png)

## 双分支

### 双分支基本语法和说明

   ![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114191309.png)

### 双分支的流程图

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114191418.png)

## 多分支

### 多分支基本语法和说明

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114192353.png)

### 多分支的流程图

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114192407.png)

## 嵌套分支

### 嵌套分支基本语法和说明

 ![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114195211.png)

## Switch分支结构

### Switch分支基本语法和说明

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114203125.png) 

### Switch分支的流程图

注意《穿透》

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114204003.png)

### Switch分支的细节讨论

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114205144.png)

# 循环

## for循环

### for循环基本语法和说明

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230114233805.png)

### for循环流程图

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230115111458.png)

### for循环的细节

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230115112146.png)

## while循环

### while循环基本语法和说明

 ![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230115122615.png)

### while循环流程图

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230115123006.png)

### while循环的细节

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230115123738.png)

 

## do - while循环

### do - while循环基本语法和说明

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230115125253.png)

### do - while循环流程图

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230115125657.png)      

### do - while循环的细节

 ![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230115130621.png)



## 多重循环控制(重点、难点)

### 多重循环的说明

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230115131603.png)

# 跳转控制语句

## break

### break基本语法和说明

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230115190335.png)

### 以while循环为例的流程图

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230115190611.png)

### break的细节

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230115191201.png)  

## continue

### continue基本语法和说明

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230115194141.png)

### 以while循环为例的流程图

 ![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230115194453.png)

# 数组

## 数组介绍

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230116184230.png)                       

## 数组的使用

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230116190908.png)

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230116205657.png)

  ![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230116205928.png)

## 数组使用的注意事项和细节

   ![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230116210211.png)

## 数组赋值机制

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230116214854.png)

代码：

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230116215200.png)

### 数组赋值的内存图

   ![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230116220313.png)

## 数组拷贝

 ![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230116222833.png)



![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230116222843.png)

## 数组翻转

### 方法一：找规律

 ![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230116223311.png)

### 方法二：使用逆序赋值的方式

  ![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230116223828.png)

## 数组的扩容

要求：

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230116224033.png)

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230116224432.png)

# 排序

## 排序介绍

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230117233742.png)

## 冒泡排序的基本思想

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230117233905.png)

## 冒泡排序的分析和特点

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230117235458.png)

## 冒泡排序的代码

以五个数字为例

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118000454.png)

# 查找

## 顺序查找

例题：

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118001143.png)

# 二维数组

 ## 快速入门

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118121643.png)

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118122231.png)

## 二维数组的使用

### 使用方式1：动态初始化

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118122729.png)

###  二维数组在内存的存在形式（重要）

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118124053.png)

### 使用方式2：动态初始化

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118124308.png)

### 使用方式3：动态初始化-列数不确定

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118124431.png)

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118124946.png)

### 使用方式4：静态初始化

![image-20230118125252327](/Users/lvqingrui/Library/Application Support/typora-user-images/image-20230118125252327.png)

## 例题：杨辉三角

打印前10行的杨辉三角

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118130150.png)

## 二维数组使用细节和注意事项

![image-20230118130340008](/Users/lvqingrui/Library/Application Support/typora-user-images/image-20230118130340008.png)



## 例题：

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118131626.png)



# 类与对象

## 类与对象的区别和联系

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118155417.png)

## 对象在内存中的存在形式（非常重要）

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118160022.png)

## 属性的概念

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118160440.png)

## 属性的注意事项和细节

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118164724.png)

## 创建对象访问属性

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118165035.png)

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118165050.png)

## 类与对象的内存分配机制（重要）

思考题：

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118165307.png)

内存图： 重要↓ √

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118170425.png)

## 对象创建过程

### Java内存的结构分析

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118171549.png)

### Java创建对象的流程

![image-20230118171834023](/Users/lvqingrui/Library/Application Support/typora-user-images/image-20230118171834023.png)

## 成员方法

### 基本介绍

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118172724.png)

### 方法调用机制原理

用上面的getSum 方法 来演示

![ ](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118180408.png) 

### 成员方法的好处

 ![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118181455.png)



### 方法的定义

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118181831.png)



### 方法的注意事项和使用细节

   



![](/Users/lvqingrui/Library/Application Support/typora-user-images/image-20230118222111635.png)







![image-20230118222213094](/Users/lvqingrui/Library/Application Support/typora-user-images/image-20230118222213094.png)









![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118223453.png)

![image-20230118230027402](/Users/lvqingrui/Library/Application Support/typora-user-images/image-20230118230027402.png)

### 成员方法的传参机制

值传递：

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118232653.png)

引用传递：
![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230118233902.png)

 

## 递归

### 基本介绍

![image-20230122213617367](/Users/lvqingrui/Library/Application Support/typora-user-images/image-20230122213617367.png)



# 方法重载（Overload）

## 基本介绍

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230130010131.png)

## 细节

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230130010812.png)



例子：

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230130010848.png)

# 可变参数

## 基本概念与语法

![image-20230130131631243](/Users/lvqingrui/Library/Application Support/typora-user-images/image-20230130131631243.png)

## 注意事项和使用细节

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230131222452.png)

# 作用域

## 基本使用

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230131224519.png)

## 注意事项和细节

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230131225143.png)

![image-20230131230848616](/Users/lvqingrui/Library/Application Support/typora-user-images/image-20230131230848616.png)

# 构造器

## 基本用法

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230131231142.png)

## 基本介绍

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230131231349.png)

## 注意事项和使用细节

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230131232049.png)

  

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230201135427.png)



# 对象创建的流程分析(非常重要)

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230201141755.png)

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230201142146.png)



# this关键字

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230201145122.png)

## 使用细节

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230201150402.png)





如有版权，请看Readme.md文档
