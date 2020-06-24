## Rust 有问有答之 crate 是什么

文章尽量以一个初学者的角度开始 Rust 的学习，但显然很难不带个人主观色彩和角度，只能尽力去客观写。

第一次知道 Rust 的时候，免不了搜索，百度、谷歌、必应等都可以搜出来官网地址：[Rust Programming Language](https://www.rust-lang.org/) 。首页看到一个字眼 `crate`，于我而言是陌生的。

> In 2018, the Rust community decided to improve programming experience for a few distinct domains (see [the 2018 roadmap](https://blog.rust-lang.org/2018/03/12/roadmap.html)). For these, you can find many high-quality crates and some awesome guides on how to get started.

crate 是什么？

crate 类似于 .NET class library，因为我对 .Net 更熟悉，所以会拿 .Net 做比对，类比是学习的好方式。 

但是显然不能真的认为它们非常相似，并且试图寻找它们的相同点，做比对是为了帮助理解。

.Net 引用类库的关键字是 using，Rust 引用 crate 的关键字是 use。

.Net 声明命名空间关键字是 namespace，Rust 声明 module 的关键字是 mod。

C# 对类型和类型成员规定了几种可访问性级别，同样 Rust 也有访问性级别规定。mod 中的方法，默认私有访问，同 mod 下可访问，外部访问该模块的方法的话，需使用关键字 pub 定义该方法。我想关键字 pub，可类比 C# 的 public 修饰符。当然二者绝对不可等同。 pub 可用于加载深层目录下的模块 - `pub mod` 或者 `pub use`  [^1]。

.Net 项目中添加一个 nuget package，需要一个程序包源，地址是 https://api.nuget.org/v3/index.json 。如果想在线浏览查看有多少种或者有哪些包，可访问 [NuGet Gallery | Packages](https://www.nuget.org/packages) 。Rust 也有类似的地址，可以查看有哪些 crate 可供选择，可访问 [Crates - crates.io: Rust Package Registry](https://crates.io/crates) 。

最后还是要给出一个定义，回答 crate 是什么这个问题。

> Rust 中，`crate` 是一个独立的可编译单元。具体说来，就是一个或一批文件（如果是一批文件，那么有一个文件是这个 crate 的入口）。它编译后，会对应着生成一个可执行文件或一个库。

各位看官或许会觉得奇怪，上面的一堆比对又是为了什么呢？是为了通过比对加深理解和记忆，将不熟悉的概念和知识内化为自己的知识，通过熟悉的知识作为桥接，使其易于自己接受。

同时在不断引申和解读的过程，也会不断的产生问题，例如为什么有关键字 use mod pub ，它们的出现是为了解决什么问题，这些关键字有没有更多的使用场景，显然我在上文中并没有展开写；还有如何生成一个 crate，并将其上传到 crates.io。 

所以有问有答的学习方式，似乎是真的非常适合我。我会尽量保持这种不断挖掘好奇心的方式。

参考：

* [Rust - 维基百科，自由的百科全书](https://zh.wikipedia.org/wiki/Rust)

* [模块 module 和包 crate · RustPrimer](https://rustcc.gitbooks.io/rustprimer/content/module/module.html)
* [.NET 类库概述 | Microsoft Docs](https://docs.microsoft.com/zh-cn/dotnet/standard/class-library-overview)

* [常规类型系统 | Microsoft Docs](https://docs.microsoft.com/zh-cn/dotnet/standard/base-types/common-type-system)

* [命名空间 - C# 编程指南 | Microsoft Docs](https://docs.microsoft.com/zh-cn/dotnet/csharp/programming-guide/namespaces/)

* [crates.io: Rust Package Registry](https://crates.io/)



[^1]: 具体使用方法不在本篇详细叙述