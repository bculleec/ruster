# ruster
The most cracked web based raster editor written in Rust, WebAssembly and JavaScript.

## Introduction
Rust and WASM live inside a linear memory buffer. JavaScript lives outside that buffer. They cannot see each other's memory.

For this raster editor to work, we need to allocate a pixel buffer in WASM, and let JS render that buffer by reading from the shared linear memory.

## Why Rust
Rust provides reliable performance on WASM. Moreover, the produced .wasm file from Rust is extremely lean. You get low-level control with a wide choice of modern libraries.
