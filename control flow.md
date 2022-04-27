### if

- branch your code to execute
- if 用在赋值表达式时，编译器会在编译时静态检查if表达式返回值类型是否匹配

```rust 
fn main() {
    let condition = true;
    let number = if  { 5 } else { 6 };  // ok. type is i32
    let number = if { 5} else { "six" }; //error, str mismatch i32
    println!("number is: {}", number);  
}
```



### loop

- while 使用 break 终止循环，break本地循环或break labeled循环, break可返回值
- for 循环可使用标准库提供的Range来表达循环次数.



```rust
// while
fn main(){
    let mux count = 0;
    'counting_loop': loop {
        let mut remaining = 10;
        loop {
            if remaining == 9 {
                break;
            }
            if count == 2 {
                break 'counting_loop'; // labled loop
            }
            remaining - = 1;
        }
        count += 1;
    }
}

// break
fn  main() {
    let mut counter = 0;
    let result = loop {
        counter += 1;
        if counter == 10 {
            break counter * 2；
        }
    }； // let
}
```



