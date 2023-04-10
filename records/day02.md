# day02

1.复习link_app.s代码，查看一个python脚本(pack.py)，重新温习了如何通过汇编incbin去包含所有用户程序的二进制。然后再通过一个python脚本（kenerlld.py）去生成链接脚本：此链接脚本中需要在data setction中声明一下app数据的起止符号。再根据此链接脚本进行链接。



2.值得注意的是usertrap函数是用来判断trap类型的！此指针在每次run下一个app的时候都要重新被赋值为usertrap函数指针（但其实没有必要），但由于trapframe每次都要清空他才这样做。
