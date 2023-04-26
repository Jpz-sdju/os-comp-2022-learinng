# day13

1.成功pass tests，mmap和unmap的问题是这个跨页map或者unmap的问题，代码逻辑写的不是很到位，引入了循环进行依次map后就可以了。并且值得一提的是[addr,addr + len]的重叠检测问题，这个问题我使用了walkaddr函数来解决，walkaddr函数可以在检测出当前页被映射时返回pte，而如果没被映射则返回0.这个函数是天助我也，很好的满足了我的检测重叠的需求。



2.准备进行ch5
