<div align="center">
    <img width="auto" height="118" alt="Kraken Language" src="https://raw.githubusercontent.com/kraken-lang/.github/refs/heads/main/images/kraken-logo.png">
    <h1>Kraken Language Support for VS Code</h1>
</div>

## Features

Provides rich language support for the Kraken programming language, including:

- **Syntax Highlighting** - Full syntax highlighting for `.kr` and `.krak` files
- **Code Snippets** - Quick templates for functions, structs, classes, and control flow
- **Auto-Completion** - Smart bracket, quote, and parenthesis pairing
- **Code Folding** - Collapse and expand code blocks
- **Comment Support** - Line (`//`) and block (`/* */`) comments

## Syntax Highlighting

The extension provides comprehensive syntax highlighting for:

- **Keywords**: `fn`, `let`, `mut`, `if`, `else`, `while`, `for`, `match`, `struct`, `class`, `interface`, `async`, `await`
- **Types**: `int`, `float`, `bool`, `string`, `void`, `i8`, `i16`, `i32`, `i64`, `u8`, `u16`, `u32`, `u64`, `f32`, `f64`
- **Operators**: Arithmetic, comparison, logical, bitwise, and assignment operators
- **Literals**: Numbers (decimal, hex, binary, octal, float), strings, booleans
- **Comments**: Line and block comments
- **Functions**: Function names and declarations

## Code Snippets

Type these prefixes and press Tab to expand:

- `fn` - Function declaration
- `main` - Main function
- `struct` - Struct definition
- `class` - Class definition
- `interface` - Interface definition
- `if` - If statement
- `ifelse` - If-else statement
- `while` - While loop
- `for` - For loop
- `match` - Match statement
- `let` - Variable declaration
- `letmut` - Mutable variable
- `asyncfn` - Async function

## Example

```kraken
fn main() -> int {
    let message = "Hello, Kraken!";
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
1. Download the `.vsix` file
2. Open VS Code
3. Go to Extensions
4. Click "..." menu → "Install from VSIX"
5. Select the downloaded file

## Development

To work on this extension:

```bash
# Install dependencies
npm install

# Package the extension
npm run package

# Install locally
code --install-extension kraken-lang-0.1.0.vsix
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License - See LICENSE file for details

## Links

- [Kraken Language Repository](https://github.com/kraken-lang/kraken)
- [VS Code Extension Repository](https://github.com/kraken-lang/kraken-vscode)
- [Report Issues](https://github.com/kraken-lang/kraken-vscode/issues)

## Release Notes

See [CHANGELOG.md](CHANGELOG.md) for details.