## use 是什么

use 是 Rust 编程语言的关键字。using 是 编程语言 C# 的关键字。

> 关键字是预定义的保留标识符，对编译器有特殊意义。

> `using` 关键字有三个主要用途：

- > [using 语句](https://docs.microsoft.com/zh-cn/dotnet/csharp/language-reference/keywords/using-statement)定义一个范围，在此范围的末尾将释放对象。

- > [using 指令](https://docs.microsoft.com/zh-cn/dotnet/csharp/language-reference/keywords/using-directive)为命名空间创建别名，或导入在其他命名空间中定义的类型。

- > [using static 指令](https://docs.microsoft.com/zh-cn/dotnet/csharp/language-reference/keywords/using-static)导入单个类的成员。

## use的用途是什么

类比using，use的用途有：

- 用于引用某个外部模块
- 直接使用枚举值，而无需手动加上作用域
- 为某个作用域下的方法或作用域创建别名

 ### 用于引用某个外部模块

外部模块 a.rs，代码内容如下

```rust
mod a
{
	fn print_function()
	{
		println!("This is a.print_function.");
	}
}
```

主函数 main.rs 想要调用 print_function，需要对 mod 标识访问级别，使用关键字 pub。所以 a.rs 的内容变动如下

```rust
pub mod a
{
	fn print_function()
	{
		println!("This is a.print_function.");
	}
}
```

主函数 main.rs 调用 print_function 如下，使用关键字 use：

```rust
use a;

fn main()
{
	a::print_function();
}
```

### 直接使用枚举值，而无需手动加上作用域

```rust
enum Status {
    Rich,
    Poor,
}

fn main()
{
    use Status::{Poor, Rich};
    let status = Poor;
}
```

上述代码使用关键字 `use` 显示声明了枚举 Status，所以在 `let status = Poor;` 这行代码中无需使用 `Status::Poor` 手动加上作用域的方式声明 `Poor`。

当然如果枚举值过多时，可以使用 `*` 声明所有枚举值，即 `use Status::*;` 。

### 为某个作用域下的方法或作用域创建别名

```rust
pub mod a 
{
    pub mod b
    {
        pub fn function()
        {
            println!("This is a::b::function");
        }

        pub fn other_funtion()
        {
            println!("This is a::b::other_funtion");
        }
    }
}

use a::b as ab;
use a::b::other_funtion as ab_funtion;

fn main()
{
    ab::function();
    ab::other_funtion();
    ab_funtion();
}
```

如上述例子所示

`use a::b as ab;`使用关键字 use 为作用域创建别名。

`use a::b::other_funtion as ab_funtion;` 为方法 other_funtion 创建别名 ab_funtion 。

参考：

* [C# 关键字 | Microsoft Docs](https://docs.microsoft.com/zh-cn/dotnet/csharp/language-reference/keywords/)

* [using 语句 - C# 参考 | Microsoft Docs](https://docs.microsoft.com/zh-cn/dotnet/csharp/language-reference/keywords/using-statement)

* [using 静态指令 - C# 参考 | Microsoft Docs](https://docs.microsoft.com/zh-cn/dotnet/csharp/language-reference/keywords/using-static)

* [using 指令 - C# 参考 | Microsoft Docs](https://docs.microsoft.com/zh-cn/dotnet/csharp/language-reference/keywords/using-directive)

* [use 声明 - 通过例子学 Rust](http://llever.com/rust-by-example-cn/mod/use.html)

* [使用 use - 通过例子学 Rust](http://llever.com/rust-by-example-cn/custom_types/enum/enum_use.html)

* [模块 module 和包 crate · RustPrimer](https://rustcc.gitbooks.io/rustprimer/content/module/module.html)