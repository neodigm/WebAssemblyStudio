# "Hello, World!" Rust Project

This is a sample Rust project which uses the [`wasm_bindgen` crate][crate] to
enable richer interactions between Rust and JS such as communicating with
strings rather than just numbers.

Typically `wasm-bindgen` is paired with a bundler but here we're not using a
bundler so you can poke around all the raw output!

Some files you may be interested in are:

* `lib.rs` - this is the main body of Rust code, annotated with
  `#[wasm_bindgen]` to have its functionality exported to JS.
* `main.js` - this is the application's supporting JS, automatically run by
  `main.html`. Here you'll import items implemented in Rust through the
  `wasmBindgen` global.

When building the project you'll get `out/main_bg.wasm`, the generated wasm
filtered through the `wasm-bindgen` CLI tool, as well as `out/main.js` which is
an auxiliary JS file generated by the `wasm-bindgen` tool, included by default
in `main.html`. The `out/main.js` file is responsible for creating the
`wasmBindgen` global and filling it in.

[crate]: https://github.com/rustwasm/wasm-bindgen
