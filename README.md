# mem-throttle
litmu-memguard  
1、任务运行前throttle，改变内存带宽值  
让任务正确运行在内存带宽限定下  
或者回调  
  
2、rt_param添加任务参数ck_stop ck_begin  
实时任务，接收edf发送的信号ck_stop，=1暂停任务，每秒判断一次ck_begin是否=1，=1继续任务，=0继续sleep一秒  
edf中stop_c=1，向memguard发送cpu和budget值  
memguard中，get_membudget return0  
edf中，如果return0，则将任务link到cpu  
  
3.需要更改的文件  
rt_param.h,memguard.c,  
step1  
sched_gsnedm.c,blackscholes.c  
step2
rt_param.h复制一份到任务文件夹里QAQ  
3.3  
rt_task写入和读取需要set和get  

4.参数传递顺序不对  