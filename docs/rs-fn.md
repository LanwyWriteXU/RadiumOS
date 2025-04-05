# 函数和结构体
***
>重复的内容我们完全可以通过函数来代替!

## 函数相关
- `def <func>(<value>){code};` 定义一个名为`<func>`的函数，并需要传入参数`<value>`

参数应该在传入和调用之前定义其类型，如var、list等。

若函数包含`return`，那么其可以作为一个右值使用，反之则不能作为一个右值。

## 结构体相关
>结构体就像一个可以存储不同类型对象和值的大型"库"

- `struct <name> {content};` 定义一个结构体类
- `<name> <object>;` 定义一个`<name>`类型的结构体名为`<boject>`
- `<name> <boject> {value};` 定义并赋值
- `<object> = {value};` 赋值
- `<object>.<content>` 访问内容
- `<object>.<content> = <value>;` 赋值