# Regex Tutorial
A Regex is shorthand for regular expressions.
A Regex is a string of text that lets you create patterns that help match,locate,and manage text.
These expressions are extremely useful for extracting data like phone numbers,emails, that follow a specific pattern from text. They can also be used in conjunction with any programming language including JavaScript.


## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.Here is a basic template that you can use to create your own cheatsheet:

## Table of Contents

- [Basic Syntax](#Basic-Syntax)
- [Anchors][def]
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

### Basic Syntax

 A regular expression is a sequence of characters that defines a search pattern. It can contain letters, numbers, and special characters. Some common special characters include:

'.' (dot): matches any single character except a newline

'*' (asterisk): matches the preceding character zero or more times

'+' (plus): matches the preceding character one or more times

'?' (question mark): matches the preceding character zero or one time

'^' (caret): matches the beginning of a string

'$' (dollar sign): matches the end of a string

### Anchors

'\b '- Matches the boundary between a word and a non-word character.

''\B' - Matches the boundary between two word characters or two non-word characters.

'^' - Matches the start of the string.

'$' - Matches the end of the string.


### Quantifiers
Quantifiers allow you to specify how many times a character or group of characters should be matched. Some common quantifiers include:
'* '- Matches zero or more occurrences of the previous character or group.

'+ '- Matches one or more occurrences of the previous character or group.

'? '- Matches zero or one occurrence of the previous character or group.

'{m}' - Matches exactly m occurrences of the previous character or group.
'{m,n}' - Matches between m and n occurrences of the previous character or group.

### OR Operator
The "or" operator is denoted by the vertical bar | character. For example, the pattern cat|dog would match either "cat" or "dog". You can also use parentheses to group patterns together with the "or" operator. For example, the pattern (red|blue) car would match either "red car" or "blue car".

It's worth noting that the "or" operator has lower precedence than other operators, such as quantifiers and anchors. This means that if you use the "or" operator in a complex regex, you may need to use parentheses to group patterns together and ensure that the operator is applied correctly.

Here are some additional examples of how to use the "or" operator in regular expressions:

-(Jan|Feb|Mar)uary matches "January", "February", or "March"

-apple|orange|banana matches "apple", "orange", or "banana"

-(http|https)://www.example.com matches URLs that start with "http://www.example.com" or "https://www.example.com

### Character Classes

Character classes allow you to match specific types of characters. Some common character classes include:

'\d': matches any digit (0-9).

'\w': matches any word character (letter, digit, or underscore).

'\s': matches any whitespace character (space, tab, newline, etc.).

'[]': matches any single character in the brackets.

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)


[def]: #anchors