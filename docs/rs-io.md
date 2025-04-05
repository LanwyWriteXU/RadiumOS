# 输入和输出
***
>获取用户输入和打印内容是计算机和外界交流的重要方式。

## 输入相关
- `input(<content>)` 获取用户输入并返回，在获取之前打印`<content>`

可用的方法:
- `.fill(<list>[],'ch')` 将用户输入以`'ch'`字符分割后覆盖到列表中。比如`input().fill(list[],' ');`就是以空格分隔输入并覆盖到`list`中
- `.sfill(<list>[])` 将用户输入单个字符拆分后覆盖到列表中

## 输出相关
- `print(<content>);` 打印`<content>`并换行

可用的方法:
- `printf(<content>,<rule>);` 以`<rule>`为规则打印`<content>`

可用的`<rule>`:
- `%bn` 保留n位有效数字
- `%fn` 保留n位小数
- `%n` 转换字符而 Unicode 码后打印