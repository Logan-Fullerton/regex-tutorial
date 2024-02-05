# Title Regex Tutorial
For challenge 17 I will be breaking down a commonly used regular expression into its components. A regular expression is a sequence of charecters that are used to search for certain charecters or patterns within a string. They are commonly used when adding restraints or validations in code. To better understand how regex functions work I will break down a common regex into its parts and explain what each of them do


## Summary

In this tutorial, I will be braking down a password validation regex function. This function serves as a way to require certain charecter types to be included in a user's input. For the purpose of this challenge we will require at least one number 0-9, at least one uppercase charecter, at least one lower case charecter and at least one special charecter. The pattern for this expression would be as follows:
^(?=.*[0-9])(?=.*[a-z])(?=.*[A-Z])(?=.*[*.!@$%^&(){}[]:;<>,.?/~_+-=|\]).{8,32}$

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
^(?=.*[0-9])(?=.*[a-z])(?=.*[A-Z])(?=.*[*.!@$%^&(){}[]:;<>,.?/~_+-=|\]).{8,32}$
### Anchors
The anchors are the symbols that indicate the beginning and the end of the string. The beginning anchor tag is "^" and the closing anchor tag is "$". 
### Quantifiers
To insure that the user has entered a password that is within the desired min/max charecter limit, a quantifier is used. Quantifiers can set restrictions on the number of charecters required within a string. In the case of the given expression, the quantifiers come at the end of the expression in the curly brackets "{8,32}". This means that the password must be between 8 and 32 charecters long

### Grouping Constructs
Grouping is the use of parentheses to tie individual subexpressions together. The grouping method is applied in the given expression for each of the validations we want to apply. The first component (?=.*[0-9]) is validating that a number is present somewhere in the string. The second grouping we have is (?=.*[a-z]), this component validates that at least one lowercase charecter a-z is present in the string. The third grouping we see is is (?=.*[A-Z]), this grouping does the same as the one before but for uppercase charecters. The final grouping is used to validate that one or more special charecters is present in the string.

### Bracket Expressions

The charecters within the square brackets in each of the groupings talked about above are used to specify what range of charecters we want to include. In the first expression for example, 0-9 is within brackets because we want to include any charecter that is between 0 and 9. 

### Character Classes
Charecter classes are a range of charecters that we want to include at some position in the string. In the case of the password validation function we have several charecter classes for each of the criteria we required for our password input.
