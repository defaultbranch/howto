# Rust Project

Homepage: https://rust-lang.org/

Tools:

- toolchain: `rustup`
- toolchain folder: `~/.cargo/bin`

# Install Rust

There is some installer:

```
curl -O https://static.rust-lang.org/rustup/dist/x86_64-unknown-linux-gnu/rustup-init
curl -O https://static.rust-lang.org/rustup/dist/x86_64-unknown-linux-gnu/rustup-init.sha256
```

# Hello World File

```
fn main() {
    println!("Hello, world!");
}
```

```
rustc main.rs
```

Creates a 3.7 MiB `main` (debug build).

# Hello World Project

```
cargo new hello_world
```

creates:

```
hello_world/
├── Cargo.toml
└── src
    └── main.rs
```

## Release Build

```
cargo build --release
```

Creates a 436 kiB `hello_world` (release build):

```
hello_world/
├── Cargo.lock
└── target
    ├── CACHEDIR.TAG
    └── release
        ├── build
        ├── deps
        │   ├── hello_world-3000b9669cba3230
        │   └── hello_world-3000b9669cba3230.d
        ├── examples
        ├── hello_world
        ├── hello_world.d
        └── incremental
```

# The println macro

Rust leverages some compilation work through a macro preprocessor. `println!` uses `print!` which calls `std::io::_print`.


