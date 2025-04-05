# <font color="66ccff">RadiumScript</font>
<small>注:以下内容为 **RadiumScript** 第三版内容</small>
> 为什么不在Scratch里再创造一个Scratch呢？
>
> 让我们重新定义Scratch——
***

## 介绍：
**RadiumScript** 是一个还需完善的解释性语言。通过在 Scratch 中建立了一个解释器，自主编写了个解释器，来运行 Scratch 代码。与其他大多数 Scratch 自制语言不同的是，RadiumScript 是完全与 Scratch 原有的代码分离的，但是你又可以在里面调用 Scratch 的某些函数。

RadiumScript 支持 **局部变量**，**指针变量**，**复合结构**(比如结构体)，**面向对象编程** 等高级语言功能，通过编写 RS 代码并将其在解释器中运行，你可以为 RadiumOS 编写软件等。而且，RS 语法，虚拟机等都是开源的。你只需要遵守 GPL 协议就可以随意改变或移植。

## 语法：
RS 的语法借鉴了 C++ 和 Python，所以我几乎可以用 C++ 的上色模式来上色 RS：

```cpp
import math;
var a;
a = input("Type a number:");
print(sin(a));
```

假如用户输入30，上述的代码就将在控制台输出`0.5`。而这一切计算都是由 Scratch 来完成的(所以精度也和在 Scratch 中计算的一样，一般是保留十位小数)。在 RadiumScript ，你几乎可以像用 Scratch 一样写代码，就像某 SQY 制作的 S++ 一样。但是在下面的代码中，输出却既然不同。首先是 S++ 的代码：

```Python
a=114
print(a)
    a=514
    print(a)
print(a)
```
上述代码在 S++ 中(S++ 中使用缩进表示域)输出应该是：
```
114
114
114
```
然后是 RadiumScript ：

```cpp
{
    a = 114;
    print(a);
    {
        a = 514;
        print(a);
    };
    print(a);
}
```
上述代码在 RS 中(RadiumScript 中使用花括号表示域)输出应该是：
```
114
514
114
```
可以看出，相较于 S++，RS 拥有更直观的域表示，以及**局部域**的区别。

S++ 中，第二个赋值语句未正确执行，是因为这是错误语法。S++ 中本身没有域的概念，即使缩进表示域，也不能正确运行。在赋值给`a`的时候，S++ 的解释器将缩进和a连接起来作为了一个对象(即`  a`)赋值，所以导致错误。这很反直觉，但是事实就是如此。

RadiumScript 的定位是高级语言，所以也有 **OOP** 的概念。所以，接下来让我们详细介绍 RadiumScript 的语法吧。