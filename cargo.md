### new

- 默认创建 src目录 和 Cargo.toml 配置文件，主目录还可放置 README.md 或其他与代码无关文件
- 使用 --vcs=git 可以同时创建 .git本地仓库

### build & check & run

- build 跑编译生成可执行程序，目录 /target/debug/
- check 跑编译但不生成可执行程序，适用于检查代码是否可以成功编译
- run 跑编译并且运行可执行程序
- 编译时生成 Cargo.lock文件，自动生成无需改动

### release

- 使用release命令生成性能优化的可执行程序，目录 /target/release



```rust
#shell

$ cargo new helloworld --vcs=git
$ cd helloworld
$ cargo build
$ ./target/debug/helloworld
$ cargo run
$ cargo check
$ cargo build --release
```



### 好处

- 更容易组织程序，源代码在 /src目录，目标程序在 /target目录
- 将非cargo转cargo，只需遵循上述这点即可转cargo