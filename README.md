# regex-cheat-sheet
Regular Expressions cheat sheet


(regexr.com)[https://regexr.com/]


# Regular Expressions

## Examples
- ` /^(?=.*\d)(?=.*[a-z])(?=.*[A-Z])(?=.*[a-zA-Z]).{8,}$/g ` Password checker Contain a capital letter, lowercase letter, number, and min length of 8
- `/(<script(\s|\S)*?<\/script>)|(<style(\s|\S)*?<\/style>)|(<!--(\s|\S)*?-->)|(<\/?(\s|\S)*?>)/g` Replace all HTML tags

## Basic Syntax

- `/ expression /` flags, i.e `/[A-Z]+/g` basic format 
- `/.../`: Start and end regex delimiters
- `/ hello\?\*\\/` escape special characters with backslashes
- `()` group with parentheses
- `|` logical OR


## Character classes

- `\w` word `\d` digit `\s` whitespace (tabs, line breaks)
- `\W` NOT word `\D` NOT digit `\S` NOT whitespace
- `\t` tabs, `\n` line breaks
- `.` any character (except newline)


## Brackets

- `[xyz]` match any x, y, z
- `[J-Z]` match any capital letters between J & Z.
- `[^xyz]` NOT x, y, z


## Quantification
- `bob|alice` match bob or alice
- `z?` zero or one occurrences
- `z*` zero or multiple occurrences
- `z+` one or multiple occurrences
- `z{n}` n occurrences
- `z{min,max}` min/max occurrences


## Anchors

- `hello` world exact match
- `^hello` start of the strings
- `world$` end of the string




## Position Matching

- `^`: Start of string or start of line in multi-line mode
- `\A`: Start of string
- `$`: End of string or end of line in multi-line mode
- `\Z`: End of string
- `\b`: Word boundary
- `\B`: Not word boundary
- `\<`: Start of word
- `\>`: End of word


## Character Classes

- `\s`: Whitespace
- `\S`: Not whitespace
- `\w`: Word
- `\W`: Not word
- `\d`: Digit
- `\D`: Not digit
- `\x`: Hexade­cimal digit
- `\O`: Octal digit


## Special Characters

- `\n`: Newline
- `\r`: Carriage return
- `\t`: Tab
- `\v`: Vertical tab
- `\f`: Form feed
- `\xxx`: Octal character xxx
- `\xhh`: Hex character hh


## Groups and Ranges

- `.`: Any character except newline (\n)
- `(a|b)`: a or b
- `(…)`: Group
- `(?:…)`: Passive (non-c­apt­uring) group
- `[abc]`: a, b or c
- `[^abc]`: Not a, b or c
- `[a-z]`: Letters from a to z
- `[A-Z]`: Uppercase letters from A to Z
- `[0-9]`: Digits from 0 to 9

> Note: Ranges are inclusive.


## Quantifiers

- `*`: 0 or more
- `+`: 1 or more
- `?`: 0 or 1
- `{3`: Exactly 3
- `{3,}`: 3 or more
- `{3,5}`: 3, 4 or 5

> Note: Quantifiers are greedy - they match as many times as possible. Add a ? after the quantifier to make it ungreedy.


## Escape Sequences

- `\`:Escape following character. Used to escape any of the following metacharacters: {}[]()^$.|*+?\.
- `\Q`: Begin literal sequence
- `\E`: End literal sequence


## String Replacement

- `$1`: 1st group
- `$2`: 2nd group
- `$n`: nth group
- `$``: Before matched string
- `$'`: After matched string
- `$+`: Last matched string
- `$&`: Entire matched string

> Note: Some regex implem­ent­ations use \ instead of $.


## Assertions

- `?=`: Lookahead assertion
- `?!`: Negative lookahead
- `?<=`: Lookbehind assertion
- ``?!=, ?<!``: Negative lookbehind
- `?>`: Once-only subexp­ression
- `?()`: Condition if-then
- `?()|`: Condition if-then-else
- `?#`: Comment


## POSIX

- `[:upper:]`: Uppercase letters
- `[:lower:]`: Lowercase letters
- `[:alpha:]`: All letters
- `[:alnum:]`: Digits and letters
- `[:digit:]`: Digits
- `[:xdigit:]`: Hexade­cimal digits
- `[:punct:]`: Punctu­ation
- `[:blank:]`: Space and tab
- `[:space:]`: Blank characters
- `[:cntrl:]`: Control characters
- `[:graph:]`: Printed characters
- `[:print:]`: Printed characters and spaces
- `[:word:]`: Digits, letters and underscore


## Pattern Modifiers

- `g`: Global match
- `i`: Case-i­nse­nsitive
- `m`: Multi-line mode. Causes ^ and $ to also match the start/end of lines.
- `s`: Single-line mode. Causes . to match all, including line breaks.
- `x`: Allow comments and whitespace in pattern
- `e`: Evaluate replac­ement
- `U`: Ungreedy mode
