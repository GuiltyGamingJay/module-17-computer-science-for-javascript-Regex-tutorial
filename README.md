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

* '.' (dot): matches any single character except a newline

* '*' (asterisk): matches the preceding character zero or more times

* '+' (plus): matches the preceding character one or more times

* '?' (question mark): matches the preceding character zero or one time

* '^' (caret): matches the beginning of a string

'$' (dollar sign): matches the end of a string
<br>
<br>

### Anchors

* '\b '- Matches the boundary between a word and a non-word character.

* '\B' - Matches the boundary between two word characters or two non-word characters.

* '^' - Matches the start of the string.

* '$' - Matches the end of the string.
<br>
<br>

### Quantifiers
Quantifiers allow you to specify how many times a character or group of characters should be matched. Some common quantifiers include:
* '* '- Matches zero or more occurrences of the previous character or group.

* '+'- Matches one or more occurrences of the previous character or group.

* '?'- Matches zero or one occurrence of the previous character or group.

'{m}' - Matches exactly m occurrences of the previous character or group.
'{m,n}' - Matches between m and n occurrences of the previous character or group.
<br>
<br>
### OR Operator
The "or" operator is denoted by the vertical bar | character. For example, the pattern cat|dog would match either "cat" or "dog". You can also use parentheses to group patterns together with the "or" operator. For example, the pattern (red|blue) car would match either "red car" or "blue car".
<br>

It's worth noting that the "or" operator has lower precedence than other operators, such as quantifiers and anchors. This means that if you use the "or" operator in a complex regex, you may need to use parentheses to group patterns together and ensure that the operator is applied correctly.

Here are some additional examples of how to use the "or" operator in regular expressions:

* (Jan|Feb|Mar)uary matches "January", "February", or "March"

* apple|orange|banana matches "apple", "orange", or "banana"

* (http|https)://www.example.com matches URLs that start with "http://www.example.com" or "https://www.example.com
<br>
<br>
### Character Classes

Character classes allow you to match specific types of characters. Some common character classes include:

* '\d': matches any digit (0-9).

* '\w': matches any word character (letter, digit, or underscore).

* '\s': matches any whitespace character (space, tab, newline, etc.).

* '[]': matches any single character in the brackets.
<br>
<br>
### Flags
Flags are modifiers that can change the behavior of the pattern matching. Flags are usually specified after the closing delimiter of the regular expression and are denoted by a single letter.

Here are some common flags and their meanings:
<br>
<br>
* 'i' (case-insensitive): Makes the matching case-insensitive. For example, the pattern /apple/i would match "apple", "Apple", "aPpLe", and so on.

* 'g' (global): Matches all occurrences of the pattern in the input string. For example, the pattern /a/g would match all occurrences of the letter "a" in the input string.

* 'm' (multiline): Allows the ^ and $ anchors to match the beginning and end of each line in a multiline string, instead of just the beginning and end of the entire string.

* 's' (dot-all): Allows the . character to match any character, including newlines.

* 'u' (unicode): Enables full Unicode support. This is useful for matching characters from non-Latin scripts or for working with text that contains characters outside the ASCII range.

* 'y' (sticky): Matches the pattern starting at the current position in the string, without backtracking. This flag is useful for finding matches in large strings or for implementing custom text editors.

To use flags in a regular expression, you simply append the flag letter after the closing delimiter of the expression. For example, the pattern /apple/i would match "apple", "Apple", "aPpLe", and so on, because the i flag makes the matching case-insensitive.
<br>
<br>

Note that different programming languages and tools may have slightly different syntax for specifying flags, so be sure to consult the documentation for your specific implementation.
<br>
<br>
### Grouping and Capturing
Grouping allows you to apply a quantifier to a group of characters. Some common grouping syntax include:

* '()' (parentheses): group characters together

* '|' (pipe): match one of several possible patterns

* '(?)' (non-capturing parentheses): group characters without capturing the match
<br>
<br>

### Bracket Expressions
In regular expressions, bracket expressions (also known as character classes) allow you to match any one character from a set of characters. A bracket expression is enclosed in square brackets [] and contains a list of characters or character ranges that you want to match.

Here are some examples of bracket expressions:

* '[abc]': Matches any one character that is either "a", "b", or "c".

* '[a-z]': Matches any one lowercase letter from "a" to "z".

* '[A-Z]': Matches any one uppercase letter from "A" to "Z".

* '[0-9]': Matches any one digit from "0" to "9".

* '[aeiou]': Matches any one lowercase vowel.

You can also use the ^ character at the beginning of a bracket expression to create a negated character class. For example, [^abc] matches any one character that is not "a", "b", or "c".

You can include special characters, such as . or *, inside a bracket expression, but they will match literally, not as metacharacters. For example, [*+] matches either "*" or "+", not any number of the preceding character.

Here are some additional examples of bracket expressions:

* '[\d]': Matches any one digit (equivalent to [0-9]).

* '[\w]': Matches any one word character, which includes letters, digits, and underscores (equivalent to [a-zA-Z0-9_]).

* '[\s]': Matches any one whitespace character, such as a space or a tab.

* '[aeiouyAEIOUY]': Matches any one vowel, either lowercase or uppercase.



### Greedy and Lazy Match
In regular expressions, quantifiers such as *, +, and ? are greedy by default, which means they match as many characters as possible while still allowing the overall pattern to match. However, you can make a quantifier lazy (or non-greedy) by appending a question mark ? after it.

For example, consider the input string "ababab". The pattern /a.*b/ would match the entire string, because the * quantifier is greedy and matches all occurrences of any character between "a" and "b". 

However, the pattern' /a.*?b/ 'would only match the substring "ab", because the *? quantifier is lazy and matches as few characters as possible between "a" and "b".

Here are some additional examples of greedy and lazy matching:

* The pattern '/a+/' would match one or more occurrences of the letter "a" in the input string, while the pattern '/a+?/' would match as few occurrences of "a" as possible.

* The pattern '/a.*c/' would match any substring that starts with "a" and ends with "c", while the pattern /a.*?c/ would match the shortest such substring.

* The pattern '/<.*>/' would match any text enclosed in angle brackets, while the pattern '/<.*?>/' would match the shortest such text.

In general, it's a good idea to use lazy matching when you know that there may be multiple possible matches within a string, and you want to find the shortest match that satisfies the pattern. However, it's also important to be aware of the potential performance implications of using lazy matching, especially for large or complex input strings.

### Boundaries


### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)


[def]: #anchors