1
```rust
fn main() {
    // 使用尽可能多的方法来通过编译
    let x = String::from("hello, world");
    let y = x.clone();
    println!("{},{}", x, y);
}

```
```rust
fn main() {
    // 使用尽可能多的方法来通过编译
    let x = String::from("hello, world");
    let y = x;
    println!("{}", y);
}

```
```rust
fn main() {
    // 使用尽可能多的方法来通过编译
    let x = String::from("hello, world");
    let y = String::from("hello, world");
    println!("{},{}", x, y);
}

```
2
```rust
// 不要修改 main 中的代码
fn main() {
    let s1 = String::from("hello, world");
    let s2 = take_ownership(s1);

    println!("{}", s2);
}

// 只能修改下面的代码!
fn take_ownership(s: String) -> String {
    println!("{}", s);
    s
}

```
3
```rust
fn main() {
    let s = give_ownership();
    println!("{}", s);
}

// 只能修改下面的代码!
fn give_ownership() -> String {
    let s = String::from("hello, world");
    // convert String to Vec
    // 将 String 转换成 Vec 类型
    let _s = s.clone().into_bytes();
    s
}

```
4
```rust
// 修复错误，不要删除任何代码行
fn main() {
    let s = String::from("hello, world");

    print_str(s.clone());

    println!("{}", s);
}

fn print_str(s: String) {
    println!("{}", s)
}

```
5
```rust
// 不要使用 clone，使用 copy 的方式替代
fn main() {
    let x = (1, 2, (), "hello");
    let y = x;
    println!("{:?}, {:?}", x, y);
}

```
6
```rust
fn main() {
    let s = String::from("hello, ");

    // 只修改下面这行代码 !
    let mut s1 = s;

    s1.push_str("world")
}

```
7
```rust
fn main() {
    let x = Box::new(5);

    let mut y = Box::new(3); // 完成该行代码，不要修改其它行！

    *y = 4;

    assert_eq!(*x, 5);
}

```
8
```rust
fn main() {
    let t = (String::from("hello"), String::from("world"));

    let _s = t.0;

    // 仅修改下面这行代码，且不要使用 `_s`
    println!("{:?}", t.1);
}

```
9
```rust
fn main() {
    let t = (String::from("hello"), String::from("world"));

    // 填空，不要修改其它代码
    let (s1, s2) = &t;

    println!("{:?}, {:?}, {:?}", s1, s2, t); // -> "hello", "world", ("hello", "world")
}

```