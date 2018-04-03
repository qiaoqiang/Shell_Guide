[![Fedora Project Wiki](https://fedoraproject.org/w/skins/Fedora/resources/images/fedorawiki_logo.png)](https://fedoraproject.org/wiki/Fedora_Project_Wiki)

- ​

# Anaconda/Kickstart/zh-cn

## Contents

 [[hide](undefined)] 

- [1Chapter 1. 引言](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#Chapter_1._.E5.BC.95.E8.A8.80)[1.1什么是Kickstart安装?](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#.E4.BB.80.E4.B9.88.E6.98.AFKickstart.E5.AE.89.E8.A3.85.3F)
- [1.2如何使用kickstart进行系统安装?](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#.E5.A6.82.E4.BD.95.E4.BD.BF.E7.94.A8kickstart.E8.BF.9B.E8.A1.8C.E7.B3.BB.E7.BB.9F.E5.AE.89.E8.A3.85.3F)
- [1.3创建Kickstart文件](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#.E5.88.9B.E5.BB.BAKickstart.E6.96.87.E4.BB.B6)
- [1.4引用磁盘的特殊说明](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#.E5.BC.95.E7.94.A8.E7.A3.81.E7.9B.98.E7.9A.84.E7.89.B9.E6.AE.8A.E8.AF.B4.E6.98.8E)
- [2Chapter 2. Kickstart选项](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#Chapter_2._Kickstart.E9.80.89.E9.A1.B9)[2.1auth 或者 authconfig(必需)](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#auth_.E6.88.96.E8.80.85_authconfig.28.E5.BF.85.E9.9C.80.29)[2.2autopart](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#autopart)[2.3autostep](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#autostep)[2.4bootloader(必需)](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#bootloader.28.E5.BF.85.E9.9C.80.29)[2.5btrfs](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#btrfs)[2.6clearpart](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#clearpart)[2.7cmdline](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#cmdline)[2.8device](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#device)[2.9dmraid](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#dmraid)[2.10driverdisk](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#driverdisk)[2.11fcoe](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#fcoe)[2.12firewall](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#firewall)[2.13firstboot](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#firstboot)[2.14group](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#group)[2.15graphical](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#graphical)[2.16halt](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#halt)[2.17ignoredisk](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#ignoredisk)[2.18install](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#install)[2.18.1cdrom](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#cdrom)[2.18.2harddrive](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#harddrive)[2.18.3liveimg](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#liveimg)[2.18.4nfs](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#nfs)[2.18.5url](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#url)[2.19iscsi](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#iscsi)[2.20iscsiname](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#iscsiname)[2.21keyboard(必需)](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#keyboard.28.E5.BF.85.E9.9C.80.29)[2.22lang(需要)](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#lang.28.E9.9C.80.E8.A6.81.29)[2.23logvol](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#logvol)[2.24logging](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#logging)[2.25mediacheck](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#mediacheck)[2.26monitor](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#monitor)[2.27multipath](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#multipath)[2.28network](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#network)[2.29part or partition(必需)](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#part_or_partition.28.E5.BF.85.E9.9C.80.29)[2.30poweroff](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#poweroff)[2.31raid](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#raid)[2.32realm](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#realm)[2.33reboot](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#reboot)[2.34repo](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#repo)[2.35rescue](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#rescue)[2.36rootpw](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#rootpw)[2.37selinux](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#selinux)[2.38services](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#services)[2.39shutdown](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#shutdown)[2.40sshpw](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#sshpw)[2.41skipx](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#skipx)[2.42text](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#text)[2.43timezone](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#timezone)[2.44updates](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#updates)[2.45upgrade](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#upgrade)[2.46user](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#user)[2.47vnc](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#vnc)[2.48volgroup](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#volgroup)[2.49xconfig](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#xconfig)[2.50zerombr](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#zerombr)[2.51zfcp](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#zfcp)[2.52%include](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#.25include)[2.53%ksappend](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#.25ksappend)
- [3Chapter 3. 包的选择](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#Chapter_3._.E5.8C.85.E7.9A.84.E9.80.89.E6.8B.A9)
- [4Chapter 4. 预安装脚本](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#Chapter_4._.E9.A2.84.E5.AE.89.E8.A3.85.E8.84.9A.E6.9C.AC)[4.1Example](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#Example)
- [5Chapter 5. 后安装脚本](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#Chapter_5._.E5.90.8E.E5.AE.89.E8.A3.85.E8.84.9A.E6.9C.AC)[5.1Examples](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#Examples)
- [6Chapter 6. 让Kickstart文件可用](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#Chapter_6._.E8.AE.A9Kickstart.E6.96.87.E4.BB.B6.E5.8F.AF.E7.94.A8)[6.1Creating a Kickstart Boot Diskette](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#Creating_a_Kickstart_Boot_Diskette)[6.2Creating a Kickstart Boot CD-ROM](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#Creating_a_Kickstart_Boot_CD-ROM)[6.3Making the Kickstart File Available on the Network](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#Making_the_Kickstart_File_Available_on_the_Network)[6.3.1HTTP Headers](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#HTTP_Headers)
- [7Chapter 7. 让安装树可用](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#Chapter_7._.E8.AE.A9.E5.AE.89.E8.A3.85.E6.A0.91.E5.8F.AF.E7.94.A8)
- [8Chapter 8. 开始kickstart安装](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#Chapter_8._.E5.BC.80.E5.A7.8Bkickstart.E5.AE.89.E8.A3.85)[8.1Boot Diskette](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#Boot_Diskette)[8.2CD-ROM #1 and Diskette](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#CD-ROM_.231_and_Diskette)[8.3With Driver Disk](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#With_Driver_Disk)[8.4Boot CD-ROM](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#Boot_CD-ROM)[8.5Other kickstart options:](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#Other_kickstart_options:)[8.6Example Kickstart Script](https://fedoraproject.org/wiki/Anaconda/Kickstart/zh-cn#Example_Kickstart_Script)

# Chapter 1. 引言

## 什么是Kickstart安装?

许多系统管理员都希望能够使用自动化安装的方式来在他们的机器上安装Fedora或红帽企业版Linux。为了满足这样的需求，红帽公司创建了kickstart安装方式。通过使用kickstart，系统管理员能够创建一个单独的、包含安装过程中遇到的所有问题答案的文件。

kickstart文件能被存储在服务器系统之上，机器在安装系统的时候可以读取该文件。这种安装方式支持只用一个kickstart文件就可以在多台机器上安装Fedora和红帽企业版Linux的特性，这对于网络和系统管理员来说非常理想。

Fedora安装指南([http://docs.fedoraproject.org/en-US/index.html](http://docs.fedoraproject.org/en-US/index.html)) 中有关于kickstart的详细说明。

## 如何使用kickstart进行系统安装?

使用kickstart来安装系统可以通过本地CD-ROM、本地磁盘、或者通过NFS、FTP、HTTP来进行。

为了使用kickstart，你必须：

1. 创建一个kickstart文件
2. 创建一个带有kickstart文件的启动磁盘，或者让kickstart可以通过网络访问
3. 使能安装树
4. 开始kickstart安装

本章节详细地解释了这些步骤。

## 创建Kickstart文件

kickstart文件是一个简单的文本文件，它包含了一个项目列表，列表中的每一个项目都有一个关键字用来识别。你可以通过Kickstart Configurator程序来生成kickstart文件，也可以手动编辑。Fedora或者红帽企业版Linux安装程序已经根据你在安装过程中的选择创建了一个简单的kickstart文件。它就是/root/anaconda-ks.cfg。你应该可以使用能够识别ASCII编码的文本编辑器或文字处理软件来编辑它。

首先，在创建kickstart文件的时候应该注意以下问题：

- 有一条并不严格的要求，kickstart文件中各部分(section)要遵循一定的顺序。每个部分中的项(Item)并不需要按照一定的顺序排列，除非有其他要求。各部分的顺序如下：
  1. 命令部分 -- (参考第二章节)列出的kickstart选项(option)，必须包含要求的选项。
  2.  %packages部分 -- 详细内容参见第三章节。
  3.  %pre, %post, 以及%traceback部分 -- 这些部分的顺序可以任意排列，更详细的内容请参考第四和第五章节。
-  %packages, %pre, %post以及%traceback部分需要以%end结束。
- 不要求的项(Item)可以被省略。
- 省略任何一个被要求的项将会导致安装程序向用户询问相关的问题，就像典型安装过程向用户询问那样。一旦用户给出了答案，安装过程将会继续自动进行，除非又遇到缺失的项。
- 以(#)开头的行作为注释行被忽略。
- 如果在kickstart安装中使用了不推荐的命令、选项或者语法，警告日志将会被记录到anaconda日志中。因为在一个或者两个发行版之间这些不推荐的项经常会被删掉，所以检查安装日志以确保没有使用这些项非常必要。当使用ksvalidator的时候，这些不推荐的项会导致错误。

## 引用磁盘的特殊说明

传统上，Kickstart一直通过设备节点名(例如 `sda`)来引用磁盘。Linux内核采用了更加动态的方法，设备名并不会在重启时保持不变。因此，这会使得在Kickstart脚本中引用磁盘变得复杂。为了满足稳定的设备命名，你可以在项(Item)中使用`/dev/disk`代替设备名。例如，你可以使用：

```
part / --fstype=ext4 --onpart=/dev/disk/by-path/pci-0000:00:05.0-scsi-0:0:0:0-part1
part / --fstype=ext4 --onpart=/dev/disk/by-id/ata-ST3160815AS_6RA0C882-part1

```

来代替：

`part / --fstype=ext4 --onpart=sda1`

这种方式提供了对磁盘的持久引用，因而比仅仅使用`sda`更加有意义。 这在大的存储环境中特别有意义。

你也可以使用类似于shell的入口来应用磁盘。这种方式主要用来简化大的存储环境中`clearpart`以及`ignoredisk`命令的使用。例如，为了替代：

`ignoredisk --drives=sdaa,sdab,sdac`

你可以使用如下的入口：

`ignoredisk --drives=/dev/disk/by-path/pci-0000:00:05.0-scsi-*`

最后，如果想要在任何地方引用已经存在的分区或者文件系统（例如，在`part --ondisk=`中），你可以通过文件系统标签(label)或者UUID来进行。例如：

```
part /data --ondisk=LABEL=data
part /misc --ondisk=UUID=819ff6de-0bd6-4bf4-8b72-dbe41033a85b

```

# Chapter 2. Kickstart选项

如下的选项可以放到kickstart文件中。如果你喜欢图形化的接口，可以使用Kickstart Configurator程序。

[![Stop (medium size).png](https://fedoraproject.org/w/uploads/thumb/6/61/Stop_%28medium_size%29.png/35px-Stop_%28medium_size%29.png)](https://fedoraproject.org/wiki/File:Stop_(medium_size).png)

**如果选项后接等号(=)，等号后面必须指定选项的值。** 在示例命令中， **[方括号]**中的选项是可选的。****

[![Stop (medium size).png](https://fedoraproject.org/w/uploads/thumb/6/61/Stop_%28medium_size%29.png/35px-Stop_%28medium_size%29.png)](https://fedoraproject.org/wiki/File:Stop_(medium_size).png)

**pykickstart处理命令参数的方式和shell相似。** 如果一个参数列表(多个参数)传进来，这些参数必须以逗号隔开，并且不能有多余的空格。 如果参数列表需要多余的空格，那么整个参数列表就要用双引号括起来。如果引号、空格或者其他特殊字符需要被加入到参数列表，必须将它们进行转义。****

## auth 或者 authconfig(必需)

auth命令设置系统的授权选项。它只是authconfig程序的封装，因而所有被authconfig程序识别的选项都可以应用于auth命令。想要获取完整的列表，请参考authconfig手册页。

默认情况下，密码一般会被加密但并不会放在shadow文件中。

## autopart

自动创建分区--一个根分区(/)、一个swap分区，以及一个适合体系架构(architecture)的boot分区。如果磁盘驱动器足够大，也会创建/home分区。

[![Stop (medium size).png](https://fedoraproject.org/w/uploads/thumb/6/61/Stop_%28medium_size%29.png/35px-Stop_%28medium_size%29.png)](https://fedoraproject.org/wiki/File:Stop_(medium_size).png)

**autopart命令不能和part/partition, raid, volgroup 或者 logvol 命令存在与同一kickstart文件里。**

`--type=`


`--encrypted`


`--passphrase=`


`--escrowcert=`


`--backuppassphrase`


`--cipher`


## autostep

通常情况下，kickstart安装时跳过了不必要的屏幕显示。该选项可以让安装过程简单地显示每一步的屏幕。autostep多用于调试。

`--autoscreenshot`


## bootloader(必需)

该命令指明了引导程序(bootloader)如何被安装.

[![Important.png](https://fedoraproject.org/w/uploads/thumb/f/ff/Important.png/35px-Important.png)](https://fedoraproject.org/wiki/File:Important.png)

**BIOS引导分区**
从Fedora16开始，包含GPT/GUID的磁盘必须有一个bios引导分区，用来安装引导程序。该分区必须用kickstart选项`part biosboot --fstype=biosboot --size=1`创建。然而，如果一个磁盘已经有了bisoboot分区，就没有必要使用"part biosboot"了。

`--append=`




`--boot-drive=`


`--leavebootorder`


`--driveorder`




`--location=`


`--password=`


`--iscrypted=`


`--md5pass=`


`--timeout=`


`--default=`


`--extlinux`


## btrfs

(anaconda-17.3引入)

定义一个BTRFS卷或者子卷(subvolume)。该命令的形式如下：

定义卷：

`btrfs  --data= --metadata= --label= `

定义子卷：

`btrfs  --subvol --name= `

``(表示可以列出多个分区)列出了添加到BTRFS卷上的BTRFS标示符。对于子卷来说，<parent>应该是这些子卷对应的父卷的标示符。

``


`--data=`


`--metadata=`


`--label=`


`--noformat`


`--useexisting`


下面的例子展示了如何从分别位于三个磁盘上的三个分区创建一个BTRFS卷和子卷，子卷用于root和home。在示例中，主卷并没有挂载和直接使用--仅使用了root和home子卷。

```
part btrfs.01 --size=6000 --ondisk=sda
part btrfs.02 --size=6000 --ondisk=sdb
part btrfs.03 --size=6000 --ondisk=sdc

btrfs none --data=0 --metadata=1 --label=f17 btrfs.01 btrfs.02 btrfs.03
btrfs / --subvol --name=root LABEL=f17
btrfs /home --subvol --name=home f17

```

## clearpart

从系统中删除分区，先于新分区的创建。默认不删除任何分区。

[![Stop (medium size).png](https://fedoraproject.org/w/uploads/thumb/6/61/Stop_%28medium_size%29.png/35px-Stop_%28medium_size%29.png)](https://fedoraproject.org/wiki/File:Stop_(medium_size).png)

**如果使用了clearpart，--onpart命令不能用于该逻辑分区**

`--all`


`--drives=`




`--list=`




`--initlabel`


`--linux`


`--none` (default)


## cmdline

以完全非交互的命令行模式安装。任何导致交互的动作都会使安装过程停止。这种模式对于带有x3270控制台的S/390系统非常有用。

## device

在大多数PCI系统上，安装程序会正确地自动探测以太网和SCSI卡。然而，在旧系统和一些PCI系统上，kickstart需要一个提示来寻找正确的设备。device命令告诉安装程序以如下的形式安装额外的模块：

`device  --opts=`

``


`--opts=`




## dmraid

`dmraid --name= --dev=`

## driverdisk

kickstart安装过程可以使用磁盘(Driver diskettes)。你需要把磁盘的内容拷贝到系统硬盘上一个分区的根目录。然后使用driverdisk命令告诉安装程序哪里可以找到磁盘内容。

`driverdisk |--source=|--biospart=`

``


`--source=`


`--biospart=`


## fcoe

## firewall

该选项对应安装程序中的防火墙配置界面：

`firewall --enabled|--disabled  [options]`

`--enabled` or `--enable`


`--disabled` or `--disable`


`--trust=`


``










`--port=`




`--service=`




## firstboot

决定是否在第一次启动系统后运行设置代理程序(Setup Agent)。如果使能，firstboot包必须被安装。如果没有使能，firstboot缺省是禁用的。

`--enable` or `--enabled`


`--disable` or `--disabled`


`--reconfig`


## group

在系统上创建一个新的用户组。如果指定的组名或者GID已经存在，则该命令失效。除此之外，`user`命令会为新创建的用户创建新的用户组。

`group --name= [--gid=]`

`--name=`


`--gid=`


## graphical

以图形模式完成kickstart安装。这是默认的。

## halt

在安装的最后，显示提示消息并等待用户按键来重启系统。这是默认的操作。

## ignoredisk

控制anaconda对系统磁盘的访问。下面的两个选项中可能只有一个被用到。

`ignoredisk --drives=[disk1,disk2,...]`


`ignoredisk --only-use=[disk1,disk2,...]`


`ignoredisk --interactive`


## install

告诉系统是安装一个全新的系统而不是升级存在的系统（默认）。安装时，你可以从cdrom、硬盘驱动器、nfs、或者url(ftp,http安装)中指定安装类型。install命令和安装方法必须在不同的行设置。

[![Important.png](https://fedoraproject.org/w/uploads/thumb/f/ff/Important.png/35px-Important.png)](https://fedoraproject.org/wiki/File:Important.png)

**注意：从F18起，anaconda不再支持升级。升级必须由FedUp(Fedora升级工具)来完成。**

### cdrom

`cdrom`


### harddrive

`harddrive [--biospart= | --partition=] [--dir=]`
















### liveimg

`liveimg --url= [--proxy=] [--checksum=] [--noverifyssl]`


















### nfs

`nfs --server= --dir= [--opts=]`


















### url

`url --url=|--mirrorlist= [--proxy=] [--noverifyssl]`


















## iscsi

指定在安装时附加的iSCSI存储。如果要使用iscsi参数，你必须通过iscsiname参数指定iSCSI节点的名字。iscsiname参数在kickstart文件中的位置必须在iscsi参数前面。

`iscsi --ipaddr= [options]`

无论在哪里使用，我们都推荐在系统BIOS或者固件(Intel系统的iBFT)中配置iSCSI存储，而不是使用iscsi参数。*Anaconda*会自动探测和使用BIOS或者固件中的磁盘配置，不需要在kickstart文件中另外配置。

如果你必须使用iscsi参数，请确保在安装开始时网络是激活的，以及iscsi参数在kickstart文件中的位置应该在引用iscsi磁盘的参数(如clearpart或ignoredisk)之前。

`--ipaddr=` (mandatory)


`--port=`


`--target=`


`--iface=`


`--user=`


`--password=`


`--reverse-user=`


`--reverse-password=`


## iscsiname

给电脑分配一个发起端名字。如果你在kickstart文件中使用了iscsi参数，该参数是强制的，而且要在iscsi参数之前出现。

`iscsiname `

## keyboard(必需)

设置系统键盘类型。可以参考`--vckeymap`选项的文档以及该节后面的建议来获得此命令能够接受的值。

[![Important.png](https://fedoraproject.org/w/uploads/thumb/f/ff/Important.png/35px-Important.png)](https://fedoraproject.org/wiki/File:Important.png)

**从Fedora18开始，keyboard命令有三个新的选项:**

`keyboard [--vckeymap=] [--xlayouts=,,...,] [--switch=...] [arg]`






`--vckeymap=`


`--xlayouts=,,...,`


`--switch=,...,`


[![Idea.png](https://fedoraproject.org/w/uploads/thumb/a/a4/Idea.png/35px-Idea.png)](https://fedoraproject.org/wiki/File:Idea.png)

如果只知道版式的说明(如Czech (qwerty))，你可以使用http://vpodzime.fedorapeople.org/layouts_list.py 来列出所有可用的版式，然后找到你想要的一种。方括号中的字符串有效的版式规格，因为Anaconda接受它。切换选项可以用同样的方法([http://vpodzime.fedorapeople.org/switching_list.py](http://vpodzime.fedorapeople.org/switching_list.py)) (两个脚本都需要安装版本为>= 5.1-1的libxklavier)

## lang(需要)

`lang `

设置安装时的语言，以及所安装系统的默认语言为``。可以设置所有可以被环境变量$LANG识别的值，尽管安装过程中并不是识别所有的语言。

某些语言(主要是中文、日语、韩语以及印度语)在文本模式安装时并不支持。如果这些语言中的一种被lang命令指定，安装将会继续使用英语，尽管安装后的系统会默认使用指定的语言。

/usr/share/system-config-language/locale-list文件(system-config-language软件包中的文件)每一行的第一列提供了一个有效语言码的列表。

## logvol

为逻辑卷管理(LVM)创建创建一个逻辑卷。

`logvol  --vgname= --size= --name= `

`--noformat`


`--useexisting`


`--fstype=`


`--fsoptions=`


`--grow`


`--maxsize=`


`--recommended`


`--percent`


`--encrypted`


`--passphrase=`


`--escrowcert=`


`--backuppassphrase`


`--thinpool`


`--metadatasize=`


`--chunksize=`


`--thin`


`--poolname=`


首先创建分区，创建逻辑卷组，然后创建逻辑卷。例如：

```
part pv.01 --size 3000
volgroup myvg pv.01
logvol / --vgname=myvg --size=2000 --name=rootvol

```

## logging

该命令控制anaconda安装过程中的错误日志，并不影响安装系统。

`--host=`


`--port=`


`--level=`




## mediacheck

如果指定，将会强制anaconda在安装介质上运行mediacheck。该命令需要安装过程被干预，所以默认是禁用的。

## monitor

如果指定了monitor命令，anaconda将会使用X来自动探测监视器设置。请在手动配置监视器之前先试一试该命令。

`--hsync=`


`--monitor=`


`--noprobe`


`--vsync=`


## multipath

`multipath --name= --device= --rule=`

## network

配置目标系统的网络信息，在安装环境中激活网络设备。如果需要网络，如从网络安装的情形或者使用到了VNC，第一个network命令的设备会被激活。设备的激活也可以明确地使用`--activate`选项。如果设备在获取kickstart文件的时候已经被激活(例如，使用boot选项的配置或者进入装载器UI)，它会根据kickstart文件的配置重新激活。

在F15上，第一个network命令的设备即使在非网络安装的情形下也会被激活，而且不会根据kickstart文件的配置重新激活设备。

kickstart文件中配置的其它的设备能够在安装器上使用`--activate`激活(自F16起)。

`--bootproto=[dhcp|bootp|static|ibft]`






```
network --bootproto=static --ip=10.0.2.15 \
--netmask=255.255.255.0 --gateway=10.0.2.254 \
--nameserver=10.0.2.1

```






`--device=`






`--ip=`


`--ipv6=`


`--gateway=`


`--nodefroute`


`--nameserver=`


`--nodns`


`--netmask=`


`--hostname=`


`--ethtool=`


`--essid=`


`--wepkey=`


`--wpakey=`


`--onboot=`


`--dhcpclass=`


`--mtu=`


`--noipv4`


`--noipv6`


`--bondslaves`


`--bondopts`


`--vlanid`


`--teamslaves`


`--teamconfig`


```
network --device team0 --activate --bootproto static --ip=10.34.102.222 --netmask=255.255.255.0 --gateway=10.34.102.254 --nameserver=10.34.39.2  \
--teamslaves="p3p1'{\"prio\": -10, \"sticky\": true}',p3p2'{\"prio\": 100}'" \
--teamconfig="{\"runner\": {\"name\": \"activebackup\"}}"

```

## part or partition(必需)

在系统上创建一个分区。

[![Stop (medium size).png](https://fedoraproject.org/w/uploads/thumb/6/61/Stop_%28medium_size%29.png/35px-Stop_%28medium_size%29.png)](https://fedoraproject.org/wiki/File:Stop_(medium_size).png)

**创建的所有分区在安装过程中都会被格式化，除非使用了--noformat和--onpart **

`part `

``是分区将要被挂载的地方，必须是以下格式中的一种：


















`--size=`


`--grow`


`--maxsize=`


`--noformat`


`--onpart=` or `--usepart=`


[![Stop (medium size).png](https://fedoraproject.org/w/uploads/thumb/6/61/Stop_%28medium_size%29.png/35px-Stop_%28medium_size%29.png)](https://fedoraproject.org/wiki/File:Stop_(medium_size).png)

**Anaconda也许会以特殊的顺序创建分区，所以使用标签比只用分区名要安全些**

`--ondisk=` or `--ondrive=`


`--asprimary`


`--fsprofile=`


`--fstype=`


`--fsoptions=`


`--label=`


`--recommended`


`--onbiosdisk=`


`--encrypted`


`--passphrase=`


`--escrowcert=`


`--backuppassphrase`


[![Stop (medium size).png](https://fedoraproject.org/w/uploads/thumb/6/61/Stop_%28medium_size%29.png/35px-Stop_%28medium_size%29.png)](https://fedoraproject.org/wiki/File:Stop_(medium_size).png)

**如果分区失败，诊断信息将会被输出到虚拟终端3.**

## poweroff

安装完成后关闭机器。通常，kickstart在重起之前会显示一条消息并等待用户键入任意字符。

## raid

装配一个软件RAID设备，命令形式如下：

`raid  --level= --device= `

``


`--level=`


`--device=`


`--spares=`


`--fstype=`


`--fsoptions=`


`--label=`


`--noformat`


`--useexisting`


`--encrypted`


`--passphrase=`


`--escrowcert=`


`--backuppassphrase`


下面的例子展示了如何为/创建一个RAID1的分区，以及如何为/usr创建一个RAID5的分区(假定系统上有3个磁盘)。也创建了3个swap分区，每个驱动器一个。

```
part raid.01 --size=6000 --ondisk=sda
part raid.02 --size=6000 --ondisk=sdb
part raid.03 --size=6000 --ondisk=sdc

part swap1 --size=512 --ondisk=sda
part swap2 --size=512 --ondisk=sdb
part swap3 --size=512 --ondisk=sdc

part raid.11 --size=6000 --ondisk=sda
part raid.12 --size=6000 --ondisk=sdb
part raid.13 --size=6000 --ondisk=sdc

raid / --level=1 --device=md0 raid.01 raid.02 raid.03
raid /usr --level=5 --device=md1 raid.11 raid.12 raid.13

```

## realm

连接FreeIPA域的一个活动目录。

`realm join `

`--computer-ou=`


`--no-password`


`--one-time-password=`


`--client-software=`


`--server-software=`


`--membership-software=`


```
realm join --one-time-password=12345 DC.EXAMPLE.COM

```

## reboot

安装完成后重启。通常情况下，kickstart显示消息并在重启之前等待用户按键。

`--eject`


## repo

Configures additional yum repositories that may be used as sources for package installation. Multiple repo lines may be specified. By default, anaconda has a configured set of repos taken from /etc/anaconda.repos.d plus a special Installation Repo in the case of a media install. The exact set of repos in this directory changes from release to release and cannot be listed here. There will likely always be a repo named "updates".

Note: If you want to enable one of the repos in /etc/anaconda.repos.d that is disabled by default (like "updates"), you should use --name=<repoid> but none of the other options. anaconda will look for a repo by this name automatically. Providing a baseurl or mirrorlist URL will result in anaconda attempting to add another repo by the same name, which will cause a conflicting repo error.

`repo --name= [--baseurl=|--mirrorlist=] [options]`

`--name=`


`--baseurl=`


`--mirrorlist=`


`--cost=`


`--excludepkgs=`


`--includepkgs=`


`--proxy=[protocol://][username[:password]@]host[:port]`


`--ignoregroups=true`


`--noverifyssl`


## rescue

Automatically enter the installer's rescue mode. This gives you a chance to repair the system should something catastrophic happen.

`rescue [--nomount|--romount]`

`--nomount|--romount]`


## rootpw

This required command sets the system's root password to the `` argument.

`rootpw [options] `

`--iscrypted|--plaintext`


`--lock`


## selinux

Sets the state of SELinux on the installed system. SELinux defaults to enforcing in anaconda.

`selinux [--disabled|--enforcing|--permissive]`

`--disabled`


`--enforcing`


`--permissive`


## services

Modifies the default set of services that will run under the default runlevel. The services listed in the disabled list will be disabled before the services listed in the enabled list are enabled.

`services [--disabled=] [--enabled=]`

`--disabled=`


`--enabled=`


## shutdown

At the end of installation, shut down the machine. This is the same as the poweroff command. Normally, kickstart displays a message and waits for the user to press a key before rebooting.

## sshpw

The installer can start up ssh to provide for interactivity and inspection, just like it can with telnet. The "inst.sshd" option must be specified on the kernel command-line for Anaconda to start an ssh daemon. The sshpw command is used to control the accounts created in the installation environment that may be remotely logged into. For each instance of this command given, a user will be created. These users will not be created on the final system - they only exist for use while the installer is running.

Note that by default, root has a blank password. If you don't want any user to be able to ssh in and have full access to your hardware, you must specify sshpw for username root. Also note that if Anaconda fails to parse the kickstart file, it will allow anyone to login as root and have full access to your hardware.

`sshpw --username=  [--iscrypted|--plaintext] [--lock]`

`--username=`


`--iscrypted|--plaintext`


`--lock`


## skipx

If present, X is not configured on the installed system.

## text

Perform the kickstart installation in text mode. Kickstart installations are performed in graphical mode by default.

## timezone

This required command sets the system time zone to <timezone> which may be any of the time zones listed by timeconfig.

`timezone [--utc] `

`--utc`


[![Idea.png](https://fedoraproject.org/w/uploads/thumb/a/a4/Idea.png/35px-Idea.png)](https://fedoraproject.org/wiki/File:Idea.png)

To get the list of supported timezones, you can either run this script: [http://vpodzime.fedorapeople.org/timezones_list.py](http://vpodzime.fedorapeople.org/timezones_list.py) or look at this list:[http://vpodzime.fedorapeople.org/timezones_list.txt](http://vpodzime.fedorapeople.org/timezones_list.txt)

[![Important.png](https://fedoraproject.org/w/uploads/thumb/f/ff/Important.png/35px-Important.png)](https://fedoraproject.org/wiki/File:Important.png)

**Starting with Fedora 18 the timezone command has two new options:**

`timezone [--utc] [--nontp] [--ntpservers=,,...,] `

`--nontp`


`--ntpservers=,,...,`




## updates

Specify the location of an updates.img for use in installation. See anaconda-release-notes.txt for a description of how to make an updates.img.

`updates [URL]`




## upgrade

[![Important.png](https://fedoraproject.org/w/uploads/thumb/f/ff/Important.png/35px-Important.png)](https://fedoraproject.org/wiki/File:Important.png)

**Note that from F18 onward, upgrades are no longer supported in anaconda and should be done with FedUp, the Fedora update tool.**

Tells the system to upgrade an existing system rather than install a fresh system. You must specify one of cdrom, harddrive, nfs, or url (for ftp and http) as the location of the installation tree. Refer to install for details.

`--root-device=` (optional)


## user

Creates a new user on the system.

`user --name= [--gecos=] [--groups=] [--homedir=] [--password=] [--iscrypted|--plaintext] [--lock] [--shell=] [--uid=]`

`--name=`


`--gecos=`


`--groups=`


`--homedir=`


`--lock`


`--password=`


`--iscrypted|--plaintext`


`--shell=`


`--uid=`


## vnc

Allows the graphical installation to be viewed remotely via VNC. This method is usually preferred over text mode, as there are some size and language limitations in text installs. With no options, this command will start a VNC server on the machine with no password and will print out the command that needs to be run to connect a remote machine.

`vnc [--host=] [--port=] [--password=]`

`--host=`


`--port=`


`--password=`


## volgroup

Use to create a Logical Volume Management (LVM) group.

`volgroup   `

``


`--noformat`


`--useexisting`


`--pesize=`


`--reserved-space=`


`--reserved-percent=`


Create the partition first, create the logical volume group, and then create the logical volume. For example:

```
part pv.01 --size 3000
volgroup myvg pv.01
logvol / --vgname=myvg --size=2000 --name=rootvol

```

## xconfig

Configures the X Window System. If this option is not given, anaconda will use X to attempt to automatically configure. Please try this before manually configuring your system.

`--defaultdesktop=`


`--startxonboot`


## zerombr

If zerombr is specified, any disks whose formatting is unrecognized are initialized. This will destroy all of the contents of disks with invalid partition tables or other formatting unrecognizable to the installer. It is useful so that the installation program does not ask if it should initialize the disk label if installing to a brand new hard drive.

## zfcp

`--devnum=`

`--fcplun=`

`--wwpn=`

## %include

Use the `%include /path/to/file` or `%include ` command to include the contents of another file in the kickstart file as though the contents were at the location of the %include command in the kickstart file.

## %ksappend

The `%ksappend url` directive is very similar to `%include` in that it is used to include the contents of additional files as though they were at the location of the`%ksappend` directive. The difference is in when the two directives are processed. `%ksappend` is processed in an initial pass, before any other part of the kickstart file. Then, this expanded kickstart file is passed to the rest of anaconda where all `%pre` scripts are handled, and then finally the rest of the kickstart file is processed in order, which includes `%include` directives.

Thus, `%ksappend` provides a way to include a file containing `%pre` scripts, while `%include` does not.

# Chapter 3. 包的选择

Use the %packages command to begin a kickstart file section that lists the packages you would like to install.

Packages can be specified by group or by individual package name. The installation program defines several groups that contain related packages. Refer to the repodata/*comps.xml file on the first CD-ROM for a list of groups. Each group has an id, user visibility value, name, description, and package list. In the package list, the packages marked as mandatory are always installed if the group is selected, the packages marked default are selected by default if the group is selected, and the packages marked optional must be specifically selected even if the group is selected to be installed.

In most cases, it is only necessary to list the desired groups and not individual packages. Note that the Core group is always selected by default, so it is not necessary to specify it in the %packages section.

The %packages section is required to be closed with %end. Also, multiple %packages sections may be given. This may be handy if the kickstart file is used as a template and pulls in various other files with the %include mechanism.

Here is an example %packages selection:

```
%packages
@X Window System
@GNOME Desktop Environment
@Graphical Internet
@Sound and Video
dhcp
%end

```

As you can see, groups are specified, one to a line, starting with an @ symbol followed by the full group name as given in the comps.xml file. Groups can also be specified using the id for the group, such as gnome-desktop. Specify individual packages with no additional characters (the dhcp line in the example above is an individual package).

You can also specify environments using the @^ prefix followed by full environment name as given in the comps.xml file. If multiple environments are specified, only the last one specified will be used. Environments can be mixed with both group specifications (even if the given group is not part of the specified environment) and package specifications.

Here is an example of requesting the GNOME Desktop environment to be selected for installation:

```
%packages
@^gnome-desktop-environment
%end

```

Additionally, individual packages may be specified using globs. For instance:

```
%packages
vim*
kde-i18n-*
%end

```

This would install all packages whose names start with "vim" or "kde-i18n-".

You can also specify which packages or groups not to install from the default package list:

```
%packages
-autofs
-@Sound and Video
%end

```

The following options are available for the %packages option:


























In addition, group lines in the %packages section can take options as well:








# Chapter 4. 预安装脚本

You can add commands to run on the system immediately after the ks.cfg has been parsed and the lang, keyboard, and url options have been processed. This section must be at the end of the kickstart file (after the commands) and must start with the %pre command. You can access the network in the %pre section; however, name service has not been configured at this point, so only IP addresses will work.

Preinstallation scripts are required to be closed with %end.

[![Stop (medium size).png](https://fedoraproject.org/w/uploads/thumb/6/61/Stop_%28medium_size%29.png/35px-Stop_%28medium_size%29.png)](https://fedoraproject.org/wiki/File:Stop_(medium_size).png)

**If your script spawns a daemon process, you must make sure to close stdout and stderr.** Doing so is standard procedure for creating daemons. If you do not close these file descriptors, the installation will appear hung as anaconda waits for an EOF from the script.****

[![Stop (medium size).png](https://fedoraproject.org/w/uploads/thumb/6/61/Stop_%28medium_size%29.png/35px-Stop_%28medium_size%29.png)](https://fedoraproject.org/wiki/File:Stop_(medium_size).png)

**Note that the pre-install script is not run in the chroot environment.**












## Example

Here is an example %pre section:

```
%pre
#!/bin/bash
hds=""
mymedia=""

for file in /sys/block/sd*; do
hds="$hds $(basename $file)"
done

set $hds
numhd=$(echo $#)

drive1=$(echo $hds | cut -d' ' -f1)
drive2=$(echo $hds | cut -d' ' -f2)


if [ $numhd == "2" ]  ; then
echo "#partitioning scheme generated in %pre for 2 drives" > /tmp/part-include
echo "clearpart --all" >> /tmp/part-include
echo "part /boot --fstype ext4 --size 512 --ondisk sda" >> /tmp/part-include
echo "part / --fstype ext4 --size 10000 --grow --ondisk sda" >> /tmp/part-include
echo "part swap --recommended --ondisk $drive1" >> /tmp/part-include
echo "part /home --fstype ext4 --size 10000 --grow --ondisk sdb" >> /tmp/part-include
else
echo "#partitioning scheme generated in %pre for 1 drive" > /tmp/part-include
echo "clearpart --all" >> /tmp/part-include
echo "part /boot --fstype ext4 --size 521" >> /tmp/part-include
echo "part swap --recommended" >> /tmp/part-include
echo "part / --fstype ext4 --size 2048" >> /tmp/part-include
echo "part /home --fstype ext4 --size 2048 --grow" >> /tmp/part-include
fi
%end

```

This script determines the number of hard drives in the system and writes a text file with a different partitioning scheme depending on whether it has one or two drives. Instead of having a set of partitioning commands in the kickstart file, include the line:

`%include /tmp/part-include`

The partitioning commands selected in the script will be used.

# Chapter 5. 后安装脚本

You have the option of adding commands to run on the system once the installation is complete. This section must be at the end of the kickstart file and must start with the %post command. This section is useful for functions such as installing additional software and configuring an additional nameserver.

You may have more than one %post section, which can be useful for cases where some post-installation scripts need to be run in the chroot and others that need access outside the chroot.

Each %post section is required to be closed with a corresponding %end.

[![Stop (medium size).png](https://fedoraproject.org/w/uploads/thumb/6/61/Stop_%28medium_size%29.png/35px-Stop_%28medium_size%29.png)](https://fedoraproject.org/wiki/File:Stop_(medium_size).png)

**If you configured the network with static IP information, including a nameserver, you can access the network and resolve IP addresses in the %post section.** If you configured the network for DHCP, the /etc/resolv.conf file has not been completed when the installation executes the %post section. You can access the network, but you can not resolve IP addresses. Thus, if you are using DHCP, you must specify IP addresses in the %post section.****

[![Stop (medium size).png](https://fedoraproject.org/w/uploads/thumb/6/61/Stop_%28medium_size%29.png/35px-Stop_%28medium_size%29.png)](https://fedoraproject.org/wiki/File:Stop_(medium_size).png)

**If your script spawns a daemon process, you must make sure to close stdout and stderr.** Doing so is standard procedure for creating daemons. If you do not close these file descriptors, the installation will appear hung as anaconda waits for an EOF from the script.****

[![Stop (medium size).png](https://fedoraproject.org/w/uploads/thumb/6/61/Stop_%28medium_size%29.png/35px-Stop_%28medium_size%29.png)](https://fedoraproject.org/wiki/File:Stop_(medium_size).png)

**The post-install script is run in a chroot environment; therefore, performing tasks such as copying scripts or RPMs from the installation media will not work.**
















## Examples

Run a script named runme from an NFS share:

```
%post
mkdir /mnt/temp
mount 10.10.0.2:/usr/new-machines /mnt/temp
open -s -w -- /mnt/temp/runme
umount /mnt/temp
%end

```

Copy the file /etc/resolv.conf to the file system that was just installed:

```
%post --nochroot
cp /etc/resolv.conf /mnt/sysimage/etc/resolv.conf
%end

```

[![Stop (medium size).png](https://fedoraproject.org/w/uploads/thumb/6/61/Stop_%28medium_size%29.png/35px-Stop_%28medium_size%29.png)](https://fedoraproject.org/wiki/File:Stop_(medium_size).png)

**If your kickstart is being interpreted by the livecd-creator tool, you should replace /mnt/sysimage above with $INSTALL_ROOT.**

# Chapter 6. 让Kickstart文件可用

A kickstart file must be placed in one of the following locations:

- On a boot diskette


- On a boot CD-ROM


- On a network

Normally a kickstart file is copied to the boot diskette, or made available on the network. The network-based approach is most commonly used, as most kickstart installations tend to be performed on networked computers.

Let us take a more in-depth look at where the kickstart file may be placed.

## Creating a Kickstart Boot Diskette

To perform a diskette-based kickstart installation, the kickstart file must be named ks.cfg and must be located in the boot diskette's top-level directory. Refer to the section Making an Installation Boot Diskette in the Red Hat Enterprise Linux Installation Guide for instruction on creating a boot diskette. Because the boot diskettes are in MS-DOS format, it is easy to copy the kickstart file under Linux using the mcopy command:

`mcopy ks.cfg a:`

Alternatively, you can use Windows to copy the file. You can also mount the MS-DOS boot diskette in Linux with the file system type vfat and use the cp command to copy the file on the diskette.

## Creating a Kickstart Boot CD-ROM

To perform a CD-ROM-based kickstart installation, the kickstart file must be named ks.cfg and must be located in the boot CD-ROM's top-level directory. Since a CD-ROM is read-only, the file must be added to the directory used to create the image that is written to the CD-ROM. Refer to the Making an Installation Boot CD-ROM section in the Red Hat Enterprise Linux Installation Guide for instruction on creating a boot CD-ROM; however, before making the file.iso image file, copy the ks.cfg kickstart file to the isolinux/ directory.

## Making the Kickstart File Available on the Network

Network installations using kickstart are quite common, because system administrators can easily automate the installation on many networked computers quickly and painlessly. In general, the approach most commonly used is for the administrator to have both a BOOTP/DHCP server and an NFS server on the local network. The BOOTP/DHCP server is used to give the client system its networking information, while the actual files used during the installation are served by the NFS server. Often, these two servers run on the same physical machine, but they are not required to.

To perform a network-based kickstart installation, you must have a BOOTP/DHCP server on your network, and it must include configuration information for the machine on which you are attempting to install Fedora or Red Hat Enterprise Linux. The BOOTP/DHCP server will provide the client with its networking information as well as the location of the kickstart file.

If a kickstart file is specified by the BOOTP/DHCP server, the client system will attempt an NFS mount of the file's path, and will copy the specified file to the client, using it as the kickstart file. The exact settings required vary depending on the BOOTP/DHCP server you use.

Here is an example of a line from the dhcpd.conf file for the DHCP server:

```
filename "/usr/new-machine/kickstart/";
server-name "blarg.redhat.com";

```

Note that you should replace the value after filename with the name of the kickstart file (or the directory in which the kickstart file resides) and the value after server-name with the NFS server name.

If the filename returned by the BOOTP/DHCP server ends with a slash ("/"), then it is interpreted as a path only. In this case, the client system mounts that path using NFS, and searches for a particular file. The filename the client searches for is:

`-kickstart`

The <ip-addr> section of the filename should be replaced with the client's IP address in dotted decimal notation. For example, the filename for a computer with an IP address of 10.10.0.1 would be 10.10.0.1-kickstart.

Note that if you do not specify a server name, then the client system will attempt to use the server that answered the BOOTP/DHCP request as its NFS server. If you do not specify a path or filename, the client system will try to mount /kickstart from the BOOTP/DHCP server and will try to find the kickstart file using the same <ip-addr>-kickstart filename as described above.

### HTTP Headers

When Anaconda requests the kickstart over the network it includes several custom HTTP headers:

`X-Anaconda-Architecture: x86_64` indicates the architecture of the system being installed to.

`X-Anaconda-System-Release: Fedora` indicates the product name being installed.

There are also 2 optional headers, controlled by the kernel command line options [kssendmac](https://fedoraproject.org/wiki/Anaconda/Options#kssendmac) and [kssendsn](https://fedoraproject.org/wiki/Anaconda/Options#kssendsn)

# Chapter 7. 让安装树可用

The kickstart installation needs to access an installation tree. An installation tree is a copy of the binary Fedora or Red Hat Enterprise Linux CD-ROMs with the same directory structure.

If you are performing a CD-based installation, insert the Fedora or Red Hat Enterprise Linux CD-ROM #1 into the computer before starting the kickstart installation.

If you are performing a hard-drive installation, make sure the ISO images of the binary Fedora or Red Hat Enterprise Linux CD-ROMs are on a hard drive in the computer.

If you are performing a network-based (NFS, FTP, or HTTP) installation, you must make the installation tree available over the network. Refer to the Preparing for a Network Installation section of the Red Hat Enterprise Linux Installation Guide for details.

# Chapter 8. 开始kickstart安装

To begin a kickstart installation, you must boot the system from a Fedora or Red Hat Enterprise Linux boot diskette, Fedora or Red Hat Enterprise Linux boot CD-ROM, or the Fedora or Red Hat Enterprise Linux CD-ROM #1 and enter a special boot command at the boot prompt. In order to get to the boot prompt you must hit escape at the CD or DVD boot menu. In case you don't know what I'm talking about I took a screenshot. The installation program looks for a kickstart file if the ks command line argument is passed to the kernel.

[https://fedoraproject.org/wiki/File:Fedora_boot_screen.png](https://fedoraproject.org/wiki/File:Fedora_boot_screen.png)

## Boot Diskette

If the kickstart file is located on a boot diskette as described in the Section called Creating a Kickstart Boot Diskette in Chapter 6, boot the system with the diskette in the drive, and enter the following command at the boot: prompt:

`linux ks=floppy`

## CD-ROM #1 and Diskette

The linux ks=floppy command also works if the ks.cfg file is located on a vfat or ext2 file system on a diskette and you boot from the Fedora or Red Hat Enterprise Linux CD-ROM #1.

An alternate boot command is to boot off the Fedora or Red Hat Enterprise Linux CD-ROM #1 and have the kickstart file on a vfat or ext2 file system on a diskette. To do so, enter the following command at the boot: prompt:

`linux ks=hd:fd0:/ks.cfg`

## With Driver Disk

If you need to use a driver disk with kickstart, specify the dd option as well. For example, to boot off a boot diskette and use a driver disk, enter the following command at the boot: prompt:

`linux ks=floppy dd`

## Boot CD-ROM

If the kickstart file is on a boot CD-ROM as described in the Section called Creating a Kickstart Boot CD-ROM in Chapter 6, insert the CD-ROM into the system, boot the system, and enter the following command at the boot: prompt (where ks.cfg is the name of the kickstart file):

`linux ks=cdrom::/ks.cfg`

## Other kickstart options:

`ks=nfs::/`


`ks=http:///`


`ks=floppy`


`ks=floppy:/`


`ks=hd::/`


`ks=bd::/`


`ks=file:/`


`ks=cdrom:/` or in newer versions `ks=cdrom::/`


`ks`








`ksdevice=`


## Example Kickstart Script

Since I got tons of errors I thought I would share an example of a kickstart script that works. This also has an example of an lvm setup. I couldn't find a good example of an lvm anywhere else. I also added comments where I thought would help. Please modify if you think you have some other good examples.

```
# Kickstart file automatically generated by anaconda.

#version=DEVEL
#url --url http://mirrors.kernel.org/fedora/releases/7/Fedora/i386/os
#ks=http://127.0.0.1/ks.cfg
#ks=http://localhost/ks.cfg
url --url http://ftp.usf.edu/pub/fedora/linux/releases/14/Fedora/i386/os
install
cdrom
lang en_US.UTF-8
keyboard us
network --onboot yes --device eth0 --bootproto dhcp --noipv6
timezone --utc America/New_York
rootpw  --iscrypted $6$s9i1bQbmW4oSWMJc$0oHfSz0b/d90EvHx7cy70RJGIHrP1awzAgL9A3x2tbkyh72P3kN41vssaI3/SJf4Y4qSo6zxc2gZ3srzc4ACX1
selinux --permissive
authconfig --enableshadow --passalgo=sha512 --enablefingerprint
firewall --service=ssh
# The following is the partition information you requested
# Note that any partitions you deleted are not expressed
# here so unless you clear all partitions first, this is
# not guaranteed to work

#I am deleting the old partitions with this
clearpart --all --drives=sda

#I am creating partitions here
#I will create the lvm stuff farther down
part /boot --fstype=ext4 --size=500 --ondisk=sda --asprimary
part pv.5xwrsR-ldgG-FEmM-2Zu5-Jn3O-sx9T-unQUOe --grow --size=500 --ondisk=sda --asprimary

#Very important to have the two part lines before the lvm stuff
volgroup VG --pesize=32768 pv.5xwrsR-ldgG-FEmM-2Zu5-Jn3O-sx9T-unQUOe
logvol / --fstype=ext4 --name=lv_root --vgname=VG --size=40960
logvol /home --fstype=ext4 --name=lv_home --vgname=VG --size=25600
logvol swap --fstype swap --name=lv_swap --vgname=VG --size=4096

bootloader --location=mbr --driveorder=sda --append="rhgb quiet"

%packages
@admin-tools
#@editors
#@fonts
@gnome-desktop
#@games
#@graphical-internet
#@graphics
@hardware-support
@input-methods
#@java
#@office
#@online-docs
@printing
@sound-and-video
@text-internet
@base-x
xfsprogs
mtools
#gpgme
#openoffice.org-opensymbol-fonts
#gvfs-obexftp
hdparm
#gok
#iok
#vorbis-tools
jack-audio-connection-kit
#ncftp
gdm
%end

# Reboot after installation
reboot

```

------

[Category](https://fedoraproject.org/wiki/Special:Categories): [Anaconda](https://fedoraproject.org/wiki/Category:Anaconda)

Copyright © 2018 Red Hat, Inc. and others. All Rights Reserved. For comments or queries, please [contact us](https://fedoraproject.org/wiki/Communicating_and_getting_help).

The Fedora Project is maintained and driven by the community and sponsored by Red Hat. This is a community maintained site. Red Hat is not responsible for content.

- This page was last edited on 19 September 2016, at 20:22.
- Content is available under [Attribution-Share Alike 3.0 Unported](https://fedoraproject.org/wiki/Legal:Main) unless otherwise noted.


- [Privacy policy](https://fedoraproject.org/wiki/Fedora_Project_Wiki:Privacy_policy)
- [About Fedora Project Wiki](https://fedoraproject.org/wiki/Fedora_Project_Wiki:About)
- [Disclaimers](https://fedoraproject.org/wiki/Fedora_Project_Wiki:General_disclaimer)
- [Sponsors](http://fedoraproject.org/en/sponsors)
- [Legal](http://fedoraproject.org/wiki/Legal:Main)
- [Trademark Guidelines](http://fedoraproject.org/wiki/Legal:Trademark_guidelines)