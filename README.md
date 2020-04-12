[![Crates.io](https://img.shields.io/crates/v/open.svg)](https://crates.io/crates/open)
[![cross-platform-testing](https://github.com/Byron/open-rs/workflows/cross-platform-testing/badge.svg)](https://github.com/Byron/open-rs/actions?query=workflow%3Across-platform-testing)

Use this library to open a path or URL using the program configured on the system. It is equivalent to running one of the following:

```bash
# OSX
$ open <path-or-url>
# Windows
$ start <path-or-url>
# Linux
$ open <path-or-url> || xdg-open <path-or-url> || gnome-open <path-or-url> || kde-open <path-or-url>
```

# Usage

Add this to your Cargo.toml
```toml
[dependencies]
open = "1"
```
…and open something using…
```Rust
open::that("https://rust-lang.org");
```

…or, open something with an application of your choice
```Rust
open::with("https://rust-lang.org", "firefox");
```

Follow this link for the [massive API docs](http://byron.github.io/open-rs).

# Credits

The implementation is based on the respective functionality of [cargo](https://github.com/rust-lang/cargo), but was improved to allow some error handling.
