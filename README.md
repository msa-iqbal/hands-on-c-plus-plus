# Hands-on C

C is a general-purpose, procedural, and case-sensitive programming language developed in the early 1970s by Dennis Ritchie at Bell Labs. It is considered one of the most influential languages in computer science history and is often referred to as the "mother of all modern programming languages."

## Table of Contents

1. [Introduction](#introduction)
1. [Comments in C](#comments-in-c)
1. [Keywords in C](#keywords-in-c)
1. [Escape sequences](#escape-sequences)
1. [Variables](#variables)
1. [Input and Output](#input-and-output)
1. [Data Types & Format Specifiers](#data-types--format-specifiers)
1. [Operators](#operators)
1. [Control Structures](#control-structures)
1. [Function](#function)
1. [String](#string)
1. [Array](#array)
1. [Pointers](#pointers)
1. [Structure, Union and Enum](#structure-union-and-enum)
1. [Dynamic Memory Allocation](#dynamic-memory-allocation)
1. [Typedef and Type Casting](#typedef-and-type-casting)
1. [File Handling](#file-handling)
1. [Preprocessor Directives](#preprocessor-directives)
1. [Error Handling](#error-handling)
1. [Practice Problems and Solutions](#practice-problems-and-solutions)

### <img src="https://fonts.gstatic.com/s/e/notoemoji/latest/2699_fe0f/512.gif" alt="⚙" width="15" height="15"> C/C++ Development Setup

**Recommended Tools**

- **Editor**: [Visual Studio Code](https://code.visualstudio.com/) with the official [C/C++ Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)
- **IDE**: [Code::Blocks](http://www.codeblocks.org/) — preconfigured and suitable for beginners
- **Online Compiler**: [CodeChef IDE](https://www.codechef.com/ide) — for quick practice and testing

---

## Introduction

### Key Features

- **Procedural Language:** Emphasizes functions and step-by-step procedures.

- **Low-level Access:** Offers direct memory manipulation using pointers.

- **Portability:** C programs can be compiled and run on many types of machines with minimal changes.

- **Efficient Performance:** Known for its speed and close-to-hardware behavior.

- **Rich Library Support:** Comes with a standard library for I/O, string manipulation, memory allocation, etc.

- **Modular Code:** Code can be organized into functions for reusability and clarity.

### Why C is Important

- **Foundation Language:** Languages like C++, Java, C#, and even Python are influenced by C.

- **Operating Systems:** Core components of OSs like Linux, Windows, and macOS are written in C.

- **Embedded Systems:** Used extensively in firmware and microcontroller programming.

- **Compilers & Interpreters:** Many compilers (e.g., GCC) and interpreters are themselves written in C.

### Basic Example

```c
#include <stdio.h>

int main() {
    printf("Hello, World!\n");
    return 0;
}
```

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Comments in C

In **C language**, comments are used to explain the code and make it more readable. Comments are ignored by the compiler, so they don’t affect program execution.

**Single-line Comment:**

```c
// This is a single-line comment
int x = 10;  // This sets x to 10
```

**Multi-line Comment:**

```c
/* This is a multi-line comment
   It can span multiple lines
*/
int y = 20;
```

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Keywords in C

Keywords are reserved words in C language that have special, predefined meanings. They cannot be used as identifiers, such as variable names, function names, or label names, because they are an essential part of the C syntax and grammar.

**C language keyword list (based on the C99 standard, which is very widely used):**

| No. | Keyword    | No. | Keyword    | No. | Keyword    | No. | Keyword          |
| --: | ---------- | --: | ---------- | --: | ---------- | --: | ---------------- |
|   1 | `auto`     |  14 | `for`      |  27 | `long`     |  40 | `void`           |
|   2 | `break`    |  15 | `goto`     |  28 | `register` |  41 | `volatile`       |
|   3 | `case`     |  16 | `if`       |  29 | `restrict` |  42 | `while`          |
|   4 | `char`     |  17 | `inline`   |  30 | `return`   |  43 | `_Bool`          |
|   5 | `const`    |  18 | `int`      |  31 | `short`    |  44 | `_Complex`       |
|   6 | `continue` |  19 | `long`     |  32 | `signed`   |  45 | `_Imaginary`     |
|   7 | `default`  |  20 | `restrict` |  33 | `sizeof`   |  46 | `_Alignas`       |
|   8 | `do`       |  21 | `signed`   |  34 | `static`   |  47 | `_Alignof`       |
|   9 | `double`   |  22 | `sizeof`   |  35 | `struct`   |  48 | `_Atomic`        |
|  10 | `else`     |  23 | `static`   |  36 | `switch`   |  49 | `_Generic`       |
|  11 | `enum`     |  24 | `struct`   |  37 | `typedef`  |  50 | `_Noreturn`      |
|  12 | `extern`   |  25 | `typedef`  |  38 | `union`    |  51 | `_Static_assert` |
|  13 | `float`    |  26 | `union`    |  39 | `unsigned` |  52 | `_Thread_local`  |

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Escape sequences

Escape sequences (also known as **backslash character constants**) are special character combinations that begin with a backslash (`\`). They are used to represent characters that cannot be typed directly or have special meaning in strings or characters.

**List of Common Escape Sequences:**

| Escape Sequence | Meaning                           | Example in Code              | Output          |
| --------------- | --------------------------------- | ---------------------------- | --------------- |
| `\n`            | New line                          | `printf("Hello\nWorld");`    | Hello<br>World  |
| `\t`            | Horizontal tab                    | `printf("Hello\tWorld");`    | Hello  World    |
| `\b`            | Backspace                         | `printf("Helloo\b!");`       | Hello!          |
| `\r`            | Carriage return                   | `printf("Hello\rWorld");`    | World           |
| `\f`            | Form feed (page break)            | _Rarely used_                | —               |
| `\a`            | Alert (bell sound)                | `printf("\a");`              | 🔔 (beep sound) |
| `\\`            | Backslash                         | `printf("\\");`              | `\`             |
| `\'`            | Single quote                      | `printf("\'");`              | `'`             |
| `\"`            | Double quote                      | `printf("\"");`              | `"`             |
| `\?`            | Question mark                     | `printf("\?");`              | `?`             |
| `\0`            | Null character (end of string)    | _Used in string terminators_ | —               |
| `\ooo`          | Octal number (e.g., `\141` = 'a') | `printf("\141");`            | `a`             |
| `\xhh`          | Hexadecimal (e.g., `\x61` = 'a')  | `printf("\x61");`            | `a`             |

**Example:**

```c
#include <stdio.h>

int main() {
    printf("Line1\nLine2\n");      // newline
    printf("Tab\tSpace\n");        // tab
    printf("Backslash: \\\n");     // backslash
    printf("Quote: \' \" \n");     // single and double quote
    printf("Beep\a\n");            // beep (if supported)
    return 0;
}
```

> [!NOTE]
>
> - Escape sequences are used in both **character** (`'\n'`) and **string** (`"\n"`) literals.
> - They are vital for **text formatting**, **controlling output**, and representing special characters.
> - Some (like `\f`, `\a`) may not have visible effects in modern terminals, but they are still standard.

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Variables

A **variable** is a **named memory location** used to store a value that can be changed during program execution.

- Acts as a **storage unit** for data.
- Must be **declared** with a data type before use.
- The value of a variable **can be changed** during program execution.

**Syntax:**

```c
<data_type> <variable_name>;
<data_type> <variable_name> = value;
```

**Example:**

```c
int age;         // Declaration
age = 25;        // Assignment
float pi = 3.14; // Declaration + Assignment
```

### Rules for Naming Variables

| Rule No. | Rule                                                            |
| -------: | --------------------------------------------------------------- |
|        1 | Must begin with a **letter** (A–Z or a–z) or **underscore `_`** |
|        2 | Can include **letters, digits (0–9), and underscores**          |
|        3 | **Cannot start with a digit**                                   |
|        4 | **Cannot use C keywords** (like `int`, `return`, etc.)          |
|        5 | **Case-sensitive** (`Age` and `age` are different)              |
|        6 | Should be **meaningful** (use descriptive names)                |

### Types of Variables

| Type         | Description                                                     | Scope          |
| ------------ | --------------------------------------------------------------- | -------------- |
| **Local**    | Declared inside a function/block                                | Function/block |
| **Global**   | Declared outside all functions, accessible by all functions     | Whole program  |
| **Static**   | Retains value between function calls, has local scope           | Block/function |
| **Extern**   | Declared in one file, defined in another file (shared globally) | Global         |
| **Register** | Suggests storing variable in a CPU register (faster access)     | Local          |

**Example (Different Variable Types):**

```c
#include <stdio.h>

int globalVar = 10; // Global variable

void function() {
    static int staticVar = 0; // Static variable
    staticVar++;
    printf("Static: %d\n", staticVar);
}

int main() {
    int localVar = 5; // Local variable

    printf("Global: %d\n", globalVar);
    printf("Local: %d\n", localVar);

    function();
    function();

    return 0;
}
```

**Output:**

```markdown
Global: 10
Local: 5
Static: 1
Static: 2
```

**Example - ✅ Good Practice:**

```c
int studentAge = 20;
float temperature = 36.6;
char grade = 'A';
```

### Constants vs Variables

| Feature      | Variable                    | Constant                     |
| ------------ | --------------------------- | ---------------------------- |
| Value change | Can change during execution | Cannot change after assigned |
| Declaration  | `int age = 20;`             | `const int age = 20;`        |

> [!TIP]
>
> - Variable values are stored in **RAM**.
> - Use `const` for **read-only** values.
> - Initialize variables to **avoid garbage values**.
> - Use meaningful names for better **code readability**.

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Input and Output

C uses **standard input/output functions** provided by the `stdio.h` header file for data communication between the user and the program.

**Header File:**

```c
#include <stdio.h>
```

All input/output operations in C require the `stdio.h` header file.

### Output

**`printf()` – Formatted Output**

- Used to display output to the screen.
- Supports format specifiers like `%d`, `%f`, `%c`, etc.

**Syntax:**

```c
printf("format string", variables);
```

**Example:**

```c
int age = 20;
printf("Age is %d", age);  // Output: Age is 20
```

### Input

**`scanf()` – Formatted Input**

- Used to read input from the user.
- Requires **address-of operator (`&`)** for variables (except strings).

**Syntax:**

```c
scanf("format string", &variables);
```

**Example:**

```c
int age;
scanf("%d", &age);
```

### Format Specifiers (Common)

| Data Type      | Format Specifier | Used With         |
| -------------- | ---------------- | ----------------- |
| `int`          | `%d`, `%i`       | `scanf`, `printf` |
| `float`        | `%f`             | `scanf`, `printf` |
| `double`       | `%lf`            | `scanf`, `printf` |
| `char`         | `%c`             | `scanf`, `printf` |
| `string`       | `%s`             | `scanf`, `printf` |
| `unsigned int` | `%u`             | `scanf`, `printf` |
| `long int`     | `%ld`            | `scanf`, `printf` |
| `pointer`      | `%p`             | `printf` only     |

**Example (Input and Output Program):**

```c
#include <stdio.h>

int main() {
    int age;
    float salary;
    char initial;
    char name[50];

    // Input
    printf("Enter your age: ");
    scanf("%d", &age);

    printf("Enter your salary: ");
    scanf("%f", &salary);

    printf("Enter your first initial: ");
    scanf(" %c", &initial);  // Space before %c to ignore newline

    printf("Enter your name: ");
    scanf("%s", name);  // no & for string input

    // Output
    printf("\n--- OUTPUT ---\n");
    printf("Age: %d\n", age);
    printf("Salary: %.2f\n", salary);
    printf("Initial: %c\n", initial);
    printf("Name: %s\n", name);

    return 0;
}
```

### Other I/O Functions

| Function    | Purpose                           |
| ----------- | --------------------------------- |
| `getchar()` | Reads a single character          |
| `putchar()` | Outputs a single character        |
| `gets()`    | Reads a string (⚠️ unsafe, avoid) |
| `puts()`    | Outputs a string with newline     |
| `fgets()`   | Reads a string safely (preferred) |
| `fprintf()` | Outputs to a file stream          |
| `fscanf()`  | Inputs from a file stream         |

**Example: `fgets()` and `puts()`**

```c
char name[100];
printf("Enter your full name: ");
fgets(name, sizeof(name), stdin);
puts("Hello,");
puts(name);
```

> [!NOTE]
>
> - `scanf("%s", str)` reads only a **single word** (no spaces). Use `fgets()` for full-line input.
> - `printf()` does not require the address-of operator.
> - Be careful with buffer issues when mixing `scanf()` with `gets()` or `fgets()`.

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Data Types & Format Specifiers

**Data types** specify the type of data a variable can hold. Different **format specifiers** are used in **printf** and **scanf** to handle the input and output of these data types.

**Basic Data Types:**

- **`char`**: Stores a single character.
  - Size: 1 byte
  - Range: `-128` to `127` (signed) or `0` to `255` (unsigned)
- **`int`**: Stores integer values.

  - Size: 2 or 4 bytes (depending on system architecture)
  - Range: `-32,768` to `32,767` (16-bit) or `-2^31` to `2^31 - 1` (32-bit)

- **`float`**: Stores single-precision floating point numbers.

  - Size: 4 bytes
  - Range: `1.2E-38` to `3.4E+38`

- **`double`**: Stores double-precision floating point numbers.

  - Size: 8 bytes
  - Range: `2.3E-308` to `1.7E+308`

- **`void`**: Represents an absence of data. It is used in functions that do not return a value.

**Derived Data Types:**

- **`array`**: Collection of elements of the same type.
- **`pointer`**: A variable that stores the memory address of another variable.
- **`struct`**: Collection of variables of different data types.
- **`union`**: Collection of variables that share the same memory location.
- **`enum`**: A user-defined data type with a set of named integer constants.

### **Modifiers**

Modifiers alter the range of fundamental data types.

- **`signed`**: Allows negative numbers.
- **`unsigned`**: Disallows negative numbers, expanding the positive range.
- **`long`**: Increases the range of `int` and `double`.
- **`short`**: Reduces the size of `int` to save memory.

### **Format Specifiers in C**

**For `printf` (Output)**

| Data Type      | Format Specifier | Example                      | Output         |
| -------------- | ---------------- | ---------------------------- | -------------- |
| `char`         | `%c`             | `printf("%c", 'A');`         | A              |
| `int`          | `%d`, `%i`       | `printf("%d", 25);`          | 25             |
| `float`        | `%f`             | `printf("%f", 3.14);`        | 3.140000       |
| `double`       | `%lf`            | `printf("%lf", 3.141592);`   | 3.141592       |
| `unsigned int` | `%u`             | `printf("%u", 123);`         | 123            |
| `long`         | `%ld`            | `printf("%ld", 1234567890);` | 1234567890     |
| `short`        | `%hd`            | `printf("%hd", 25);`         | 25             |
| `string`       | `%s`             | `printf("%s", "Hello");`     | Hello          |
| `pointer`      | `%p`             | `printf("%p", &x);`          | 0x7ffdfd9cdbd0 |

**For `scanf` (Input)**

| Data Type      | Format Specifier | Example               |
| -------------- | ---------------- | --------------------- |
| `char`         | `%c`             | `scanf("%c", &ch);`   |
| `int`          | `%d`, `%i`       | `scanf("%d", &num);`  |
| `float`        | `%f`             | `scanf("%f", &num);`  |
| `double`       | `%lf`            | `scanf("%lf", &num);` |
| `unsigned int` | `%u`             | `scanf("%u", &num);`  |
| `long`         | `%ld`            | `scanf("%ld", &num);` |
| `short`        | `%hd`            | `scanf("%hd", &num);` |
| `string`       | `%s`             | `scanf("%s", str);`   |
| `pointer`      | `%p`             | `scanf("%p", &ptr);`  |

**Example:**

```c
#include <stdio.h>

int main() {
    int x = 10;
    float pi = 3.14159;

    // Using format specifiers
    printf("Integer: %d\n", x);   // %d for int
    printf("Float: %f\n", pi);    // %f for float
    printf("Pointer: %p\n", &x);  // %p for pointer
    return 0;
}
```

> [!NOTE]
>
> - `%d` and `%i` can be used interchangeably for integers in **printf** and **scanf**.
> - `%lf` is used for **double** in **printf** but can be used as `%f` in **scanf**.
> - The `long` and `short` modifiers help control the size and range of data types in C.
> - The `%p` specifier is used to print the address of a variable (pointer).

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Operators

Operators in C are **symbols** used to perform operations on **variables and values**.

**Types of Operators:**

### **Arithmetic Operators**

Used for mathematical operations.

| Operator | Meaning             | Example | Result       |
| -------- | ------------------- | ------- | ------------ |
| `+`      | Addition            | `a + b` | 10 + 5 = 15  |
| `-`      | Subtraction         | `a - b` | 10 - 5 = 5   |
| `*`      | Multiplication      | `a * b` | 10 \* 5 = 50 |
| `/`      | Division            | `a / b` | 10 / 5 = 2   |
| `%`      | Modulus (remainder) | `a % b` | 10 % 3 = 1   |

### **Relational (Comparison) Operators**

Used to compare two values.

| Operator | Meaning          | Example  | Result    |
| -------- | ---------------- | -------- | --------- |
| `==`     | Equal to         | `a == b` | false (0) |
| `!=`     | Not equal to     | `a != b` | true (1)  |
| `>`      | Greater than     | `a > b`  | true (1)  |
| `<`      | Less than        | `a < b`  | false (0) |
| `>=`     | Greater or equal | `a >= b` | true (1)  |
| `<=`     | Less or equal    | `a <= b` | false (0) |

### **Logical Operators**

Used to combine multiple conditions.

| Operator | Meaning     | Example           | Result               |
| -------- | ----------- | ----------------- | -------------------- |
| `&&`     | Logical AND | `a > 5 && b < 10` | true if both true    |
| `┃┃`     | Logical OR  | `a > 5 ┃┃ b < 10` | true if any one true |
| `!`      | Logical NOT | `!(a > 5)`        | reverses result      |

### **Assignment Operators**

Used to assign values.

| Operator | Meaning             | Example  | Equivalent To |
| -------- | ------------------- | -------- | ------------- |
| `=`      | Assign              | `a = 10` | —             |
| `+=`     | Add and assign      | `a += 5` | `a = a + 5`   |
| `-=`     | Subtract and assign | `a -= 5` | `a = a - 5`   |
| `*=`     | Multiply and assign | `a *= 2` | `a = a * 2`   |
| `/=`     | Divide and assign   | `a /= 2` | `a = a / 2`   |
| `%=`     | Modulus and assign  | `a %= 3` | `a = a % 3`   |

### **Increment / Decrement Operators**

Increase or decrease a value by 1.

| Operator | Meaning   | Example | Description                       |
| -------- | --------- | ------- | --------------------------------- |
| `++`     | Increment | `a++`   | Post-increment (use then add)     |
| `--`     | Decrement | `--a`   | Pre-decrement (subtract then use) |

### **Bitwise Operators**

Operate on binary digits.

| Operator | Meaning     | Example  |
| -------- | ----------- | -------- |
| `&`      | AND         | `a & b`  |
| `┃`      | OR          | `a  ┃ b` |
| `^`      | XOR         | `a ^ b`  |
| `~`      | NOT         | `~a`     |
| `<<`     | Left shift  | `a << 1` |
| `>>`     | Right shift | `a >> 1` |

**Condition**:

- Work with bit/byte
- Work into only integer number

**Operation Steps:**

```plaintext
1. First, convert the decimal or integer number to a binary number.
   Example:
         let, int x=32, y=12;      128 | 64 | 32 | 16 | 8 | 4 | 2 | 1  (from: 2^n)
                                   -----------------------------------
          Convert to Binary, x=32=  0    0     1    0   0   0   0   0
          Convert to Binary, y=12=  0    0     0    0   1   1   0   0

2. Operation:
             Bitwise AND: &
             Condition: If Both input are '1' then out: 1. Otherwise; out: 0
             Binary,  x=32= 0 0 1 0 0 0 0 0
             Binary,  y=12= 0 0 0 0 1 1 0 0
             --------------------------------
             Multiply[x*y]= 0 0 0 0 0 0 0 0  (= result: 0)


             Bitwise OR: |
             Condition: If Both/Any input are '1' then out: 1. Otherwise; out: 0
             Binary,  x=32= 0 0 1 0 0 0 0 0
             Binary,  y=12= 0 0 0 0 1 1 0 0
             ---------------------------------
             Addition[x+y]= 0 0 1 0 1 1 0 0  (= result: 44)


             Bitwise EX-OR: ^
             Condition: If Both input are same then out: 0. Otherwise; out: 1
             Binary,  x=32= 0 0 1 0 0 0 0 0
             Binary,  y=12= 0 0 0 0 1 1 0 0
             ---------------------------------
             Ex-OR [x^y]  = 0 0 1 0 1 1 0 0  (= result: 44)
```

### **Conditional (Ternary) Operator**

A shorthand for `if-else`.

```c
condition ? expression_if_true : expression_if_false;
```

**Example:**

```c
 int a = 10, b = 20;
 int max = (a > b) ? a : b;  // Output: 20
```

### **Sizeof Operator**

Returns size of a variable or data type.

**Example:**

```c
printf("%zu", sizeof(int));  // Output: 4
```

### **Comma Operator**

Evaluates multiple expressions, returns the last.

**Example:**

```c
int x = (a = 5, b = 10);  // x = 10
```

### **Pointer Operators**

Used for pointer operations.

| Operator | Meaning     | Example |
| -------- | ----------- | ------- |
| `*`      | Dereference | `*ptr`  |
| `&`      | Address-of  | `&var`  |

**Example:**

```c
#include <stdio.h>

int main() {
    int a = 5, b = 2;

    printf("Addition: %d\n", a + b);
    printf("Greater? %d\n", a > b);
    printf("AND logic: %d\n", (a > 0) && (b > 0));
    printf("Bitwise AND: %d\n", a & b);
    printf("Ternary Max: %d\n", (a > b) ? a : b);

    return 0;
}
```

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Control Structures

Control structures in C determine the **flow of execution** of the program — **which blocks of code get executed** and when.

**Types of Control Structures:**

1. **Conditional Statements (Decision-making)**
2. **Looping Statements (Iteration)**
3. **Jump Statements (Branching)**

### **Conditional Statements**

Used to **execute code based on conditions**.

**`if` Statement**

```c
if (condition) {
    // code to execute if condition is true
}
```

Example:

```c
 #include <stdio.h>

  int main() {
      int number = 10;

      if (number > 0) {
          printf("The number is positive.\n");
      }

      return 0;
  }

// OUTPUT: The number is positive.
```

**`if-else` Statement**

```c
if (condition) {
    // if true
} else {
    // if false
}
```

Example:

```c
  #include <stdio.h>
  int main() {

      int number = 10;

      if (number > 0) {
          printf("The number is positive.\n");
      } else {
          printf("The number is not positive.\n");
      }

      return 0;
  }

// OUTPUT: The number is positive.
```

**`else-if` Ladder**

```c
if (condition1) {
    // block 1
} else if (condition2) {
    // block 2
} else {
    // default block
}
```

Example:

```c
  #include <stdio.h>

  int main() {
      int number = 0;

      if (number > 0) {
          printf("The number is positive.\n");
      } else if (number < 0) {
          printf("The number is negative.\n");
      } else {
          printf("The number is zero.\n");
      }

      return 0;
  }

// OUTPUT: The number is Zero.
```

**Nested `if`**

```c
if (condition1) {
    if (condition2) {
        // block
    }
}
```

Example:

```c
#include <stdio.h>

int main() {
    int number = 25;

    if (number > 0) {
        if (number < 100) {
            printf("Number is positive and less than 100.\n");
        }
    }

    return 0;
}

// OUTPUT: Number is positive and less than 100.
```

**Switch-case**

Used for multiple constant values.

```c
switch (expression) {
    case constant1:
        // code
        break;
    case constant2:
        // code
        break;
    default:
        // default code (Optional)
}
```

Example:

```c
  #include <stdio.h>

  int main() {
      int day = 3;

      switch (day) {
          case 1:
              printf("Saturday\n");
              break;
          case 2:
              printf("Sunday\n");
              break;
          case 3:
              printf("Monday\n");  //this block is activated
              break;
          case 4:
              printf("Tuesday\n");
              break;
          case 5:
              printf("Wednesday\n");
              break;
          case 6:
              printf("Thursday\n");
              break;
          case 7:
              printf("Friday\n");
              break;
          default:
              printf("Invalid day\n");
              break;
      }

      return 0;
  }

// OUTPUT: Monday
```

### **Looping Statements**

Used to **repeat a block of code** multiple times.

**`for` Loop**

```c
for (initialization; condition; increment) {
    // code block
}
```

Example:

```c
#include <stdio.h>

int main() {
    // Print numbers from 1 to 5
    for (int i = 1; i <= 5; i++) {
        printf("%d ", i);
    }

    return 0;
}

// OUTPUT: 1 2 3 4 5
```

**`while` Loop**

```c
while (condition) {
    // code block
}
```

Example:

```c
#include <stdio.h>

int main() {
    int i = 1;

    // Print numbers from 1 to 5
    while (i <= 5) {
        printf("%d ", i);
        i++; // increment i
    }

    return 0;
}

// OUTPUT: 1 2 3 4 5
```

**`do-while` Loop**

```c
do {
    // code block
} while (condition);
```

💡 Executes at least once even if condition is false.

Example:

```c
#include <stdio.h>

int main() {
    int i = 1;

    // Print numbers from 1 to 5 using do-while loop
    do {
        printf("%d ", i);
        i++; // increment i
    } while (i <= 5);

    return 0;
}

// OUTPUT: 1 2 3 4 5
```

**Different between `while` vs `do...while`**

| **Feature**        | `while` **Loop**                                            | `do-while` **Loop**                                                          |
| ------------------ | ----------------------------------------------------------- | ---------------------------------------------------------------------------- |
| Condition check    | Before loop body                                            | After loop body                                                              |
| Minimum executions | 0                                                           | 1                                                                            |
| Use cases          | When you're unsure if the loop should execute at least once | When you want the loop to execute at least once, regardless of the condition |

### **Jump Statements**

Used to **control the flow** of loops and functions.

| Keyword    | Description                                       |
| ---------- | ------------------------------------------------- |
| `break`    | Exits loop or switch block                        |
| `continue` | Skips rest of the loop for current iteration      |
| `goto`     | Jumps to a labeled part of the program (⚠️ avoid) |
| `return`   | Exits from a function                             |

**Example (break):**

```c
#include <stdio.h>

int main() {

    for (int i = 1; i <= 10; i++) {
        if (i == 5)
            break;
        printf("%d ", i);     // Output: 1 2 3 4
    }
}
```

**Example (continue):**

```c
#include <stdio.h>

int main() {

    for (int i = 1; i <= 5; i++) {
        if (i == 3)
            continue;
        printf("%d ", i);   // Output: 1 2 4 5
    }
}
```

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Function

A **function** in C is a **block of code** that performs a specific task. It helps in organizing code, avoiding repetition, and improving reusability.

> Real-life analogy to understand function:
>
> > A function in C is like a coffee machine — you press a button (input), it brews coffee (process), and gives you a cup (output).

**Types of Functions**

1. **User-defined Funtions:** Created by the programmer.

2. **Built-in (Library) Functions:** Provided by C libraries.

### **User-defined Funtions:**

**Syntax (Declaration + Definition + Call):**

```c
// ❏ Function Declaration
returnType functionName (dataType1 parameter1, dataType2 parameter2, ...);

 // ❏ Function Definition
returnType functionName (dataType1 parameter1, dataType2 parameter2, ...) {

    // code... block

    return value; // If the function returns a value
}

// ❏ Function Call
functionName (arguments);
```

**The Function Components are -**

- **Function Declaration**
- **Function Definition**
- **Function Call**

**Function Declaration:**  
Tells the compiler about the function's name, return type, and parameters — before it is used.

```c
int add(int a, int b);  // Declaration
```

- Return type: `int`

- Function name: `add`

- Parameters: `int a, int b`

_💡 Think of this as informing the compiler: “Hey! I’ll use a function like this later.”_

**Function Definition**  
Contains the actual **code (body)** that runs when the function is called.

```c
int add(int a, int b) {
    return a + b;
}
```

- This is where the logic of **addition** is implemented.

**Function Call**

Used to **invoke/execute** the function and get the result.

```c
int result = add(3, 5);  // Function call
```

- Passes arguments `3` and `5` to the function

- Stores the returned value in `result`

**Full Example with All Components**

```c
#include <stdio.h>

// 1. Function Declaration
int add(int a, int b);

int main() {
    // 3. Function Call
    int sum = add(10, 20);
    printf("Sum = %d\n", sum);
    return 0;
}

// 2. Function Definition
int add(int a, int b) {
    return a + b;
}
```

**Output:**

```markdown
Sum = 30
```

**Example (No return, no parameters):**

```c
#include <stdio.h>

void greet() {
    printf("Hello, World!\n");
}

int main() {
    greet();
    return 0;
}
```

**Output:**

```markdown
Hello, World!
```

**Example (With return, with parameters):**

```c
#include <stdio.h>

int add(int a, int b) {
    return a + b;
}

int main() {
    int sum = add(4, 5);
    printf("Sum = %d\n", sum);
    return 0;
}
```

**Output:**

```markdown
Sum = 9
```

**Example (Function Declaration (Prototype)):**

```c
#include <stdio.h>

int multiply(int, int); // function declaration

int main() {
    printf("Result = %d\n", multiply(3, 4));
    return 0;
}

int multiply(int x, int y) {
    return x * y;
}
```

**Output:**

```markdown
Result = 12
```

**Recursive Function**

A recursive function is a function that calls itself to solve smaller versions of a problem.

> Real-life analogy to understand function:
>
> > Like opening a set of nested boxes — each box opens the next, until the smallest box is reached.

```c
#include <stdio.h>

int factorial(int n) {
    if (n == 0) return 1;
    return n * factorial(n - 1);
}

int main() {
    printf("Factorial of 5 = %d\n", factorial(5));
    return 0;
}
```

**Output:**

```markdown
Factorial of 5 = 120
```

**Return Types in C Functions:**

| Return Type | Meaning             | Example           |
| ----------- | ------------------- | ----------------- |
| `void`      | No return value     | `void show()`     |
| `int`       | Returns integer     | `int getSum()`    |
| `float`     | Returns float value | `float avg()`     |
| `char`      | Returns a character | `char getGrade()` |

**Parameter Types:**

| Type               | Example                 | Description                      |
| ------------------ | ----------------------- | -------------------------------- |
| No Parameters      | `void greet(void)`      | Takes no input                   |
| With Parameters    | `int sum(int a, int b)` | Takes input values               |
| Default (Not in C) | ❌                      | C doesn’t support default params |
| Variable Arguments | `int printf(...)`       | Use `stdarg.h`                   |

**Function Categories:**

| Function Type              | Parameters | Return Value | Example                   |
| -------------------------- | ---------- | ------------ | ------------------------- |
| No Parameters, No Return   | No         | No           | `void greet(void)`        |
| With Parameters, No Return | Yes        | No           | `void greet(char name[])` |
| No Parameters, With Return | No         | Yes          | `int getTime(void)`       |
| With Parameters and Return | Yes        | Yes          | `int add(int a, int b)`   |

### **Built-in (Library) Functions:**

These are pre-defined functions provided by C's standard library.

Example: `printf()`, `scanf()`, `strlen()`, `malloc()`, etc.

**Header Files:**

You don't need to define these functions, but you must include the appropriate header files.

_Example: `#include <stdio.h>` (for `printf()`)._

Some Header File List:

- `stdio.h` (Standard input-output.header):

  - Inside of Header: `printf()`, `scanf()`, `getchar()`, `putchar()`, `gets()`, `puts()`, `fopen()`, `fclose()`, `feof()`

- `conio.h` (Console input-output.header) - Contains declaration for console I/O

  - Inside of Header: `clrscr()`, `getch()`, `exit()`

- `ctype.h` (Character Type.header) - Used for Character-handling.

  - Inside of Header: `isupper()`, `islower()`, `isalpha()`

- `math.h` (Mathematics.header) - Declares mathematical functions and macros.

  - Inside of Header: `pow()`, `sqrt()`, `sin()`, `cos()`, `tan()`, `log()`

- `stdlib.h` (Standard Library.header) - For number conversion, storage allocation

  - Inside of Header: `rand()`, `srand()`

- `string.h` (String.header) - Used for manipulate strings.

  - Inside of Header: `strlen()`, `strctp()`, `strcmp()`, `strcat()`, `strlwr()`, `strupr()`,`strrev()`

**Example: `sizeof()`**

Determines the size of a variable, data type, or expression in bytes. It’s useful for understanding memory usage and performing size-based operations.

```c
char a; int b; float c; double d;

printf("Size of Character is: %d \n", sizeof(a));
printf("Size of Integer is: %d \n", sizeof(b));
printf("Size of Float is: %d \n", sizeof(c));
printf("Size of Double is: %d  \n", sizeof(d));
```

**Example (Character): `toupper();` `tolower();`**

Convert a lowercase letter to uppercase or vice versa.

```c
#include <stdio.h>

int main()
{
    char lower, upper;

    printf("Enter any lowercase letter: ");
    scanf("%c", &lower);

    upper = toupper(lower);
    printf("The uppercase letter is: %c \n", upper);
    return 0;
}

// Similarly Replace: tolower();
```

**Example (Mathematics): `abs()`**

Calculates the absolute value of a numerical expression. Returns the positive equivalent of a negative number, or the original value if the number is already positive.

```c
int x= -12;
x = abs(-12);
printf("%d \n", x);  //result: 12
```

**Example (Mathematics): `sqrt()`**

Calculates the square root of a non-negative floating-point number. Returns the positive square root of the given number.

```c
int x=4;
double result = sqrt(x);
printf("%.2lf \n", result); //result: 2
```

**Example (Mathematics): `pow()`**

Calculates the power of a number. Raises a base number to a given exponent.

```c
double x = pow(4,2);    //formula: 4^2=16
printf("%.2lf \n", x);  //result: 16
```

**Example (Mathematics): `log()`**

The `log()` function in C is used to calculate the natural logarithm of a positive number. The natural logarithm is the logarithm to the base e, where e is approximately 2.71828.

```c
int x=10.5;
double result = log(x);
printf("%.2lf \n", result); //result: 2.30
```

**Example (Mathematics): `log10()`**

The `log10()` function in C is used to calculate the base-10 logarithm of a positive number. This means it finds the power to which 10 must be raised to get the given number.

```c
int x=10.5;
double result = log10(x);
printf("%.2lf \n", result); //result: 1.00
```

**Example (Mathematics): `exp()`**

Calculates the exponential function of a number. Finds the value of e raised to the power of the given number, where e is approximately 2.71828.

```c
int x=5;
double result = exp(x);
printf("%.2lf \n", result); //result: 148.41
```

**Example (Mathematics): `sin()`, `cos()`, `sec()`, `cosec()`, `tan()`, `cot()`**

Calculates the trigonometric (functions sine/cosine/tangent/secant/cosecant/cotangent) of an angle expressed in radians.

```c
int x=46;
double result = sin(x);
printf("%.2lf \n", result); //result: 0.90

// Similarly Replace: sin() | sec(); | cosec(); | tan(); | cot();
```

**Example (Mathematics): `round()`**

Calculate round or fraction-less number from any value from a mathematical equation

Here, 5.36=5, 5.56=6 and 5.99=6

```c
int x=4.6;
double result = sin(x);
printf("%.2lf \n", result); //result: 4.00

```

**Example (Mathematics): `ceil()`**

```plaintext
--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--

 -7 -6 -5 -4 -3 -2 -1  0  1  2  3  4  5  6  7
```

For non-integers, `Ceiling - Floor = 1`

Ceiling rounds up:
⌈5.36⌉ = 6, ⌈5.12⌉ = 6, ⌈5.99⌉ = 6

```c
int x=4.6;
double result = ceil(x);
printf("%.2lf \n", result); //result: 5.00
```

**Example (Mathematics): `floor()`**

```plaintext
--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--

 -7 -6 -5 -4 -3 -2 -1  0  1  2  3  4  5  6  7
```

For non-integers, `Ceiling - Floor = 1`

Floor rounds down:
⌊5.36⌋ = 5, ⌊5.56⌋ = 5, ⌊5.99⌋ = 5

```c
int x=4.6;
double result = floor0(x);
printf("%.2lf \n", result); //result: 4.00
```

**Example (Mathematics): `trunc()`**;

Convert `Integer` from `float` or fraction number.

```C
int x=6.6;
double result = sin(x);
printf("%.2lf \n", result); //result: 6.00
```

**Example (Mathematics): `rand()`**

Create Random numbers.

```C
#include <stdio.h>
#include <stdlib.h>  //Using header file for random numbers

int main()
{
    for (int i=1; i<=5; i++){
        int randonNum = rand(); //Random numbers create
        printf(" Random Number: %d \n", randonNum);
    }
    return 0;
}
```

**Example (String): `strlen()`**

Calculate the String length.

```c
char name [] = "Nazrull";
int len = strlen(name);
printf("Length: %d", len);
```

**Example (String): `strcpy()`**

Copy string Using function.

```c
char source [] = "Michael Scofield";
char destination [100];
strcpy(destination, source);
printf("Check 'strcpy()' for 'destination': %s \n", destination);
```

**Example (String): `strcat()`**

String Concatenation by using function. (Adding Every Characters)

```c
char name1 [] = "Michael ";
char name2 [] = "Scofield";
strcat(name1, name2);
printf("Print the Concatenation: %s \n", name1);
```

**Example (String): `strcmp()`**

Compare different different String for check they equal or not.

```c
char name1 [50] = "Michael ";
char name2 [] = "Scofield";
int result = strcmp(name1, name2); //If both string are same then return '0'
if(result == 0)
    printf("String are equal");
else
    printf("String aren't equal");
```

**Example (String): `strrev()`**

Reverse String from given string.

```c
char name [] = "Michael Scofield";
strrev(name); //Only Support One parameter
printf("The reverse string is: %s", name);
```

**Example (String): `strupr()`**

For UpperCase Letter from given string.

```c
char name [] = "Michael Scofield";
strupr(name); //Only Support One parameter
printf("The UpperCase string is: %s", name);
```

**Example (String): `strlwr()`**

For Lowercase Letter from given string.

```c
char name [] = "Michael Scofield";
strlwr(name); //Only Support One parameter
printf("The Lowercase string is: %s", name);
```

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## String

In C, a string is a sequence of characters terminated by a null character (`'\0'`).
Unlike some high-level languages, **C does not have a built-in `string` data type.**
Strings are implemented as arrays of characters.

**Declaration of String**

```c
char str[10]; // Can store up to 9 characters + 1 null character '\0'
```

### Ways to Initialize a String

**Using String Literal**

```c
char str[] = "Hello";
```

Automatically appends `\0` at the end.

**Using Character Array**

```c
char str[] = {'H', 'e', 'l', 'l', 'o', '\0'};
```

**Example: Basic String Input and Output**

```c
#include <stdio.h>

int main() {
    char name[20];

    printf("Enter your name: ");
    scanf("%s", name);  // Reads a single word (no spaces)

    printf("Hello, %s!\n", name);

    return 0;
}
```

**Output:**

```c
Enter your name: Alice
Hello, Alice!
```

**Example: Using `gets()` and `puts()` for Full Line Input**

```c
#include <stdio.h>

int main() {
    char fullName[50];

    printf("Enter your full name: ");
    gets(fullName);  // Reads full line including spaces (unsafe)

    puts("Your name is:");
    puts(fullName);

    return 0;
}
```

**Output:**

```c
Enter your full name: Alice Johnson
Your name is:
Alice Johnson

```

> [!WARNING]
>
> `gets()` is unsafe and deprecated in modern C. Use `fgets()` instead.

**Example: Using `fgets()` Safely**

```c
#include <stdio.h>

int main() {
    char fullName[50];

    printf("Enter your full name: ");
    fgets(fullName, sizeof(fullName), stdin);  // Safe input with spaces

    printf("Hello, %s", fullName);

    return 0;
}
```

**Output:**

```c
Enter your full name: Alice Johnson
Hello, Alice Johnson
```

### String Functions (`<string.h>`)

| Function        | Description                      | Example                 |
| --------------- | -------------------------------- | ----------------------- |
| `strlen(s)`     | Returns length                   | `strlen("Hi") → 2`      |
| `strcpy(d, s)`  | Copies string `s` into `d`       | `strcpy(dest, src)`     |
| `strcat(d, s)`  | Concatenates `s` to `d`          | `strcat(dest, src)`     |
| `strcmp(s1,s2)` | Compares two strings             | Returns 0 if equal      |
| `strrev(s)`     | Reverses a string (non-standard) | `strrev("abc") → "cba"` |

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Array

An **array** in C is a **collection of elements** of the same data type stored in **contiguous memory locations**.

> Real-life analogy to understand array:
>
> > An array is like a bookshelf, where each shelf slot holds one book and you can find any book by its position number.

**Syntax:**

```c
data_type array_name[array_size];
```

**Explanation:**

- **`data_type`**: The data type of the array elements (e.g., `int`, `float`, `char`).
- **`array_name`**: The name of the array.
- **`array_size`**: The number of elements the array can hold.

**Example:**

```c
#include <stdio.h>

int main() {
    int numbers[5] = {10, 20, 30, 40, 50};

    printf("First number: %d\n", numbers[0]);  // index 0
    printf("Third number: %d\n", numbers[2]);  // index 2

    return 0;
}
```

**Output:**

```markdown
First number: 10
Third number: 30
```

> [!NOTE]
>
> - **Index starts at `0`:** The first element is accessed as `array[0]`
> - **Fixed size:** The size of the array must be defined at the time of declaration
> - **Same type:** All elements must be of the same type (e.g., all `int`, `float`, etc.)

**Array Declaration, Initialization and Accessing:**

```c
// Declaration and Initialization
int numbers[5] = {10, 20, 30, 40, 50};

// Accessing elements
printf("%d", numbers[0]);  // Output: 10
printf("%d", numbers[2]);  // Output: 30
```

**Array Accessing Diagram:**

```plaintext
Index:     0    1    2    3    4
Value:    10   20   30   40   50
           ↑         ↑
     numbers[0]  numbers[2]
```

**Types of Arrays**

1. Linear or 1D Arrays
2. Multi-Dimensional:
   1. Matrix or 2D Array
   2. 3D Array

### Linear or 1D Array

A single-dimensional array is the simplest form of an array. It is a **linear collection of elements** of the same data type, accessible using a single index.

**Syntax:**

```c
datatype array_name [array_size];             // array declaration

datatype array_name [array_size] = {value};  // array initialization

array_name [index];                          // accessing array elements
```

**Example (1D Array):**

```c
#include <stdio.h>

int main() {
    int numbers[5] = {10, 20, 30, 40, 50};

    for (int i = 0; i < 5; i++) {
        printf("%d ", numbers[i]);
    }

    return 0;
}
```

**Output:**

```markdown
10 20 30 40 50
```

### **Matrix or 2D Arrays**

A two-dimensional array in C is an array of arrays, which can be visualized as a matrix with rows and columns.

**Syntax:**

```c
// array declaration
datatype array_name [rows] [columns];

// array initialization
datatype array_name [row_size] [column_size] = {

    {column1, column2, column3},   // total: 2 row and 3 columns
    {column1, column2, column3}
};

// accessing array elements
datatype variable_name = array_name [rows] [columns];
```

**Explanation:**

- **`type`**: The data type of the array elements (e.g., `int`, `float`).
- **`rows`**: The number of rows in the array.
- **`columns`**: The number of columns in the array.

**Example:**

```c
#include <stdio.h>

int main() {

    // 2D Array Declaration and Initialization
    int matrix[3][4] = {
        {1, 2, 3, 4},
        {5, 6, 7, 8},
        {9, 10, 11, 12}
    };

    // Accessing a Value from a Specific Index
    int element = matrix[1][2];  // 2nd row, 3rd column → value is 7

    printf("Access Single Element: %d\n\n", element);

    // Printing all elements of the 2D array
    printf("Matrix Elements:\n");
    for (int i = 0; i < 3; i++) {          // rows
        for (int j = 0; j < 4; j++) {      // columns
            printf("%2d ", matrix[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```

**Output:**

```markdown
Access Single Element: 7

Matrix Elements:
1 2 3 4
5 6 7 8
9 10 11 12
```

**Visual Representation:**

```plaintext
      Columns →
        0   1   2   3
Rows ↓
  0     1   2   3   4
  1     5   6   7   8
  2     9  10  11  12
```

### Multi-dimensional or 3D Array

A three-dimensional array can be visualized as an array of 2D arrays. It's like having multiple matrices stacked together.

**Syntax:**

```c
// array declaration
datatype array_name [size1] [size2] [size3];

// array initialization
datatype array_name [numOf_2D_Array] [rowSize_each2D] [columnSize_each2D] = {

    {
        {column1, column2, column3},   // total: 2 row and 3 columns
        {column1, column2, column3}
    },
    {
        {column1, column2, column3},   // total: 2 row and 3 columns
        {column1, column2, column3}
    }
};

// accessing array elements
datatype variable_name = array_name [size1] [size2] [size3];
```

**Explanation:**

- **`size1`**: The size of the first dimension (number of 2D arrays).
- **`size2`**: The size of the second dimension (number of rows in each 2D array).
- **`size3`**: The size of the third dimension (number of columns in each 2D array).

> [!NOTE]
>
> - **Fixed Size:** The size of each dimension must be specified at compile time (except for the first dimension, which can sometimes be omitted in the declaration if the array is initialized).
> - **Memory Layout:** Multi-dimensional arrays are stored in a contiguous block of memory. For a 2D array, the elements are stored row by row.
> - **Access:** Elements are accessed using multiple indices, one for each dimension.

**Example:**

```c
#include <stdio.h>

int main() {

    int arr[2][3][4] = {  // A 3D array with 2 "planes," each with 3 rows & 4 columns.
        {
            {1, 2, 3, 4},
            {5, 6, 7, 8},
            {9, 10, 11, 12}
        },
        {
            {13, 14, 15, 16},
            {17, 18, 19, 20},
            {21, 22, 23, 24}
        }
    };

    // Accessing Value from Specific Index
    int element = arr[1][2][3];
    // Accesses the element in the 2nd plane, 3rd row, 4th column (value is 24)

    printf("Access Single Element: %d\n\n", element); //

    // Printing all elements of the 3D array
    for (int i = 0; i < 2; i++) {
        printf("Plane %d:\n", i);
        for (int j = 0; j < 3; j++) {
            for (int k = 0; k < 4; k++) {
                printf("%2d ", arr[i][j][k]);
            }
            printf("\n");
        }
        printf("\n");
    }

    return 0;
}
```

**Output:**

```markdown
Access Single Element: 24

Plane 0:
1 2 3 4
5 6 7 8
9 10 11 12

Plane 1:
13 14 15 16
17 18 19 20
21 22 23 24
```

### Array Initialization

| Method                         | Syntax Example                   |
| ------------------------------ | -------------------------------- |
| Full initialization            | `int arr[3] = {1, 2, 3};`        |
| Partial initialization         | `int arr[3] = {1}; // {1, 0, 0}` |
| Zero initialization            | `int arr[3] = {0};`              |
| Size inferred from initializer | `int arr[] = {1, 2, 3, 4};`      |

**Example (Input from User):**

```c
#include <stdio.h>

int main() {
    int a[5];

    printf("Enter 5 numbers: ");
    for (int i = 0; i < 5; i++) {
        scanf("%d", &a[i]);
    }

    printf("You entered: ");
    for (int i = 0; i < 5; i++) {
        printf("%d ", a[i]);
    }

    return 0;
}
```

**Output (if input = 1 2 3 4 5):**

```markdown
Enter 5 numbers: You entered: 1 2 3 4 5
```

### Accessing and Modifying Array Elements

```c
arr[2] = 100;  // modifies the 3rd element
int x = arr[0];  // gets the 1st element
```

**Example (Sum of Array Elements):**

```c
#include <stdio.h>

int main() {
    int a[5] = {1, 2, 3, 4, 5};
    int sum = 0;

    for (int i = 0; i < 5; i++) {
        sum += a[i];
    }

    printf("Sum = %d\n", sum);
    return 0;
}
```

**Output:**

```markdown
Sum = 15
```

### Passing Arrays to Functions

In C, when you pass an **array to a function**, **you’re passing the address of the first element** — not the entire array.

This means that **any changes made to the array inside the function affect the original array**.

**Syntax**

```c
// Function declaration
void displayArray(int arr[], int size);

// Function call
displayArray(arr, size);
```

**Example:**

```c
#include <stdio.h>

void displayArray(int arr[], int size) {
    for(int i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
}

int main() {
    int nums[] = {10, 20, 30, 40, 50};
    int length = sizeof(nums) / sizeof(nums[0]);

    printf("Array elements: ");
    displayArray(nums, length);

    return 0;
}
```

**Output:**

```c
Array elements: 10 20 30 40 50
```

### **Array of Pointers**

An array of pointers holds memory addresses, and each element of the array is a pointer to a variable or another array.

**Example:**

```c
#include <stdio.h>

int main() {

    int numbers[] = {10, 20, 30, 40, 50};
    int *ptrs[5]; // Array of 5 integer pointers

    // Assign pointers to elements of the numbers array
    for (int i = 0; i < 5; i++) {
        ptrs[i] = &numbers[i];
    }

    // Access elements using pointers
    for (int i = 0; i < 5; i++) {
        printf("Element %d: %d\n", i + 1, *ptrs[i]);
    }

    return 0;
}
```

**Output:**

```markdown
Element 1: 10
Element 2: 20
Element 3: 30
Element 4: 40
Element 5: 50
```

**Multi-Dimensional Arrays of Pointers**  
These arrays are arrays of pointers that can be used to manage more complex data structures, such as arrays of arrays where each sub-array can be of different sizes.

**Example:**

```c
#include <stdio.h>
int main() {

    int numbers[3][4] = {{1, 2, 3, 4}, {5, 6, 7, 8}, {9, 10, 11, 12}};
    int *ptrs[3][4];

    // Assign pointers to elements of the numbers array
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 4; j++) {
            ptrs[i][j] = &numbers[i][j];
        }
    }

    // Access elements using pointers
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 4; j++) {
            printf("Element [%d][%d]: %d\n", i, j, *ptrs[i][j]);
        }
    }

    return 0;
}
```

**Output:**

```markdown
Element [0][0]: 1
Element [0][1]: 2
Element [0][2]: 3
Element [0][3]: 4
Element [1][0]: 5
Element [1][1]: 6
Element [1][2]: 7
Element [1][3]: 8
Element [2][0]: 9
Element [2][1]: 10
Element [2][2]: 11
Element [2][3]: 12
```

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Pointers

A **pointer** is a **variable that stores the address of another variable**.

**Syntax:**

```c
data_type *pointer_name;
```

- The **`data_type`** of the variable that the pointer will point to.

- `*` indicates it’s a pointer.

- `pointer_name` stores the address of an integer variable.

**Example:**

```c
int *pointer_name;    // Pointer to an integer
char *pointer_name;   // Pointer to a character
float *pointer_name;  // Pointer to a float
```

Instead of holding a data value, it holds the **memory address** of a variable. Here,

- `&` symbol is used to get the address of the variable.
- `*` symbol is used to get the value of the variable that the pointer is pointing to.

**Assigning a Value to a Pointer**

Pointers are assigned the address of a variable using the address-of operator (`&`).

**Example:**

```c
#include <stdio.h>

int main() {
    int a = 10;
    int *p;
    p = &a;  // Assign the address of 'a' to pointer 'p'

    // Output information
    printf("Value of a: %d\n", a);
    printf("Address of a: %p\n", &a);
    printf("Pointer p stores address: %p\n", p);
    printf("Value pointed by p (*p): %d\n", *p);

    return 0;
}
```

**Output:**

```c
Value of a: 10
Address of a: 0x7ffee8e73abc      // Actual output may vary
Pointer p stores address: 0x7ffee8e73abc
Value pointed by p (*p): 10
```

**Accessing the Value at the Pointer Address**

To access or modify the value stored at the memory location pointed to by a pointer, you use the dereference operator (`*`).

**Example:**

```c
#include <stdio.h>
int main(){
   int a = 10;
   int *p = &a;

   printf("Value of a: %d\n", a);
   printf("Value of a via pointer: %d\n", *p);

   *p = 20;  // Modify the value of 'a' through the pointer
   printf("New value of a: %d\n", a);

   return 0;
}
```

**Output:**

```c
Value of a: 10
Value of a via pointer: 10
New value of a: 20
```

### Pointer Arithmetic

Pointers can be incremented or decremented, and can be used in arithmetic operations to navigate through arrays or other memory structures.

**Example:**

```c
#include <stdio.h>
int main(){

   int arr[] = {10, 20, 30, 40, 50};
   int *p = arr;  // Points to the first element of the array

   printf("%d\n", *p);
   p++;  // Move to the next element in the array
   printf("%d\n", *p);
   return 0;
}
```

**Output:**

```c
10
20
```

### Pointers and Arrays

Pointers and arrays are closely related in C. The name of an array is actually a constant pointer to the first element of the array.

**Example:**

```c
#include <stdio.h>
int main(){

   int arr[5] = {10, 20, 30, 40, 50};
   int *p = arr;

   for (int i = 0; i < 5; i++) {
       printf("Element %d: %d\n", i, *(p + i));
       // Accessing array elements via pointer
   }
   return 0;
}
```

**Output:**

```c
  Element 0: 10
  Element 1: 20
  Element 2: 30
  Element 3: 40
  Element 4: 50
```

### Pointers to Pointers

A pointer can also point to another pointer, creating multiple levels of indirection.

**Example:**

```c
#include <stdio.h>
int main(){
      int a = 10;
   int *p = &a;
   int **pp = &p;

      printf("Value of a: %d\n", **pp);

      return 0;
}
```

**Output:**

```c
Value of a: 10
```

### Dynamic Memory Allocation (Pointer)

Pointers are essential for dynamic memory allocation in C, using functions like `malloc`, `calloc`, `realloc`, and `free`.

**Example:**

```c
#include <stdio.h>
int main(){

   int *p;
   p = (int *)malloc(5 * sizeof(int));
   // Allocates memory for an array of 5 integers

   for (int i = 0; i < 5; i++) {
       p[i] = i * 10;  // Initialize array elements
   }

   for (int i = 0; i < 5; i++) {
       printf("%d ", p[i]);
   }

   free(p);  // Free the allocated memory

      return 0;
}
```

**Output:**

```c
0 10 20 30 40
```

### Function Pointers

Pointers can also be used to point to functions, allowing for dynamic function calls and passing functions as arguments.

**Example:**

```c
#include <stdio.h>

void display(int n) {
    printf("Number: %d\n", n);
}

int main() {
    void (*funcPtr)(int);
    // Declare a pointer to a function that takes an int and returns void

    funcPtr = display;     // Assign function 'display' to the pointer

    funcPtr(5);  // Call the function using the pointer

    return 0;
}
```

**Output:**

```c
Number: 5
```

### Why Pointer?

- Pointers are powerful features in C/C++ that set them apart from languages like Java and Python.

- They enable efficient memory management, making software faster and more resource-aware.

- However, overusing pointers can make code harder to understand and maintain.

  <!-- START "Jump to Top"-->
  <p align="right">
    <a href="#table-of-contents">Jump to Top ▲</a>
  </p>
  <!-- END "Jump to Top" -->

## Structure, Union and Enum

C provides powerful user-defined data types that help group different data under one name. These include:

- `struct` → Structure
- `union` → Union
- `enum` → Enumeration

### Structure

A **structure** is a user-defined data type in C that allows grouping variables of different types under one name.

**Syntax:**

```c
struct StructName {
    datatype member1;
    datatype member2;
    ...
};
```

**Example:**

```c
#include <stdio.h>

struct Person {
    char name[50];
    int age;
};

int main() {
    struct Person p1 = {"Alice", 25};

    printf("Name: %s\n", p1.name);
    printf("Age: %d\n", p1.age);

    return 0;
}
```

**Output:**

```c
Name: Alice
Age: 25
```

### Union

A **union** is like a structure, but all members **share the same memory location.** This saves memory but only one member can hold a value at any time.

**Syntax:**

```c
union UnionName {
    datatype member1;
    datatype member2;
    ...
};
```

**Example:**

```c
#include <stdio.h>

union Data {
    int i;
    float f;
};

int main() {
    union Data d;
    d.i = 10;

    printf("d.i = %d\n", d.i);

    d.f = 3.14;
    printf("d.f = %.2f\n", d.f);

    // d.i is now overwritten
    printf("d.i after setting d.f = %d\n", d.i);

    return 0;
}
```

**Output:**

```c
d.i = 10
d.f = 3.14
d.i after setting d.f = 1078523331   // Undefined result (due to memory sharing)
```

### Enum

An **enum (enumeration)** is a user-defined data type that assigns **names to a set of integer constants.**

**Syntax:**

```c
enum EnumName {CONST1, CONST2, CONST3, ...};
```

By default, `CONST1 = 0`, `CONST2 = 1`, etc.

**Example:**

```c
#include <stdio.h>

enum Weekday { Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday };

int main() {
    enum Weekday today = Friday;

    printf("Numeric value of Friday: %d\n", today);

    return 0;
}
```

**Output:**

```c
Numeric value of Friday: 5
```

💡 You can also manually assign custom values to enum constants:

```c
enum Color { Red = 1, Green = 3, Blue = 5 };
```

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Dynamic Memory Allocation

Dynamic memory allocation allows you to **allocate memory at runtime** using pointers.  
Unlike static memory allocation (fixed size), dynamic memory can **grow or shrink as needed** while the program is running.

**Dynamic Memory Functions**

| Function    | Description                                        |
| ----------- | -------------------------------------------------- |
| `malloc()`  | Allocates a block of memory                        |
| `calloc()`  | Allocates memory and initializes all bytes to zero |
| `realloc()` | Resizes previously allocated memory block          |
| `free()`    | Frees allocated memory to avoid memory leaks       |

### `malloc()` – Memory Allocation

The `malloc()` function in C is used to **dynamically allocate memory** at runtime from the heap. It stands for **Memory Allocation**.

- It returns a `void *` (pointer to void), which should be **typecast** to the appropriate type.
- The allocated memory contains **garbage values** (uninitialized).

**Syntax:**

```c
ptr = (castType *) malloc(size);
```

**Example:**

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int *arr;
    arr = (int *)malloc(3 * sizeof(int));  // allocate memory for 3 integers

    if (arr == NULL) {
        printf("Memory not allocated.\n");
        return 1;
    }

    arr[0] = 10; arr[1] = 20; arr[2] = 30;

    for (int i = 0; i < 3; i++) {
        printf("%d ", arr[i]);
    }

    free(arr);  // free the allocated memory
    return 0;
}
```

**Output:**

```c
10 20 30
```

### `calloc()` – Contiguous Allocation

The `calloc()` function in C is used to **dynamically allocate memory** at runtime — just like `malloc()`, but with two key differences:

- It allocates **contiguous memory blocks**.
- It **initializes** all allocated memory to **zero**.

**Syntax:**

```c
ptr = (castType *) calloc(n, size);
```

**Example:**

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int *arr;
    arr = (int *)calloc(3, sizeof(int));  // allocates and initializes to 0

    if (arr == NULL) {
        printf("Memory not allocated.\n");
        return 1;
    }

    for (int i = 0; i < 3; i++) {
        printf("%d ", arr[i]);
    }

    free(arr);
    return 0;
}
```

**Output:**

```c
0 0 0
```

### `realloc()` – Reallocate Memory

The `realloc()` function in C is used to **resize previously allocated memory** (via `malloc()` or `calloc()`), either increasing or decreasing its size.

- It avoids the need to manually allocate a new block and copy data.
- Contents up to the **minimum of old and new sizes** are preserved.

**Syntax:**

```c
ptr = realloc(ptr, newSize);
```

**Example:**

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int *arr = malloc(2 * sizeof(int));
    arr[0] = 5; arr[1] = 10;

    arr = realloc(arr, 4 * sizeof(int));
    arr[2] = 15; arr[3] = 20;

    for (int i = 0; i < 4; i++) {
        printf("%d ", arr[i]);
    }

    free(arr);
    return 0;
}
```

**Output:**

```c
5 10 15 20
```

### `free()` – Release Memory

The `free()` function is used to **release dynamically allocated memory** back to the system once you're done using it.

- Prevents **memory leaks**
- Only used for memory allocated with `malloc()`, `calloc()`, or `realloc()`

**Example:**

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int *arr;
    int n = 5;

    // Allocate memory for 5 integers
    arr = (int *)malloc(n * sizeof(int));

    if (arr == NULL) {
        printf("Memory allocation failed.\n");
        return 1;
    }

    // Assign values
    for (int i = 0; i < n; i++) {
        arr[i] = (i + 1) * 10;
    }

    // Print values
    printf("Values in the array: ");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    // Free the allocated memory
    free(arr);
    printf("Memory successfully freed.\n");

    return 0;
}
```

**Output:**

```c
Values in the array: 10 20 30 40 50
Memory successfully freed.
```

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Typedef and Type Casting

Here’s a well-structured explanation of `typedef` and `Type Casting`:

### Typedef

The `typedef` keyword allows you to create **new names (aliases)** for existing data types. It improves code readability and portability.

**Syntax:**

```c
typedef existing_type new_name;
```

**Example: Using `typedef`**

```c
#include <stdio.h>

typedef unsigned int uint;

int main() {
    uint a = 10;
    printf("Value of a: %u\n", a);
    return 0;
}
```

**Output:**

```c
Value of a: 10
```

### Type Casting in C

Type casting allows you to **convert one data type into another**.
There are two types:

1. **Implicit (automatic)** – Done by compiler
2. **Explicit (manual)** – Done by programmer

**Syntax:**

```c
(type) expression;
```

**Example: Integer to Float**

```c
#include <stdio.h>

int main() {
    int a = 5, b = 2;
    float result;

    result = (float)a / b;
    printf("Result: %.2f\n", result);
    return 0;
}
```

**Output:**

```c
Result: 2.50
```

Without casting, `a / b` would result in integer division (`2` instead of `2.50`).

**Example 2: Float to Integer**

```c
#include <stdio.h>

int main() {
    float num = 7.89;
    int intNum = (int)num;

    printf("Original: %.2f\n", num);
    printf("Converted to int: %d\n", intNum);
    return 0;
}
```

**Output:**

```c
Original: 7.89
Converted to int: 7
```

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## File Handling

File handling in C allows you to **create**, **read**, **write**, and **manipulate files** on disk — making your programs more powerful and persistent.

### Types of File Access Modes

| Mode   | Description                                                         |
| ------ | ------------------------------------------------------------------- |
| `"r"`  | Open for reading. Error if file doesn't exist.                      |
| `"w"`  | Open for writing. Creates file if not exists. Overwrites if exists. |
| `"a"`  | Open for appending. Creates if not exists. Writes at end of file.   |
| `"r+"` | Open for reading and writing. File must exist.                      |
| `"w+"` | Open for reading and writing. Overwrites file.                      |
| `"a+"` | Open for reading and appending. Creates if not exists.              |

### Basic File Operations

| Function               | Purpose                        |
| ---------------------- | ------------------------------ |
| `fopen()`              | Opens a file                   |
| `fclose()`             | Closes an opened file          |
| `fprintf()`            | Writes formatted data to file  |
| `fscanf()`             | Reads formatted data from file |
| `fgets()` / `fputs()`  | String-based file I/O          |
| `fread()` / `fwrite()` | Binary I/O                     |

**Example: Writing to a File**

```c
#include <stdio.h>

int main() {
    FILE *fp = fopen("output.txt", "w");  // Open file for writing

    if (fp == NULL) {
        printf("Error opening file!\n");
        return 1;
    }

    fprintf(fp, "Hello, File Handling in C!\n");
    fclose(fp);

    printf("Data written successfully.\n");

    return 0;
}
```

**Output: (Console)**

```c
Data written successfully.
```

**Output: File (`output.txt`)**

```c
Hello, File Handling in C!
```

**Example: Reading from a File**

```c
#include <stdio.h>

int main() {
    FILE *fp = fopen("output.txt", "r");  // Open file for reading
    char buffer[100];

    if (fp == NULL) {
        printf("File not found!\n");
        return 1;
    }

    while (fgets(buffer, sizeof(buffer), fp)) {
        printf("%s", buffer);  // Print each line
    }

    fclose(fp);
    return 0;
}
```

**Output:**

```c
Hello, File Handling in C!
```

### File I/O Error Handling

- Always check if `fopen()` returns `NULL`.

- Always call `fclose()` to free resources.

- Ensure proper file permissions (read/write access).

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Preprocessor Directives

Preprocessor directives are instructions to the C preprocessor that **prepare the code** before the actual compilation begins. They are used to **modify** or **define certain aspects** of the code before the program is compiled.

Preprocessor directives begin with a `#` symbol and are **not terminated by a semicolon**.

**Common Preprocessor Directives**

| Directive            | Description                                                          |
| -------------------- | -------------------------------------------------------------------- |
| `#include`           | Includes header files (standard or user-defined) into the program    |
| `#define`            | Defines macros or constants that are replaced throughout the code    |
| `#undef`             | Undefines a macro (removes its definition)                           |
| `#ifdef` / `#ifndef` | Conditional compilation — checks if a macro is defined or not        |
| `#else` / `#elif`    | Specifies alternate compilation paths for conditional compilation    |
| `#endif`             | Ends a conditional preprocessor block                                |
| `#if`                | Evaluates a condition (true/false) and includes code accordingly     |
| `#pragma`            | Provides additional instructions to the compiler (compiler-specific) |

### `#include` – Include Files

The `#include` directive is used to include standard or custom header files into the program.

**Syntax:**

```c
#include <header_file>   // Standard library headers
#include "header_file"   // User-defined header files
```

**Example:**

```c
#include <stdio.h>

int main() {
    printf("Hello, World!\n");
    return 0;
}
```

**Output:**

```c
Hello, World!
```

`stdio.h` is a standard header file included via `<>`.

### `#define` – Define Macros

The `#define` directive defines a `macro` or `constant value` that is replaced by the preprocessor.

**Syntax:**

```c
#define MACRO_NAME value
```

**Example:**

```c
#include <stdio.h>

#define PI 3.14  // Defining a constant

int main() {
    float area = PI * 5 * 5;  // Using the defined constant
    printf("Area of circle: %.2f\n", area);
    return 0;
}
```

**Output:**

```c
Area of circle: 78.50
```

### `#undef` – Undefine Macros

The `#undef` directive is used to `remove a macro definition.`

**Syntax:**

```c
#undef MACRO_NAME
```

**Example:**

```c
#include <stdio.h>

#define MAX 100

int main() {
    printf("Max value: %d\n", MAX);
    #undef MAX  // Undefine MAX
    // printf("Max value: %d\n", MAX);  // Error: MAX is undefined
    return 0;
}
```

**Output:**

```c
Max value: 100
```

### `#ifdef` / `#ifndef` – Conditional Compilation

The `#ifdef` (if defined) and `#ifndef` (if not defined) directives allow you to conditionally include code based on whether a macro is defined.

**Syntax:**

```c
#ifdef MACRO_NAME
    // Code to include if the macro is defined
#endif

#ifndef MACRO_NAME
    // Code to include if the macro is not defined
#endif
```

**Example:**

```c
#include <stdio.h>

#define DEBUG 1

int main() {
    #ifdef DEBUG
        printf("Debugging is enabled.\n");
    #else
        printf("Debugging is not enabled.\n");
    #endif
    return 0;
}
```

**Output:**

```c
Debugging is enabled.
```

### `#else` / `#elif` – Conditional Compilation Else

The `#else` and `#elif` directives allow you to specify alternate paths for conditional compilation.

**Syntax:**

```c
# ifdef MACRO_NAME

    // Code if macro is defined

# elif MACRO_NAME_2

    // Code if the second macro is defined

# else

    // Code if none of the above conditions are true

# endif
```

**Example:**

```c
# include <stdio.h>

# define VERBOSE 0

int main() {

# if VERBOSE

printf("Verbose mode is enabled.\n");

# else

printf("Verbose mode is disabled.\n");

# endif

return 0;
}
```

**Output:**

```c
Verbose mode is disabled.
```

### `#pragma` – Compiler Specific Instructions

The `#pragma` directive provides additional instructions to the compiler, often used to manage compiler warnings or optimizations. The use of `#pragma` can vary between compilers.

**Example:**

```c
#include <stdio.h>

#pragma GCC optimize("O3")  // Optimize for maximum speed

int main() {
    for (int i = 0; i < 1000000; i++);
    printf("Loop completed with optimization.\n");
    return 0;
}
```

**Output:**

```c
Loop completed with optimization.
```

> [!CAUTION]
>
> Actual speed improvement may not be visible in such a small loop but is useful in performance-critical code.

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Error Handling

Error handling refers to the **process of responding to and recovering from errors** in a program.

C does not have built-in exception handling like modern languages (e.g., try-catch), so error detection and response are done using:

- Return values (status codes)
- `errno` (global error variable)
- `perror()` and `strerror()` for error messages

**Common Techniques for Error Handling in C**

| Method       | Description                                               |
| ------------ | --------------------------------------------------------- |
| Return Codes | Functions return `0` or a non-zero code to indicate error |
| `errno`      | Global variable set by system/library calls on error      |
| `perror()`   | Prints a human-readable error message to `stderr`         |
| `strerror()` | Returns a string describing an error code (`errno`)       |

**Example: Return Code Check**

```c
#include <stdio.h>

int divide(int a, int b, int *result) {
    if (b == 0) return 1; // Error: division by zero
    *result = a / b;
    return 0; // Success
}

int main() {
    int res;
    if (divide(10, 0, &res)) {
        printf("Error: Division by zero is not allowed.\n");
    } else {
        printf("Result: %d\n", res);
    }
    return 0;
}
```

**Output:**

```c
Error: Division by zero is not allowed.
```

**Example: Using `errno`, `perror()`, and `strerror()`**

```c
#include <stdio.h>
#include <errno.h>
#include <string.h>

int main() {
    FILE *fp = fopen("nonexistent.txt", "r");

    if (fp == NULL) {
        perror("Error opening file");  // Print error to stderr
        printf("Error Code: %d\n", errno);
        printf("Error Description: %s\n", strerror(errno));
    }

    return 0;
}
```

**Output:**

```c
Error opening file: No such file or directory
Error Code: 2
Error Description: No such file or directory
```

> [!IMPORTANT]
>
> - Always check the return value of functions like `fopen()`, `malloc()`, `read()`, etc.
> - Use `perror()` or `strerror(errno)` to understand the error.
> - Avoid relying on `errno` if the function you're calling does not explicitly set it.

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Practice Problems and Solutions

This section contains a curated set of common C programming problems with complete solutions and sample outputs. It is designed to reinforce core programming concepts such as conditionals, loops, functions, arrays, pointers, and memory management through hands-on practice.

Want to explore the code? **[Click this Repo](https://github.com/msa-iqbal/c-code-solutions)** to dive into each solution and start learning by doing!

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->
