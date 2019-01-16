# ncat工具

```
NCAT 的意思就是　连接和重定向套接字(Concatenate and redirect sockets)

使用方法呢也是ncat [OPTIONS...] [hostname] [port]

描述

ncat是一个功能强大的网络工具，能从网络之中通过命令行读取和写入数据．

ncat是为nmap项目编写的，是从nmap项目中分离出来的最好的部分

它设计是一个可靠的后端工具，以提供即时网络连接到其他用户和应用程序

ncat不仅仅可以工作在ipv4和ipv6下，还可以为用户提供无限潜能的用途

ncat最大的特征就是能够链接Ncat's在一起(chain Ncat's together)．

提供TCP, UDP的重定向功能，并且还有SSL的支持

还有通过SOCKS4和HTTP代理（可选代理认证）连接到代理

一些一般的原则适用于大多数的应用程序，从而给你其它应用程序一般不会提供在，但是可以马上增加软件的网络能力的能力．



OPTIONS SUMMARY

-4　仅仅使用IPV4

-6　仅仅使用IPV6

-U,  --unixsock　仅仅使用Unix套接字

　　　这个选项使用Unix的域名套接字，而不是网络套接字，这个选项可以用在自己的流式套接字，或结合UDP数据包套接字

-C, --crlf　使用CRLF代替EOL句子

-c, --sh-exec <command>　通过/bin/sh执行命令行

-e, --exec <command>　执行传递的命令行

-e, --lua-exec <filename>　执行传递的Lua脚本

-g hop1[,hop2,...]　松散的源路由跳点(最大是８)

　　　松散源路由跳数设置为ipv4，可以用逗号隔开一个分割列表，　用多个时间的单跳来构建列表，或者把两者结合起来．hops可以使用ip地址和主机名

-G <n>　松散的源路由跳指针(4,8,12,...)

　　　　设置ipv4的源路由指针，参数必须是4的倍数，并非所有的操作系统支持这个指针直到4

-m, --max-conns <n>　最大同时连接数

　　　100是默认值（windows中是60）

-h, --help　显示帮助文档

-d, --delay <time>　等待写和读之间的间隔

-o, --output <filename>　将会话数据转储到文件

-x, --hex-dump <filename>　将会话数据转储成十六进制格式

-i, --idle-timeout <time>　空闲读写超时

-p, --source-port port　指定使用特定的源端口

-s, --source addr　指定使用特定的地址(不影响 -l 选项)

-l, --listen　连接和收听到来的连接

-k, --keep-open　接受多个听模式的连接

　　　一般只接受一个连接，当连接关闭时，则退出．这个选项使得它可以接受多个同时连接，并等待更多的连接，并等待他们都关闭．它必须和监听模式一起使用．这种模式　　　下ncat是无法知道输入完成的，这也意味着它不会关闭输出流．所以所有的ncat程序一直会在寻找EOF挂起．

-n, --nodns　不通过DNS解析主机名

-t, --telnet　回答telnet的谈判

-u, --udp　使用UDP代替默认的TCP

-u, --sctp　使用SCTP代替默认的TCP

　　　SCTP支持TCP兼容模式

-v, --verbose　设置的详细程度(可以使用几次)

-w, --wait <time>　连接超时

-w, --append-output　追加指定文件而不是乱码

-w, --send-only　只传送数据，忽略接收，退出是EOF

-w, --recv-only　只接收数据，不发送任何东西

-w, --allow　只允许特定的主机连接到ncat

-w, --allowfile　一种允许连接到ncat的文件

-w, --deny　拒绝连接到ncat

-w, --denyfile　拒绝文件连接到ncat

-w, --broker　使用ncat的代理连接模式

　　　允许多个组织连接到ncat的服务器和其他人交流．ncat能创建一个经纪人在连接和系统之间通过NAT或者其他的直接连接．这个选项是和监听模式一起使用的．这会使监　　　听端口的经纪人模式启动

-w, --chat　开启一个简单的ncat聊天服务器

　　　聊天模式，用于几个用户之间交换文本．的这个模式下，连接代理是打开的．ncat设置一个前缀ID在每个收到的消息在转发到其他连接之前．

　　　这个ID对于每个客户是唯一的．这有助于区分谁发送了什么．此外，非打印字符，如控制字符，是被拒绝的．

-w, --proxy <addr[:port]>　指定主机的地址代理通过

　　　请求代理通过 host[:port]来使用指定的协议的代理类型．如果没有指定端口代理，将使用著名的端口代替（SOCKS是1080, HTTP是3128）

　　　当指定一个ipv6的HTTP的代理服务器的时候，最后使用ip地址，而不是主机名．端口号必须指定好．如果代理服务器要求使用身份验证，使用--proxy-auth

-w, --proxy-type <type>　指定代理类型

　　　在连接模式下，这个选项请求通过代理指定的代理主机连接协议．

　　　在监听模式下，这个选项ncat作为一个使用指定的协议的代理服务器．

　　　目前可用的是HTTP连接方式和SOCKS(SOCKSv4)．目前只支持HTTP的服务器．如果不使用这个选项．默认的协议是HTTP

-w, --proxy-auth <auth>　验证的HTTP或SOCKS代理服务器

　　　在连接模式下，给出用于连接代理服务器的凭据．

　　　在监听模式下，给出了连接客户端所需要的凭据．

　　　使用 --proxy-type http时，格式应该是 user:pass

　　　使用 --proxy-type socks4,应该只有一个username

-w, --ssl　使用ssl来监听或者连接

　　　在连接模式下，这个选项透明的协商一个ssl会话和一个ssl安全加密连接．这对于启动ssl和http服务器是特别有用的．

　　　在服务器模式下，这个选项监听传入的ssl连接，代替明显的非隧道传输．

-w, --ssl-cert　指定ssl证书文件来监听

　　　这个选项提供一个PEM-encoded证书文件定位来证实服务器（监听模式下）或者客户（连接模式下）的真实性．

　　　和--ssl-key选项一起使用．

-w, --ssl-key　指定ssl私钥来监听

　　　这个选项定位PEM-encoded私钥文件．和--ssl-cert一起使用．

-w, --ssl-verify　验证证书和域名的真实性

　　　在客户端模式下，ssl验证除非它也需要ssl服务器证书验证．ncat中有一组默认文件中的可信证书的CA束．

　　　一些操作系统提供一个可信的证书的默认列表．这些也将被使用．如果可以，使用ssl trustfile来自定义列表．使用-v来获得验证失败的详细信息．

　　　ncat并不检测吊销的证书．

-w, --ssl-trustfile　PEM文件包含受信任的ssl证书

　　　这个选项将为证书验证设置一个可信任的证书列表．它如果不和--ssl-verify一起使用是没有意义的．这个选项的参数是PEM的名字．

　　　含有可信息的证书文件．通常，这个文件将包含颁发机构的证书．虽然还会包含服务器证书，但是，这个选项下，ncat并不使用其默认证书．

-w, --ssl-ciphers　使用包含ssl密码的密码表

　　　这个选项将设置连接到服务器或者接受客户的ssl连接时的密码表．语法是在OpenSSL的密码描述．

-w, --version　查看ncat的版本信息



连接和监听模式：

ncat主要工作在两种模式：连接模式和监听模式（连接模式应该就是不停发送数据，监听模式应该就是不发送数据），还有特殊的其他模式，如HTTP代理服务器模式．

在连接模式下，ncat做为客户端，在监听模式下，ncat作为服务器．

在连接模式下，主机和端口参数告诉怎么连接．主机名必须要，可以是一个主机名或者ip地址．还可以追加一个端口号，必须是十进制的，如果省略，默认是31337．

在监听模式下，主机名和端口控制的地址服务器将被绑定．这两个参数是可选的（也就是说你可以不选），如果主机名被忽略，默认监听所有的ipv4和ipv6的所有地址，如果省略端口，默认为31337
```





