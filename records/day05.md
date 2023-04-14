# day05

1.熟悉分时多任务系统章节要求，看set timer代码

2.一个小trick：在userret函数中，a0作为传参寄存器，指向trapframe，但是在返回为用户状态之前这个a0需要用来进行访存寻址（load xx,x(a0））这种操作。那么a0应该在最后被设置为用户的a0，做法是暂存a0在sccratch中，最后使用a0在访存操作结束后csrrw a0,xxx,a0。
