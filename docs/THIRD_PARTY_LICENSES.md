# Third-Party Licenses

This document enumerates the third-party components included in the fudebako standalone HTML distribution whose licenses require attribution or notice preservation. Full license texts are reproduced in `NOTICES.txt` shipped alongside the HTML artifact.

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

## 4. Optional Python packages (bundle-dependent)

When the distribution includes specific Python packages, their licenses additionally apply. Each package's `LICENSE` and `METADATA` files are reproduced in the accompanying `NOTICES.txt`.

| Package | Upstream license |
|---------|------------------|
| matplotlib | PSF-2.0 AND Matplotlib License |
| numpy | BSD-3-Clause |
| pandas | BSD-3-Clause |
| httpx | BSD-3-Clause |
| micropip | MPL-2.0 |

---

## License summary

All licenses are permissive or file-level weak copyleft. No GPL/LGPL/AGPL.

| License | Type |
|---------|------|
| MIT | Permissive |
| OFL-1.1 | Permissive (fonts) |
| MPL-2.0 | File-level weak copyleft |
| PSF-2.0 | Permissive |
| BSD-3-Clause | Permissive |
| Apache-2.0 | Permissive |

MPL-2.0 does not require the distributing project to be open-sourced; it only requires preservation of notices and, for modified MPL files, release of those modifications under MPL. This distribution does not modify any MPL-licensed files.

## Font license notice

Noto Sans JP and Noto Sans Mono are copyright Google Inc., licensed under the SIL Open Font License, Version 1.1. The full OFL text is in [`licenses/OFL-1.1.txt`](../licenses/OFL-1.1.txt). Canonical source: https://openfontlicense.org/

## Full license texts

Complete license texts for every component listed above are reproduced in `NOTICES.txt` accompanying this distribution.
