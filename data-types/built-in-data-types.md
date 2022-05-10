# Built-in Data Types

## Primitives

### `INTEGER`

A signed whole number

**e.g.** `42`

### `REAL`

A signed floating point number

**e.g.** `3.14`

### `CHAR`

A single ASCII character

**e.g.** `'D'`

### `BOOLEAN`

A type with only two possible values

**e.g.** `TRUE` OR `FALSE`

## Composite

### `STRING`

A sequence of characters. It is indexable.

**e.g.** `"Hello"`

### `DATE`

A [RFC 3339](https://datatracker.ietf.org/doc/html/rfc3339) datetime.

**e.g.** `1989-11-09` OR `1969-07-20T20:17:40`

### `ARRAY`

A sequence type. Can only store elements of one type. It is indexable.

**e.g.**

In literal form:

`[1, 2, 3, 4, 5]`

1-indexed filled with default values:

`ARRAY[1:100] OF REAL`

0-indexed:

`ARRAY[0:15] OF CHAR`

5×5 2D Array, 1st dimension 1-indexed, 2nd dimension 0-indexed:

`ARRAY[1:5, 0:4] OF BOOLEAN`

## Pointers

A reference type that points to a value in memory

### Declaration

`DECLARE {ident} : ^{type}`

**e.g.**

`DECLARE AgePtr : ^INTEGER`

### Get pointer to a value

`@{ident}`

**e.g.**

`AgePtr <- @Age`

### Access value behind pointer

`{ptr}^`

**e.g.**

`Age <- AgePtr^ + 1`

[← back to index](../readme.md#contents)
