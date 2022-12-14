# 2022 秋季 OS 训练营 
## Rustlings 集训班 github classroom 地址：<https://classroom.github.com/a/U37u3veU>

# rustlings 🦀❤️

Greetings and welcome to `rustlings`. This project contains small exercises to get you used to reading and writing Rust code. This includes reading and responding to compiler messages!

_...looking for the old, web-based version of Rustlings? Try [here](https://github.com/rust-lang/rustlings/tree/rustlings-1)_

Alternatively, for a first-time Rust learner, there are several other resources:



- [The Book](https://doc.rust-lang.org/book/index.html) - The most comprehensive resource for learning Rust, but a bit theoretical sometimes. You will be using this along with Rustlings!
- [Rust By Example](https://doc.rust-lang.org/rust-by-example/index.html) - Learn Rust by solving little exercises! It's almost like `rustlings`, but online

## Getting Started

_Note: If you're on MacOS, make sure you've installed Xcode and its developer tools by typing `xcode-select --install`._
_Note: If you're on Linux, make sure you've installed gcc. Deb: `sudo apt install gcc`. Yum: `sudo yum -y install gcc`._

You will need to have Rust installed. You can get it by visiting https://rustup.rs. This'll also install Cargo, Rust's package/project manager.

## MacOS/Linux

Just run:

```bash
curl -L https://raw.githubusercontent.com/rust-lang/rustlings/main/install.sh | bash
# Or if you want it to be installed to a different path:
curl -L https://raw.githubusercontent.com/rust-lang/rustlings/main/install.sh | bash -s mypath/
```

This will install Rustlings and give you access to the `rustlings` command. Run it to get started!

## Windows

In PowerShell (Run as Administrator), set `ExecutionPolicy` to `RemoteSigned`:

```ps1
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

Then, you can run:

```ps1
Start-BitsTransfer -Source https://raw.githubusercontent.com/rust-lang/rustlings/main/install.ps1 -Destination $env:TMP/install_rustlings.ps1; Unblock-File $env:TMP/install_rustlings.ps1; Invoke-Expression $env:TMP/install_rustlings.ps1
```

To install Rustlings. Same as on MacOS/Linux, you will have access to the `rustlings` command after it.

If you get a permission denied message, you might have to exclude the directory where you cloned Rustlings in your antivirus.

## Browser

[Run on Repl.it](https://repl.it/github/rust-lang/rustlings)

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/rust-lang/rustlings)

## Manually

Basically: Clone the repository at the latest tag, run `cargo install --path .`.

```bash
# find out the latest version at https://github.com/rust-lang/rustlings/releases/latest (on edit 5.2.1)
git clone -b 5.2.1 --depth 1 https://github.com/rust-lang/rustlings
cd rustlings
cargo install --force --path .
```

If there are installation errors, ensure that your toolchain is up to date. For the latest, run:

```bash
rustup update
```

Then, same as above, run `rustlings` to get started.

## Doing exercises

The exercises are sorted by topic and can be found in the subdirectory `rustlings/exercises/<topic>`. For every topic there is an additional README file with some resources to get you started on the topic. We really recommend that you have a look at them before you start.

The task is simple. Most exercises contain an error that keeps them from compiling, and it's up to you to fix it! Some exercises are also run as tests, but rustlings handles them all the same. To run the exercises in the recommended order, execute:

```bash
rustlings watch
```

This will try to verify the completion of every exercise in a predetermined order (what we think is best for newcomers). It will also rerun automatically every time you change a file in the `exercises/` directory. If you want to only run it once, you can use:

```bash
rustlings verify
```

This will do the same as watch, but it'll quit after running.

In case you want to go by your own order, or want to only verify a single exercise, you can run:

```bash
rustlings run myExercise1
```

Or simply use the following command to run the next unsolved exercise in the course:

```bash
rustlings run next
```

In case you get stuck, you can run the following command to get a hint for your
exercise:

```bash
rustlings hint myExercise1
```

You can also get the hint for the next unsolved exercise with the following command:

```bash
rustlings hint next
```

To check your progress, you can run the following command:

```bash
rustlings list
```

## Testing yourself

After every couple of sections, there will be a quiz that'll test your knowledge on a bunch of sections at once. These quizzes are found in `exercises/quizN.rs`.

## Enabling `rust-analyzer`

Run the command `rustlings lsp` which will generate a `rust-project.json` at the root of the project, this allows [rust-analyzer](https://rust-analyzer.github.io/) to parse each exercise. 

## Continuing On

Once you've completed Rustlings, put your new knowledge to good use! Continue practicing your Rust skills by building your own projects, contributing to Rustlings, or finding other open-source projects to contribute to.

## Uninstalling Rustlings

If you want to remove Rustlings from your system, there are two steps. First, you'll need to remove the exercises folder that the install script created
for you:

```bash
rm -rf rustlings # or your custom folder name, if you chose and or renamed it
```

Second, since Rustlings got installed via `cargo install`, it's only reasonable to assume that you can also remove it using Cargo, and
exactly that is the case. Run `cargo uninstall` to remove the `rustlings` binary:

```bash
cargo uninstall rustlings
```

Now you should be done!

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md).

Development-focused discussion about Rustlings happens in the [**rustlings** stream](https://rust-lang.zulipchat.com/#narrow/stream/334454-rustlings)
on the [Rust Project Zulip](https://rust-lang.zulipchat.com). Feel free to start a new thread there
if you have ideas or suggestions!

## Contributors ✨

Thanks goes to the wonderful people listed in [AUTHORS.md](./AUTHORS.md) 🎉

## 笔记

### primitive_types2.rs
  
is_alphabetic
is_numeric 
两个字符上的API，判断字符类型的内容是字母表还是数字。
存在而这都不是的情况：option + 任意字母键

```rust
let your_character = '1'; // Finish this line like the example! What's your favorite character?
                          // Try a letter, try a number, try a special character, try a character
                          // from a different language than your own, try an emoji!
if your_character.is_alphabetic() {
    println!("Alphabetical!");
} else if your_character.is_numeric() {****
    println!("Numerical!");
} else {
    println!("Neither alphabetic nor numeric!");
}
```

### primitive_type3.rs

如何快速创建一个数组，语法忘记了。

1. 数组需要给定类型和大小
2. 类型是统一的
3. 数组使用 [] 包裹
4. 数组元素相同时的快速创建方式：`let a: [i32; 500] = [0; 500];`
5. 数组切片创建: &a[1..4]; (primitive_type4.rs)

## primitive_type6.rs

- 元组元素读取以及定义

```rust
let numbers = (1, 2, 3);
// Replace below ??? with the tuple indexing syntax.
let second = numbers.1;
```
## vecs1.rs

向量的几种定义方式
- Vec::new()
- vec![10, 20, 30]
- vec.get(2)
  - 向量获取元素的两种方式以及区别
- vec.push(32)
- 通过枚举存储多种类型数据

## vecs2.rs

此处用到了闭包，闭包在Rust中的概念有些遗忘。
- 可以捕获当前环境中的变量。

- Vector 遍历方法

```rust
for i in v.iter_mut() {
    *i *= 2;
}
```
遍历的到的是引用，如果需要改变原数，需要解引用

```rust
v.iter().map(|num| {
    // TODO: Do the same thing as above - but instead of mutating the
    // Vec, you can just return the new number!
    num + 1
})
.collect()
```

[collect 消费迭代器](https://kaisery.github.io/trpl-zh-cn/ch13-02-iterators.html#%E4%BA%A7%E7%94%9F%E5%85%B6%E4%BB%96%E8%BF%AD%E4%BB%A3%E5%99%A8%E7%9A%84%E6%96%B9%E6%B3%95)

类似JS函数式编程中的延迟执行，iter 以及 map 创建的迭代器，如果不去通过 collect 消费，那么其中的内容就永远不会执行。

## move_semantics1.rs

移动语意：




