# Challenge 17 Regular Expressions Tutorial

This tutorial aims to elucidate the concept of regular expressions (regex) and their practical applications. Regular expressions are invaluable for identifying specific character patterns within strings, making them ideal for tasks like data extraction and validation. For instance, this tutorial provides a detailed example of using regex to validate email addresses.

## Summary

Throughout this tutorial, we'll use the following regex code to illustrate various components:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

This code effectively matches email addresses and serves as a practical example for understanding regex components.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

Anchors (`^` and `$`) specify the start and end of the regex pattern, respectively. In our email matching code:

* `^([a-z0-9_\.-]+)` signifies that matching text must begin with this pattern

* `\.([a-z\.]{2,6})$` ensures the match ends correctly, with a valid domain suffix.

### Quantifiers

Quantifiers like + dictate how many times a specific character or group must appear for a match. For example,
  
`([a-z0-9_\.-]+)` requires at least one occurrence of the characters inside the brackets.

### OR Operator

The OR operator (`|`) allows for alternatives in the regex pattern. For instance, in a hex code regex:

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`


This matches either a 6-character or 3-character hex code preceded optionally by `#`.

### Character Classes
Character classes, such as `\d` in our email regex, match specific types of characters. `\d` ensures that only digits (`0-9`) are valid immediately following the `@` in an email address.
### Flags
Regex flags (`g`, `m`, `i`) provide additional matching options:

* `g` (global): Matches all instances in a string.

* `m` (multiline): Processes each line separately.

* `i` (case-insensitive): Ignores case distinctions.

### Grouping and Capturing
In our email regex:

* (`[a-z0-9_\.-]+`) is a capturing group that matches the username part.

* (`[\da-z\.-]+`) captures the domain name.

* (`[a-z\.]{2,6}`) captures the top-level domain (TLD).

### Bracket Expressions
Bracket expressions (`[...]`) define specific sets of characters that can match. For instance, `[a-z0-9_\.-]` allows lowercase letters, digits, underscore, hyphen, and period.

### Greedy and Lazy Match
Greedy and lazy matching control how regex patterns consume characters in a string, optimizing for either maximum (`greedy`) or minimum (`lazy`) matches. This tutorial does not feature these concepts.

### Boundaries

Regex boundaries (`\b`) define where specific patterns can start or end within a string. This tutorial does not cover boundary usage. 

### Back-references

Back-references (`\1`, `\2`, etc.) refer to previously captured groups within the regex pattern. This tutorial does not utilize back-references.

### Look-ahead and Look-behind

Look-ahead (`(?=...)`) and look-behind (`(?<=...)`) assertions allow checking for patterns without including them in the match. This tutorial does not include these advanced features.
## Author

This tutorial was created by Shawn Carlson.

Conatct Shawn:

[GitHub](https://github.com/oxmagnus)

[Email](dev@example.com)
