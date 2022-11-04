# day10

### 今日已完成的计划

1.新的这个cl不可以线上做了，clone新的cl，rustclassroom cl 1-20，当作复习了吧，哈哈

2.总结

### 完成过程

1.完成，总结在下头。

---

2.

有些点可能忘了，刚好在这里做个大总结吧

1.数组重复某个元素初始化：[7;101].

2.(1,2,3)元组索引使用 .x,（1，2，3）.1  等于等于2

3.某种方法可以提取出vec里的所有元素：

```
    let a = [10, 20, 30, 40]; // a plain array
    // let v = Vec::new(10,20,30,40);// TODO: declare your vector here with the macro for vectors
    let v = vec![10,20,30,40];
    assert_eq!(a, v[..]);
```
