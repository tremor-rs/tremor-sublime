# ** sublime-syntax **

The `bat` cat replacement uses sublime-syntax files for highlighting.
This project enables highlighting for tremor when using bat through a
minimal sublime IDE support.

## Installation

Create a local syntax directory for the `bat` tool, if needed

```bash
$ mkdir $(bat --config-dir)/syntaxes
$ cd $(bat --config-dir)/syntaxes
```

Sparse download the latest ( main branch ) syntax and save into your local bat syntax directory

```bash
$ wget -O tremor.sublime-syntax Tremor.sublime-syntax https://raw.githubusercontent.com/tremor-rs/tremor-sublime/main/Tremor.sublime-syntax
```

Update your bat syntax cache

```bash
$ bat cache --build
```

Verify bat now understands tremor syntax

```bash
bat --list-languages | rg tremor
TREMOR:tremor,trickle,troy,json
```

You should now have syntax highlighting via bat for the tremor DSLs

```bash
bat /path/to/tremor-runtime/**/**/*.tremor
```
