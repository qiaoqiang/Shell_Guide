# Bash下的字符串处理



## grep



## awk



## sed

用sed命令在行首或行尾添加字符的命令有以下几种：

假设处理的文本为test.file



在每行的头添加字符，比如"HEAD"，命令如下：

sed 's/^/HEAD&/g' test.file

在每行的行尾添加字符，比如“TAIL”，命令如下：

sed 's/$/&TAIL/g' test.file

运行结果如下图：

```shell
root@Martin:~# cat test.file 
abc
ab cd
root@Martin:~# sed 's/^/HEAD&/g' test.file
HEADabc
HEADab cd
root@Martin:~# sed 's/$/&TAIL/g' test.file
abcTAIL
ab cdTAIL
```



几点说明：

1."^"代表行首，"$"代表行尾

2.'s/$/&TAIL/g'中的字符g代表每行出现的字符全部替换，如果想在特定字符处添加，g就有用了，否则只会替换每行第一个，而不继续往后找了

例：

```shell
root@Martin:~# cat test.file
abcabc
ab cd
root@Martin:~# sed 's/a/INSERT/g' test.file
INSERTbcINSERTbc
INSERTb cd
root@Martin:~# sed 's/a/INSERT/' test.file
INSERTbcabc
INSERTb cd
```



3.如果想导出文件，在命令末尾加"> outfile_name"；如果想在原文件上更改，添加选项"-i"，如

```shell
root@Martin:~# cat test.file
abcabc
ab cd
root@Martin:~# sed -i 's/a/INSERT/' test.file
root@Martin:~# cat test.file
INSERTbcabc
INSERTb cd
```



4.也可以把两条命令和在一起，在test.file的每一行的行头和行尾分别添加字符"HEAD"、“TAIL”，命令：sed '/./{s/^/HEAD&/;s/$/&TAIL/}' test.file



dos文件转换为unix，去掉"\r" ，用命令`sed -i 's/\r//' test.file`