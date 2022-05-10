# Calling Procedures and Functions

## Without parameters

### Procedure

`CALL {ident}`

**e.g.**

`CALL InputOddNumber`

### Function

`{ident}`

**e.g.**

`Number <- InputOddNumberFn`

## With parameters

### Procedure

`CALL {ident}({expr}, ...)`

**e.g.**

`CALL IsOdd(Number)`

### Function

`{ident}({expr}, ...)`

**e.g.**

`Valid <- IsOddFn(Number + 3)`

[← back to index](./mod.md#contents)
