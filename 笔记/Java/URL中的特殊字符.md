# URL中的特殊字符

URL出现了有+，空格，/，?，%，#，&，=等特殊符号的时候，可能在服务器端无法获得正确的参数值，此时需要对字符进行转译。

URL中一些字符的特殊含义，基本编码规则如下：
1、空格换成加号(+)
2、正斜杠(/)分隔目录和子目录
3、问号(?)分隔URL和查询
4、百分号(%)制定特殊字符
5、#号指定书签
6、&号分隔参数

如果需要在URL中用到，需要将这些特殊字符换成相应的十六进制的值
\+ %2B
/ %2F
? %3F
% %25
\# %23
& %26

```java
String str = "adfaf+afaf";
String s = str.replaceAll("\\+", "%2b");
```

使用URLEncode编码后也行：

```java
String str = "";
str = URLEncoder.encode(str, "UTF-8");
```
