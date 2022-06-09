# 枚举

## Enum

`enum` 定义的是一个数据结构，其值是可以枚举的。例如：

```rust
#[derive(Debug)]
enum Color {
    RGB,
    HEX
}

fn print_color(color: Color) {
    println!("{:?}", color);
}

fn main() {
    let rgb = Color::RGB;
    let hex = Color::HEX;

    print_color(rgb); // RGB
    print_color(hex); // HEX
}
```

枚举值是可以带类型的，例如：

```rust
#[derive(Debug)]
enum Color {
    RGB(u8, u8, u8),
    HEX(String)
}

fn print_color(color: Color) {
    println!("{:?}", color);
}

fn main() {
    let rgb = Color::RGB(255, 0, 0);
    let hex = Color::HEX(String::from("#ff0000"));

    print_color(rgb); // RGB(255, 0, 0)
    print_color(hex); // HEX("#ff0000")
}
```

## Option