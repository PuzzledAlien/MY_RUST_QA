* [Hello, World! - The Rust Programming Language](https://doc.rust-lang.org/book/ch01-02-hello-world.html)

在官网文档中给出的 Hello world 例子中，我看到了编译的命令使用了 rustc 。

## rustc 怎么来的

以 windows 10 为例，下载 [rustup-init.exe 64位](https://static.rust-lang.org/rustup/dist/x86_64-pc-windows-msvc/rustup-init.exe) 并正确安装，rustc 也会被安装。存放 rustc.exe 的位置是 `%HomePath%\.cargo\bin` 。

```shell
>dir /b
cargo-clippy.exe
cargo-fmt.exe
cargo-miri.exe
cargo.exe
clippy-driver.exe
rls.exe
rust-gdb.exe
rust-lldb.exe
rustc.exe
rustdoc.exe
rustfmt.exe
rustup.exe
```

## rustc 是什么

rustc 是 编程语言 Rust 的编译器。rustc 将源代码编译生成二进制代码，展示的形式是库或者可执行文件。

在实际项目中，人们不会直接使用 rustc 编译所有的文件，而是使用 cargo 命令。执行 `cargo build --verbose` 可以查看它如何使用 `rustc` 。

参考：

* [What is rustc? - The rustc book](https://doc.rust-lang.org/rustc/what-is-rustc.html)

* [What is rustc? |《rustc 手册 2020》| Rust 技术论坛](https://learnku.com/docs/rustc-book/2020/what-is-rustc/8859)