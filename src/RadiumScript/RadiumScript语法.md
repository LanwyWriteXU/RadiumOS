# <font color="66ccff">RadiumScript</font> 语法设计

> 为什么不在Scratch里再创造一个Scratch呢？
> 让我们重新定义Scratch——

## 关键字 var(iable)
变量相关
***
### 通用语法：
- ```var <variableName>;```
创建一个名为&lt;variableName&gt;的变量。
- ```var <variableName> <value>;```
创建一个名为&lt;variableName&gt;的变量并设为&lt;value&gt;。

### 高级语法：
- ```var.s <variableName> <value>;```
将名为&lt;variableName&gt;的变量设为&lt;value&gt;。
- ```var.c <variableName> <value>;```
将名为&lt;variableName&gt;的变量增加&lt;value&gt;。
- ```var.d <variableName>;```
删除名为&lt;variableName&gt;的变量。
- ```varr.<variableName>```
调用变量

### 可用的类：
- ```.name```
最没用的类，返回该变量的变量名（发明这个的人真是个天才）。
- ```.length```
返回变量的字符长度。

### 示例：
``` RadiumScript
var abc 114;
var.s abc 514;
var.c abc -1;
print abc;
```
控制台将输出：
```
> 513
```

## 关键字 list
列表相关
***
### 通用语法：
- ```list <listName>;```
创建一个名为&lt;listName&gt;的列表。
- ```list <listName> <value1> <value2> ... ;```
创建一个名为&lt;listName&gt;的列表并将所有&lt;value&gt;添加到列表中。

### 高级语法：
- ```list.a <listName> <value>;```
将&lt;value&gt;添加到列表&lt;listName&gt;中。
- ```list.d <listName> <index>;```
将列表&lt;listName&gt;中的第&lt;index&gt;项删除。
- ```list.c <listName>;```
清空&lt;listName&gt;列表中的所有项目。
- ```list.i <listName> <index> <value>;```
在&lt;listName&gt;列表的第&lt;index&gt;项前插入&lt;value&gt;。
- ```list.r <listName> <index> <value>;```
将&lt;listName&gt;列表的第&lt;index&gt;项替换为&lt;value&gt;。
- ```list.d <listName>;```
删除名为&lt;listName&gt;的列表。
- ```<listName>[]```
调用列表。

### 可用的类：
- ```.name```
最没用的类，返回该列表的列表名。
- ```.length```
返回列表的项目数。
- ```[<value>]```
返回列表的第&lt;value&gt;项，就像 ```list[2]``` 会返回列表list的第2项一样。
- ```<-<value>```
判断列表是否包含&lt;value&gt;，返回布尔值true或false。

### 示例：
``` RadiumScript
list test 114 514;
list.d test 1;
list.a 514;
list.r test 1 114;
print test[];
list.i test 1 "amns";
print test[1];
print test[];
```
控制台将输出：
```
>114 514
>amns
>amns 114 514
```

## 关键字 input
输入相关
***
### 通用语法：
- ```input <variableName/listName>;```
将屏幕输入（包括空格）设为变量&lt;variableName&gt;的值 / 添加到列表&lt;listName&gt;中 。

### 高级语法：
- ```input.t <variableName/listName> <tips>;```
在输入之前打印提示&lt;tips&gt;.