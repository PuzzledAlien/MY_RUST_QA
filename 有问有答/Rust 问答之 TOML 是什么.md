### TOML 是什么

先解释问题的来源。在阅读以下文档时，看到了 toml。自然要了解 toml 是什么。

* [cargo/Cargo.toml at master · rust-lang/cargo](https://github.com/rust-lang/cargo/blob/master/Cargo.toml)
* [Cargo.toml vs Cargo.lock - The Cargo Book](https://doc.rust-lang.org/cargo/guide/cargo-toml-vs-cargo-lock.html)

直奔主题，上菜：

> TOML 旨在成为一个语义显著而易于阅读的最低限度的配置文件格式。

所以，可知，TOML 是一种配置文件格式。

.Net Framework 的配置文件是 XML，.NET Core 的配置文件是 JSON。那么为什么 Rust 选择了 TOML。

### Rust 为什么选择了 TOML

* [Rust的工程配置为何用toml格式？ - 知乎](https://www.zhihu.com/question/31523723?sort=created)

看来也会有人有类似的困惑。

那么要多了解以下 TOML。

### TOML 介绍文档

* [toml-lang/toml: Tom's Obvious, Minimal Language](https://github.com/toml-lang/toml)

* [TOML 教程 - 可能是目前最好的配置文件格式 - 知乎](https://zhuanlan.zhihu.com/p/50412485)

* [LongTengDao/TOML: 汤小明语的官方文档翻译。Wiki 中有教程。🡭](https://github.com/LongTengDao/TOML/)

* [Home · LongTengDao/TOML Wiki](https://github.com/LongTengDao/TOML/wiki)

* [rust-wiki/toml.md at master · rust-lang-cn/rust-wiki](https://github.com/rust-lang-cn/rust-wiki/blob/master/src/rust-related/toml.md)

### TOML 的优点

TOML 作为配置文件有以下优势

- 手工编辑配置，TOML 更方便和易读
- 完全以配置为导向，专为易于处理配置项
- 支持必要的数据类型和嵌套

