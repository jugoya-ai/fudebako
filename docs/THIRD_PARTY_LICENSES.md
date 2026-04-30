# Third-Party Licenses

This document enumerates the third-party components included in the fudebako standalone HTML distribution whose licenses require attribution or notice preservation. Full license texts are reproduced in `NOTICES.txt` (or `NOTICES-lite.txt` / `NOTICES-pygame.txt`) shipped alongside the HTML artifact.

The distribution ships in three editions, with overlapping component sets:

- **fudebako-lite**: in-browser runtime + Python runtime + WASM renderer crates
- **fudebako** (default): everything in lite, plus optional Python packages and onnxruntime-web
- **fudebako-pygame**: everything in default, plus **pygame-ce** (LGPL-2.1) and **SDL2** (zlib)

Component coverage per edition is noted in the tables below.

---

## 1. In-browser runtime

Components present in the final standalone HTML and executed in the browser.

| Package | Version | License |
|---------|---------|---------|
| [Tailwind CSS](https://tailwindcss.com/) | 4.2.2 | MIT |
| [Noto Sans JP Variable](https://fontsource.org/fonts/noto-sans-jp) | 5.2.10 | OFL-1.1 |
| [Noto Sans Mono Variable](https://fontsource.org/fonts/noto-sans-mono) | 5.2.10 | OFL-1.1 |

## 2. Python runtime (WebAssembly)

| Package | Version | License |
|---------|---------|---------|
| [Pyodide](https://pyodide.org/) | 0.29.3 | MPL-2.0 |
| [CPython standard library](https://www.python.org/) | 3.13.x | PSF-2.0 |

Pyodide source code is available at https://github.com/pyodide/pyodide (per MPL-2.0 §3.2(b)).

## 3. Rust crates statically linked into the WASM renderer

Compiled code from these crates is included in the standalone HTML artifact.

| Crate | License |
|-------|---------|
| wasm-bindgen | MIT OR Apache-2.0 |
| js-sys | MIT OR Apache-2.0 |
| web-sys | MIT OR Apache-2.0 |
| serde | MIT OR Apache-2.0 |
| serde_json | MIT OR Apache-2.0 |
| serde_repr | MIT OR Apache-2.0 |

## 4. Optional Python packages — default + pygame editions

The default and pygame editions bundle the same set of optional Python packages. Each package's `LICENSE` and `METADATA` files are reproduced in the accompanying `NOTICES.txt` / `NOTICES-pygame.txt`.

| Package | Upstream license |
|---------|------------------|
| numpy | BSD-3-Clause |
| pandas | BSD-3-Clause |
| matplotlib (when bundled) | PSF-2.0 AND Matplotlib License |
| pillow | HPND |
| lxml | BSD-3-Clause |
| cryptography | Apache-2.0 OR BSD-3-Clause |
| pdfplumber | MIT |
| pdfminer.six | MIT |
| charset-normalizer | MIT |
| micropip | MPL-2.0 |
| onnxruntime-web (WASM) | MIT |
| OpenSSL 1.1.1w | OpenSSL License + SSLeay License (dual) |

## 5. SDL graphics stack — pygame edition only

The pygame edition additionally bundles pygame-ce and statically links SDL2. These are present **only** in `fudebako-pygame-vX.Y.Z.html`; the lite and default editions have zero exposure to LGPL-2.1.

| Package | Upstream license |
|---------|------------------|
| pygame-ce | **LGPL-2.1** |
| SDL2 | zlib |

Per LGPL-2.1 §6, complete source code for the shipped pygame-ce version is available at https://github.com/pygame-community/pygame-ce. The full LGPL-2.1 text is reproduced in `NOTICES-pygame.txt`. The SDL2 zlib license text is in [`licenses/SDL2.txt`](../licenses/SDL2.txt). Canonical SDL2 source: https://github.com/libsdl-org/SDL

---

## License summary

| License | Editions | Type |
|---------|----------|------|
| MIT | all | Permissive |
| OFL-1.1 | all | Permissive (fonts) |
| MPL-2.0 | all (Pyodide), default + pygame (micropip) | File-level weak copyleft |
| PSF-2.0 | all (CPython) | Permissive |
| BSD-3-Clause | default + pygame (numpy / pandas / lxml) | Permissive |
| Apache-2.0 | default + pygame (cryptography) | Permissive |
| HPND | default + pygame (pillow) | Permissive |
| OpenSSL + SSLeay (dual) | default + pygame (OpenSSL) | Permissive |
| **LGPL-2.1** | **pygame only** (pygame-ce) | **Weak copyleft** |
| zlib | pygame only (SDL2) | Permissive |

**fudebako-lite** and **fudebako** (default) ship under permissive / weak-file-copyleft licenses only — no LGPL/GPL/AGPL exposure.

**fudebako-pygame** introduces LGPL-2.1 via pygame-ce. End users who redistribute or modify the pygame edition must preserve the LGPL-2.1 obligations (notice preservation and source availability for the pygame-ce component).

MPL-2.0 does not require the distributing project to be open-sourced; it only requires preservation of notices and, for modified MPL files, release of those modifications under MPL. This distribution does not modify any MPL-licensed files.

## Font license notice

Noto Sans JP and Noto Sans Mono are copyright Google Inc., licensed under the SIL Open Font License, Version 1.1. The full OFL text is in [`licenses/OFL-1.1.txt`](../licenses/OFL-1.1.txt). Canonical source: https://openfontlicense.org/

## Full license texts

Complete license texts for every component listed above are reproduced in `NOTICES.txt` (default), `NOTICES-lite.txt` (lite), or `NOTICES-pygame.txt` (pygame) accompanying each edition's HTML artifact.
