# Kopi

Kopi is a tiny, simple programming language built for learning and experimenting. It is meant to be easy to read, easy to change, and easy to understand.

## What Kopi is for

- Learn how a language works by reading the source code.
- Experiment with new ideas like functions, loops, and simple control flow.
- Build short programs without getting lost in complex syntax.
- Share ideas and grow a small community around language design.

## Run Kopi

Use the interpreter with a `.kopi` file:

```bash
./kopi run examples/basics.kopi
```

Or use Python directly:

```bash
python3 main.kopi examples/basics.kopi
```

### Making `kopi` available globally

To use `kopi run` from anywhere, add the Kopi directory to your PATH:

```bash
export PATH="$PATH:/path/to/Kopi"
```

Then you can run:

```bash
kopi run path/to/file.kopi
```

## What you can write in Kopi

### Values

- Strings are written with double quotes:
  - `"Hello, Kopi!"`
- Numbers are written normally:
  - `42`
  - `-5`
- Booleans are written as `true` or `false`.
- Lists are written with square brackets:
  - `[1, 2, 3]`
  - `["one", "two", "three"]`

### Variables

Use `let` to create a new name for a value:

```kopi
let count = 3
```

Change a value later using `=`:

```kopi
count = count + 1
```

### Print to the screen

Use `print(...)` to show values:

```kopi
print("Hello, world!")
print(count)
```

### Read from the user

Use `read(...)` to ask the user for input and store their answer:

```kopi
let name = read("What is your name? ")
print("Hello, " + name)
```

### Functions

A function is a named block of code that can use values and return a result:

```kopi
def add(a, b) {
    return a + b
}

let total = add(5, 7)
print(total)
```

### Loops

Use `while` to repeat code until a condition becomes false:

```kopi
let count = 1
while (count <= 5) {
    print(count)
    count = count + 1
}
```

Use `for` to loop with a start, condition, and change:

```kopi
for (let i = 0; i < 5; i = i + 1) {
    print(i)
}
```

Use `break` and `continue` to control loop flow:

```kopi
for (let i = 0; i < 5; i = i + 1) {
    if (i == 2) {
        continue
    }
    if (i == 4) {
        break
    }
    print(i)
}
```

### Lists and indexing

Access list items using `[...]` and find size with `len(...)`:

```kopi
let items = ["red", "green", "blue"]
print(items[0])
print(len(items))
```

Modify a list with `append(...)`:

```kopi
let numbers = [1, 2]
append(numbers, 3)
print(numbers)
```

### Useful built-in functions

- `len(value)` — number of items in a list or length of a string
- `range(n)` — list of numbers from `0` to `n-1`
- `range(a, b)` — list of numbers from `a` to `b-1`
- `range(a, b, step)` — list by step
- `append(list, value)` — add a value to a list
- `int(value)` — convert a string to a number
- `str(value)` — convert a value to text

### Conditionals

Use `if` and `else` to run different code paths:

```kopi
let score = 10
if (score > 5) {
    print("Great job")
} else {
    print("Keep trying")
}
```

### Comments

Add comments with `#`:

```kopi
# This is a note for people reading the code
let message = "Hello"
```

## Syntax highlighting in VS Code

Kopi files use `.kopi` as the extension. A basic VS Code workspace setting is included so VS Code can treat `.kopi` files like JavaScript and color-code them for easier reading.

## Example lesson: `examples/basics.kopi`

This interactive lesson teaches you the basics of Kopi by having you type in your own values! Run it and follow along:

```bash
python3 main.kopi examples/basics.kopi
```

The lesson covers:
- Variables and storing user input
- Loops that run multiple times
- Conditionals that make choices
- Functions that hold reusable code

Each section prompts you to enter information, then uses it in the code.

For a second example that shows lists, `for` loops, built-ins like `len()` and `range()`, and list indexing, run:

```bash
python3 main.kopi examples/advanced.kopi
```

## How Kopi works

- `main.kopi` reads your file and sends it to the lexer, parser, and runtime.
- `lexer.kopi` turns text into small parts called tokens.
- `parser.kopi` turns tokens into a tree of statements and expressions.
- `runtime.kopi` runs that tree and produces output.

## Want to help?

Kopi is best when people try new features and share what works.

- Add more lessons in `examples/`
- Try adding `for` loops or `else if`
- Improve error messages when the code is wrong
- Share your ideas for new Kopi syntax
