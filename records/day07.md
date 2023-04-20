# day07

1.完成实验，准备debug。

2.碰到的第一个bug：sys_info系统调用应该在返回前就给数字加一，而不是返回后再加一。

3.第二个bug： sys_task_info line 33

```
    assert(info.time < t3 - t1 + 100);
```

是单位的问题。cpu_frequency比较大，我们需要给分子乘以1000转为毫秒。之后顺利通过ch3_task_info测试。push上去看看
