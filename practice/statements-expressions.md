1
```rust
// 使用两种方法让代码工作起来
fn main() {
    let v = {
        let mut x = 1;
        x += 2;
        x
    };

    assert_eq!(v, 3);
}


```
```rust
// 使用两种方法让代码工作起来
fn main() {
    let v = {
        let mut x = 1;
        x + 2
    };

    assert_eq!(v, 3);
}

```
```rust
// 使用两种方法让代码工作起来
fn main() {
    let v = {
        let mut x = 1;
        x += 2;
    };

    assert_eq!(v, ());
}

```
2
```rust
fn main() {
    let x = 3;
    let v = x;

    assert!(v == 3);
}

```
3
```rust
fn main() {
    let s = sum(1, 2);
    assert_eq!(s, 3);
}

fn sum(x: i32, y: i32) -> i32 {
    x + y
}

```