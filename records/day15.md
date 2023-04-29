# day15

1.今天做ch5的任务时，先是遇到了merge的bug。bug来源于上一章节的mmap增加的虚拟页面没有被free，在进程结束free时free到了叶子节点（对于这块不是很熟），于是报错。今天增加了max_page的修改逻辑，就过了。

2.仍然存在的问题，发现代码框架中ch5B_usertest 的exit(-1)导致我的usertest assert无法成功，询问了助教看看怎么回事。助教还没有回复。
