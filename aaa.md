

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

### 关系运算符 

![](https://xingqiu-tuchuang-1256524210.cos.ap-shanghai.myqcloud.com/1892/Typora20230111213929.png)

### 逻辑运算符

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

 
