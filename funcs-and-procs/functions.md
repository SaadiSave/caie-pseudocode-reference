# Functions

## Without parameters

```peg
FUNCTION {ident} RETURNS {type}
    {statement}
    ...
ENDFUNCTION
```

**e.g.**

```pseudocode
FUNCTION InputOddNumberFn RETURNS INTEGER
    DECLARE Number : INTEGER

    REPEAT
        INPUT "Enter an odd number: " Number
    UNTIL Number MOD 2 = 1

    RETURN Number
ENDFUNCTION
```

## With parameters

```peg
FUNCTION {ident}({ident} : {type}, ...) RETURNS {type}
    {statement}
    ...
ENDFUNCTION
```

**e.g.**

```pseudocode
FUNCTION IsOddFn(Number : INTEGER) RETURNS BOOLEAN
    IF Number MOD 2 = 1
      THEN
        RETURN TRUE
    ELSE
        RETURN FALSE
    ENDIF
ENDFUNCTION
```

[← back to index](./mod.md#contents)
