Moved
=====

This crate is published separately but is no longer maintained in its own Git
repository. It is now part of
[oc-wasm-rust](https://gitlab.com/Hawk777/oc-wasm-rust).

About
=====

OC-Wasm-Cassette provides a convenient wrapper that makes it easy to use an
`async fn` as a top-level function in an OC-Wasm application.

Usage is as simple as:
```rust
async fn main() -> Infallible {
	// Your code here
}

#[no_mangle]
pub extern "C" fn run(arg: i32) -> i32 {
	oc_wasm_cassette::run(arg, main)
}
```