## 使用案例

```
ncat使用案例



（1）连接目标端口

ncat lybbn.cn 80


（2）端口转发

ncat --sh-exec  "www.lybbn.cn 80" -l 8080 --keep-open


（3）使用代理（使用socks4代理连接邮件服务器）

ncat --proxy  www.lybbn.cn  --proxy-type socks4 --proxy-auth user smtphost 25


（4）创建本地HTTP代理

ncat -l --proxy-type http localhost 8888


（5）文件传输（可以反向传输）


服务端



root@lalays:~# ncat -lv 333 > lybbn.txt


注意：服务端的文件可以不用存在，传输时会自动创建


客户端

C:\&gt;ncat -nv 172.16.0.182 333 < lybbnclient.txt


6）客户端使用ncat加密连接服务器


服务端

root@lalays:~# ncat -nvl 333 -c bash --ssl

客户端

C:\&gt; ncat -nv 172.16.0.182 333 --ssl
```



#ncat用法

**nc命令**是**netcat命令**的简称，都是用来设置路由器。

### 语法 

```
nc/netcat(选项)(参数)
```

### 选项 

```
-g<网关>：设置路由器跃程通信网关，最多设置8个；
-G<指向器数目>：设置来源路由指向器，其数值为4的倍数；
-h：在线帮助；
-i<延迟秒数>：设置时间间隔，以便传送信息及扫描通信端口；
-l：使用监听模式，监控传入的资料；
-n：直接使用ip地址，而不通过域名服务器；
-o<输出文件>：指定文件名称，把往来传输的数据以16进制字码倾倒成该文件保存；
-p<通信端口>：设置本地主机使用的通信端口；
-r：指定源端口和目的端口都进行随机的选择；
-s<来源位址>：设置本地主机送出数据包的IP地址；
-u：使用UDP传输协议；
-v：显示指令执行过程；
-w<超时秒数>：设置等待连线的时间；
-z：使用0输入/输出模式，只在扫描通信端口时使用。
```

