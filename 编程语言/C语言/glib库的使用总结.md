# glib库的使用总结

## ubuntu glib安装
1. sudo apt-get update
2. sudo apt-get install libglib2.0-dev
3. pkg-config --modversion glib-2.0
4. gcc `pkg-config --cflags --libs glib-2.0` your_program.c -o your_program
* https://wenku.csdn.net/answer/88f6f5330dd74175bf90137224134851

## glib事件循环机制
