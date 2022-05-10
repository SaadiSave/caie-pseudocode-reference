# Iteration

## Count-controlled loop

```peg
DECLARE {ident@counter} : {type@ctype}
{...}
FOR {counter} <- {lit:ctype} TO {lit:ctype} STEP {expr:INTEGER}
    {statement}
    ...
NEXT {counter}
```

**e.g.**

```pseudocode
DECLARE i : INTEGER

FOR i <- 2 TO 14 STEP 3
    OUTPUT i, ' '
NEXT i

// Output: 2 5 8 11 14
```

## Post-condition loop

```peg
REPEAT
    {statement}
    ...
UNTIL {expr:BOOLEAN}
```

**e.g.**

```pseudocode
REPEAT
    INPUT "Enter Y or N: " Answer
UNTIL Answer = "Y"
```

## Pre-condition loop

```peg
WHILE {expr:BOOLEAN} DO
    {statement}
    ...
ENDWHILE
```

**e.g.**

```pseudocode
WHILE Answer <> "Y" DO
    INPUT "Enter Y or N: " Answer
ENDWHILE
```

[← back to index](./readme.md#contents)
