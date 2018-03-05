# Shell_Guide
The brief guide of shellscripts.

## shell简介

本文采用在CentOS 7.2下的bash环境作为基础环境。

## 入门

### 入参

特俗符号'$'的特殊含义。

| 符号   | 含义                                       | 备注   |
| ---- | ---------------------------------------- | ---- |
| $$   | 当前脚本的进程ID号                               |      |
| $*   | 全体参数（包括脚本文件或函数名称参数）                      |      |
| $#   | 全体参数的个数                                  |      |
| $n   | n大于0的整数，作为函数或执行脚本的入参位置，\$1代表第一个参数，$2代表第二个参数 |      |
|      |                                          |      |
|      |                                          |      |



### 变量

使用'$'标记变量

### 函数

```shell
function func1()
{
  echo "this is func1"
  # do something
}
```

或者省略掉关键字

```shell
func1()
{
  echo "this is func1"
  # do something
}
```



### 返回

shell脚本中使用exit进行推出，默认退出返回码为0。支持自定义，使用方式为`exit 1`这种加参数的方式进行返回。

shell的返回含义。



## 进阶

shell中的锁

使用标记（距离cat end <<）

```shell
root@Martin:~# cat <<END
> a
> b
> c
> END
a
b
c
root@Martin:~# 
```

字符处理

## 编程建议
