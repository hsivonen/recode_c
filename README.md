# recode-c

recode-c is a test/sample app that's written in C and uses
[encoding-rs](https://github.com/hsivonen/encoding-rs).

It expects encoding-rs to have been checked out to an adjacent directory.

## Licensing

Please see the file named COPYRIGHT.

## Building

Git, GNU Make and a version of GCC recent enough to accept `-std=c11` are
assumed to be already installed.

###0. Install Rust (including Cargo) if you haven't already

See the [Rust download page](https://www.rust-lang.org/downloads.html). For
Linux and OS X, this means:
```
curl -sSf https://static.rust-lang.org/rustup.sh | sh
```

###1. Clone encoding-rs

```
git clone https://github.com/hsivonen/encoding-rs.git
```

###2. Enable staticlib support for encoding-rs

Edit `encoding-rs/Cargo.toml` and uncomment the line
```
# crate-type = ["rlib", "staticlib"]
```

(The line is commented out due to a
[rustfmt bug](https://github.com/rust-lang-nursery/rustfmt/issues/828).)

###3. Clone recode-c

```
git clone https://github.com/hsivonen/recode-c.git
```

###4. Build recode-c

```
cd recode-c
make
```
