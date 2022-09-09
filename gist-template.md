# What is a regex?

A regex, or a regualr expression, is a specific sequence of characters that specifies a search patern in text.  The most commonly used search patterns are string-searching or alorithms that find operations in strings which is used in input validation.  Regex techniques were developed in theoretical computer science and formal language theory.

## Summary

The regex I will be covering is one that matches 99% of valid eamil addresses.  The reason I say 99% is because one that matches 100% of them doesnt not truely does not exist.  When validating emails, a good practice, which can almost be sure that a user will match the regex is to limit what characters can input.  A common way to do so is guarentee that the user has to input something like 'gmail.com', 'yahoo.com', or 'xfinity.com'.

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
Regex components for are /^([a-zA-Z0-9_.-]+)@([\da-zA-Z.-]+).([a-zA-Z.]{2,})$/. What does that mean?

1. [a-zA-Z0-9_.-]+ is the name section of the characters that will comfirm that each character is either a upper or lower case letter, a number from 0-9, a allowed special character that is in the code.  The '+' symbol at the end of the characters means that there can be 1 to a infinite amounte of characters allowed in this section.
2. @([\da-zA-Z.-]+) is the domain section that does the the samething as the name section, but it is validating that the domain address for the email is valid.
3. ([a-zA-Z.]{2,}) is the extension section for confirming that the email address extension is valid.  Usually a .com, .mail. or .net  A typical email address is able to end with 2 characters as such as .co email addresses.  Sometimes for international email addresses there will be an extension such as .uk or .ca.

### Anchors


### Quantifiers

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
