## find
```
find ./-name test.cpp
```

find 命令是完全匹配的，必须和搜索关键字一模一样才会列出。

```
[root@localhost ~]# touch CANGLS
[root@localhost ~]# touch cangls
#建立大写和小写文件
[root@localhost ~]#find.-iname cangls
./CANGLS
./cangls
#使用-iname，大小写文件通吃
```
http://c.biancheng.net/view/779.html#:~:text=Linux%20find%E5%91%BD%E4%BB%A4%EF%BC%9A%E5%9C%A8%E7%9B%AE%E5%BD%95%E4%B8%AD%E6%9F%A5%E6%89%BE%E6%96%87%E4%BB%B6%EF%BC%88%E8%B6%85%E8%AF%A6%E8%A7%A3%EF%BC%89%201%20%E5%91%BD%E4%BB%A4%E6%A0%BC%E5%BC%8F%20%5Broot%40localhost%20~%5D%23%20find%20%E6%90%9C%E7%B4%A2%E8%B7%AF%E5%BE%84,%E6%8C%89%E7%85%A7%E6%9D%83%E9%99%90%E6%90%9C%E7%B4%A2%20%E5%9C%A8%20find%20%E4%B8%AD%EF%BC%8C%E4%B9%9F%E5%8F%AF%E4%BB%A5%E6%8C%89%E7%85%A7%E6%96%87%E4%BB%B6%E7%9A%84%E6%9D%83%E9%99%90%E6%9D%A5%E8%BF%9B%E8%A1%8C%E6%90%9C%E7%B4%A2%E3%80%82%20%E6%9D%83%E9%99%90%E4%B9%9F%E6%94%AF%E6%8C%81%20%5B%2B%2F-%5D%20%E9%80%89%E9%A1%B9%E3%80%82%20
