---
title: "Rust vs C++"
menus: none
date: 2025-11-16 14:44:34
lastmod: 2025-11-16 18:26:21
outputs: "Reveal"
tags:
- presentation
- rust
- c++
- cargo
---

## Rust vs C++

Comparing the developer experience

## The tools

### C++

- Building: Make (and CMake because Makefiles are horrendous to write manually)
- Testing: Catch2 or GTest
- Documentation: Doxygen

### Rust

- Building: cargo build
- Testing: cargo test
- Documentation: cargo doc

## Using Packages

### C++

- Find a package
- Download the minimum source code that provides the interface for the package
- Download the package's prebuilt binaries for your system
OR
- Download the entire source code and build the binary yourself
OR
- Download the entire source code and include it directly in YOUR source code so it gets built directly into YOUR binaries
- Redo all previous steps every time you want to bump the version of the package

### Rust

- Find a package that's available as a Crate
- Add its name and required version to `cargo.toml`
- To bump the version, update the version specified in the `cargo.toml`

## Building for WASM

### C++

- Install the dependencies required by the the Emscripten Software Development Kit
- Install the the Emscripten Software Development Kit
- Build your code to wasm `emcc hello.c -o hello.html -s WASM=1`
- Manually open `hello.html` in a browser

### Rust

- `cargo install trunk`
- `trunk serve` (this builds the code to WASM, hosts a dev server, automatically opens the webpage in your browser, and automatically rebuilds and refreshes your browser window whenever you make a code change)

## The code

It's easier to write C++ that compiles than Rust that compiles.
But C++ will let you write inefficient code, and actually pushes you towards it.

### Passing Arguments

Naiive C++:

```c++
function myFunction(Item item)...

myFunction(item);
```

Optimised C++:

```c++
function myFunction(const Item& item)...

myFunction(item);
```

Naiive Rust:

```rust
fn myFunction(item: Item) // this will MOVE the `item` object automatically, not copy it.

myFunction(item)
```

Technically the same as the C++ version but in Rust:

```rust
fn myFunction(&item: Item)

myFunction(item)
```
