# mem-throttle
litmu-memguard
1、任务运行前throttle，改变内存带宽值
让任务正确运行在内存带宽限定下
或者回调

2、rt_param添加任务参数ck_stop ck_begin
实时任务，接收edf发送的信号ck_stop，=1暂停任务，每秒判断一次ck_begin是否=1，=1继续任务，=0继续sleep一秒
