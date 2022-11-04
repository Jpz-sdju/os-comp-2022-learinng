# day11

### 今日已完成的计划

1.rustclassroom cl 20-50

2.总结

### 完成过程

1.完成，总结在下头。

---

2.

当外部的模块项 `A` 被引入到当前模块中时，它的可见性自动被设置为私有的，如果你希望允许其它外部代码引用我们的模块项 `A`，那么可以对它进行再导出：

```
#![allow(unused)]
fn main() {
mod front_of_house {
    pub mod hosting {
        pub fn add_to_waitlist() {}
    }
}

pub use crate::front_of_house::hosting;

pub fn eat_at_restaurant() {
    hosting::add_to_waitlist();
    hosting::add_to_waitlist();
    hosting::add_to_waitlist();
}
}
```

如上，使用 `pub use` 即可实现。这里 `use` 代表引入 `hosting` 模块到当前作用域，`pub` 表示将该引入的内容再度设置为可见。

3.hashmap3和quiz 。这两道题教会了我一个道理。。一定要善用，多用rust-lang上的api查询。。。坐了很久
