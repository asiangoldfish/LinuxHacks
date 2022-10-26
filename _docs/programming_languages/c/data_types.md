---
layout: default
title: Data Types
parent: C
grand_parent: Programming Languages
---

# Data Types

## Integers - Whole numbers

| Type          | Description                                   | Example   | Formatting        |
|:--------------|:----------------------------------------------|:----------|:------------------|
| int           | A whole number                                | 2         | %i, %o or %x      |
| long int      | Usually the same size as int                  | 3 or 3L   | %li               |
| long long int | Always 64-bit                                 | 27        | %lli              |
| short int     | Smaller sized version of int. No less than 16-bit | 13    | %hi, %ho or %hx   |

## Floating Point Numbers

| Type          | Description                                   | Example   | Formatting        |
|:--------------|:----------------------------------------------|:----------|:------------------|
| float         | Decimal numbers                               | 1.3       | %f, %e or %g      |
| double        | Decimal numbers (approx x2 size of float)     | 2.0       | %f, %e or %g      |
| long double   | Decimal numbers                               |           | %Lf, %Le or %Lg   |

## Characters

| Type          | Description                                   | Example   | Formatting        |
|:--------------|:----------------------------------------------|:----------|:------------------|
| char          | A single character                            | A         | %c                |

## Strings

| Type          | Description                                   | Example   | Formatting        |
|:--------------|:----------------------------------------------|:----------|:------------------|
| char[]        | Array of chars                                | Foo       | %s                |

## Bools

| Type          | Description                                   | Example   | Formatting        |
|:--------------|:----------------------------------------------|:----------|:------------------|
| \_Bool        | Signifies whether a value is true or false    | 1 or 0    | %i                |

## Pointers

| Type          | Description                                   | Example   | Formatting        |
|:--------------|:----------------------------------------------|:----------|:------------------|
| Pointer       | Prints the address of a given poitner         | 0x6f821d  | %#x               |

### Formatting with printf()
Variables may be formatted to take up a fixed amount of space to create virtual columns.
To format it in such way: `%10i`. This means to reserve 10 columns to the integer value.
This works with other datatypes that `printf` supports. Example:

```c
#include <stdio.h>

void main(void)
{
    char[10] name = Charles;
    int age = 21;

    printf("Name: %10s", name);
    printf("Age: %10i", age);
}
```

**Format**
Print memory address:
```c
printf("%p", &name);
```
