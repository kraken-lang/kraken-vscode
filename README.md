<div align="center">
    <img width="auto" height="118" alt="Kraken Language" src="https://raw.githubusercontent.com/kraken-lang/.github/refs/heads/main/images/kraken-logo.png">
    <h1>Kraken Language Support for VS Code</h1>
</div>

Provides rich language support for the [Kraken](https://github.com/kraken-lang/kraken) programming language.

**Version:** `v0.2.0` — Aligned with Kraken language v0.9.2.

## Features

- **Syntax Highlighting** — Full highlighting for `.kr` files
- **Code Snippets** — Quick templates for functions, structs, enums, classes, traits, and control flow
- **Auto-Completion** — Smart bracket, quote, and parenthesis pairing
- **Code Folding** — Collapse and expand code blocks
- **Comment Support** — Line (`//`), block (`/* */`), and doc comments (`///`, `//!`)
- **Attribute Support** — Highlighting for `#[...]` attributes

## Syntax Highlighting

- **Keywords**: `fn`, `let`, `mut`, `const`, `if`, `else`, `while`, `for`, `match`, `return`, `break`, `continue`, `defer`, `struct`, `enum`, `union`, `class`, `interface`, `trait`, `impl`, `type`, `pub`, `import`, `module`, `async`, `await`, `spawn`, `unsafe`, `where`, `static_assert`, `move`, `dyn`, `in`
- **Types**: `int`, `float`, `bool`, `string`, `str`, `bytes`, `void`, `i8`–`i64`, `u8`–`u64`, `f32`, `f64`, `char`
- **Operators**: Arithmetic, comparison, logical, bitwise, assignment, and compound assignment
- **Literals**: Numbers (decimal, hex, binary, octal, float), strings, characters, booleans, `null`
- **Comments**: Line, block, and doc comments
- **Attributes**: `#[...]` annotations
- **Functions**: Function names and declarations

## Code Snippets

Type these prefixes and press Tab to expand:

- `fn` — Function declaration
- `pubfn` — Public function
- `main` — Main function
- `asyncfn` — Async function
- `struct` — Struct definition
- `enum` — Enum definition
- `union` — Union definition
- `class` — Class definition
- `interface` — Interface definition
- `trait` — Trait definition
- `impl` — Impl block
- `if` — If statement
- `ifelse` — If-else statement
- `while` — While loop
- `for` — For loop
- `match` — Match expression
- `let` — Variable declaration
- `letmut` — Mutable variable
- `defer` — Defer block
- `import` — Import declaration
- `module` — Module declaration
- `spawn` — Spawn async task

## Example

```kraken
import std.io;

fn main() -> int {
    let message = "Hello, Kraken!";
    io.println(message);
    return 0;
}
```

## Requirements

No additional requirements. This extension provides editor support only.

To compile Kraken code, you need the [Kraken compiler](https://github.com/kraken-lang/kraken).

## Installation

### From VS Code Marketplace
1. Open VS Code
2. Go to Extensions (Ctrl+Shift+X / Cmd+Shift+X)
3. Search for "Kraken Language"
4. Click Install

### From VSIX
1. Download the `.vsix` file from [Releases](https://github.com/kraken-lang/kraken-vscode/releases)
2. Open VS Code
3. Go to Extensions
4. Click "..." menu → "Install from VSIX"
5. Select the downloaded file

## Development

```bash
npm install
npm run package
code --install-extension kraken-lang-0.2.0.vsix
```

## Contributing

Contributions are welcome. Please submit a Pull Request.

## License

Apache-2.0 — See [LICENSE](LICENSE) for details.

## Links

- [Kraken Language](https://github.com/kraken-lang/kraken)
- [Tree-sitter Grammar](https://github.com/kraken-lang/tree-sitter-kraken)
- [Language Server](https://github.com/kraken-lang/kraken-lsp)
- [Report Issues](https://github.com/kraken-lang/kraken-vscode/issues)