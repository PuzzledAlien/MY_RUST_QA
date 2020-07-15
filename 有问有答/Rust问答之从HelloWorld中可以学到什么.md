```rust
fn main() {
    println!("Hello, world!");
}
```

### main 函数

 rust 也将 main 函数作为可执行程序的入口点。main 函数是默认的主函数入口，该函数无返回值，无参数。

### 关键字 fn

fn 是 function 的缩写。当写一个函数定义时，fn 必不可少。

### 编译

main.rs 的文件后缀是 `.rs`。编译需要执行 `rustc main.rs` 。

### 语句

语句需以 `;` 结尾。语句块使用大括号。

### 打印输出

`println!` 是个打印输出的宏，不是一个函数。宏和函数怎么区分呢？感叹号，`println` 后跟了一个感叹号，这代表它是一个宏。

### 执行

Windows编译之后，生成 exe 文件，可执行命令 `.\main.exe`。linux 下，执行命令 `./main` 。

### 参考

* [Hello, World! - The Rust Programming Language](https://doc.rust-lang.org/book/ch01-02-hello-world.html)

* [What is rustc? - The rustc book](https://doc.rust-lang.org/rustc/)