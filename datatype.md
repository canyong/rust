### Scalar types

- integer:  
  - i8(signed) & u8;   isize & usize (依赖于机器实现)
  - 数值溢出会做mod到该类型能表示的数值. 如 257 % 256 = 1, u8 = 257 => 1;
  - literal: 
    - 10_000 (可以使用下划线来提高可读性)
    - 0b 1111_0000 (二进制)
    - b'A' (Byte类型u8)
  - 数字类型都支持add, sub, product, division, remainder(mod)操作
- float:   
  - f32(单精度) & f64:   默认f64,  f32和f64 cpu处理速度相同  
- bool
- char:
  - rust的char，占4个字节，可以表示 Unicode、中文等.

### Compound types

- tuple:
  - 读值可以是pattern读取或者索引下标读取
  - 空tuple 写作 (), 类型称为unit type,  值叫做 unit value.此表达式隐式返回unit value.
- array:
  - 语言提供定长数组，库提供vector
  - 通过索引下标的方式访问语言会执行运行时越界检查

```rust
// u32 类型注释不可省略，省略编译报错?,  parse功能 str2num,  expect异常处理
let guess : u32 = "42".parse(). expect("Not a number!"); 

let x = 2.0;  // f64
let y : f32 = 3.0;

let floored = 2 / 3;  // result is 0

let t = true;
let f : bool = false;   // 显示类型注释(annotation)

let heart_eyed_cat = '😻';  // unicode char

// tuple
let tup = (500, 6.4, 1);  // 可选类型注释 let tup : (i32, f64, u8)
let (x, y, z)  =  tup;  // x = 500, y = 6.4,  z = 1
let five_hundred = tup.0;  // element of index 0

// array
let a : [i32; 5] = [ 1, 2, 3, 4, 5 ];  //有5个元素的i32数组
let a = [3; 5];  // 有5个元素，每个元素的初始值为3
let first = a[0]; // element of index 0

```

