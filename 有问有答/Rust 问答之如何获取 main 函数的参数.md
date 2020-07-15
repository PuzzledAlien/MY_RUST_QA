rust 的 main 函数和其他语言的 main函数都不太一样，它没有入参和返回值。

以 hello world 为例。

c#

```c#
using System;

namespace ConsoleApp
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World!");
        }
    }
}
```

c++

```c++
#include <iostream>

int main()
{
    std::cout << "Hello World!\n";
}
```

rust

```rust
fn main() {
    println!("Hello, world!");
}
```

其他语言的 main 函数会有入参或返回值。那么 rust 的入参怎么获取，又如何处理返回值。

rust 有专门的函数处理入参和返回值。

```
fn main() {
    for arg in std::env::args()
    {
        println!(arg);
    }
    
    std::process::exit(0);
}
```

进程退出函数 exit 的入参是返回值。 函数 args 可以获取所有的入参。 