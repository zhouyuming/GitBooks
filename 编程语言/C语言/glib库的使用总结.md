# glib库的使用总结

## ubuntu glib安装
1. sudo apt-get update
2. sudo apt-get install libglib2.0-dev
3. pkg-config --modversion glib-2.0
4. gcc your_program.c -o your_program `pkg-config --cflags --libs glib-2.0`
* https://wenku.csdn.net/answer/88f6f5330dd74175bf90137224134851
* https://www.cnblogs.com/wangbin/p/17144499.html
* http://mirror.accum.se/pub/GNOME/sources/glib/

## glib事件循环机制
* https://zhuanlan.zhihu.com/p/512939620?utm_id=0