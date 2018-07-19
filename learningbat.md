###delims
```
delims==,?
则表示以=,?这三个符号为分隔符
```


```
批处理、Bat 截取文本中指定的字符：
for /f "eol=- tokens=1 delims= " %%i in (result.txt) do echo %%i>>s2.txt
参数详解：
for /f       这个这个参数表示对文本操作
tokens       表示截取
tokens=1,2   表示选取1，2两个部分
eol          表示忽略
eol=-        表示忽略-开始的行
delims       表示分割符
delims=,     表示对每行以“,”为分割符号对行进行分割字符
```

###echo
```
echo /?
显示消息，或者启用或关闭命令回显。
  ECHO [ON | OFF]
  ECHO [message]

补充：
当echo后面引用变量的值为空时，会提示
例如：
@echo off
set p=
echo %p%

根据@echo off 的设定，由于p为空，则输出结果为：
echo 处于关闭状态
```
