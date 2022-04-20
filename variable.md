

### 变量

- 默认 不可变，值和类型都不可变
- 使用 let 关键字声明
- 使用 mux 关键字使其可变
- 可以使用let重新命令变量(相同名)来改变值或类型，mux只能改变值



### 常量

- 一直不可变，编译时计算
-  使用const关键字，用全大写+下划线命名
- 通过用在需要程序多个模块知晓的情况



```rust
const THREE_HOURS_IN_SECONDS: u32 = 60 * 60 * 3;

fn main() {
    let x = 5;
    let x = x + 1;
    {
        let x = x * 2;
        println!("value : ", x);   // 12
    }
    println!("value: ", x);  // 6
}
```

