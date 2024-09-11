---
layout: default
title: Flow Control
parent: C
grand_parent: Programming Languages
---

# Flow Control

Flow control is a technique to dynamically change a program's behaviour based on determined conditions. In C, we mainly have the following flow control mechanisms:

- if statements
- switch cases
- for loop
- while loop
- do-while loop
- 

## Related Keywords

| Keyword  | Description                                                                                                                   |
| :------- | :---------------------------------------------------------------------------------------------------------------------------- |
| break    | Exits a loop and ignores the loop condition                                                                                   |
| continue | Regardless of where in a loop the program execution is at, ignores the rest of the block to evaluate the loop condition again |

## While Loop

This loop repeats a set of commands if a given condition is met. Syntax:
```c
while (/* condition */)
{
    /* code */
}
```

Optionally, the while loop may be used without a code block. Syntax:
```c
while(/* condition */);
```

## Do While Loop
This loop behaves like the while loop, but executes the block first before evaluating the condition. Syntax:
```c
do
{
    /* code */
} while (/* condition */)
```

## For loop
Unlike the while loop, the for loop keeps track of an integer variable and treats it as a flow control index. Syntax:
```c
// for (index; condition; index increment or decrement)
for (int i = 0; i < 10; i++)
{
    /* code */
}
```