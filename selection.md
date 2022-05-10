# Selection

## `IF...THEN`

```peg
IF {expr:BOOLEAN}
  THEN
    {statement}
    ...
ENDIF
```

**e.g.**

```pseudocode
IF x < 0
  THEN
    OUTPUT "Negative"
ENDIF
```

## `IF...THEN...ELSE`

```peg
IF {expr:BOOLEAN}
  THEN
    {statement}
    ...
  ELSE
    {statement}
    ...
ENDIF
```

**e.g.**

```pseudocode
IF x < 0
  THEN
    OUTPUT "Negative"
  ELSE
    OUTPUT "Whole number"
ENDIF
```

## Nested `IF`

```peg
IF {expr:BOOLEAN}
  THEN
    {statement}
    ...
  ELSE
    {IF...THEN | IF...THEN..ELSE}
ENDIF
```

**e.g.**

```pseudocode
IF x < 0
  THEN
    OUTPUT "Negative"
  ELSE
    IF x = 0
      THEN
        OUTPUT "Is zero"
      ELSE
        OUTPUT "Positive"
    ENDIF
ENDIF
```

## `CASE` statement

```peg
CASE OF {expr}
  {lit} : {statement}
  {lit}, ... : {statement}
  {lit} TO {lit} : {statement}
  OTHERWISE {statement}
ENDCASE
```

If r.h.s. has mutiple statements, use a 2-space indentation

**e.g.**

```pseudocode
CASE OF Grade
  'A' :
    Pass <- TRUE
    OUTPUT "Excellent"
  'B' TO 'E' :
    Pass <- TRUE
    OUTPUT "Can do better"
  'F', 'U' :
    Pass <- FALSE
    OUTPUT "Must work harder"
  OTHERWISE OUTPUT "Invalid Grade"
ENDCASE
```

[← back to index](./readme.md#contents)
