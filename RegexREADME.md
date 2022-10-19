# Regex tutorial for matching URLs

A Regex, or regular expression, is a string of characters that defines a search pattern. it's very specific and very long and is used for searching strings to find specific character patterns.

## Summary

This is a Regex for finding a URL
`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`
A regex always begins with /^. its a way of symbolizing the start of the expression. The first set of parentheses is used to define a capture group. The `\` indicates the start of a new character. they're basically there to confuse you. the a-z indicates what characters are allowed. when you see `\.` its an escape sequence to indicate the next character. the `\*` indicates the previous argument may occur more than once. and `$` indicates the end of the string.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

anchors indicate the start and end of a string. for our regex it was `^` and `$`
these are used to keep the regex separate from the rest of the code. the `$` indicates that the last character of the string must match that character in the regex. the `^` indicates the character immediately following the `^` must match that which has been defined in the regex. Used together it's saying that that the input string must match the requirements inside the regex

### Quantifiers

theres two types of qunatifiers. Greedy and lazy. this dynamic duo indicate the the character or expression to their left must conform to the regex.
these are `\*` `?` and `+` characters. `?` indicates that one character to the left of the quantifier can be optional. while the `*` indicates that more than one character to the left is optional.
for instance in our regex `/^(https?:\/\/)?` is used to indicate that either http:// or https:// is a valid input.
in the same vein the `$` indicates that multiple instances are optional. so when we see this in our regex `([\/\w \.-]*)*` its stating that any number of characters can be added there to flesh out the domain.

### Grouping Constructs

Grouping constructs are just the `()` that help keep things a little more organized and compartmentalized. You can think of them like parentheses in math expressions pretty much.
for example in our regex `(https?:\/\/)` is grouping the http string in one section the `([\da-z\.-]+)` is separating out the logic for the domain name, `([a-z\.]{2,6})` allow for any kind of top level domain such as .io or .com or whatever the domain is.
finally `([\/\w \.-]*)` groups together the logic for the rest of the url.

### Bracket Expressions

`[]` anything between those is a bracket expression
this is used to match the characters inside the brackets. while the other operators helped to differentiate and apply logic this is used to match characters to that which is in the brackets. they're often used in conjunction with quantifiers to help define exactly what characters are allowed in the string and then the quantifier defines how strict the brackets are at allowing different characters.

### Character Classes

classes make sure that characters match up to their overall sets
`\w` is used to match the expression with a letter and `\d` is used to match any digit to the expression

### Character Escapes

`\.` are the character escapes this indicates the end of one section of the expression and allows for the next part to be added in without interfering with previous logic.

## Author

My name is Landon Tucker and the link to my github is https://github.com/AugustusXI
