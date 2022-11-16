# error while loading shared libraries: libncurses.so.5: cannot open shared object file: No such file

ncurses 提供字符终端处理库，包括面板和菜单。它提供了一套控制光标、建立窗口、改变前景/背景颜色及处理鼠标操作的函数，  
使用户在字符终端编写应用程序时绕过了那些恼人的底层机制。   
简而言之，它是一个可以使应用程序直接控制终端屏幕显示的函数库。   

没有找到共享库，解决缺少libncurses.so.5库文件：
## 思路一：安装
```
$ sudo apt install apt-file
$ sudo apt-file update
$ sudo apt-file find libncurses.so.5
$ sudo apt install libncurses5
```

## 思路二：创建软链接
查找libncurses.so.5，可能有libncurses.so不同版本的文件，使用命令
```
find / -name 'libncurses*'
```
查找，我找到的是
```
/usr/lib64/libncurses.so.6.2
```
建立软链接
```
ln -s libncurses.so.6.2 libncurses.so.5
```
如果没有找到的话，使用yum或apt安装即可
