# day12

### 今日已完成的计划

1.rustclassroom cl 51-67

2.总结

### 完成过程

1.完成，总结在下头。

---

2.对于问号？在错误处理中的用法又快生疏了！幸亏复习了一下，哈哈。总结：

问号位于一个返回result的表达式最后：代表若OK，继续执行；若ERR，则该函数不继续执行直接返回Err<T>。

3.小知识：现在暂时未用：dyn 后跟某个trait，也就是这个Box可以装符合改trait的东西。

4.如果结构体里只有一个变量位置，可以不写名字。

```
impl<T> Wrapper<T> {
    pub fn new(value: T) -> Self {
        Wrapper { value }
    }
}
```

5.记录一个问题：打算问问助教：

traits1.rs:

```
trait AppendBar {
    fn append_bar(mut self) -> Self;
}

impl AppendBar for String {
    //Add your code here
    fn append_bar(mut self) -> Self{
        self.push_str("Bar");
        self
    }
}
```

这个竟然会编译报错。如果去除第一个mut就不报错了，trait的声明和impl不应该一样吗？？

6.可以将trait作为参数，传入函数。。感触：昨晚trait4，5，这块的语法真是太花里胡哨了。。麻了

7.
