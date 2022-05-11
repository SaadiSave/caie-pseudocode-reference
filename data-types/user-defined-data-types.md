# User-defined data types

## Type alias

`TYPE {ident} <- {type}`

**e.g.**

`TYPE IntPtr <- ^INTEGER`

## Record type

### Declaration

```peg
TYPE {ident}
    DECLARE {ident} : {type}
    ...
ENDTYPE
```

**e.g.**

```pseudocode
TYPE Person
    DECLARE Name   : STRING
    DECLARE Height : REAL
ENDTYPE
```

## Usage

`DECLARE Olaf : Person`

### Assign field

`{ident}.{ident} <- {expr}`

**e.g.**

```pseudocode
Olaf.Name <- "Olaf"
Olaf.Height <- 1.68
```

### Access field

`{ident}.{ident}`

**e.g.**

`OUTPUT Olaf.Name`

## Enumerated data type

When an enumerated data type is declared, all its possible values are identified

`TYPE {ident} = ({ident}, ...)`

**e.g.**

`TYPE Direction = (North, South, East, West)`

The `BOOLEAN` type can be thought of as special case of enum with only two possible values:

`TYPE BOOLEAN = (TRUE, FALSE)`

[← back to index](../readme.md#contents)
