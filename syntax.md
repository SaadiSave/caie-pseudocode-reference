# General Syntax

## Comments

`// This is a comment`

## Declaring variables

`DECLARE {ident} : {type}`

**e.g.**

`DECLARE Age : INTEGER`

## Declaring constants

`CONSTANT {ident} = {lit}`

**e.g.**

`CONSTANT MeaningOfLife = 42`

## Assignment

`{ident} <- {expr}`

**e.g.**

`Age <- 17`

`Total <- A + B + C`

## Operators

| Operator | Operation                |
|----------|--------------------------|
| +        | Addition                 |
| -        | Subtraction              |
| *        | Multiplication           |
| /        | Division                 |
| ^        | Exponent                 |
| DIV      | Integer division         |
| MOD      | Modulus (Remainder)      |
| =        | Equal                    |
| <>       | Not equal                |
| >        | Greater than             |
| <        | Less than                |
| >=       | Greater than or equal to |
| <=       | Less than or equal to    |

## Logical operators

### `AND`

Returns `TRUE` only if all of its operands are `TRUE`.

`{expr:BOOLEAN} AND {expr:BOOLEAN} ...`

### `OR`

Returns `TRUE` if any of its operands are `TRUE`.

`{expr:BOOLEAN} OR {expr:BOOLEAN} ...`

### `NOT`

Flips the value of a boolean. Takes only one operand.

`NOT {expr:BOOLEAN}`

## Display output

`OUTPUT {expr}`

`OUTPUT {expr}, ...`

**e.g.**

```pseudocode
OUTPUT "Hello, World!"
OUTPUT Age
OUTPUT "Meaning of life: ", MeaningOfLife
OUTPUT (42 + 38)
```

## Get user input

`INPUT {lit:STRING} {ident}`

**e.g.**

`INPUT "Enter your name: " Name`

## Concatenation

`{expr} & ...`

where `expr` is of a built-in data type

**e.g.**

`Message <- "The meaning of life is " & MeaningOfLife & '.'`

## Indexing

`{expr:(STRING | ARRAY)}[{expr:INTEGER}]`

**e.g.**

`IntArray[3]`

`"Hello"[1]`

[← back to index](./readme.md#contents)
