# Procedures

## Without parameters

```peg
PROCEDURE {ident}
    {statement}
    ...
ENDPROCEDURE
```

**e.g.**

```pseudocode
PROCEDURE InputOddNumber
    DECLARE Number : INTEGER
    
    REPEAT
        INPUT "Enter an odd number: " Number
    UNTIL Number MOD 2 = 1
ENDPROCEDURE
```

## With parameters

```peg
PROCEDURE {ident}({ident} : {type}, ...)
    {statement}
    ...
ENDPROCEDURE
```

**e.g.**

```pseudocode
PROCEDURE IsOdd(Number : INTEGER)
    IF Number MOD 2 = 1
      THEN
        OUTPUT "Number is odd"
    ELSE
        OUTPUT "Number is even"
    ENDIF
ENDPROCEDURE
```

[← back to index](./mod.md#contents)
