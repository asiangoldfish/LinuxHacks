---
layout: default
title: C Basics
parent: C
grand_parent: Programming Languages
back_to_top: true
nav_order: 1
---

# C Basics
This page walks through the basics of a C program, and essential concepts in computer science. Navigate to your subject of interest in the table of contents below, or head over to [Program Structure](#program-structure) to begin right away.

## Table of Contents
- TOC
{:toc}

## Program Structure
In short, a C program most important function is the [`main()`](https://en.cppreference.com/w/c/language/main_function) function. The function tells the compiler where to look for your program's entry point. The basic C program looks as follows:

```c
int main() {

    return 0;
}
```

Let's break down what the code does:
- `int main()` is the program's entry point.
- `return 0` is `main()` return [statement](https://www.w3schools.com/c/c_statements.php).

## Variables
A program is a list of instructions that tell the computer what to do. To make it more useful to us humans, we introduce variables. These help us introduce variety to the program. A classical first program is a calculator. Let's add some code that `assigns` a value to a variable.

{: .note }
*Assigning* a value to a variable means we store some data in a memory chunk, accessible via a variable.

```c
int main() {
    int product = 9;

    return 0;
}
```

We have now created a variable named `product` of type [`int`](https://en.wikipedia.org/wiki/C_data_types). An int is short for integer and represents a whole number. Some other commonly used [*primary*](https://en.wikipedia.org/wiki/C_data_types) in C are as follows:
- `int`: Whole number.
- `float`: Floating point number
- `double`: Double-precision floating point number.
- `_Bool`: Boolean value. Its value is zero or non-zero.

{: .note }
[C99](https://en.wikipedia.org/wiki/C99) added the `bool` type in *stdbool.h*. It is an alias to the `_Bool` type and includes the `true` and `false` macros to `1` and `0` accordingly.

You can read more about the C primary types on [Wikipedia](https://en.wikipedia.org/wiki/C_data_types). For a short overview of C data types, refer to [Data Types](./data_types.html).

## Comments
There are two primary comment variations in C: single-line and block comments. They are both inline. Example:

```c
/**
 * This is a comment at the beginning of the file.
 *
 * Comments here typicallyd describes the file as a whole.
 */

 int main() {
    // This is a single-line comment.
    int product = 40;

    int factor = 3; // You can also inline comments like this

    /* In older C code, you may find single-line code written with
    block comment */
 }
```

## Libraries
While the [C standard library](https://en.wikipedia.org/wiki/C_standard_library) is small in comparison to the Java or Go standard libraries, it covers all the fundamental operations for a simple yet powerful program. You will find anything from IO operations to multithreading.

## Functions
A function signature in C fundamentally begins with the return type, followed by the function name, parameters and lastly the function body.

```c
/**
 * This function adds two integer functions together.
 */
int add(int a, int b) {
    // Using a return statement, we can output the result of
    // adding the two inputs together.
    return a + b;
}
```

You may have noticed we used curly brackets `{}` in the code above. This is the same brackets used in the `main()` function. In fact, the two functions have the same structure.

A scope is a designated area where variables *declared* in the scope only exists there. Once the program exits the function, the variable no longer exists. 

{: .note }
>Two commonly referred terms in programming is *declaring* and *defining* a variable. Although related, they are distinct and have different meanings.
>
>To declare a variable means we well the compiler this variable exists. When the program refers to this variable, it knows what the variable exists in the program.
>
>To define a variable means to specify what value should be assigned to the variable.

[Next page](./02_data_structures.html)