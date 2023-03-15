1
```rust
// 移除某个部分让代码工作
fn main() {
    let x: i32 = 5;
    let mut y = 5;

    y = x;

    let z = 10; // 这里 z 的类型是?
}

```
2
```rust
// 填空
fn main() {
    let v: u16 = 38_u8 as u16;
}

```
3
```rust
// 修改 `assert_eq!` 让代码工作
fn main() {
    let x = 5;
    assert_eq!("i32".to_string(), type_of(&x));
}

// 以下函数可以获取传入参数的类型，并返回类型的字符串形式，例如  "i8", "u8", "i32", "u32"
fn type_of<T>(_: &T) -> String {
    format!("{}", std::any::type_name::<T>())
}

```
4
```rust
// 填空，让代码工作
fn main() {
    assert_eq!(i8::MAX, 127i8);
    assert_eq!(u8::MAX, 255u8);
}

```
5
```rust
// 解决代码中的错误和 `panic`
fn main() {
    let v1 = 251_u8 - 8;
    let v2 = u8::checked_add(251, 8).unwrap();
    println!("{},{}", v1, v2);
}

```
6
```rust
// 修改 `assert!` 让代码工作
fn main() {
    let v = 1_024 + 0xff + 0o77 + 0b1111_1111;
    assert!(v == 1597);
}

```
7
```rust
// 将 ? 替换成你的答案
fn main() {
    let x = 1_000.000_1; // f64
    let y: f32 = 0.12; // f32
    let z = 0.01_f64; // f64
}

```
8
```rust
fn main() {
    assert!((0.1_f64 + 0.2 - 0.3).abs() < 0.000001);
}

```
9
```rust
fn main() {
    let mut sum = 0;
    for i in -3..-2 {
        sum += i
    }

    assert!(sum == -3);

    for c in 'a'..='z' {
        println!("{}", c as i32);
    }
}

```
10
```rust
// 填空
use std::ops::{Range, RangeInclusive};
fn main() {
    assert_eq!((1..5), Range { start: 1, end: 5 });
    assert_eq!((1..=5), RangeInclusive::new(1, 5));
}

```
11
```rust
// 填空，并解决错误
fn main() {
    // 整数加法
    assert!(1u32 + 2 == 3_u32);

    // 整数减法
    assert!(1i32 - 2 == -1_i32);
    assert!(1i8 - 2 == -1);

    assert!(3 * 50 == 150);

    assert!(9 / 3 == 3); // error ! 修改它让代码工作

    assert!(24 % 5 == 4);

    // 逻辑与或非操作
    assert!(true && false == false);
    assert!(true || false == true);
    assert!(!true == false);

    // 位操作
    println!("0011 AND 0101 is {:04b}", 0b0011u32 & 0b0101);
    println!("0011 OR 0101 is {:04b}", 0b0011u32 | 0b0101);
    println!("0011 XOR 0101 is {:04b}", 0b0011u32 ^ 0b0101);
    println!("1 << 5 is {}", 1u32 << 5);
    println!("0x80 >> 2 is 0x{:x}", 0x80u32 >> 2);
}

```



