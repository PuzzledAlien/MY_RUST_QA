### Cargo：Rust 的构建工具和包管理器

文章标题来自于 Rust 官网：

* [入门 - Rust 程序设计语言](https://www.rust-lang.org/zh-CN/learn/get-started)

在安装 Rustup 时，也会安装 Rust 构建工具和包管理器的最新稳定版，即 Cargo。Cargo 可以做很多事情：

- `cargo build` 可以构建项目
- `cargo run` 可以运行项目
- `cargo test` 可以测试项目
- `cargo doc` 可以为项目构建文档
- `cargo publish` 可以将库发布到 [crates.io](https://crates.io/)。

要检查您是否安装了 Rust 和 Cargo，可以在终端中运行：

```shell
cargo --version
```



我在其他文章中提到自己是 .net developer ，所以在看 cargo 命令时，我有强烈的熟悉感。

这是因为它：

* [dotnet 命令 - .NET Core CLI | Microsoft Docs](https://docs.microsoft.com/zh-cn/dotnet/core/tools/dotnet)

如果模仿 Rust 官网入门文档中对 Cargo 的介绍，dotnet cli 的介绍应该是这样的：

在安装 .net core 时，也会安装 .NET Core CLI 的通用驱动程序 - dotnet。dotnet 可以做很多事情：

- [dotnet build](https://docs.microsoft.com/zh-cn/dotnet/core/tools/dotnet-build) - 可以生成项目及其所有依赖项
- [dotnet run](https://docs.microsoft.com/zh-cn/dotnet/core/tools/dotnet-run) \- 无需任何显式编译或启动命令即可运行源代码
- [dotnet test](https://docs.microsoft.com/zh-cn/dotnet/core/tools/dotnet-test) - 用于执行单元测试的 .NET 测试驱动程序
- [dotnet publish](https://docs.microsoft.com/zh-cn/dotnet/core/tools/dotnet-publish) - 将应用程序及其依赖项发布到文件夹以部署到托管系统



不得不称赞这种管理工具的便捷，或许也是云原生大趋势的体现，方便做规模化集成化的管理。

### 如何更多地了解 Cargo

阅读官网提供的文档：

* [Introduction - The Cargo Book](https://doc.rust-lang.org/cargo/index.html)

该文档的开源地址：

* [cargo/src/doc/src at master · rust-lang/cargo](https://github.com/rust-lang/cargo/tree/master/src/doc/src)

Cargo 的源码：

* [rust-lang/cargo: The Rust package manager](https://github.com/rust-lang/cargo)

请尽量阅读官方提供的英文文档，中文翻译文档可能有所滞后。比如：

* [《Cargo 教程》 | Rust 技术论坛](https://learnku.com/docs/cargo-book/2018)

