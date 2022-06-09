# Methood

- 使用 `impl`
- 方法第一个参数为：
	- `&self`：不可变引用
	- `&mut self`：可变引用
	- `self`：获取所有权，很少使用

```rust
struct Rectangle {
    width: u32,
    height: u32,
}

impl Rectangle {
    fn area(&self) -> u32 {
        self.width * self.height
    }

    fn resize(&mut self, scale: u32) {
        self.width *= scale;
        self.height *= scale;
    }
}

fn main() {
    let mut rect = Rectangle {
        width: 30,
        height: 30,
    };
    println!("area is {}", rect.area()); // area is 900

    rect.resize(2);
    println!("area is {}", rect.area()); // area is 3600
}
```