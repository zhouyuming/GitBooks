# 动态链接库的反解析

* 使用addr2line反编译.dbg文件获取函数和代码行信息

addr2line -C -e xxx.dbg -f \[so中的相对地址]

注：

1、调用栈信息直接为出错地址在so中的相对地址

2、objdump获取函数在so中的相对地址，再加上函数内偏移
