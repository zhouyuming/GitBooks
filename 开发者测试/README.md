# 内存检测工具ASAN

## 1、简介

&#x20;   ASAN（Address-Sanitizier）早先是LLVM中的特性，后被加入GCC 4.8，在GCC 4.9后加入对ARM平台的支持。因此GCC 4.8以上版本使用ASAN时不需要安装第三方库，通过在编译时指定编译CFLAGS即可打开开关。

## 2、使用

* 添加编译选项和链接选项

CFLAGS += -fno-common -g -fsanitize=address -fsanitize-recover=address

LDFLAGS += -fsanitize=address -g1 -lpthread -ldl -lm -lrt -lstdc++ -static-libasan

\-fsanitize=address(启用ASAN)

\-fno-omit-frame-pointer(让栈追溯信息更加友好)

* 配置相关环境变量参数

export ASAN\_OPTIONS= halt\_on\_error=0:&#x20;

use\_sigaltstack=0:&#x20;

detect\_leaks=1:(内存泄露)&#x20;

malloc\_context\_size=15:&#x20;

log\_path=/usr/zhouyuming/asan.log;

&#x20;detect\_stack\_use\_after\_return=1;(使用栈上返回的变量)

&#x20;‘stack\_trace\_format="\[frame=%n, function=%f, location=%S]"’;(输出格式化)&#x20;

help=1;(输出所有支持的参数)&#x20;
