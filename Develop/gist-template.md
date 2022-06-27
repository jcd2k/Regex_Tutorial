# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

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

Regular Expressions, otherwise known as Regex, are powerful components that are used to precisely manipulate a string or a line of code. They have the potential to consolidate multiple operations into a more simply written expression which makes the file more not only more intuitive, but also more readable. Although its application in the context of this course will be strictly with JavaScript, it is also compatible with other back-end development languages such as Python, Perl, or PHP. Although these expressions are rather esoteric with their syntax, they are very practical and can boost your overall efficiency, as a developer, for all the reasons aforementioned.

### Anchors

In Regex, anchors are a form of a mathcing component. However, unlike dot notation or the other methods of matching code elements we've implemented, anchors are used to match positions on the line or string. This is in contrast to the previous methods, which were only useful for matching individual characters. Two of the most common Regex anchors are the:

caret ('^') - matches to the beginning of a line or string

and

dollar ('$') - matches to the end of a line or a string

There are many more anchors, some of which are synonymous in their functionality. Nevertheless, there are plenty to choose from when attempting to manipulate the positioning of a string or line of code.

Anchor examples:

^Hello          matches any string starting with `Hello`
World$          matches any string ending with `World`
^Hello World$   matches exact string
goodbye         matches any string that has the exact text `goodbye` in it

### Quantifiers

Quantifies, also referred to as repetition operators, are quite simple in their functionality. They act as a sort of toggle when attampting to read a token which precedes a certain element or component. With this being said, there are two common quantifiers:

asterisk ('*') - tells the server to read the token zero or more times

and

plus ('+') - tells the server to read the token one or more times

These operators are useful when matching two elements which are in proximity to each other in your syntax. Another handy operator for quantifying is:

{min,max} - specifies how many times the token will be repeated

With this being said, you'll spare yourself from having to manually copy elements by simply using a quantifier, allowing you to work more efficiently.

Quantifier examples:

xyz*        matches a string that has xy followed by zero or more z
xyz+        matches a string that has xy followed by one or more z
xyz?        matches a string that has xy followed by zero or one z

### Grouping Constructs

In Regex, grouping is exactly how it sounds, it allows you to group together various elements inside of rounded brackets or parentheses. Much like a math equation, whatever Regex function is applied from outside of the group will be applied to each individual element inside of the group. As previously stated, the two ways to create a group are:

Rounded Brackets ('{}') - used to specify a group

or

Parentheses ['()'] - used to specify a group

With the group being establlished, you may place another operator such as an anchor, which would then perform anchor mathcing on each element iside of the group. This allows the repetitive operations to be applied to each of the proper elements in one brief, consolidated statement. 

Grouping Construct examples:

x(yz)           parentheses create a capturing group with value yz
x(?:yz)*        using ?: we disable the capturing group
x(?<cat>yz)     using ?<cat> we assign a name to the group

### Bracket Expressions

Bracket expressions in Regex act in the same manner as character classes, they match a single character from a string. They use essentially the same syntax, with one notable distinction which is the omission of the backlash ('\') when specifying which character to select. Like the name might suggest, the syntax for this expression is:

Brackets ('[\]') - specifies a single character to be isolated from a string

The reason why brackets are useful form of character classing is due to their ability to isolate certain characters into a locale, where they can be specifically manipulated.

Bracket examples:

[xyz]         matches a string that etiher has x or x y or x z (same as x|y|z)
[x-y]         similar to case above
[u-zU-Z0-9]   a string that represents a single hexadecimal digit, case insensitively

### Character Classes

With character classes, you have the ability to instruct Regex to match a charcater or series of characters. Inside of the expression, the isolated is then matched with all of its common elements regardless of the order of characters inside the string. The syntax for character sets, similarly to bracket expressions, simply includes:

Brackets ('[]') (no backslash) - specifies a series of characters to be isolated from a string

As touched on previously in bracket expressions, character classes allow such common elements to be isolated so that more specific operations may be performed on them.

Character Class examples:

\d    matches a single any digit 0-9
\w    matches a single any character that is a-z
\s    matches ` `
.     matches any character

### The OR Operator

The OR Regex operation allows for the possibility of multiple expressions to be read, based on operational perameters which have been established. This provides a sort of grouping which can be called under different circumstances, depending on the desired outcome. These expressions usually follow some sort of function with multiple resulting possibilities. For syntax, the OR operator uses:

Double Vertical Lines ('||') - used to separate multiple desired resulting expressions

With the OR operator, you are able to achieve flexibility in the outcomes of a single function. In terms of consolidation, this saves you from writing the same conditional function for each outcome you wish to be possible.

OR Operator examples:

x(y||z)  matches a string that has x followed by y or z (and captures y or z)

### Flags

A flag in Regex is a condition which is used to modify search/querying operations. There are only six different flag operators, however each one is especially specific in its ability to fine tune a search that is performed. A few of the flag operators include:

('i' Ignore Casing) - makes the search blind to expression casing

and

('g' Global) - searches for all instances of an expression

Although fairly simple in their functionality, flags are useful operators in the sense that they allow the developer to more precisely define the scope of their queries.

Flag examples:

/Hello/g   matches all `Hello` in the test
/Hello/i   matches all `hello` despite casing (eg. HellO, heLLo, etc.)

### Character Escapes

Lastly, character escapes are another operator which can be used to negate elements from a particular operation. They are most commonly used in conjunction with character classes, being that they are often the most specific Regex identifier, but can be used more simply to evade common syntax issues.  The syntex for character escapes is simply:

Backslash '(\)' - used to exclude a character(s) from an operation

For example, '(\s)' is commonly used as reference for a space in string syntax. However, excluding 's' from something, such as a search operation, where a space may need to be implied in the query operation.

## Author

Regex Tutorial by:
Joshua Dominguez

github: jcd2k
