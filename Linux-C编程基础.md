---
title: Linux C编程基础
author: Dai
categories: 操作系统
tags:
  - Linux命令
  - 操作系统	
  - C语言
---





# Linux C编程基础 



### 实验环境 

**Ubuntu 5.4.0-6ubuntul~16.04.10**

### 实验目的 

1. 了解UNIX/LINUX命令及使用格式
2. 熟悉UNIX/LINUX的常用基本命令
3. 复习C语言程序基本知识
4. 练习并掌握LINUX提供的vi编辑器来编辑C语言
5. 学会利用gcc、gdb编译、调试C程序
6. 熟悉UNIX/LINUX的常用基本命令如ls、who、w、p
7. 用vi编写一个简单的、显示"Hello,World!"的C程序，用gcc编译并观察编译后的结果
8. 利用gdb调试该程序
9. 运行生成的可执行文件。

### 常用命令

> 一、LINUX的登录与退出
>
> 1、登录
>
>    步骤如下：
>
> ​      login：     （输入student）
>
> ​      password：    （输入密码:student）
>
> 2、退出
>
>    在LINUX系统提示符$下，输入logout、exit或shutdown 。
>
> 例：$ logout
>
> 三、常用命令
>
> 1、目录操作
>
> （1）显示目录文件  ls
>
> （2）建新目录  mkdir
>
> （3）删除目录　　rmdir
>
> （4） 改变工作目录位置  cd
>
> （5）显示当前所在目录pwd
>
> （6）查看目录大小du
>
> （7）显示环境变量
>
> （8）修改环境变量，在bash下用export,如：
>
>   
>
> 2、文件操作
>
> （1）查看文件(可以是二进制的)内容 cat
>
> （2）删除文件 rm
>
> （3）复制文件 cp
>
> （4）移动或更改文件、目录名称mv
>
> 3、系统询问与权限口令
>
> （1）查看系统中的使用者
>
> 执行格式：  who
>
> （2）查看username
>
> 执行格式：  who am I  查看自己的username
>
> （3）改变自己的username的帐号与口令  su
>
>    执行格式：  su  username
>
>    例：   su  username    输入帐号
>
> ​       password      输入密码
>
> （4）文件属性的设置  chmod 
>
> 改变文件或目录的读、写、执行的允许权
>
> 执行格式：   chmod [-R] mode name
>
> （5）改变文件或目录所有权  chown
>
> 执行格式：   chown [-R] username name   
>
> （6）检查用户所在组名称   groups
>
> 执行格式：    groups 
>
>   touch  name
>
> 4、进程操作
>
> （1）查看系统目前的进程  ps 
>
> （2）查看正在background中执行的process
>
> （3）结束或终止进程  kill
>
> （4）显示系统中程序的执行状态
>
>  
>
> 5、I/O命令
>
> （1）管道（pipe-line）的使用
>
> 执行格式： command1|command2  
>
> 功能：将command1的执行结果送到command2 作为输入
>
> 6、其它常用命令
>
> （1）**命令在线帮助  man**
>
> **执行格式： man  command**
>
> **例：  man ls    查询ls这个指令的用法**
>
> （2）设定命令记录表长度  history
>
> （3）显示说明  info
>
> 四、用cat 命令查看 /proc 动态文件系统目录下的文件,辨识其中的系统信息.

### 实验过程

- 显示目录文件

![image-20210928162027236](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20210928162027236.png)

- 创建目录

  ![image-20210928162235726](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20210928162235726.png)

- 删除目录

![image-20210928162303636](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20210928162303636.png)

- 利用vi编辑器新建hello.c文件

  ![image-20210928162507954](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20210928162507954.png)

- 写入一段代码，并保存退出

  ![image-20210928162643639](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20210928162643639.png)

- 利用gcc命令编译运行C语言程序

  ![image-20210928162742159](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20210928162742159.png)

- 接下来演示利用gdb调试，重新编写了一段C语言程序

  ![image-20210928163316290](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20210928163316290.png)

- 生成调试信息

  ![image-20210928163533203](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20210928163533203.png)

- 设置断点、查看变量

  ![image-20210928163647284](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20210928163647284.png)

- 利用display命令绑定查询变量

  ![](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20210928164027131.png)

- 退出gdb

  ![image-20210928164112879](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20210928164112879.png)



### 实验总结

​	通过本次实验，我对C语言执行过程有了更深的理解，这是集成开发环境中学习不到的内容，Linux系统为我们提供了C语言编程最基础的环境，深入理解Linux操作系统对我们的程序编写一定有十分重要的作用。