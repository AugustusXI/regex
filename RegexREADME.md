# Regex tutorial for matching URLs

A Regex, or regular expression, is a string of characters that defines a search pattern. it's very specific and very long and is used for searching strings to find specific character patterns.

## Summary

This is a Regex for finding a URL
`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`
A regex always begins with /^. its a way of symbolizing the start of the expression. The first set of parentheses is used to define a capture group. The \ indicates the start of a new character. they're basically there to confuse you. the a-z indicates what characters are allowed. when you see \. its an escape sequence to indicate the next character. the \* indicates the previous argument may occur more than once. and $ indicates the end of the string.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

anchors indicate the start and end of a string. for our regex it was `^` and `$`
these are used to keep the regex separate from the rest of the code.

### Quantifiers

theres two types of qunatifiers. Greedy and lazy. this dynamic duo indicate the the character or expression to their left must conform to the regex.
these are `\*` `?` and `+` characters

### Grouping Constructs

goruping constructs are just the `()` that help keep things a little more organized and compartmentalized. You can think of them like parentheses in math expressions pretty much.
for example `(https?:\/\/)` is saying that we can have either http https or nothing at all.

### Bracket Expressions

`[]` anything between those is a bracket expression

### Character Classes

classes make sure that characters match up to their overall sets
`\w` is used to match a word up.

### The OR Operator

### Flags

### Character Escapes

`\.` are the character escapes

## Author

My name is Landon Tucker and the link to my github is https://github.com/AugustusXI
