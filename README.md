# 📘 JavaScript Fundamentals

This repository contains a series of beginner-level JavaScript scripts. Each file demonstrates a specific concept in JavaScript such as working with command-line arguments, loops, functions, recursion, and data type conversions. These exercises are designed to be run using Node.js and help build a strong foundation in JS programming.

## 🧠 Difficulty Table

| File                        | Description                                | Difficulty |
|----------------------------|--------------------------------------------|------------|
| `1-multi_languages.js`     | Print 3 lines directly                     | 🟢 Easy    |
| `2-arguments.js`           | Count command-line arguments               | 🟢 Easy    |
| `3-value_argument.js`      | Print first argument                       | 🟢 Easy    |
| `4-concat.js`              | Concatenate two arguments                  | 🟢 Easy    |
| `5-to_integer.js`          | Convert input to integer                   | 🟡 Medium  |
| `6-multi_languages_loop.js`| Print multiple lines using loop + array    | 🟡 Medium  |
| `7-multi_c.js`             | Loop print based on input count            | 🟡 Medium  |
| `8-square.js`              | Print a square of `X`                      | 🟡 Medium  |
| `9-add.js`                 | Add two numbers using a function           | 🟢 Easy    |
| `10-factorial.js`          | Recursive factorial function               | 🔴 Hard    |

> 🟢 Easy – Basic syntax and printing  
> 🟡 Medium – Requires understanding of loops, type conversion  
> 🔴 Hard – Uses recursion and base cases

...

## 📂 File Descriptions

### `1-multi_languages.js`
Prints 3 lines directly using `console.log()`:

---

### `2-arguments.js`
Prints a message depending on the number of command-line arguments passed:
- Prints `"No argument"` if no argument is passed.
- Prints `"Argument found"` if only one argument is passed.
- Prints `"Arguments found"` if more than one argument is passed.

> 🔍 **Explanation**:
> - `process.argv` is an array that stores command-line arguments.
> - The actual arguments start from index `2`, so we use `process.argv.length - 2`.

---

### `3-value_argument.js`
Prints the first argument passed to the script. If no argument is provided, it prints `"No argument"`.

---

### `4-concat.js`
Prints a sentence combining two arguments:
If arguments are missing, it prints `undefined is undefined`.

---

### `5-to_integer.js`
Checks if the first argument can be converted to an integer:
- If so, prints: `My number: <converted number>`
- Otherwise, prints: `Not a number`

> 🔍 **Explanation**:
> - Uses `parseInt()` to convert the argument to an integer.
> - If the result is `NaN`, the input was not a valid number.

---

### `6-multi_languages_loop.js`
Prints the same three lines from file 1, but using:
- An array of strings
- A loop (`for` or `while`)
- Only one `console.log` call inside the loop

---

### `7-multi_c.js`
Prints "C is fun" as many times as specified by the first argument.
- If no valid integer is provided, it prints: `Missing number of occurrences`.

---

### `8-square.js`
Prints a square of `"X"` characters where the size is defined by the first argument.

Example (size = 2):

- If the argument is not a valid integer, it prints: `Missing size`.

---

### `9-add.js`
Adds two numbers passed as arguments and prints the result.

```js
function add(a, b) {
  return a + b;
}
$ node 9-add.js 5 7
12
```

### `10-factorial.js`

Computes and prints the factorial of a number **recursively**.

- `factorial(3)` returns `6` (`3 * 2 * 1`)
- If the input is not a number, prints `1` (by definition)

> 🔍 **What is recursion?**  
> A function that calls itself with a smaller/simpler input, until a base case is reached.

---
## Notes on Difficult Parts

- **Recursive function in `10-factorial.js`:**  
  This function calls itself with a decremented value until it reaches 1 or a non-number input, at which point it stops and returns 1. This is a common pattern in recursion problems.

- **Handling of command-line arguments:**  
  Most scripts use `process.argv` array but avoid using `.length` or `var` as per instructions, which requires careful indexing and checking.

- **Type conversion without try/catch:**  
  In scripts like `5-to_integer.js` and `7-multi_c.js`, input strings are converted to integers using `parseInt` and validated using `isNaN`, which is a safe way to validate numbers without exceptions.

---
