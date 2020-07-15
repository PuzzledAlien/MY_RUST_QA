rust 的函数使用关键字 fn 开头，fn 是 function 的简写。main函数是一个无参数，无返回值的函数。

```rust
fn main() {
    println!("Hello, world!");
}
```

上面的 main 函数是主程序入口函数。可执行程序必定有 main 函数作为程序入口，而对于库函数 main 函数就不必须了。

下面以简单的加法为例。定义一个 add 函数，输入两个 int 型的参数 x 和 y，返回 int 型。

如果是 c# 的话，该函数应该这么写

```c#
int add(int x, int y)
{
    return x + y;
}
```

而对于 rust，需要有更明确的数据类型定义，因为对于 c# 而言，int 指的是 Int32，所以对应的 rust 加法函数应该是

```rust
fn add(x:i32, y:i32) -> i32 {
    return x + y;
}
```