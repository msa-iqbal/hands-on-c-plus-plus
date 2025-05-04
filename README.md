# Hands-on C

C is a general-purpose, procedural, and case-sensitive programming language developed in the early 1970s by Dennis Ritchie at Bell Labs. It is considered one of the most influential languages in computer science history and is often referred to as the "mother of all modern programming languages."

## Table of Contents

1. [Introduction](#introduction)
1. [Comments in C++](#comments-in-c)
1. [Keywords in C++](#keywords-in-c)
1. [Escape sequences](#escape-sequences)
1. [Variables](#variables)
1. [Input and Output:](#input-and-output)
1. [Data Types](#data-types)
1. [Operators](#operators)
1. [Control Flow](#control-flow)
1. [Function](#function)
1. [String](#string)
1. [Array](#array)
1. [Pointers](#pointers)
1. [Object-Oriented Programming (OOP)](#object-oriented-programming-oop)
1. [Inheritance](#inheritance)
1. [Polymorphism](#polymorphism)
1. [Encapsulation](#encapsulation)
1. [Abstraction](#abstraction)
1. [Operator Overloading](#operator-overloading)
1. [Templates and Generics](#templates-and-generics)
1. [Structure, Union and Enum](#structure-union-and-enum)
1. [Dynamic Memory Allocation](#dynamic-memory-allocation)
1. [Type Conversion and Typecasting](#type-conversion-and-typecasting)
1. [File Handling](#file-handling)
1. [Preprocessor Directives](#preprocessor-directives)
1. [Error Handling](#error-handling)
1. [Practice Problems and Projects](#practice-problems-and-projects)

### <img src="https://fonts.gstatic.com/s/e/notoemoji/latest/2699_fe0f/512.gif" alt="⚙" width="15" height="15"> C/C++ Development Setup

**Recommended Tools**

- **Editor**: [Visual Studio Code](https://code.visualstudio.com/) with the official [C/C++ Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)
- **IDE**: [Code::Blocks](http://www.codeblocks.org/) — preconfigured and suitable for beginners
- **Online Compiler**: [CodeChef IDE](https://www.codechef.com/ide) — for quick practice and testing

---

## Introduction

**C++** is a **general-purpose, high-performance programming language** developed as an extension of the **C language** by **Bjarne Stroustrup** at Bell Labs in **1979**. It supports both **procedural** and **object-oriented programming**, making it a **multi-paradigm language**.

### Key Features of C++

- **Compiled Language** – Translates source code into machine code for faster execution.
- **Object-Oriented** – Supports classes, objects, inheritance, polymorphism, encapsulation, and abstraction.
- **Low-Level Manipulation** – Allows direct manipulation of memory using pointers.
- **Rich Standard Library** – Includes the Standard Template Library (STL) for data structures and algorithms.
- **Portable** – Write once, run anywhere (on systems with the same compiler).
- **Fast Execution** – Closer to hardware, C++ is often used in performance-critical applications.

### Why Learn C++?

- Foundation for understanding programming and computer science.
- Teaches memory management, performance tuning, and data structures.
- Used widely in industry and competitive programming.

### Applications of C++

- **Game Development:** Unreal Engine, game engines, physics simulations.
- **System Programming:** Operating systems, device drivers.
- **Embedded Systems:** Firmware for electronic devices.
- **GUI Applications:** Tools using Qt, wxWidgets
- **Financial Systems:** High-frequency trading, banking software.
- **Compilers & Tools:** GCC, LLVM

### Basic Example

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello, World!" << endl;   // Output: Hello, World!
    return 0;
}
```

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Comments in C++

In **C++**, comments are used to document code and improve its readability. Just like in C, **comments are ignored by the compiler**, so they do not affect how the program runs.

C++ supports two types of comments:

### Single-line Comment

Use `//` for single-line comments.

```cpp
// This is a single-line comment
int x = 10;  // This sets x to 10
```

### Multi-line Comment

Use `/* */` for multi-line comments.

```cpp
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

## Keywords in C++

**Keywords** are reserved words in **C++** that have special, predefined meanings. These words form the **syntax and structure** of the language and **cannot be used as identifiers** (such as variable names, function names, or class names).

C++ inherits most of its keywords from C and introduces additional ones to support **object-oriented programming**, **templates**, **exception handling**, **namespaces**, and more.

### C++ Keyword List (based on C++17 standard)

| No. | Keyword   | No. | Keyword        | No. | Keyword            | No. | Keyword        |
| --: | --------- | --: | -------------- | --: | ------------------ | --: | -------------- |
|   1 | `alignas` |  17 | `do`           |  33 | `mutable`          |  49 | `template`     |
|   2 | `alignof` |  18 | `double`       |  34 | `namespace`        |  50 | `this`         |
|   3 | `and`     |  19 | `dynamic_cast` |  35 | `new`              |  51 | `thread_local` |
|   4 | `and_eq`  |  20 | `else`         |  36 | `noexcept`         |  52 | `throw`        |
|   5 | `asm`     |  21 | `enum`         |  37 | `not`              |  53 | `true`         |
|   6 | `auto`    |  22 | `explicit`     |  38 | `not_eq`           |  54 | `try`          |
|   7 | `bitand`  |  23 | `export`       |  39 | `nullptr`          |  55 | `typedef`      |
|   8 | `bitor`   |  24 | `extern`       |  40 | `operator`         |  56 | `typeid`       |
|   9 | `bool`    |  25 | `false`        |  41 | `or`               |  57 | `typename`     |
|  10 | `break`   |  26 | `float`        |  42 | `or_eq`            |  58 | `union`        |
|  11 | `case`    |  27 | `for`          |  43 | `private`          |  59 | `unsigned`     |
|  12 | `catch`   |  28 | `friend`       |  44 | `protected`        |  60 | `using`        |
|  13 | `char`    |  29 | `goto`         |  45 | `public`           |  61 | `virtual`      |
|  14 | `class`   |  30 | `if`           |  46 | `register`         |  62 | `void`         |
|  15 | `compl`   |  31 | `inline`       |  47 | `reinterpret_cast` |  63 | `volatile`     |
|  16 | `const`   |  32 | `int`          |  48 | `return`           |  64 | `wchar_t`      |

> [!NOTE]
>
> - Some older keywords (like `register`, `goto`, `volatile`) are rarely used in modern C++ code.
> - Meanwhile, keywords like `auto`, `nullptr`, `constexpr`, `decltype`, and `template` are heavily used in modern C++.

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Escape sequences

**Escape sequences** (also called **backslash character constants**) are special character combinations starting with a backslash (`\`). They are used to represent characters that either can't be typed directly or perform special actions in strings and characters.

They are essential in **text formatting**, **output control**, and **special character representation**.

### Common Escape Sequences in C++

| Escape Sequence | Meaning                           | Example in Code            | Output:         |
| --------------- | --------------------------------- | -------------------------- | --------------- |
| `\n`            | New line                          | `cout << "Hello\nWorld";`  | Hello<br>World  |
| `\t`            | Horizontal tab                    | `cout << "Hello\tWorld";`  | Hello  World    |
| `\b`            | Backspace                         | `cout << "Helloo\b!";`     | Hello!          |
| `\r`            | Carriage return                   | `cout << "Hello\rWorld";`  | World           |
| `\f`            | Form feed (page break)            | _Rarely used_              | —               |
| `\a`            | Alert (bell sound)                | `cout << "\a";`            | 🔔 (beep sound) |
| `\\`            | Backslash                         | `cout << "\\";`            | `\`             |
| `\'`            | Single quote                      | `cout << "\'";`            | `'`             |
| `\"`            | Double quote                      | `cout << "\"";`            | `"`             |
| `\?`            | Question mark                     | `cout << "\?";`            | `?`             |
| `\0`            | Null character (end of string)    | _Used in character arrays_ | —               |
| `\ooo`          | Octal number (e.g., `\141` = 'a') | `cout << "\141";`          | `a`             |
| `\xhh`          | Hexadecimal (e.g., `\x61` = 'a')  | `cout << "\x61";`          | `a`             |

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Line1\nLine2\n";           // newline
    cout << "Tab\tSpace\n";             // tab
    cout << "Backslash: \\\n";          // backslash
    cout << "Quote: \' \" \n";          // single and double quotes
    cout << "Beep\a\n";                 // beep sound (if supported)
    return 0;
}
```

> [!NOTE]
>
> - Escape sequences are used in both character literals (`'\n'`) and string literals (`"\n"`).
> - They are crucial for:
>
>   - Formatting output
>   - Representing invisible/special characters
>   - Handling control characters in streams
>
> - Some escape sequences (`\a`, `\f`, etc.) may not have visible effects in all modern terminal environments.

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Variables

A **variable** in C++ is a **named memory location** used to store data that can be modified during program execution.

- Acts as a **storage unit** for data.
- Must be **declared** with a data type before use.
- Its value **can be changed** at any time during execution.

**Syntax:**

```cpp
<data_type> <variable_name>;
<data_type> <variable_name> = value;
```

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int age;         // Declaration
    age = 25;        // Assignment

    float pi = 3.14; // Declaration + Assignment

    cout << "Age: " << age << endl;
    cout << "Pi: " << pi << endl;

    return 0;
}
```

**Output:**

```plaintext
Age: 25
Pi: 3.14
```

### Rules for Naming Variables

| Rule No. | Rule                                                            |
| -------: | --------------------------------------------------------------- |
|        1 | Must begin with a **letter** (A–Z or a–z) or **underscore `_`** |
|        2 | Can include **letters, digits (0–9), and underscores**          |
|        3 | **Cannot start with a digit**                                   |
|        4 | **Cannot use C++ keywords** (like `int`, `return`, etc.)        |
|        5 | **Case-sensitive** (`Age` and `age` are different)              |
|        6 | Should be **meaningful** (use descriptive names)                |

### Types of Variables in C++

| Type         | Description                                                 | Scope          |
| ------------ | ----------------------------------------------------------- | -------------- |
| **Local**    | Declared inside a function/block                            | Function/block |
| **Global**   | Declared outside all functions, accessible by all functions | Whole program  |
| **Static**   | Retains value between function calls, has local scope       | Block/function |
| **Extern**   | Declared in one file, defined in another (shared globally)  | Global         |
| **Register** | Suggests storing variable in a CPU register (faster access) | Local          |

**Example: (Variable Types)**

```cpp
#include <iostream>
using namespace std;

int globalVar = 10; // Global variable

void function() {
    static int staticVar = 0; // Static variable
    staticVar++;
    cout << "Static: " << staticVar << endl;
}

int main() {
    int localVar = 5; // Local variable

    cout << "Global: " << globalVar << endl;
    cout << "Local: " << localVar << endl;

    function();
    function();

    return 0;
}
```

**Output:**

```plaintext
Global: 10
Local: 5
Static: 1
Static: 2
```

**✅ Good Practice Example**

```cpp
int studentAge = 20;
float temperature = 36.6;
char grade = 'A';
```

### Constants vs Variables

| Feature      | Variable                    | Constant                    |
| ------------ | --------------------------- | --------------------------- |
| Value change | Can change during execution | Cannot change once assigned |
| Declaration  | `int age = 20;`             | `const int age = 20;`       |

> [!TIP]
>
> - Variables store values in RAM.
> - Use const for read-only values.
> - Always initialize variables to avoid garbage values.
> - Use descriptive names to improve code readability.

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Input and Output

C++ uses **standard input/output objects** provided by the `iostream` header for communication between the user and the program.

### Header File

```cpp
#include <iostream>
```

💡 You must include this header to use cin, cout, and other standard I/O utilities.

### Output: `cout`

**`cout`** is used for output to the console. It uses the **insertion operator (`<<`)**.

**Syntax:**

```cpp
cout << "text" << variable;
```

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int age = 20;
    cout << "Age is " << age << endl;
    return 0;
}
```

**Output:**

```plaintext
Age is 20
```

### Input: `cin`

**`cin`** is used to read input from the user. It uses the **extraction operator (`>>`)**.

**Syntax:**

```cpp
cin >> variable;
```

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int age;
    cout << "Enter your age: ";
    cin >> age;
    cout << "You entered: " << age << endl;
    return 0;
}
```

**Output: (sample interaction)**

```plaintext
Enter your age: 25
You entered: 25
```

### Format Specifiers? No Need

Unlike C, **C++ does not use format specifiers** like `%d`, `%f`. It handles **type safety** with stream objects (`cin`, `cout`).

**Example: Input and Output:**

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    int age;
    float salary;
    char initial;
    string name;

    // Input
    cout << "Enter your age: ";
    cin >> age;

    cout << "Enter your salary: ";
    cin >> salary;

    cout << "Enter your first initial: ";
    cin >> initial;

    cout << "Enter your name: ";
    cin >> name; // string input (single word only)

    // Output:
    cout << "\n--- OUTPUT ---\n";
    cout << "Age: " << age << endl;
    cout << "Salary: " << salary << endl;
    cout << "Initial: " << initial << endl;
    cout << "Name: " << name << endl;

    return 0;
}
```

**Output:**

```plaintext
Enter your age: 25
Enter your salary: 65000.5
Enter your first initial: M
Enter your name: Alice

--- OUTPUT ---
Age: 25
Salary: 65000.5
Initial: M
Name: Alice
```

### Full-Line Input: `getline()`

Use `getline(cin, str)` to accept **entire lines with spaces**.

**Example: `getline()`**

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string fullName;
    cout << "Enter your full name: ";
    getline(cin, fullName);
    cout << "Hello, " << fullName << "!" << endl;
    return 0;
}
```

**Output:**

```cpp
Enter your full name: John Smith
Hello, John Smith!
```

### Other I/O Functions in C++

| Function    | Purpose                         | Notes                 |
| ----------- | ------------------------------- | --------------------- |
| `cin`       | Read input (no format needed)   | Safe and type-checked |
| `cout`      | Output: to console              | Uses `<<` operator    |
| `getline()` | Read full line including spaces | Safer for strings     |
| `cerr`      | Output: error messages          | Unbuffered            |
| `clog`      | Output: error/info messages     | Buffered              |

> [!NOTE]
>
> - Use `getline()` to handle strings with **spaces**.
> - `cin` ignores **leading whitespace**, but `getline()` does not.
> - `cin >>` stops at the first whitespace character.
> - `cout` automatically formats values (no need for `%d`, `%f`, etc.).

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Data Types

**Data types** in C++ specify the kind of data a variable can store. C++ supports both **primitive** and **user-defined** types. Unlike C, **C++ uses type-safe I/O operations** with `cin` and `cout`, so there are **no format specifiers**.

### Basic Data Types

| Data Type | Description                               | Size (Typical) | Range                                               |
| --------- | ----------------------------------------- | -------------- | --------------------------------------------------- |
| `char`    | Stores a single character                 | 1 byte         | `-128` to `127` (signed) or `0` to `255` (unsigned) |
| `int`     | Stores integer values                     | 4 bytes        | `-2,147,483,648` to `2,147,483,647`                 |
| `float`   | Single-precision floating point number    | 4 bytes        | `±3.4E±38` (approx.)                                |
| `double`  | Double-precision floating point number    | 8 bytes        | `±1.7E±308` (approx.)                               |
| `void`    | Represents absence of type (e.g., return) | 0 bytes        | N/A                                                 |

### Derived Data Types

| Type      | Description                                               |
| --------- | --------------------------------------------------------- |
| `array`   | Collection of elements of the same type                   |
| `pointer` | Stores memory address of another variable                 |
| `struct`  | Groups variables of different types together              |
| `union`   | Shares memory among multiple variables                    |
| `enum`    | User-defined type with named constants (usually integers) |

### Type Modifiers

| Modifier   | Effect                                                             |
| ---------- | ------------------------------------------------------------------ |
| `signed`   | Allows negative and positive values (default for `int` and `char`) |
| `unsigned` | Only positive values, larger upper bound                           |
| `long`     | Extends the range of `int` or `double`                             |
| `short`    | Reduces the size of `int`, saves memory                            |

**Example: Using Various Data Types**

```cpp
#include <iostream>
using namespace std;

int main() {
    char letter = 'A';
    int num = 100;
    float pi = 3.14f;
    double precisePi = 3.1415926535;
    unsigned int uNum = 250;
    long long bigNum = 1234567890123;
    short smallNum = 10;
    int* ptr = &num;

    // Output: without format specifiers
    cout << "Character: " << letter << endl;
    cout << "Integer: " << num << endl;
    cout << "Float: " << pi << endl;
    cout << "Double: " << precisePi << endl;
    cout << "Unsigned Int: " << uNum << endl;
    cout << "Long Long: " << bigNum << endl;
    cout << "Short: " << smallNum << endl;
    cout << "Pointer (address of num): " << ptr << endl;

    return 0;
}
```

**Output:**

```plaintext
Character: A
Integer: 100
Float: 3.14
Double: 3.14159
Unsigned Int: 250
Long Long: 1234567890123
Short: 10
Pointer (address of num): 0x7ffeeef4b7dc
```

> [!IMPORTANT] - Format Specifiers? Not in C++
>
> - C++ **does not use** format specifiers like `%d`, `%f`, etc. Instead:
>   - `cin >> var;` and `cout << var;` work with the variable's type.
>   - It’s **type-safe**, unlike C's `printf()`/`scanf()` which rely on specifiers.

### Want to Format Output:?

Use C++ I/O manipulators like `std::fixed`, `std::setprecision`, `std::setw`, etc. from `<iomanip>`.

**Example: Precision Formatting**

```cpp
#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    double num = 3.14159265;

    cout << "Default: " << num << endl;
    cout << "Fixed with 2 decimal places: " << fixed << setprecision(2) << num << endl;

    return 0;
}
```

**Output:**

```plaintext
Default: 3.14159
Fixed with 2 decimal places: 3.14
```

> [!NOTE]
>
> - C++ removes the need for format specifiers by overloading `<<` and `>>`.
> - Type safety makes input/output less error-prone than C.
> - You can still use `printf()` and `scanf()` in C++, but it's discouraged in modern practice.

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Operators

Operators in C++ are **symbols** used to perform operations on **variables and values**.

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

```cpp
condition ? expression_if_true : expression_if_false;
```

**Example:**

```cpp
int a = 10, b = 20;
int max = (a > b) ? a : b;
cout << "Max: " << max << endl;  // Output: 20
```

### **Sizeof Operator**

Returns the size (in bytes) of a variable or type.

**Example:**

```cpp
cout << sizeof(int);  // Output: 4 (usually)
```

### **Comma Operator**

Evaluates multiple expressions, returns the last.

**Example:**

```cpp
int x = (a = 5, b = 10);  // x = 10
```

### **Pointer Operators**

Used for pointer operations.

| Operator | Meaning     | Example |
| -------- | ----------- | ------- |
| `*`      | Dereference | `*ptr`  |
| `&`      | Address-of  | `&var`  |

**🟢🔵🟣 Complete Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 5, b = 2;

    cout << "Addition: " << a + b << endl;
    cout << "Greater? " << (a > b) << endl;
    cout << "Logical AND: " << ((a > 0) && (b > 0)) << endl;
    cout << "Bitwise AND: " << (a & b) << endl;
    cout << "Ternary Max: " << ((a > b) ? a : b) << endl;

    return 0;
}
```

**Output:**

```plaintext
Addition: 7
Greater? 1
Logical AND: 1
Bitwise AND: 0
Ternary Max: 5
```

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Control Flow

Control structures in C++ determine the **flow of execution** of the program — **which blocks of code get executed** and when.

**Types of Control Structures:**

1. **Conditional Statements (Decision-making)**
2. **Looping Statements (Iteration)**
3. **Jump Statements (Branching)**

### **Conditional Statements:**

Used to **execute code based on conditions**.

#### **`if` Statement**

```cpp
if (condition) {
    // code to execute if condition is true
}
```

Example:

```cpp
#include <iostream>
using namespace std;

int main() {
    int number = 10;

    if (number > 0) {
        cout << "The number is positive." << endl;
    }

    return 0;
}
```

Output:

```plaintext
The number is positive.
```

#### **`if-else` Statement**

```cpp
if (condition) {
    // if true
} else {
    // if false
}
```

Example:

```cpp
#include <iostream>
using namespace std;

int main() {
    int number = 10;

    if (number > 0) {
        cout << "The number is positive." << endl;
    } else {
        cout << "The number is not positive." << endl;
    }

    return 0;
}
```

Output:

```plaintext
The number is positive.
```

#### **`else-if` Ladder**

```cpp
if (condition1) {
    // block 1
} else if (condition2) {
    // block 2
} else {
    // default block
}
```

Example:

```cpp
#include <iostream>
using namespace std;

int main() {
    int number = 0;

    if (number > 0) {
        cout << "The number is positive." << endl;
    } else if (number < 0) {
        cout << "The number is negative." << endl;
    } else {
        cout << "The number is zero." << endl;
    }

    return 0;
}
```

Output:

```plaintext
The number is zero.
```

#### **Nested `if`**

```cpp
if (condition1) {
    if (condition2) {
        // block
    }
}
```

Example:

```cpp
#include <iostream>
using namespace std;

int main() {
    int number = 25;

    if (number > 0) {
        if (number < 100) {
            cout << "Number is positive and less than 100." << endl;
        }
    }

    return 0;
}
```

Output:

```plaintext
Number is positive and less than 100.
```

#### **Switch-case**

Used for multiple constant values.

```cpp
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

```cpp
#include <iostream>
using namespace std;

int main() {
    int day = 3;

    switch (day) {
        case 1:
            cout << "Saturday" << endl;
            break;
        case 2:
            cout << "Sunday" << endl;
            break;
        case 3:
            cout << "Monday" << endl;  // this block is activated
            break;
        case 4:
            cout << "Tuesday" << endl;
            break;
        case 5:
            cout << "Wednesday" << endl;
            break;
        case 6:
            cout << "Thursday" << endl;
            break;
        case 7:
            cout << "Friday" << endl;
            break;
        default:
            cout << "Invalid day" << endl;
            break;
    }

    return 0;
}
```

Output:

```plaintext
Monday
```

### **Looping Statements**

Used to **repeat a block of code** multiple times.

#### **`for` Loop**

```cpp
for (initialization; condition; increment) {
    // code block
}
```

Example:

```cpp
#include <iostream>
using namespace std;

int main() {
    // Print numbers from 1 to 5
    for (int i = 1; i <= 5; i++) {
        cout << i << " ";
    }

    return 0;
}
```

Output:

```plaintext
1 2 3 4 5
```

#### **`while` Loop**

```cpp
while (condition) {
    // code block
}
```

Example:

```cpp
#include <iostream>
using namespace std;

int main() {
    int i = 1;

    // Print numbers from 1 to 5
    while (i <= 5) {
        cout << i << " ";
        i++; // increment i
    }

    return 0;
}
```

Output:

```plaintext
1 2 3 4 5
```

#### **`do-while` Loop**

```cpp
do {
    // code block
} while (condition);
```

💡 Executes at least once even if the condition is false.

Example:

```cpp
#include <iostream>
using namespace std;

int main() {
    int i = 1;

    // Print numbers from 1 to 5 using do-while loop
    do {
        cout << i << " ";
        i++; // increment i
    } while (i <= 5);

    return 0;
}
```

Output:

```plaintext
1 2 3 4 5
```

#### **Difference between `while` and `do-while`**

| **Feature**        | `while` **Loop**                                            | `do-while` **Loop**                                                          |
| ------------------ | ----------------------------------------------------------- | ---------------------------------------------------------------------------- |
| Condition check    | Before loop body                                            | After loop body                                                              |
| Minimum executions | 0                                                           | 1                                                                            |
| Use cases          | When you're unsure if the loop should execute at least once | When you want the loop to execute at least once, regardless of the condition |

### **Jump Statements**

Used to **control the flow** of loops and functions.

| Keyword    | Description                                          |
| ---------- | ---------------------------------------------------- |
| `break`    | Exits loop or switch block                           |
| `continue` | Skips the rest of the loop for the current iteration |
| `goto`     | Jumps to a labeled part of the program (⚠️ avoid)    |
| `return`   | Exits from a function                                |

#### **Example (break):**

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 10; i++) {
        if (i == 5)
            break;
        cout << i << " ";
    }
    return 0;
}
```

**Output:**

```plaintext
1 2 3 4
```

#### **Example (continue):**

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 5; i++) {
        if (i == 3)
            continue;
        cout << i << " ";
    }
    return 0;
}
```

**Output:**

```plaintext
1 2 4 5
```

**Example (goto):**

```cpp
#include <iostream>
using namespace std;

int main() {
    int num;

start:
    cout << "Enter a positive number: ";
    cin >> num;

    if (num < 0) {
        cout << "Negative number entered. Try again.\n";
        goto start;  // jump to start label
    }

    cout << "You entered: " << num << endl;
    return 0;
}
```

**Output:**

```
Enter a positive number: -5
Negative number entered. Try again.
Enter a positive number: 10
You entered: 10
```

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Function

A **function** in C++ is a **block of code** that performs a specific task. It helps in organizing code, avoiding repetition, and improving reusability.

> **Real-life analogy to understand function:**
>
> > A function in C++ is like a coffee machine — you press a button (input), it brews coffee (process), and gives you a cup (output).

**Types of Functions**

1. **User-defined Functions**: Created by the programmer.
2. **Built-in (Library) Functions**: Provided by C++ standard libraries.

### **User-defined Functions**

**Syntax (Declaration + Definition + Call):**

```cpp
// ❏ Function Declaration
returnType functionName(dataType1 parameter1, dataType2 parameter2, ...);

// ❏ Function Definition
returnType functionName(dataType1 parameter1, dataType2 parameter2, ...) {
    // code block
    return value; // If the function returns a value
}

// ❏ Function Call
functionName(arguments);
```

**The Function Components are -**

- **Function Declaration**
- **Function Definition**
- **Function Call**

**Function Declaration:**

It tells the compiler about the function's name, return type, and parameters — before it is used.

```cpp
int add(int a, int b);  // Declaration
```

- **Return type**: `int`
- **Function name**: `add`
- **Parameters**: `int a, int b`

_💡 Think of this as informing the compiler: "Hey! I’ll use a function like this later."_

**Function Definition:**

Contains the actual **code (body)** that runs when the function is called.

```cpp
int add(int a, int b) {
    return a + b;
}
```

- This is where the logic of **addition** is implemented.

**Function Call:**

Used to **invoke/execute** the function and get the result.

```cpp
int result = add(3, 5);  // Function call
```

- Passes arguments `3` and `5` to the function.
- Stores the returned value in `result`.

### **Full Example with All Components**

```cpp
#include <iostream>

using namespace std;

// 1. Function Declaration
int add(int a, int b);

int main() {
    // 3. Function Call
    int sum = add(10, 20);
    cout << "Sum = " << sum << endl;
    return 0;
}

// 2. Function Definition
int add(int a, int b) {
    return a + b;
}
```

**Output:**

```plaintext
Sum = 30
```

**Example (No return, no parameters):**

```cpp
#include <iostream>

using namespace std;

void greet() {
    cout << "Hello, World!" << endl;
}

int main() {
    greet();
    return 0;
}
```

**Output:**

```plaintext
Hello, World!
```

**Example (With return, with parameters):**

```cpp
#include <iostream>

using namespace std;

int add(int a, int b) {
    return a + b;
}

int main() {
    int sum = add(4, 5);
    cout << "Sum = " << sum << endl;
    return 0;
}
```

**Output:**

```plaintext
Sum = 9
```

**Example (Function Declaration (Prototype)):**

```cpp
#include <iostream>

using namespace std;

int multiply(int, int); // function declaration

int main() {
    cout << "Result = " << multiply(3, 4) << endl;
    return 0;
}

int multiply(int x, int y) {
    return x * y;
}
```

**Output:**

```plaintext
Result = 12
```

### **Recursive Function**

A **recursive function** is a function that calls itself to solve smaller versions of a problem.

> **Real-life analogy to understand recursion:**
>
> > Like opening a set of nested boxes — each box opens the next, until the smallest box is reached.

**Example:**

```cpp
#include <iostream>

using namespace std;

int factorial(int n) {
    if (n == 0) return 1;
    return n * factorial(n - 1);
}

int main() {
    cout << "Factorial of 5 = " << factorial(5) << endl;
    return 0;
}
```

**Output:**

```plaintext
Factorial of 5 = 120
```

**Return Types in C++ Functions:**

| Return Type | Meaning             | Example           |
| ----------- | ------------------- | ----------------- |
| `void`      | No return value     | `void show()`     |
| `int`       | Returns integer     | `int getSum()`    |
| `float`     | Returns float value | `float avg()`     |
| `char`      | Returns a character | `char getGrade()` |

**Parameter Types:**

| Type                 | Example                 | Description                        |
| -------------------- | ----------------------- | ---------------------------------- |
| No Parameters        | `void greet(void)`      | Takes no input                     |
| With Parameters      | `int sum(int a, int b)` | Takes input values                 |
| Default (Not in C++) | ❌                      | C++ doesn’t support default params |
| Variable Arguments   | `int printf(...)`       | Use `stdarg.h`                     |

**Function Categories:**

| Function Type              | Parameters | Return Value | Example                   |
| -------------------------- | ---------- | ------------ | ------------------------- |
| No Parameters, No Return   | No         | No           | `void greet(void)`        |
| With Parameters, No Return | Yes        | No           | `void greet(char name[])` |
| No Parameters, With Return | No         | Yes          | `int getTime(void)`       |
| With Parameters and Return | Yes        | Yes          | `int add(int a, int b)`   |

### **Built-in (Library) Functions:**

These are pre-defined functions provided by C++'s standard library.

Example: `cout`, `cin`, `strlen()`, `malloc()`, etc.

**Header Files:**

You don't need to define these functions, but you must include the appropriate header files.

Some Common Header Files:

- **`<iostream>`**: For input-output.

  - Includes: `cout`, `cin`, `endl`

- **`<cmath>`**: For mathematical functions.

  - Includes: `sqrt()`, `pow()`, `sin()`, `cos()`, `tan()`

- **`<cstring>`**: For string manipulation.

  - Includes: `strlen()`, `strcpy()`, `strcmp()`, `strcat()`

**Example: `sizeof()`**

```cpp
#include <iostream>
using namespace std;

int main() {
    char a;
    int b;
    float c;
    double d;

    cout << "Size of Character is: " << sizeof(a) << " bytes" << endl;
    cout << "Size of Integer is: " << sizeof(b) << " bytes" << endl;
    cout << "Size of Float is: " << sizeof(c) << " bytes" << endl;
    cout << "Size of Double is: " << sizeof(d) << " bytes" << endl;
    return 0;
}
```

**Output:**

```
Size of Character is: 1 bytes
Size of Integer is: 4 bytes
Size of Float is: 4 bytes
Size of Double is: 8 bytes
```

**Example (String): `strlen()`**

```cpp
#include <iostream>
#include <cstring>
using namespace std;

int main() {
    char name[] = "Nazrull";
    int len = strlen(name);
    cout << "Length: " << len << endl;
    return 0;
}
```

**Output:**

```
Length: 7
```

**Example (Random Number Generator): `rand()`**

```cpp
#include <iostream>
#include <cstdlib>  // Using header file for random numbers

using namespace std;

int main() {
    for (int i = 1; i <= 5; i++) {
        int randomNum = rand(); // Random numbers generator
        cout << "Random Number: " << randomNum << endl;
    }
    return 0;
}
```

**Output:**

```
Random Number 1: 1804289383
Random Number 2: 846930886
Random Number 3: 1681692777
```

(Note: Output: will vary every time if seeded using `srand(time(0));`)

**Example (String Concatenation): `strcat()`**

```cpp
#include <iostream>
#include <cstring>
using namespace std;

int main() {
    char name1[20] = "Michael ";
    char name2[] = "Scofield";
    strcat(name1, name2);
    cout << "Concatenated Name: " << name1 << endl;
    return 0;
}
```

**Output:**

```
Concatenated Name: Michael Scofield
```

**Example (String Comparison): `strcmp()`**

```cpp
#include <iostream>
#include <cstring>
using namespace std;

int main() {
    char name1[] = "Michael";
    char name2[] = "Scofield";

    int result = strcmp(name1, name2);

    if (result == 0)
        cout << "Strings are equal" << endl;
    else
        cout << "Strings aren't equal" << endl;

    return 0;
}
```

**Output:**

```
Strings aren't equal
```

**Example (Mathematical Operations)**

**`abs()`**, **`sqrt()`**, **`pow()`**, **`log()`** etc., are similarly available in the `<cmath>` header for mathematical operations.

This C++ version preserves the same functionality and syntax from the C code, but uses C++-specific libraries like `<iostream>` for input/output and `<cstring>` for string manipulations.

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## String

In programming, a string is a sequence of characters used to represent text.

In C++, we can work with **two types of strings**:

1. **C-style strings** – like in C, implemented as character arrays ending with `'\0'`.
2. **C++ `std::string`** – part of the C++ Standard Library, safer and easier to use.

### C-style Strings

**Declaration:**

```cpp
char str[10]; // Can store up to 9 characters + null terminator '\0'
```

### Ways to Initialize

**Using String Literal**

```cpp
char str[] = "Hello";
```

Automatically appends `'\0'` at the end.

**Using Character Array**

```cpp
char str[] = {'H', 'e', 'l', 'l', 'o', '\0'};
```

**Example: Basic C-style String Input and Output:**

```cpp
#include <iostream>
using namespace std;

int main() {
    char name[20];

    cout << "Enter your name: ";
    cin >> name;  // Reads until first space

    cout << "Hello, " << name << "!" << endl;

    return 0;
}
```

**Output:**

```
Enter your name: Alice
Hello, Alice!
```

**Example: Using `cin.getline()` for Full Line Input**

```cpp
#include <iostream>
using namespace std;

int main() {
    char fullName[50];

    cout << "Enter your full name: ";
    cin.getline(fullName, 50);  // Safe input with spaces

    cout << "Your name is: " << fullName << endl;

    return 0;
}
```

**Output:**

```
Enter your full name: Alice Johnson
Your name is: Alice Johnson
```

### C++ `std::string`

**Declaration and Initialization**

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string name = "Hello";
    cout << name << endl;
    return 0;
}
```

**Example: String Input and Output: Using `std::string`**

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string name;

    cout << "Enter your name: ";
    cin >> name;  // Reads a single word

    cout << "Hello, " << name << "!" << endl;

    return 0;
}
```

**Output:**

```
Enter your name: Alice
Hello, Alice!
```

\*\*Example: Full Line Input Using `getline()`

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string fullName;

    cout << "Enter your full name: ";
    getline(cin, fullName);  // Reads full line including spaces

    cout << "Hello, " << fullName << "!" << endl;

    return 0;
}
```

**Output:**

```
Enter your full name: Alice Johnson
Hello, Alice Johnson!
```

### Common String Functions

**For C-style strings (`<cstring>`) functions**

| Function        | Description                      | Example                    |
| --------------- | -------------------------------- | -------------------------- |
| `strlen(s)`     | Returns length                   | `strlen("Hi") → 2`         |
| `strcpy(d, s)`  | Copies string `s` to `d`         | `strcpy(dest, src)`        |
| `strcat(d, s)`  | Concatenates `s` to `d`          | `strcat(dest, src)`        |
| `strcmp(s1,s2)` | Compares two strings             | `strcmp("abc", "abc") → 0` |
| `strrev(s)`     | Reverses a string (non-standard) | `strrev("abc") → "cba"`    |

**For `std::string` (more powerful)**

| Operation         | Example                    | Output:          |
| ----------------- | -------------------------- | ---------------- |
| Length            | `name.length()`            | Length of string |
| Concatenation     | `s1 + s2`                  | Combines strings |
| Comparison        | `s1 == s2`                 | `true/false`     |
| Access character  | `name[0]`                  | First letter     |
| Substring         | `name.substr(0, 5)`        | Partial string   |
| Find substring    | `name.find("John")`        | Index or `npos`  |
| Replace substring | `name.replace(0, 5, "Hi")` | Replace part     |

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Array

An **array** in C++ is a **collection of elements** of the same data type stored in **contiguous memory locations**.

> **Real-life analogy:**  
> An array is like a bookshelf. Each shelf (array index) holds one book (element), and you can access any book by its position (index).

**Syntax:**

```cpp
data_type array_name[array_size];
```

- `data_type`: Type of elements (e.g., `int`, `float`, `char`)
- `array_name`: Name of the array
- `array_size`: Number of elements

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int numbers[5] = {10, 20, 30, 40, 50};

    cout << "First number: " << numbers[0] << endl;
    cout << "Third number: " << numbers[2] << endl;

    return 0;
}
```

**Output:**

```
First number: 10
Third number: 30
```

**Array Declaration, Initialization & Access**

```cpp
// Array Declaration, Initialization
int numbers[5] = {10, 20, 30, 40, 50};

// Array Access
cout << numbers[0];  // Output: 10
cout << numbers[2];  // Output: 30
```

**Array Accessing Diagram:**

```
Index:     0    1    2    3    4
Value:    10   20   30   40   50
           ↑         ↑
     numbers[0]  numbers[2]
```

**Types of Arrays in C++**

1. Linear / 1D Arrays
2. Multi-Dimensional:

   - 2D Array (Matrix)
   - 3D Array

### Linear or 1D Array

```cpp
#include <iostream>
using namespace std;

int main() {
    int numbers[5] = {10, 20, 30, 40, 50};

    for (int i = 0; i < 5; i++) {
        cout << numbers[i] << " ";
    }

    return 0;
}
```

**Output:**

```
10 20 30 40 50
```

### Matrix or 2D Array

```cpp
#include <iostream>
using namespace std;

int main() {
    int matrix[3][4] = {
        {1, 2, 3, 4},
        {5, 6, 7, 8},
        {9, 10, 11, 12}
    };

    int element = matrix[1][2]; // 2nd row, 3rd col

    cout << "Access Single Element: " << element << endl << endl;

    cout << "Matrix Elements:" << endl;
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 4; j++) {
            cout << matrix[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}
```

**Output:**

```
Access Single Element: 7

Matrix Elements:
1 2 3 4
5 6 7 8
9 10 11 12
```

### 3D Array or Multi-dimensional

```cpp
#include <iostream>
using namespace std;

int main() {
    int arr[2][3][4] = {
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

    cout << "Access Single Element: " << arr[1][2][3] << endl << endl;

    for (int i = 0; i < 2; i++) {
        cout << "Plane " << i << ":" << endl;
        for (int j = 0; j < 3; j++) {
            for (int k = 0; k < 4; k++) {
                cout << arr[i][j][k] << " ";
            }
            cout << endl;
        }
        cout << endl;
    }

    return 0;
}
```

**Output:**

```
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

### **Array Initialization Methods:**

| Method                 | Syntax Example                   |
| ---------------------- | -------------------------------- |
| Full initialization    | `int arr[3] = {1, 2, 3};`        |
| Partial initialization | `int arr[3] = {1}; // {1, 0, 0}` |
| Zero initialization    | `int arr[3] = {0};`              |
| Size inferred          | `int arr[] = {1, 2, 3, 4};`      |

**Example: Input from User**

```cpp
#include <iostream>
using namespace std;

int main() {
    int a[5];
    cout << "Enter 5 numbers: ";

    for (int i = 0; i < 5; i++) {
        cin >> a[i];
    }

    cout << "You entered: ";
    for (int i = 0; i < 5; i++) {
        cout << a[i] << " ";
    }

    return 0;
}
```

**Output: (if input = 1 2 3 4 5):**

```
Enter 5 numbers: You entered: 1 2 3 4 5
```

**Example: Modifying Array Elements**

```cpp
#include <iostream>
using namespace std;

int main() {
    int arr[5] = {5, 10, 15, 20, 25};

    // Print original array
    cout << "Original Array: ";
    for (int i = 0; i < 5; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;

    // Modify elements
    arr[0] = 100; // change first element
    arr[3] = 400; // change fourth element

    // Print modified array
    cout << "Modified Array: ";
    for (int i = 0; i < 5; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;

    return 0;
}
```

**Output:**

```
Original Array: 5 10 15 20 25
Modified Array: 100 10 15 400 25
```

**Example: Sum of Array Elements**

```cpp
#include <iostream>
using namespace std;

int main() {
    int a[5] = {1, 2, 3, 4, 5};
    int sum = 0;

    for (int i = 0; i < 5; i++) {
        sum += a[i];
    }

    cout << "Sum = " << sum << endl;
    return 0;
}
```

**Output:**

```
Sum = 15
```

**Example: Passing Arrays to Functions**

```cpp
#include <iostream>
using namespace std;

void displayArray(int arr[], int size) {
    for (int i = 0; i < size; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
}

int main() {
    int nums[] = {10, 20, 30, 40, 50};
    int length = sizeof(nums) / sizeof(nums[0]);

    cout << "Array elements: ";
    displayArray(nums, length);

    return 0;
}
```

**Output:**

```
Array elements: 10 20 30 40 50
```

**Example: Array of Pointers**

```cpp
#include <iostream>
using namespace std;

int main() {
    int numbers[] = {10, 20, 30, 40, 50};
    int* ptrs[5];

    for (int i = 0; i < 5; i++) {
        ptrs[i] = &numbers[i];
    }

    for (int i = 0; i < 5; i++) {
        cout << "Element " << i + 1 << ": " << *ptrs[i] << endl;
    }

    return 0;
}
```

**Output:**

```
Element 1: 10
Element 2: 20
Element 3: 30
Element 4: 40
Element 5: 50
```

**Example: 2D Array of Pointers**

```cpp
#include <iostream>
using namespace std;

int main() {
    int numbers[3][4] = {{1, 2, 3, 4},
                         {5, 6, 7, 8},
                         {9, 10, 11, 12}};
    int* ptrs[3][4];

    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 4; j++) {
            ptrs[i][j] = &numbers[i][j];
        }
    }

    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 4; j++) {
            cout << "Element [" << i << "][" << j << "]: " << *ptrs[i][j] << endl;
        }
    }

    return 0;
}
```

**Output:**

```
Element [0][0]: 1
Element [0][1]: 2
...
Element [2][3]: 12
```

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Pointers

A **pointer** is a variable that stores the **memory address** of another variable.

**Syntax:**

```cpp
data_type *pointer_name;
```

- `data_type` — type of data the pointer points to
- `*` — denotes it’s a pointer
- `pointer_name` — name of the pointer variable

**Example (Declarations):**

```cpp
int *ptrInt;      // Pointer to int
char *ptrChar;    // Pointer to char
float *ptrFloat;  // Pointer to float
```

### Assigning a Value to a Pointer

You can assign the **address of a variable** using the **address-of operator (`&`)**.

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10;
    int *p;
    p = &a;

    cout << "Value of a: " << a << endl;
    cout << "Address of a: " << &a << endl;
    cout << "Pointer p stores address: " << p << endl;
    cout << "Value pointed by p (*p): " << *p << endl;

    return 0;
}
```

**Output:**

```
Value of a: 10
Address of a: 0x7ffee8e73abc   // (Actual output may vary)
Pointer p stores address: 0x7ffee8e73abc
Value pointed by p (*p): 10
```

### Accessing and Modifying Values via Pointer

You can **access or modify** values using the **dereference operator (`*`)**.

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10;
    int *p = &a;

    cout << "Value of a: " << a << endl;
    cout << "Value of a via pointer: " << *p << endl;

    *p = 20;  // Modify a via pointer
    cout << "New value of a: " << a << endl;

    return 0;
}
```

**Output:**

```
Value of a: 10
Value of a via pointer: 10
New value of a: 20
```

### Pointer Arithmetic

Pointers can be incremented or decremented to move between elements in arrays.

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int arr[] = {10, 20, 30, 40, 50};
    int *p = arr;

    cout << *p << endl;
    p++;  // Move to next element
    cout << *p << endl;

    return 0;
}
```

**Output:**

```
10
20
```

### Pointers and Arrays

In C++, array names act like pointers to their first elements.

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int arr[5] = {10, 20, 30, 40, 50};
    int *p = arr;

    for (int i = 0; i < 5; i++) {
        cout << "Element " << i << ": " << *(p + i) << endl;
    }

    return 0;
}
```

**Output:**

```
Element 0: 10
Element 1: 20
Element 2: 30
Element 3: 40
Element 4: 50
```

### Pointer to Pointer

You can create a pointer to another pointer, i.e., a **pointer to pointer**.

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10;
    int *p = &a;
    int **pp = &p;

    cout << "Value of a: " << **pp << endl;

    return 0;
}
```

**Output:**

```
Value of a: 10
```

### Dynamic Memory Allocation (Pointer)

C++ uses `new` and `delete` for dynamic memory, unlike `malloc`/`free` in C.

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int *p = new int[5];  // Allocate memory for 5 integers

    for (int i = 0; i < 5; i++) {
        p[i] = i * 10;
    }

    for (int i = 0; i < 5; i++) {
        cout << p[i] << " ";
    }
    cout << endl;

    delete[] p;  // Free memory
    return 0;
}
```

**Output:**

```
0 10 20 30 40
```

### Function Pointers

Function pointers allow calling functions dynamically or passing them as arguments.

**Example:**

```cpp
#include <iostream>
using namespace std;

void display(int n) {
    cout << "Number: " << n << endl;
}

int main() {
    void (*funcPtr)(int);  // Declare function pointer
    funcPtr = display;     // Assign function

    funcPtr(5);  // Call function via pointer
    return 0;
}
```

**Output:**

```
Number: 5
```

### Why Use Pointers in C++ ?

- Efficient memory access
- Enables dynamic memory
- Used for function callbacks
- Crucial in data structures (linked lists, trees, etc.)

> [!CAUTION]  
> Misuse can lead to bugs (e.g., memory leaks, dangling pointers), so use wisely.

<!-- START "Jump to Top"-->
<p align="right">
<a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Object-Oriented Programming (OOP)

C++ is a multi-paradigm programming language that supports Object-Oriented Programming (OOP). OOP is based on the concept of **objects**, which are instances of **classes**. OOP focuses on the following principles:

- **Encapsulation**: Grouping related data and functions into a single unit (class).
- **Abstraction**: Hiding complex details and showing only the necessary parts.
- **Inheritance**: Deriving new classes from existing ones.
- **Polymorphism**: The ability of an object to take many forms.

### Classes and Objects

#### **Class**

A **class** is a blueprint or template for creating objects. It defines properties (attributes) and behaviors (methods or functions) that the objects created from the class will have.

**Example:**

```cpp
#include <iostream>
using namespace std;

class Car {
public:
    // Attributes
    string brand;
    int year;

    // Method (Function)
    void startEngine() {
        cout << "The " << brand << " engine started.\n";
    }
};

int main() {
    // Create an object of type Car
    Car myCar;
    myCar.brand = "Toyota";
    myCar.year = 2020;

    // Call a method
    myCar.startEngine();

    return 0;
}
```

**Output:**

```
The Toyota engine started.
```

### Access Specifiers

Access specifiers define the visibility or accessibility of class members (attributes and methods).

1. **public**: Members are accessible from outside the class.
2. **private**: Members are accessible only within the class.
3. **protected**: Members are accessible within the class and derived classes.

**Example:**

```cpp
#include <iostream>
using namespace std;

class Employee {
private:
    int salary;  // private data member

public:
    void setSalary(int s) { // public method
        salary = s;
    }

    int getSalary() { // public method
        return salary;
    }
};

int main() {
    Employee emp;
    emp.setSalary(50000);  // Accessible because setSalary is public
    cout << "Employee salary: " << emp.getSalary() << endl;

    return 0;
}
```

**Output:**

```
Employee salary: 50000
```

### Constructors and Destructors

- **Constructor**: Special function that is called when an object is created. It initializes the object.
- **Destructor**: Special function that is called when an object is destroyed. It is used for cleanup.

**Example:**

```cpp
#include <iostream>
using namespace std;

class Student {
public:
    string name;
    int age;

    // Constructor
    Student(string n, int a) {
        name = n;
        age = a;
    }

    // Destructor
    ~Student() {
        cout << "Object " << name << " is being destroyed.\n";
    }
};

int main() {
    Student s1("Alice", 20);
    cout << s1.name << " is " << s1.age << " years old.\n";

    return 0;  // Destructor will be called automatically here
}
```

**Output:**

```
Alice is 20 years old.
Object Alice is being destroyed.
```

### `this` Pointer

The `this` pointer is an implicit pointer available to all non-static member functions. It points to the object for which the member function is called.

**Example:**

```cpp
#include <iostream>
using namespace std;

class Box {
public:
    int length;
    Box(int l) {
        this->length = l;  // Using 'this' pointer to differentiate member and parameter
    }

    void displayLength() {
        cout << "Length of box: " << this->length << endl;
    }
};

int main() {
    Box box1(10);
    box1.displayLength();

    return 0;
}
```

**Output:**

```
Length of box: 10
```

### Static Members

Static members belong to the class itself, rather than to individual objects. They are shared by all instances of the class.

**Example:**

```cpp
#include <iostream>
using namespace std;

class Counter {
public:
    static int count;  // Static member

    Counter() {
        count++;
    }

    static void displayCount() {  // Static method
        cout << "Count: " << count << endl;
    }
};

int Counter::count = 0;  // Initialize static member outside class

int main() {
    Counter c1, c2, c3;
    Counter::displayCount();  // Access static method using class name

    return 0;
}
```

**Output:**

```
Count: 3
```

### Friend Functions and Classes

A **friend function** or **friend class** can access the private and protected members of another class. Friend functions or classes are declared using the `friend` keyword.

**Example:**

```cpp
#include <iostream>
using namespace std;

class Box {
private:
    int width;

public:
    Box() : width(10) {}

    // Declaring a friend function
    friend void printWidth(Box b);
};

// Friend function definition
void printWidth(Box b) {
    cout << "Width of box: " << b.width << endl;
}

int main() {
    Box box;
    printWidth(box);  // Friend function can access private members

    return 0;
}
```

**Output:**

```
Width of box: 10
```

### **Object Arrays**

You can create arrays of objects just like any other type.

**Example:**

```cpp
#include <iostream>
using namespace std;

class Car {
public:
    string brand;

    Car(string b) : brand(b) {}

    void showBrand() {
        cout << "Brand: " << brand << endl;
    }
};

int main() {
    Car cars[2] = {Car("Toyota"), Car("Honda")};

    for (int i = 0; i < 2; i++) {
        cars[i].showBrand();
    }

    return 0;
}
```

**Output:**

```
Brand: Toyota
Brand: Honda
```

### **Pointers to Objects**

You can also create pointers to objects and use them to access object members.

**Example:**

```cpp
#include <iostream>
using namespace std;

class Book {
public:
    string title;

    Book(string t) : title(t) {}

    void showTitle() {
        cout << "Book Title: " << title << endl;
    }
};

int main() {
    Book* bookPtr = new Book("C++ Programming");
    bookPtr->showTitle();  // Using pointer to access member function

    delete bookPtr;  // Free memory
    return 0;
}
```

**Output:**

```
Book Title: C++ Programming
```

<!-- START "Jump to Top"-->
<p align="right">
<a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Inheritance

Inheritance is one of the core concepts of Object-Oriented Programming (OOP). It allows a class (called the **derived class**) to inherit properties and methods from another class (called the **base class**). This helps in code reuse, extension of functionality, and maintaining a hierarchical relationship between classes.

In C++, inheritance is achieved by using the `:` symbol. A derived class can inherit members (attributes and methods) from a base class.

**Types of Inheritance in C++**

1. **Single Inheritance**: A derived class inherits from only one base class.
2. **Multiple Inheritance**: A derived class inherits from more than one base class.
3. **Multilevel Inheritance**: A class inherits from a derived class which, in turn, is derived from another base class.
4. **Hierarchical Inheritance**: Multiple classes inherit from a single base class.
5. **Hybrid Inheritance**: A combination of two or more types of inheritance.

**Syntax:**

```cpp
class DerivedClass : accessSpecifier BaseClass {
    // Derived class members
};
```

- **`accessSpecifier`** can be `public`, `protected`, or `private` (more on this below).
- The **base class** is specified after the colon `:`.

### Access Specifiers in Inheritance

1. **Public Inheritance**: Public members of the base class become public members of the derived class.
2. **Protected Inheritance**: Public and protected members of the base class become protected members in the derived class.
3. **Private Inheritance**: Public and protected members of the base class become private members of the derived class.

**Example: Single Inheritance**

```cpp
#include <iostream>
using namespace std;

// Base class
class Animal {
public:
    void eat() {
        cout << "This animal eats food." << endl;
    }
};

// Derived class
class Dog : public Animal {
public:
    void bark() {
        cout << "The dog barks." << endl;
    }
};

int main() {
    Dog dog;
    dog.eat();  // Inherited function from Animal class
    dog.bark(); // Function from Dog class

    return 0;
}
```

**Output:**

```
This animal eats food.
The dog barks.
```

**Example: Multiple Inheritance**

```cpp
#include <iostream>
using namespace std;

// Base class 1
class Animal {
public:
    void eat() {
        cout << "This animal eats food." << endl;
    }
};

// Base class 2
class Machine {
public:
    void start() {
        cout << "The machine starts." << endl;
    }
};

// Derived class
class Robot : public Animal, public Machine {
public:
    void talk() {
        cout << "The robot talks." << endl;
    }
};

int main() {
    Robot robot;
    robot.eat();   // Inherited from Animal class
    robot.start(); // Inherited from Machine class
    robot.talk();  // Defined in Robot class

    return 0;
}
```

**Output:**

```
This animal eats food.
The machine starts.
The robot talks.
```

**Example: Multilevel Inheritance**

```cpp
#include <iostream>
using namespace std;

// Base class
class Animal {
public:
    void eat() {
        cout << "This animal eats food." << endl;
    }
};

// Derived class 1
class Mammal : public Animal {
public:
    void walk() {
        cout << "The mammal walks." << endl;
    }
};

// Derived class 2 (from Mammal)
class Dog : public Mammal {
public:
    void bark() {
        cout << "The dog barks." << endl;
    }
};

int main() {
    Dog dog;
    dog.eat();  // Inherited from Animal
    dog.walk(); // Inherited from Mammal
    dog.bark(); // Defined in Dog

    return 0;
}
```

**Output:**

```
This animal eats food.
The mammal walks.
The dog barks.
```

**Example: Hierarchical Inheritance**

```cpp
#include <iostream>
using namespace std;

// Base class
class Animal {
public:
    void eat() {
        cout << "This animal eats food." << endl;
    }
};

// Derived class 1
class Dog : public Animal {
public:
    void bark() {
        cout << "The dog barks." << endl;
    }
};

// Derived class 2
class Cat : public Animal {
public:
    void meow() {
        cout << "The cat meows." << endl;
    }
};

int main() {
    Dog dog;
    dog.eat();  // Inherited from Animal
    dog.bark(); // Defined in Dog

    Cat cat;
    cat.eat();  // Inherited from Animal
    cat.meow(); // Defined in Cat

    return 0;
}
```

**Output:**

```
This animal eats food.
The dog barks.
This animal eats food.
The cat meows.
```

### Constructor in Inheritance

In C++, constructors are not inherited. However, the constructor of the base class is called before the constructor of the derived class.

**Example:**

```cpp
#include <iostream>
using namespace std;

// Base class
class Animal {
public:
    Animal() {
        cout << "Animal constructor called!" << endl;
    }
};

// Derived class
class Dog : public Animal {
public:
    Dog() {
        cout << "Dog constructor called!" << endl;
    }
};

int main() {
    Dog dog; // Calls both Animal and Dog constructors
    return 0;
}
```

**Output:**

```
Animal constructor called!
Dog constructor called!
```

### Destructor in Inheritance

In inheritance, the derived class’s destructor is called first, followed by the base class’s destructor. If no destructor is explicitly defined, C++ will automatically call the base class destructor after the derived class destructor.

**Example:**

```cpp
#include <iostream>
using namespace std;

// Base class
class Animal {
public:
    Animal() {
        cout << "Animal constructor called!" << endl;
    }

    ~Animal() {
        cout << "Animal destructor called!" << endl;
    }
};

// Derived class
class Dog : public Animal {
public:
    Dog() {
        cout << "Dog constructor called!" << endl;
    }

    ~Dog() {
        cout << "Dog destructor called!" << endl;
    }
};

int main() {
    Dog dog;  // Calls constructors and destructors
    return 0;
}
```

**Output:**

```
Animal constructor called!
Dog constructor called!
Dog destructor called!
Animal destructor called!
```

<!-- START "Jump to Top"-->
<p align="right">
<a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Polymorphism

Polymorphism is a key concept in Object-Oriented Programming (OOP) that allows objects of different types to be treated as objects of a common base type. The term **polymorphism** means "many shapes," and it allows for flexibility in how objects behave based on their specific types.

In C++, polymorphism is achieved through:

1. **Compile-time Polymorphism (Static Polymorphism)**
2. **Run-time Polymorphism (Dynamic Polymorphism)**

### Compile-time Polymorphism (Static Polymorphism)

Compile-time polymorphism is achieved through **function overloading** and **operator overloading**. The decision of which function to call is made at compile time.

#### **Function Overloading**

Function overloading allows multiple functions with the same name but different parameters (different number or types of parameters).

**Example:**

```cpp
#include <iostream>
using namespace std;

class Print {
public:
    // Overloaded function for integer type
    void display(int i) {
        cout << "Integer: " << i << endl;
    }

    // Overloaded function for float type
    void display(float f) {
        cout << "Float: " << f << endl;
    }

    // Overloaded function for string type
    void display(string s) {
        cout << "String: " << s << endl;
    }
};

int main() {
    Print obj;

    obj.display(5);        // Calls the function with int argument
    obj.display(3.14f);    // Calls the function with float argument
    obj.display("Hello");  // Calls the function with string argument

    return 0;
}
```

**Output:**

```
Integer: 5
Float: 3.14
String: Hello
```

#### **Operator Overloading in C++**

Operator overloading allows defining custom behavior for operators when applied to user-defined data types.

**Example:**

```cpp
#include <iostream>
using namespace std;

class Complex {
public:
    int real, imag;

    Complex() : real(0), imag(0) {}

    // Operator overloading for adding two complex numbers
    Complex operator + (const Complex &c) {
        Complex temp;
        temp.real = real + c.real;
        temp.imag = imag + c.imag;
        return temp;
    }

    void display() {
        cout << real << " + " << imag << "i" << endl;
    }
};

int main() {
    Complex c1, c2, c3;

    c1.real = 5; c1.imag = 3;
    c2.real = 2; c2.imag = 7;

    c3 = c1 + c2; // Using overloaded operator +
    c3.display();  // Output: 7 + 10i

    return 0;
}
```

**Output:**

```
7 + 10i
```

### Run-time Polymorphism (Dynamic Polymorphism)

Run-time polymorphism is achieved using **function overriding** in the context of inheritance. The decision of which function to call is made at runtime based on the type of object pointed to by the base class pointer.

#### **Virtual Functions**

A **virtual function** is a function defined in the base class that can be overridden in the derived class. The function call is resolved at runtime based on the object type that the base class pointer is pointing to.

To enable run-time polymorphism, you need to declare a function in the base class as `virtual`.

**Example:**

```cpp
#include <iostream>
using namespace std;

// Base class
class Animal {
public:
    virtual void sound() { // Virtual function
        cout << "Animal makes a sound" << endl;
    }
};

// Derived class
class Dog : public Animal {
public:
    void sound() override { // Overridden function
        cout << "Dog barks" << endl;
    }
};

// Derived class
class Cat : public Animal {
public:
    void sound() override { // Overridden function
        cout << "Cat meows" << endl;
    }
};

int main() {
    Animal *animal;

    Dog dog;
    Cat cat;

    // Using base class pointer to call derived class functions
    animal = &dog;
    animal->sound();  // Calls Dog's sound() method

    animal = &cat;
    animal->sound();  // Calls Cat's sound() method

    return 0;
}
```

**Output:**

```
Dog barks
Cat meows
```

- The `sound()` function in the `Animal` class is a **virtual function**, which allows the derived classes (`Dog`, `Cat`) to override it.
- When the base class pointer (`animal`) points to a `Dog` object, it calls the `Dog`'s `sound()` method.
- Similarly, when the base class pointer points to a `Cat` object, it calls the `Cat`'s `sound()` method.

#### **Pure Virtual Functions and Abstract Classes**

A **pure virtual function** is a virtual function that has no implementation in the base class, making the class abstract. It is declared using `= 0` in the declaration.

```cpp
#include <iostream>
using namespace std;

class Shape {
public:
    virtual void draw() = 0; // Pure virtual function, making Shape an abstract class
};

class Circle : public Shape {
public:
    void draw() override {
        cout << "Drawing Circle" << endl;
    }
};

class Rectangle : public Shape {
public:
    void draw() override {
        cout << "Drawing Rectangle" << endl;
    }
};

int main() {
    Shape* shape;
    Circle circle;
    Rectangle rectangle;

    shape = &circle;
    shape->draw();  // Output: Drawing Circle

    shape = &rectangle;
    shape->draw();  // Output: Drawing Rectangle

    return 0;
}
```

**Output:**

```
Drawing Circle
Drawing Rectangle
```

In this example:

- `Shape` is an **abstract class** because it has a pure virtual function (`draw`).
- The `Circle` and `Rectangle` classes provide implementations for the pure virtual function.
- You cannot create an object of the `Shape` class directly.

### Advantages of Polymorphism

- **Code Reusability**: With polymorphism, one function can work with objects of different types, leading to less code duplication.
- **Maintainability**: Polymorphism makes the system easier to extend and maintain, as you can add new derived classes without modifying existing code.
- **Flexibility**: Polymorphism allows you to write more general code that can handle new types of objects, making the program flexible.

<!-- START "Jump to Top"-->
<p align="right">
<a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Encapsulation

**Encapsulation** is one of the fundamental concepts of Object-Oriented Programming (OOP) in C++. It refers to the **bundling of data and the functions** that operate on that data into a **single unit** (class), while also **restricting direct access** to some of the object's components. This is achieved using **access specifiers** (`private`, `protected`, `public`).

Encapsulation promotes **data hiding**, security, and modular code structure.

**Key Concepts of Encapsulation:**

| Feature               | Description                                                        |
| --------------------- | ------------------------------------------------------------------ |
| **Class**             | Combines data (variables) and methods (functions) in one unit      |
| **Access Specifiers** | Control access to class members (`private`, `protected`, `public`) |
| **Private Members**   | Cannot be accessed directly from outside the class                 |
| **Public Methods**    | Used to access and modify private data safely (getters/setters)    |

**Example: Simple Encapsulation**

```cpp
#include <iostream>
using namespace std;

class Account {
private:
    // Private data member
    double balance;

public:
    // Constructor to initialize balance
    Account(double b) {
        if (b >= 0)
            balance = b;
        else
            balance = 0;
    }

    // Getter function to access balance
    double getBalance() {
        return balance;
    }

    // Setter function to update balance
    void deposit(double amount) {
        if (amount > 0)
            balance += amount;
    }

    void withdraw(double amount) {
        if (amount > 0 && amount <= balance)
            balance -= amount;
        else
            cout << "Invalid withdrawal amount." << endl;
    }
};

int main() {
    Account myAccount(1000);  // Create object with initial balance

    cout << "Initial Balance: $" << myAccount.getBalance() << endl;

    myAccount.deposit(500);
    cout << "After Deposit: $" << myAccount.getBalance() << endl;

    myAccount.withdraw(300);
    cout << "After Withdrawal: $" << myAccount.getBalance() << endl;

    // myAccount.balance = 10000; // ❌ Not allowed (private access)

    return 0;
}
```

**Output:**

```
Initial Balance: $1000
After Deposit: $1500
After Withdrawal: $1200
```

### Advantages of Encapsulation

- **Data Hiding**: Internal state is hidden from outside access.
- **Improved Security**: Only validated changes are allowed through public methods.
- **Modularity**: Each object manages its own state and behavior.
- **Easy Maintenance**: Implementation changes inside the class don’t affect external code.
- **Better Control**: You can control how data is accessed or modified via setters/getters.

<!-- START "Jump to Top"-->
<p align="right">
<a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->
  
## Abstraction

**Abstraction** in C++ is an **OOP principle** that allows you to hide complex implementation details and show **only the essential features** of an object. It simplifies programming by separating **what an object does** from **how it does it**.

In C++, abstraction is mainly achieved through:

- **Abstract Classes** (with at least one pure virtual function)
- **Interfaces** (fully abstract classes)
- **Access Specifiers** (`private`, `protected`, `public`) to hide implementation details

**Key Concepts:**

| Concept                   | Description                                                           |
| ------------------------- | --------------------------------------------------------------------- |
| **Abstraction**           | Hides internal implementation, shows only necessary features          |
| **Abstract Class**        | A class with at least one **pure virtual function** (`= 0`)           |
| **Pure Virtual Function** | A function declared in a base class to be overridden in derived class |
| **Interface**             | A class with only pure virtual functions, used as a contract          |

**Example: Using Abstract Class**

```cpp
#include <iostream>
using namespace std;

// Abstract class
class Shape {
public:
    // Pure virtual function
    virtual void draw() = 0;

    void commonMethod() {
        cout << "This is a shared method in abstract class.\n";
    }
};

// Derived class: Circle
class Circle : public Shape {
public:
    void draw() override {
        cout << "Drawing a Circle.\n";
    }
};

// Derived class: Rectangle
class Rectangle : public Shape {
public:
    void draw() override {
        cout << "Drawing a Rectangle.\n";
    }
};

int main() {
    Shape* s1 = new Circle();
    Shape* s2 = new Rectangle();

    s1->draw();           // Output: Drawing a Circle.
    s2->draw();           // Output: Drawing a Rectangle.
    s1->commonMethod();   // Output: This is a shared method in abstract class.

    delete s1;
    delete s2;

    return 0;
}
```

**Output:**

```
Drawing a Circle.
Drawing a Rectangle.
This is a shared method in abstract class.
```

### Why Use Abstraction?

- **Hide Complexity**: Keep implementation details hidden from the user.
- **Improve Maintainability**: Changing internal logic doesn’t affect users.
- **Enhance Modularity**: Work with interfaces and abstract classes.
- **Encourage Polymorphism**: Let derived classes provide specific behaviors.
- **Code Reusability**: Share base behaviors and override specifics.

<!-- START "Jump to Top"-->
<p align="right">
<a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Operator Overloading

**Operator Overloading** in C++ allows you to redefine the meaning of operators (`+`, `-`, `==`, `<<`, etc.) for **user-defined types** (like classes and structs). This improves code **readability**, **flexibility**, and enables **intuitive syntax** when working with objects.

### Why Use Operator Overloading?

- Makes custom objects behave like built-in types.
- Enhances code clarity and usability.
- Enables operations like addition, comparison, assignment, etc., on class objects.

**Syntax:**

```cpp
return_type operator symbol (parameters) {
    // implementation
}
```

**Example: Overload `+` for a `Point` Class**

```cpp
#include <iostream>
using namespace std;

class Point {
    int x, y;

public:
    Point(int x = 0, int y = 0) : x(x), y(y) {}

    // Overload + operator
    Point operator+(const Point& p) {
        return Point(x + p.x, y + p.y);
    }

    void display() {
        cout << "(" << x << ", " << y << ")" << endl;
    }
};

int main() {
    Point p1(2, 3), p2(4, 5), result;

    result = p1 + p2;  // using overloaded + operator

    result.display();  // Output: (6, 8)

    return 0;
}
```

**Output:**

```
(6, 8)
```

### Common Operators You Can Overload

| Operator   | Meaning                     |
| ---------- | --------------------------- |
| `+`        | Addition                    |
| `-`        | Subtraction                 |
| `*`        | Multiplication              |
| `/`        | Division                    |
| `==`, `!=` | Comparison                  |
| `<<`, `>>` | Stream insertion/extraction |
| `=`        | Assignment                  |
| `[]`       | Subscript (array indexing)  |
| `()`       | Function call               |
| `->`       | Member access via pointer   |

### Rules & Restrictions

- At least **one operand** must be a **user-defined type**.
- You **cannot overload**:

  - `::` (scope resolution)
  - `.` (member access)
  - `.*` (member pointer access)
  - `sizeof`, `typeid`, `alignof`, etc.

- Overloaded operators **don’t change precedence** or **associativity**.

**Example: Overload `==` and `<<`**

```cpp
#include <iostream>
using namespace std;

class Book {
    string title;
    int pages;

public:
    Book(string t, int p) : title(t), pages(p) {}

    // Overload ==
    bool operator==(const Book& b) {
        return (title == b.title && pages == b.pages);
    }

    // Overload <<
    friend ostream& operator<<(ostream& out, const Book& b) {
        out << "Book: " << b.title << ", Pages: " << b.pages;
        return out;
    }
};

int main() {
    Book b1("C++ Basics", 300), b2("C++ Basics", 300);

    if (b1 == b2)
        cout << "Books are equal" << endl;

    cout << b1 << endl;

    return 0;
}
```

**Output:**

```
Books are equal
Book: C++ Basics, Pages: 300
```

<!-- START "Jump to Top"-->
<p align="right">
<a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Templates and Generics

**Templates** in C++ allow you to write **generic and reusable code**. They enable functions and classes to operate with **generic types**, so you can write a single codebase to work with different data types.

**Types of Templates in C++**

1. **Function Templates**
2. **Class Templates**

### **Function Templates**

These allow the creation of a single function that can work with **any data type**.

**Syntax:**

```cpp
template <typename T>
T functionName(T arg) {
    // function body
}
```

You can also use `class` instead of `typename` — both work the same.

**Example:**

```cpp
#include <iostream>
using namespace std;

template <typename T>
T add(T a, T b) {
    return a + b;
}

int main() {
    cout << add<int>(3, 4) << endl;      // 7
    cout << add<double>(2.5, 4.3) << endl; // 6.8
    cout << add<string>("Hi ", "there!") << endl; // Hi there!
    return 0;
}
```

**Output:**

```
7
6.8
Hi there!
```

### **Class Templates**

Class templates allow the definition of **generic classes** to handle data of any type.

**Syntax:**

```cpp
template <class T>
class ClassName {
   T data;
public:
   ClassName(T val) : data(val) {}
   void show() { cout << data << endl; }
};
```

**Example:**

```cpp
#include <iostream>
using namespace std;

template <class T>
class Box {
    T value;

public:
    Box(T val) : value(val) {}
    void display() { cout << "Value: " << value << endl; }
};

int main() {
    Box<int> intBox(10);
    Box<string> strBox("Hello");

    intBox.display();     // Value: 10
    strBox.display();     // Value: Hello

    return 0;
}
```

**Output:**

```
Value: 10
Value: Hello
```

### Template with Multiple Parameters

**Example:**

```cpp
#include <iostream>
#include <string>
using namespace std;

template <class T1, class T2>
class Pair {
    T1 first;
    T2 second;

public:
    Pair(T1 a, T2 b) : first(a), second(b) {}
    void show() {
        cout << "First: " << first << ", Second: " << second << endl;
    }
};

int main() {
    Pair<int, string> p(101, "Alice");
    p.show();  // First: 101, Second: Alice
    return 0;
}
```

**Output:**

```
First: 101, Second: Alice
```

> [!IMPORTANT]
>
> - Templates are **compiled when used**, not when defined.
> - You can provide **default types** to templates.
> - Templates support **specialization** (custom behavior for specific types).

### Function Template Overloading

Templates can coexist with regular functions. The compiler chooses the best match.

**Example:**

```cpp
#include <iostream>
using namespace std;

void show(int x) {
    cout << "Regular function: " << x << endl;
}

template <typename T>
void show(T x) {
    cout << "Template function: " << x << endl;
}

int main() {
    show(100);    // Calls regular function
    show(3.14);   // Calls template function
    return 0;
}
```

**Output:**

```
Regular function: 100
Template function: 3.14
```

<!-- START "Jump to Top"-->
<p align="right">
<a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Structure, Union and Enum

C++ supports powerful user-defined data types that help group different kinds of data under a single name:

- `struct` → Structure
- `union` → Union
- `enum` → Enumeration

### Structure (`struct`)

A **structure** in C++ allows grouping variables of **different types** under one user-defined name.

**Syntax:**

```cpp
struct StructName {
    datatype member1;
    datatype member2;
    ...
};
```

**Example:**

```cpp
#include <iostream>
#include <string>
using namespace std;

struct Person {
    string name;
    int age;
};

int main() {
    Person p1 = {"Alice", 25};

    cout << "Name: " << p1.name << endl;
    cout << "Age: " << p1.age << endl;

    return 0;
}
```

**Output:**

```
Name: Alice
Age: 25
```

### Union (`union`)

A **union** is like a structure but all members **share the same memory location**. Only one member can hold a value at any one time.

**Syntax:**

```cpp
union UnionName {
    datatype member1;
    datatype member2;
    ...
};
```

**Example:**

```cpp
#include <iostream>
using namespace std;

union Data {
    int i;
    float f;
};

int main() {
    Data d;
    d.i = 10;
    cout << "d.i = " << d.i << endl;

    d.f = 3.14f;
    cout << "d.f = " << d.f << endl;

    // d.i is now overwritten
    cout << "d.i after setting d.f = " << d.i << endl;

    return 0;
}
```

**Output: (Memory Overlap)**

```
d.i = 10
d.f = 3.14
d.i after setting d.f = 1078523331
```

> [!CAUTION] Memory sharing causes unexpected value in `d.i` after assigning to `d.f`.

### Enumeration (`enum`)

An **enum** assigns **names to a set of integer constants** to improve code readability.

**Syntax:**

```cpp
enum EnumName { CONST1, CONST2, CONST3, ... };
```

- Default: `CONST1 = 0`, `CONST2 = 1`, and so on.

**Example:**

```cpp
#include <iostream>
using namespace std;

enum Weekday { Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday };

int main() {
    Weekday today = Friday;
    cout << "Numeric value of Friday: " << today << endl;

    return 0;
}
```

**Output:**

```
Numeric value of Friday: 5
```

**Custom Enum Values**

You can assign custom values to enum constants:

```cpp
enum Color { Red = 1, Green = 3, Blue = 5 };
```

This lets you represent specific values explicitly.

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Dynamic Memory Allocation

Dynamic memory allocation in C++ lets you **allocate memory at runtime** using pointers and the `new` and `delete` operators (instead of `malloc`, `calloc`, `realloc`, and `free` in C).

It provides flexibility to create memory that can **grow or shrink** during execution.

**Memory Functions in C++**

| C Function  | C++ Equivalent               | Description                    |
| ----------- | ---------------------------- | ------------------------------ |
| `malloc()`  | `new`                        | Allocates memory               |
| `calloc()`  | `new` (initialized manually) | Allocates & initializes memory |
| `realloc()` | Manually recreate + copy     | Resize allocated memory block  |
| `free()`    | `delete` / `delete[]`        | Frees allocated memory         |

### `new` – Dynamic Allocation

The `new` operator dynamically allocates memory and returns a pointer to it. Unlike `malloc()`, it does **not require casting** and **constructs objects** if needed.

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int* arr = new int[3];  // allocate memory for 3 integers

    arr[0] = 10;
    arr[1] = 20;
    arr[2] = 30;

    for (int i = 0; i < 3; i++) {
        cout << arr[i] << " ";
    }

    delete[] arr;  // free memory
    return 0;
}
```

**Output:**

```
10 20 30
```

### Zero-Initialized Allocation (like `calloc()`)

C++ doesn't have a `calloc` equivalent, but you can manually initialize after allocation or use modern containers (e.g. `vector`). Here's how to emulate `calloc`:

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int* arr = new int[3]();  // () initializes all to zero

    for (int i = 0; i < 3; i++) {
        cout << arr[i] << " ";
    }

    delete[] arr;
    return 0;
}
```

**Output:**

```
0 0 0
```

### Resizing Memory (like `realloc()`)

C++ has no direct `realloc()` equivalent. To resize:

- Allocate new memory
- Copy old values
- Delete old memory

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int* arr = new int[2];
    arr[0] = 5;
    arr[1] = 10;

    // Create a new array with larger size
    int* newArr = new int[4];

    // Copy existing data
    for (int i = 0; i < 2; i++) {
        newArr[i] = arr[i];
    }

    // Add new data
    newArr[2] = 15;
    newArr[3] = 20;

    // Delete old array
    delete[] arr;

    // Print new array
    for (int i = 0; i < 4; i++) {
        cout << newArr[i] << " ";
    }

    delete[] newArr;
    return 0;
}
```

**Output:**

```
5 10 15 20
```

### `delete` – Freeing Memory (like `free()`)

`delete` and `delete[]` are used to free dynamically allocated memory in C++.

**Example:**

```cpp
#include <iostream>
using namespace std;

int main() {
    int n = 5;
    int* arr = new int[n];

    for (int i = 0; i < n; i++) {
        arr[i] = (i + 1) * 10;
    }

    cout << "Values in the array: ";
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;

    delete[] arr;
    cout << "Memory successfully freed." << endl;

    return 0;
}
```

**Output:**

```
Values in the array: 10 20 30 40 50
Memory successfully freed.
```

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Type Conversion and Typecasting

In C++, **Type Conversion** and **Typecasting** refer to changing a variable from one data type to another. This is essential in many operations, especially when dealing with arithmetic between different types or converting user input/output types.

### Type Conversion in C++

There are **two main types** of conversions:

1. **Implicit Conversion:** Done **automatically** by the compiler
2. **Explicit Conversion:** Done **manually** by the programmer (called typecasting)

#### **Implicit Type Conversion (Automatic)**

The compiler **automatically** converts one data type to another (usually a **higher** type to avoid data loss).

Rule:

Lower → Higher rank:
`bool → char → int → float → double`

Example:

```cpp
#include <iostream>
using namespace std;

int main() {
    int i = 42;
    double d = i;  // int implicitly converted to double

    cout << "i = " << i << endl;
    cout << "d = " << d << endl;

    return 0;
}
```

Output:

```
i = 42
d = 42
```

#### **Explicit Type Conversion (Typecasting)**

You manually **cast** a value from one type to another.

**Syntax: (3 ways)**

1. **C-style cast:**

   ```cpp
   (type)expression
   ```

2. **Function-style cast:**

   ```cpp
   type(expression)
   ```

3. **C++ cast operators:**

   - `static_cast<type>(expression)`
   - `dynamic_cast<type>(expression)` (for polymorphic classes)
   - `const_cast<type>(expression)` (remove `const`)
   - `reinterpret_cast<type>(expression)` (bitwise conversion)

**Example: C-style & Function-style Cast**

```cpp
#include <iostream>
using namespace std;

int main() {
    double pi = 3.14159;

    int intPi1 = (int)pi;       // C-style
    int intPi2 = int(pi);       // Function-style

    cout << "Original: " << pi << endl;
    cout << "C-style cast: " << intPi1 << endl;
    cout << "Function-style cast: " << intPi2 << endl;

    return 0;
}
```

**Output:**

```
Original: 3.14159
C-style cast: 3
Function-style cast: 3
```

**Example: `static_cast`**

```cpp
#include <iostream>
using namespace std;

int main() {
    float f = 9.81;
    int i = static_cast<int>(f);  // Converts float to int

    cout << "Original float: " << f << endl;
    cout << "After static_cast: " << i << endl;

    return 0;
}
```

**Output:**

```
Original float: 9.81
After static_cast: 9
```

**Example: `reinterpret_cast`**

```cpp
#include <iostream>
using namespace std;

int main() {
    int x = 65;
    char* ch = reinterpret_cast<char*>(&x);

    cout << "First byte of x as char: " << *ch << endl;
    return 0;
}
```

**Output: (on little-endian systems)**

```
First byte of x as char: A
```

### Use Case

- **`static_cast`** - Safe, standard conversion between types (int ↔ float, base ↔ derived)
- **`dynamic_cast`** - Used for safe downcasting in polymorphic class hierarchies.
- **`const_cast`** - Add/remove `const` or `volatile` qualifier
- **`reinterpret_cast`** - Low-level reinterpretation (dangerous, for bit-level tricks)

> [!TIP]
>
> - Use `static_cast` over C-style for **clarity and type safety**.
> - Avoid `reinterpret_cast` unless **absolutely necessary**.
> - Avoid implicit conversions when there's **risk of precision loss or truncation**.

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## File Handling

File handling in C++ allows you to **create, write, read, and manipulate files** (text or binary) using **file streams** provided by the `<fstream>` library.

C++ provides three main file stream classes in the `<fstream>` header:

| Class      | Description                                                   |
| ---------- | ------------------------------------------------------------- |
| `ifstream` | Input stream – for reading files (`in`)                       |
| `ofstream` | Output: stream – for writing files (`out`)                    |
| `fstream`  | Input/output stream – for both reading and writing (`in/out`) |

Include the necessary header:

```cpp
#include <fstream>
```

### Opening and Closing Files

**Syntax to open a file:**

```cpp
ifstream fin("file.txt");       // for reading
ofstream fout("file.txt");      // for writing
fstream fio("file.txt");        // for both
```

**Alternative using `.open()` method:**

```cpp
fin.open("file.txt");
```

**Closing the file:**

```cpp
fin.close();
```

**Example: Writing to a File**

```cpp
#include <iostream>
#include <fstream>
using namespace std;

int main() {
    ofstream fout("example.txt");  // creates and opens the file

    if (!fout) {
        cout << "File couldn't be opened!" << endl;
        return 1;
    }

    fout << "Hello, C++ File Handling!" << endl;
    fout << "This is a sample file." << endl;

    fout.close();  // don't forget to close the file
    return 0;
}
```

**Output: (in `example.txt`)**

```
Hello, C++ File Handling!
This is a sample file.
```

**Example: Reading from a File**

```cpp
#include <iostream>
#include <fstream>
#include <string>
using namespace std;

int main() {
    ifstream fin("example.txt");  // open file for reading
    string line;

    if (!fin) {
        cout << "File couldn't be opened!" << endl;
        return 1;
    }

    while (getline(fin, line)) {
        cout << line << endl;
    }

    fin.close();
    return 0;
}
```

**Output:**

```
Hello, C++ File Handling!
This is a sample file.
```

**Example: Reading and Writing (Using `fstream`)**

```cpp
#include <iostream>
#include <fstream>
using namespace std;

int main() {
    fstream file;

    // open file for both reading and writing
    file.open("data.txt", ios::out | ios::in | ios::trunc);

    if (!file) {
        cout << "File couldn't be opened!" << endl;
        return 1;
    }

    file << "Welcome to C++ fstream!" << endl;

    // Go back to the beginning of file to read
    file.seekg(0);

    string line;
    while (getline(file, line)) {
        cout << line << endl;
    }

    file.close();
    return 0;
}
```

### File Open Modes (`ios::` flags)

| Mode          | Description                   |
| ------------- | ----------------------------- |
| `ios::in`     | Open for reading              |
| `ios::out`    | Open for writing              |
| `ios::app`    | Append to end of file         |
| `ios::trunc`  | Delete content if file exists |
| `ios::binary` | Open in binary mode           |

You can combine them using `|` (bitwise OR):

```cpp
fstream file("data.txt", ios::in | ios::out);
```

**Example: Appending to a File**

```cpp
#include <iostream>
#include <fstream>
using namespace std;

int main() {
    ofstream fout("example.txt", ios::app);  // append mode

    fout << "New line added using append mode.\n";

    fout.close();
    return 0;
}
```

### Check File State

| Function         | Description                              |
| ---------------- | ---------------------------------------- |
| `file.is_open()` | Returns true if file opened successfully |
| `file.eof()`     | Returns true if end-of-file reached      |
| `file.fail()`    | Returns true if operation failed         |
| `file.good()`    | Returns true if no error                 |

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Preprocessor Directives

Preprocessor directives in C++ are **commands for the preprocessor** that execute before the compilation phase. They are used to:

- Include files
- Define constants/macros
- Enable conditional compilation
- Give special instructions to the compiler

All preprocessor directives begin with `#` and **do not end with a semicolon**.

**Common Preprocessor Directives in C++**

| Directive           | Description                                                 |
| ------------------- | ----------------------------------------------------------- |
| `#include`          | Includes standard or user-defined header files              |
| `#define`           | Defines macros/constants                                    |
| `#undef`            | Undefines (removes) a previously defined macro              |
| `#ifdef`, `#ifndef` | Conditional compilation based on whether macros are defined |
| `#else`, `#elif`    | Alternative blocks for conditional compilation              |
| `#endif`            | Ends a conditional block                                    |
| `#if`               | Compiles code if a condition is true                        |
| `#pragma`           | Provides compiler-specific instructions                     |

### `#include` – Include Files

Used to include header files (standard or user-defined).

**Example:**

```cpp
#include <iostream>  // Standard header

int main() {
    std::cout << "Hello, World!" << std::endl;
    return 0;
}
```

**Output:**

```
Hello, World!
```

### `#define` – Define Constants or Macros

Defines a symbolic constant or macro to be replaced before compilation.

**Example:**

```cpp
#include <iostream>
#define PI 3.14

int main() {
    float area = PI * 5 * 5;
    std::cout << "Area of circle: " << area << std::endl;
    return 0;
}
```

**Output:**

```
Area of circle: 78.5
```

### `#undef` – Undefine a Macro

Removes a previously defined macro.

**Example:**

```cpp
#include <iostream>

#define MAX 100

int main() {
    std::cout << "Max value: " << MAX << std::endl;

    #undef MAX
    // std::cout << MAX << std::endl; // Error: MAX is undefined

    return 0;
}
```

**Output:**

```
Max value: 100
```

### `#ifdef` / `#ifndef` – Conditional Compilation

Includes code if a macro is defined or not defined.

**Example:**

```cpp
#include <iostream>

#define DEBUG

int main() {
    #ifdef DEBUG
        std::cout << "Debugging is enabled." << std::endl;
    #else
        std::cout << "Debugging is not enabled." << std::endl;
    #endif

    return 0;
}
```

**Output:**

```
Debugging is enabled.
```

### `#else` / `#elif` – Alternate Compilation Paths

Selects among different blocks during compilation.

**Example:**

```cpp
#include <iostream>
#define VERBOSE 0

int main() {
    #if VERBOSE
        std::cout << "Verbose mode is enabled." << std::endl;
    #else
        std::cout << "Verbose mode is disabled." << std::endl;
    #endif

    return 0;
}
```

**Output:**

```
Verbose mode is disabled.
```

### `#pragma` – Compiler-Specific Directives

Provides additional information to the compiler, such as optimizations or warnings.

**Example (GCC specific):**

```cpp
#include <iostream>

#pragma GCC optimize("O3")  // Compiler optimization

int main() {
    for (int i = 0; i < 1000000; ++i);  // Dummy loop
    std::cout << "Loop completed with optimization." << std::endl;
    return 0;
}
```

**Output:**

```
Loop completed with optimization.
```

> [!WARNING] The actual performance gain won't be visible for such a small loop.

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Error Handling

In C++, **error handling** is done using **exceptions**, which provide a way to detect and manage runtime errors **without crashing** the program.

**Key Concepts:**

| Term             | Description                                                |
| ---------------- | ---------------------------------------------------------- |
| `try`            | Block of code that might throw an exception                |
| `throw`          | Used to **raise** an exception                             |
| `catch`          | Block of code that **handles** the exception               |
| `exception`      | An object or value representing the error                  |
| `std::exception` | Base class for standard exceptions in `<exception>` header |

**Syntax:**

```cpp
try {
    // Code that may throw an exception
    throw exception_value;
}
catch (exception_type variable) {
    // Handle the exception
}
```

**Example: Division by Zero**

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10, b = 0;

    try {
        if (b == 0)
            throw "Division by zero not allowed!";
        cout << "Result: " << a / b << endl;
    }
    catch (const char* msg) {
        cout << "Error: " << msg << endl;
    }

    return 0;
}
```

**Output:**

```
Error: Division by zero not allowed!
```

**Example: Using Standard Exception**

```cpp
#include <iostream>
#include <stdexcept>
using namespace std;

int main() {
    try {
        throw runtime_error("Something went wrong!");
    }
    catch (const runtime_error& e) {
        cout << "Caught runtime_error: " << e.what() << endl;
    }

    return 0;
}
```

**Output:**

```
Caught runtime_error: Something went wrong!
```

**Example: Multiple Catch Blocks**

```cpp
#include <iostream>
using namespace std;

int main() {
    try {
        int choice = 2;

        if (choice == 1)
            throw 100;
        else if (choice == 2)
            throw 3.14;
        else
            throw "Unknown error!";
    }
    catch (int x) {
        cout << "Caught integer exception: " << x << endl;
    }
    catch (double d) {
        cout << "Caught double exception: " << d << endl;
    }
    catch (const char* msg) {
        cout << "Caught string exception: " << msg << endl;
    }

    return 0;
}
```

**Output:**

```
Caught double exception: 3.14
```

**Example: Catch-All Handler**

```cpp
#include <iostream>
using namespace std;

int main() {
    try {
        throw 'X';
    }
    catch (...) {
        cout << "Caught an unknown exception!" << endl;
    }

    return 0;
}
```

**Output:**

```
Caught an unknown exception!
```

### Common Standard Exceptions

| Exception Class      | Header        | Description                                      |
| -------------------- | ------------- | ------------------------------------------------ |
| `std::exception`     | `<exception>` | Base class for all standard exceptions           |
| `std::runtime_error` | `<stdexcept>` | Errors detected at runtime                       |
| `std::logic_error`   | `<stdexcept>` | Logic errors in program (e.g., invalid_argument) |
| `std::out_of_range`  | `<stdexcept>` | Index out of range                               |
| `std::bad_alloc`     | `<new>`       | Memory allocation failure                        |

> [!TIP]
>
> - Use exceptions for **exceptional situations** — not for regular control flow.
> - Always catch by **reference** when using classes like `std::exception`.
> - Prefer using **standard exceptions** (`std::runtime_error`, `std::out_of_range`, etc.).
> - Use `noexcept` keyword to specify functions that don't throw exceptions.
> - Clean up dynamically allocated resources using **RAII** or smart pointers.

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->

## Practice Problems and Projects

This section offers a curated collection of frequently encountered C++ programming problems, complete with detailed solutions and sample outputs. It's tailored to strengthen your understanding of core concepts such as conditionals, loops, functions, arrays, pointers, and dynamic memory—through active, hands-on practice.

**Explore problem-solving in action:**  
[C++ Code Solutions Repository](https://github.com/msa-iqbal/c-plus-plus-code-solutions)

**Build real-world skills:**
Check out beginner-friendly to intermediate-level projects here:  
[C++ Mini Projects Repository](https://github.com/msa-iqbal/c-plus-plus-mini-projects)

<!-- START "Jump to Top"-->
<p align="right">
  <a href="#table-of-contents">Jump to Top ▲</a>
</p>
<!-- END "Jump to Top" -->
