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
The anchors used in an email address validation regex are the ^ and $ as seen in the beginning and end of the code shown.
- /^([a-zA-Z0-9_.-]+)@([\da-zA-Z.-]+).([a-zA-Z.]{2,6})$/
The ^ character 2nd to the start signifies that the regex will match with the section with code in the first set of parantheses that the character is before.  Meaning that information for each section is required in order to validate the email.  This does not apply to extensions though as they are not required.

### Quantifiers
The used quantifier in email regex is the {2,6} in the extension section.  The allowed amount of characters is from 2 to 6 characters so .co, .uk, or .ca will work, but something like .c will not work.

### Grouping Constructs
Parentheses are used to group the sections of a regex as seen in the code below.  Grouping is used to seperate meta characters from the literal characters.  Grouping can be used to isolate a part of the string to a back reference or to replace part of a string.
/^([a-zA-Z0-9_.-]+)@([\da-zA-Z.-]+).([a-zA-Z.]{2,6})$/

### Bracket Expressions
Bracket expressions are used to define the which characters will be matched within a regex.  An example from the regex being used in this email regex is below.
([a-zA-Z.]{2,6})$/
### Character Classes
The used character class in this regex is the \d in the section below.
@([\da-zA-Z.-]+)
The \d character class matches with a single character.
### The OR Operator
| acts as a boolean OR.  It will match the expression ebfore or after the | and can be used within a group or for an entire expression.
### Flags
Flags are used in a regex for advanced searching.  In this example we are using a multi-line flag that is being shown by the use of ^ and $ before the encasing / in the regex.  They are used to encase the expression across mutiple lines of code without breaking.
### Character Escapes
In a regex you will see a backslash that precedes a literal character.  Examples are \w or \s.
## Author
I am a student attending a UPENN Full Stack Web Devleopment Coding Boot Camp. I am on GitHub.
https://github.com/wyattwillner55

