# 分支与循环
***
>最有用的语句，毕竟谁不喜欢if else嵌套呢?

## 分支语句
>我们需要做判断，电脑也一样。

- `if (<condition>) {code};` 如果`<contition>`那么`{code}`
- `if (<condition>) {code} else {code};` 如果`<condition>`那么`{code}`反之执行下面的语句
- `<condition>?<value1>:<value2>` 三元运算符，如果`<condition>`成立，则返回`<value1>`，反之返回`<value2>`
- SWITCH 语句:执行`<index>`=`<item>`之后的所有代码
```cpp
switch (<index>){
case <item1>:{code1};
case <item2>:{code2};
...
case <item n>:{code n};
};
```

## 循环语句
>人类的本质是复读姬!

- `while (<condition>) {code};` 重复执行直到`<condition>`不成立
- `do {code} while (<condition>);` 先执行一次之后判断成立
- `break;` 跳出该块(花括号抱起来的部分，即一个局部域)