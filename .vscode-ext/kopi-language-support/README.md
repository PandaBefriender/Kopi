# Kopi Language Support

Provides syntax highlighting and language support for Kopi programming language files.

## Features

- **Syntax Highlighting**: Color-coded keywords, strings, comments, and operators
- **Icon**: Custom "K" icon for `.kopi` files
- **Language Configuration**: Bracket matching, auto-closing pairs, and comment configuration

## Installation

This extension is included in the Kopi repository. To use it:

1. Copy the `.vscode-ext/kopi-language-support` folder to your VS Code extensions folder
2. Restart VS Code
3. `.kopi` files will now have syntax highlighting and the custom icon

## Supported Syntax

- Keywords: `let`, `def`, `if`, `else`, `while`, `for`, `return`, `break`, `continue`, `true`, `false`
- Built-in functions: `print`, `read`, `len`, `range`, `append`, `int`, `str`
- Comments starting with `#`
- Strings in double quotes
- Numbers
- Operators: `+`, `-`, `*`, `/`, `==`, `!=`, `<`, `>`, `<=`, `>=`, `&&`, `||`
