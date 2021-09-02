# 控制流

## If

- `if`
- `let` 可以使用 `if` 达到三元表达式的效果

```rust
fn main() {
    let x = 3;
    let y = 5;

    if x > y {
        println!("x > y");
    } else if x < y {
        println!("x < y");
    } else {
    	println!("x == y");
    }

    let z = if x > y {
        x
    } else {
        y
    };
    println!("{}", z); // 5
}
```

## 循环

### loop

- `loop` 无限循环
- 通过 `break` 跳出
- 嵌套情况下可以指定标签，`break` 可以选择跳出哪一层循环
- `break` 后跟一个值，可以从循环返回值

### while

### for