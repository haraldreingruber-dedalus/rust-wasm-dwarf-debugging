# Rust+WebAssembly debugging demo

This example is based on the official Rust+Wasm Hello World example: https://rustwasm.github.io/docs/book/game-of-life/hello-world.html

## Prerequisites

- Install `wasm-pack`: https://rustwasm.github.io/wasm-pack/
- Install [Chrome DevTools C++ DWARF debugging](https://chromewebstore.google.com/detail/cc++-devtools-support-dwa/pdcpmagijalfljmkmjngeonclgbbannb) extension

## Build and run demo with DWARF debug symbols

Run the demo app:

    wasm-pack build --dev
    cd www
    npm run start

Open Chrome DevTools

- Go to "Sources" tab
- Open "file://\<your repo path\>/src/lib.rs"
- Set a breakpoint in line 12

  `alert("Hello, wasm-debug-dwarf!");`

- Reload the page and verify the DevTools debugger breaks as expected.
- 🚀 Congrats, you are ready to debug Rust+WebAssembly in the browser!
