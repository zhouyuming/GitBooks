# coredump分析与调试

* 开启core dump文件生成 &#x20;

unlimit -c unlimited

* 设置core dump文件位置

vi /etc/sysctl.conf&#x20;

kernel.core\_uses\_pid=0

这里是改为生成目录在/var/core/，%e代表程序名称，%p是进程ID

如果想直接生成在可执行文件相同目录，前面不要加任何目录，直接kernel.core\_pattern =core\_%e\_%p

* 使能修改生效

sysctl -p/etc/sysctl.conf
