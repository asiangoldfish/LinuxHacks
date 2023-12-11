---
layout: default
title: Data Structures
parent: C
grand_parent: Programming Languages
---

# Data Structures

## Table of Content
- [Enumeration](#enumeration)

## Enumeration

Short: enum  
An enumeration is a sorted list of items. It may also be considered a set or collection of items. Example:

```c
enum WeekDays {
    day1 = monday,
    day2 = tuesday,
    day3 = wednesday,
    day4 = thursday,
    day5 = friday,
    day6 = saturday,
    day7 = sunday
};

// Another way to declare an enum
enum AnotherWayToDeclareEnum {
    monday = 0, // Here we explicitly specify that monday has index 0
    tuesday,
    wednesday,
    thursday,
    friday,
    saturday,
    sunday
};
```

To use an enum:

```c
enum WeekDays weekDay = day1
enum AnotherWayToDeclareEnum anotherEnum = monday;
```

