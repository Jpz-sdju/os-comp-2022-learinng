# day13

### 今日已完成的计划

1.68-81

2.总结

### 完成过程

1.完成，总结在下头。

---

2.iter 那几道题比较考验迭代器的使用技巧。

```
fn count_iterator(map: &HashMap<String, Progress>, value: Progress) -> usize {
    map.iter().map(|(k,v)| if *v == value{1}else{0} ).sum()
}
fn count_collection_iterator(collection: &[HashMap<String, Progress>], value: Progress) -> usize {
    collection.iter().map(|map| count_iterator(map,value)).sum()
}
```

两段很漂亮的代码

3.ARC的使用比较生疏，倒是记住了：ARC的对象，如果clone他则加一引用计数，为零时消除这个对象。

4.cow1.rs跟着感觉做完了，但是看的不太懂。。准备补习一下

还有thread2
