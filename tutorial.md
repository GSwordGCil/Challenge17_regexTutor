# Matching an Email Regex Tutorial

This tutorial will explain how the "Matching an Email" regex pattern works by breaking down each component of the pattern.

## Summary

The "Matching an Email" regex pattern is used to validate email addresses. The pattern is as follows: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/



This pattern ensures that the input string has the format `username@domain.extension`, where `username` can include lowercase letters, numbers, underscores, hyphens, and periods; `domain` can include lowercase letters, numbers, hyphens, and periods; and `extension` must be a lowercase letter with a length between 2 to 6 characters.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

The anchors `^` and `$` match the beginning and end of the line, respectively.

example:
/^abc/ will match "abc" at the start of a string, but not "xyzabc".
/abc$/ will match "abc" at the end of a string, but not "abcxyz".


### Quantifiers

The quantifier `{2,6}` matches between 2 to 6 occurrences of the preceding element.

example:
/a{2,4}/ will match "aa", "aaa", and "aaaa", but not "a" or "aaaaa".


### Grouping Constructs

The grouping constructs `()` group together elements in the regex pattern. In this example, there are three groups: `([a-z0-9_\.-]+)`, `([\da-z\.-]+)`, and `([a-z\.]{2,6})`.

example:
/(abc)/ will match "abc" and remember the match.


### Bracket Expressions

The bracket expressions `[]` match any one of the characters inside the brackets.

example:
/[abc]/ will match "a", "b", or "c".


### Character Classes

The character class `\d` matches any digit.

example:
/\d/ will match any digit from 0 to 9.


### Character Escapes

The character escapes `\.`, `\d`, and `\\` match the literal characters `.`, `d`, and `\`, respectively.

example:
/\./ will match the character ".".
/\\d/ will match the characters "\d".
/\\/ will match the character "\".


## Author

This tutorial was written by [Adrian Cheung](https://github.com/GSwordGCil).
