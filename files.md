# File handling

```pseudocode
DECLARE Name : STRING
CONSTANT File = "Names.txt"
```

## Opening and closing file

```peg
OPENFILE {expr:STRING@filename} FOR {READ | WRITE | APPEND}
{...}
CLOSEFILE {filename}
```

**e.g.**

```pseudocode
OPENFILE File FOR READ
...
CLOSEFILE File
```

## Reading a file

Only one line can be read at a time

```peg
OPENFILE {expr:STRING@filename} FOR READ
READFILE {filename}, {ident:STRING}
{...}
CLOSEFILE {filename}
```

**e.g.**

```pseudocode
OPENFILE File FOR READ
READFILE File, Name
CLOSEFILE File
```

## Writing to a file

The file is overwritten as soon as it is opened in write mode. Every `WRITEFILE`
operation writes to a new line.

```peg
OPENFILE {expr:STRING@filename} FOR WRITE
WRITEFILE {filename}, {expr:STRING}
{...}
CLOSEFILE {filename}
```

**e.g.**

```pseudocode
OPENFILE File FOR READ
WRITEFILE File, "Hans"
CLOSEFILE File
```

## Appending to a file

The file is not overwritten when opened in append mode. Every write operation
writes to a newline at the end of the file.

```peg
OPENFILE {expr:STRING@filename} FOR APPEND
WRITEFILE {filename}, {expr:STRING}
{...}
CLOSEFILE {filename}
```

**e.g.**

```pseudocode
OPENFILE File FOR APPEND
WRITEFILE File, Name
CLOSEFILE File
```

## The end-of-file (EOF) marker

The following pseudocode reads a file line by line, and concatenates the
contents to a single string. The string is then output:

```pseudocode
DECLARE Text, Line : STRING

Text <- ""
Line <- ""

OPENFILE "Essay.txt" FOR READ

WHILE NOT EOF("Essay.txt") DO
    READFILE "Essay.txt", Line
    Text <- Text & Line
ENDWHILE

OUTPUT Text
```

[← back to index](./readme.md#contents)
