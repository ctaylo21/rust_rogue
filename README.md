# Roguelike in Rust
[Demo](https://ctaylo21.github.io/rust_rogue/)

This is a roguelike game following this [awesome tutorial](https://bfnightly.bracketproductions.com/chapter_0.html).

## Controls
* `w`/`a`/`s`/`d` OR `1-9` keys - movement
* `g` - pick up item
* `i` - inventory

The mouse is used for spells or items that require targeting

## Building for Web (WASM)
To build for Web Assembly, follow the instructions [here](https://bfnightly.bracketproductions.com/webbuild.html).

For this project, to ensure the latest version is avaiable on the demo page (linked above), run:
```
cargo build --release --target wasm32-unknown-unknown
wasm-bindgen target/wasm32-unknown-unknown/release/rogue.wasm --out-dir docs --no-modules --no-typescript
```

Now the current source could will be built for web inside of the `docs` folder as `rogue_bg.wasm` and `rogue.js`.

You can even run it locally using [http-server](https://www.npmjs.com/package/http-server):

```
http-server docs/
```