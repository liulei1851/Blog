2022年9月17日

1、在进行静态库编译时，报错：

错误描述：

/usr/bin/ld：找不到 -lc

collect2：错误：ld 返回 1

错误截图：

[![xwn334.png](https://s1.ax1x.com/2022/10/14/xwn334.png)](https://imgse.com/i/xwn334)

错误原因：

在新版本Linux系统下安装glibc-devel、glibc和gcc-c++时，都不会安装libc.a，只安装lib.so，所以当使用-static时，libc.a C库不能使用，会报错：找不到libc了。

解决方法：

安装glibc-static。

安装命令：yum install -y glibc-static

参考资料：

CSDN：https://blog.csdn.net/thomasyuang/article/details/84318184



2、Linux用VIM编辑好源文件保存退出时报错：

错误描述：

E492：不是编辑器的命令：WQ

错误截图：

[![xwn8gJ.png](https://s1.ax1x.com/2022/10/14/xwn8gJ.png)](https://imgse.com/i/xwn8gJ)

错误原因：

Linux命令是区分大小写的。

解决方法：

换为小写:wq即可。