### 参数 

- 主机：指定主机的IP地址或主机名称；
- 端口号：可以是单个整数或者是一个范围。

### 实例 

**远程拷贝文件**

从server1拷贝文件到server2上。需要先在server2上，用nc激活监听。

server2上运行：

```
[root@localhost2 tmp]# nc -lp 1234 > install.log
```

server1上运行：

```
[root@localhost1 ~]# ll install.log
-rw-r–r–   1 root root 39693 12月 20   2007 install.log

[root@localhost1 ~]# nc -w 1 192.168.228.222 1234 < install.log
```

**克隆硬盘或分区**

操作与上面的拷贝是雷同的，只需要由[dd](http://man.linuxde.net/dd)获得硬盘或分区的数据，然后传输即可。克隆硬盘或分区的操作，不应在已经[mount](http://man.linuxde.net/mount)的的系统上进行。所以，需要使用安装光盘引导后，进入拯救模式（或使用Knoppix工 具光盘）启动系统后，在server2上进行类似的监听动作：

```
nc -l -p 1234 | dd of=/dev/sda
```

server1上执行传输，即可完成从server1克隆sda硬盘到server2的任务：

```
dd if=/dev/sda | nc 192.168.228.222 1234
```

完成上述工作的前提，是需要落实光盘的拯救模式支持服务器上的网卡，并正确配置IP。

**端口扫描**

```
nc -v -w 1 192.168.228.222 -z 1-1000
localhost2 [192.168.228.222] 22 (ssh) open
```

**保存Web页面**

```
while true; do
    nc -l -p 80 -q 1 < somepage.html;
done
```

**聊天**

nc还可以作为简单的字符下聊天工具使用，同样的，server2上需要启动监听：

```
[root@localhost2 tmp]# nc -lp 1234
```

server1上传输：

```
[root@localhost1 ~]# nc 192.168.228.222 1234
```

这样，双方就可以相互交流了。使用Ctrl+D正常退出。

**传输目录**

从server1拷贝nginx-0.6.34目录内容到server2上。需要先在server2上，用nc激活监听，server2上运行：

```
[root@localhost2 tmp]# nc -l 1234 | tar xzvf -
```

server1上运行：

```
[root@localhost1 ~]# ll -d nginx-0.6.34
drwxr-xr-x 8 1000 1000 4096 12-23 17:25 nginx-0.6.34

[root@localhost1 ~]# tar czvf – nginx-0.6.34 | nc 192.168.228.222 1234
```



# netcat的端口转发功能的实现

方法如下：
​    $ mknod backpipe p
​    建立一个命名管道.

​    listener-to-client 转发：
​    $ nc -l -p [localport] 0< backpipe | 
​        nc [target ip] [port] |
​        tee backpipe
​    漂亮吧？
​    继续：
​    listener-to-listener 转发：
​    $ nc -l -p [localport] 0< backpipe |
​        nc -l -p [localport2] |
​        tee backpipe
​    
​    client-to-client 转发：
​    $ nc [ip1] [port1] 0< backpipe |
​        nc [ip2] [port2] |
​        tee backpipe


​    还有更雷的方法，用自身的 -e 参数：

​    $ echo nc [ip] [port] > relay.sh

​    $ chmod +x relay.sh

​    $ nc -l -p [port2] -e relay.sh







##mknod建管道

`mknod backpipe p`

## tee读取

`tee backpipe`