This repo is uploaded on behalf of [@SteinsGateON](https://space.bilibili.com/34714121).

# TH08 portable

This repository contains the source-only TH08 3.4.0 C++/SDL3 portable and Web implementation.

## Layout

- `th08_web/`: TH08 game, SDL runtime, documentation, and source tests.
- `th10_web/launcher/`: the shared Eagler Touhou launcher and browser package subsystem used by TH08.
- `portable/`: shared GLES renderer, numeric compatibility code, input code, build orchestration, and validation tools.
- `tools/`: the pinned Emscripten installer and its metadata.

## Build

Install the pinned toolchain, then build the browser runtime:

```powershell
python tools/download-emscripten.py
node portable/build.mjs --th08
```

Build outputs are written below `th08_web/artifacts/` and are intentionally not tracked.

## Assets and licensing

This repository does not include original Touhou executable, data, music, replay, or save files. A runnable package must be assembled locally from files you are legally allowed to use.

## License

This project is licensed under the MIT License.
