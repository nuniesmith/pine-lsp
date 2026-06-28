# pine-lsp

A language server for [TradingView Pine Script v6](https://www.tradingview.com/pine-script-docs/),
providing diagnostics, hover documentation, and completions.

It powers the [Pine Script extension for the Zed editor](https://github.com/nuniesmith/pine-script-zed),
but speaks standard LSP over stdio and can be used with any LSP-capable editor.

## Features

- **Diagnostics** — parse errors and lint warnings
- **Hover docs** — documentation for built-in functions and variables
- **Completions** — keywords, built-in functions, and variables

## Installation

### From a release

Download the archive for your platform from the
[releases page](https://github.com/nuniesmith/pine-lsp/releases) and place the
`pine-lsp` binary on your `PATH`.

### From source

```sh
cargo install --git https://github.com/nuniesmith/pine-lsp pine-lsp
```

## Usage

```sh
pine-lsp                 # Start the LSP server (stdio transport)
pine-lsp --check <file>  # Parse and lint a .pine file, printing diagnostics
pine-lsp --version       # Print the version
pine-lsp --help          # Show usage
```

When used with the Zed extension, the extension launches `pine-lsp` for you and
will download a release automatically if it isn't already on your `PATH`.

## Releases

Tagging a commit with a `v*` tag (e.g. `v0.1.0`) triggers the release workflow,
which builds binaries for Linux, macOS, and Windows and attaches them to a
GitHub release. The asset names match what the Zed extension expects:

- `pine-lsp-x86_64-unknown-linux-gnu.tar.gz`
- `pine-lsp-aarch64-apple-darwin.tar.gz`
- `pine-lsp-x86_64-apple-darwin.tar.gz`
- `pine-lsp-x86_64-pc-windows-msvc.zip`

## License

Released under the [MIT License](LICENSE).
