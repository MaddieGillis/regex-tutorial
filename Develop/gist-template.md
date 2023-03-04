# Matching a Hex Value

In this tutorial will we will explain how to match a hex value using Regex. A hex value is a string of either 3 or 6 digits or the letters a-f. A hex value is often used for programming colors in web design.

## Summary

The expression to use for matching a hex value is `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`. 

A basic break down of this expression is that regex is looking for a string that starts with an optional ‘#’ symbol followed by 6 characters that contain the letters a-f and or the digits 0-9. Or it’s looking for a string that might start with a ‘#’, followed by a string of 3 characters that are a-f and or 0-9. During this tutorial we will break down further what each component means.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors
Anchors are used to specify the position of the string. In our code `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`, we have 2 anchors. The first anchor is `^`, and it is used to specify that this is the start of the string we are searching for. Without specifying that it’s the start, regex will search for any string the 3 or 6 specified characters whether it’s the start middle or end of the word. This way we are telling it to look at the start.

The other Anchor used is `$`. This specifies the end of the string. Without specifying the end, the search will include everything that contains 3 or 6 of our specified characters which could be found in longer words. The `$` tells the search to look for words or strings that are fully 3 or 6 of our specified characters and not to look past that.

### Quantifiers
Quantifiers are used to specify how many of the specified characters that are before the quantifier. In our case we are looking for either 6 characters as shown by `{6}` or 3 characters `{3}`. If we were to want to look for a range of characters we could set a minimum and a maximum like this `{3,6}`. This snippet is looking for a word or string that are either 3,4,5, or 6 characters long.

### OR Operator
Just like in Javascript, when we want to specify ‘or’ we use the pipe operator, or `|`. In our case we are looking for 6 characters of a-f and or 0-9 OR 3 characters of a-f or 0-9.

### Character Classes
Character classes are used to specify the characters we are looking for. Since Hex code is digits 0-9 and letters a-f, we want our character classes to denote that. To do so we put what we want in square brackets. For our case it would look like this, `[a-f0-9]`.

### Grouping and Capturing
Grouping and capturing allows us to group multiple queries into one query. In our case we want to group together our or statement as it is all one search. We can do this by using parentheses. `([a-f0-9]{6}|[a-f0-9]{3})`

### Bracket Expressions

### Greedy and Lazy Match

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
