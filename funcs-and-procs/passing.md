# Passing parameters

## By Value

If an argument is passed by value, at call time it may be a variable or an
actual value. If it is variable, the value within the variable is copied and
passed into the function. This is the default method for passing parameters, if
`BYREF` or `BYVAL` does not precede the parameters.

`{...} {ident}({ident} : {type}, ...) {...}`

OR

`{...} {ident}(BYVAL {ident} : {type}, ...) {...}`

**e.g.**

`PROCEDURE IsOdd(Number : INTEGER) ...`

OR

`FUNCTION IsOddFn(BYVALUE Number : INTEGER) RETURNS BOOLEAN ...`

## By Reference

If an argument is passed by reference, it must be a variable. If its value
inside the subroutine changes, its value outside the subroutine changes too.

`{...} {ident}(BYREF {ident} : {type}, ...) {...}`

**e.g.**

`PROCEDURE AddElement(BYREF Array : ARRAY OF CHAR, Element : CHAR) ...`

### Note

`BYREF` is just a more readable syntax for passing
[pointers](../data-types/built-in-data-types.md#pointers) by value. The example
above is equivalent to:

`PROCEDURE AddElement(Array : ^ARRAY OF CHAR, Element : CHAR) ...`

[← back to index](./mod.md#contents)
