# day01

1.配好环境

2.运行ch1代码，成功输出helloworld

3.阅读第一章，复习C的基础知识。

4.复习批处理系统的trap handler函数汇编编写，总结一下流程：

- 设置stvec

- 在run第一个app的时候将内存结构体中的sepc设置为BASE ADDR，然后调用userret，这是假装之前trap过了，其实没有，以此来借用内存结构体中的sepc直接sret，这招蛮关键。

- 进入执行用户程序，进行下一次trap的调用。
