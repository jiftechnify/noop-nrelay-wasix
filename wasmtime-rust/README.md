# Nostr no-op relay for Wasmtime (in Rust)

## How to Build and Run
Prerequisite: Rust programming environment (`rustc`, `cargo`, `rustup`) has been installed.

1. [Install Wasmtime](https://wasmtime.dev/).
2. Add `wasm32-wasi` target to the Rust compiler.

```bash
rustup target add wasm32-wasi
```

3. Build and run the Wasm module by following commands: 

```bash
cargo build --target wasm32-wasi --release
wasmtime run -S preview2=n,tcplisten=127.0.0.1:9876 target/wasm32-wasi/release/noop-nrelay-wasmtime.wasm
```
