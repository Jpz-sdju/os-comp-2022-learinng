# day07

### 今日已完成的计划

1.rustclassroom cl 44-51

2.总结

### 完成过程

1.完成，总结在下头。

---

2.

?可以在函数返回OK时，直接将值返回等号左边；如果err，那么就报错（粗浅理解）。

error3的提示太巧妙了，如果返回err的话直接改main函数的返回值就可以了，太厉害了。



error5很难，我个人做了很久时间。最后总结出来：如果想让?返回的某些result互相转换，必须要实现from方法。像这样：

```
impl From<ParseIntError> for CreationError{
    fn from(e:ParseIntError) -> CreationError{
        match e.kind(){
            NegOverflow => {
                CreationError::Negative
            }
            Zero => {CreationError::Zero}
        }
    }
}
```

以上是将parseinterror转换为自定义的creationerror！
