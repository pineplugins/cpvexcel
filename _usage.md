# Usage 

on this page i will show how the government works well

## command list
| Command | Description | Options and Flags |
| -------------------- | ------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `-v`, `--version` | Displays the application version. | - |
| `--docs` | Displays the documentation location. | - |
| `--lic`, `--license` | Displays the application license. | - |
| `pr` | Process `.cpvxclrc` file from URL or local path. | `mode` (url/pth) - Specifies the input mode, `value` - Link URL or local file path. |
| `dw` | Download and extract the ZIP file to the `data/` folder. | `-url` - Direct link to the ZIP file (raw link). |
| `tree` | Displays the folder structure. | - |

### `pr` Command Details:

* `pr url <value>`: Uses a URL to process the `.cpvxclrc` file.
* `pr pth <value>`: Uses a local path to process the `.cpvxclrc` file.

### `dw` Command Details:

* `dw -url <URL>`: Downloads and extracts a ZIP file from the given URL into the `data/` folder.

---

## Examplr use and respon

- help
```term
$ cpvx -h
usage: cpvx [-h] [-v] [--docs] [--lic] {pr,dw,tree} ...

PNXCL - Plugin Excel CLI

positional arguments:
  {pr,dw,tree}
    pr              Proses file .cpvxclrc dari URL atau path
    dw              Download dan ekstrak ZIP ke folder data/
    tree            Tampilkan struktur folder

options:
  -h, --help        show this help message and exit
  -v, --version     show program's version number and exit
  --docs            Tampilkan lokasi dokumentasi
  --lic, --license  Tampilkan lisensi
```
- verison

```term
$ cpvx -v
cpvx v1.0.0
$ cpvx --version
cpvx v1.0.0
```

- readocs
```term
$ cpvx --docs
📚 Dokumentasi: https://pineplugins.github.io/cpvexcel/
```

- license
```term
$ cpvx --license 
# or
$ cpvx --lic
MIT License

Copyright (c) 2025 pineplugin

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

- proces 
`# cpvx pr [mode] [value]`
```term
$ cpvx pr url https://raw.githubusercontent.com/pineplugins/cpvexcel/refs/heads/main/test/question1.cpvxclrc
Nilai berhasil disalin ke clipboard.
$ cpvx pr pth data/bab1/question1.cpvxclrc
Nilai berhasil disalin ke clipboard.
```

- download question or another files

```term
# cpvx dw -url [URL]
$ cpvx dw -url https://github.com/pineplugins/cpvexcel/raw/main/test/bab1.zip
ZIP berhasil diekstrak ke folder '/home/ridwan/plugin/pnexcel-plugin/src/cpvexcel/data'
```
- tree

```term
$ cpvx tree
data/
│   ├── bab1/
│   │   └── question1.cpvxclrc
```