# day11

1.编写大致ch4 逻辑，重构taskinfo 和 gettime函数比较简单，等于是一遍过。主要是利用了copyin and copyout函数，因为从用户程序传过来的指针是在栈上的，而栈是目前唯一虚拟的并且跟实现分页机制息息相关的内存区域（见day10分析）。所以传进来的参数是虚拟地址的指针地址，于是将kernel的taskinfo copy to user space就可以了。



2.编写大致的mmap和unmap逻辑，出了几个小bug(关于U位和perm字段的)，成功解决。但是后来的大bug就没有解决了。是assert出了问题。
