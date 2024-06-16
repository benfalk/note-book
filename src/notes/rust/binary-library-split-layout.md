# `bin` / `lib` Split Cargo Layout

This is personally how I like to have my Rust general setup.
Both the `lib` and `bin` portions are top level directories:

## Rough Layout

```text
Cargo.toml
src/
  lib/
    mod.rs
  bin/
    project_name.rs
```

## `Cargo.toml`

```toml
[package]
name = "project_name"
version = "0.1.0"
edition = "2021"

[lib]
# The name here should match the name from [package] above
name = "project_name"
path = "src/lib/mod.rs"

[[bin]]
name = "project_name"
path = "src/bin/project_name.rs"
```
