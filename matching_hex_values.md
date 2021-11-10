# Matching Hex Values

In this Gist, I'll be teaching you about regular expression, commonly known as Regex, more specifically, how to match hex values with Regex!


## Summary

Before we can start discussing the process of matching hex values, do you know what hex values are? Hexadecimal values is a system to represent specific color more accurately to computers; it provides more consistency. Below, is the folowing Regex used to match hex values:

```
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
```


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)
- [Author](#author)


## Regex Components


### Anchors

```
^
```
The character above signifies the beginning of a string. For example: `^example` signifies that the string will begin at `example`. In our case, a hex values must always begin with `#` so to initate that, we have the following, `^#`.
```
$
```
Just like to start a string, we must end it so the computer knows when to stop. We use the following, `$` to signifies when the string will end, for example: `example$` signifies that the string will end at `example`. In our case, since hex code only contain 3 or 6 values, the code will end on the third or sixth character.


### Quantifiers

```
?
```
The first quantifiers we have is a `?`, this is much like a conditional statement looking for the following `{3}` or `{6}`. Depending on the hex values, depends on how many characters will be contained in the string for a specific color.
```
{3} or {6}
```
The following provides us the length for the hex code. Some hex codes are 3 charcters while most are 6 characters. The length of the hex code goes after `#`.


### Grouping Constructs

```
([a-f0-9]{6}|[a-f0-9]{3})
```
Within the grouping, we have an OR operator stating that if either the length is 3 or 6 characters, the will use the following structure: `[a-f0-9]`


### Bracket Expressions

```
[]
```
Within the brackets gives us the criteria for the following code. Whatever is in the brackets are characters used to make up the following expressions, in our case: `[a-f0-9]`


### Character Classes

```
[a-f0-9]
```
In our class, we have 2 seperate criteria for characters that can be used for hex values. The first being `a-f`, when using the alphabet for hex values, the code will never exceed `f`. The following letters will be used for hex values: `a`, `b`, `c`, `d`, `e`, and `f`. The second part being `0-9`. The following numbers will be used for hex values: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, and `9`.


### The OR Operator

```
|
```
Since hex codes can have a length of either 3 characters or 6 charcters but no both, it needs to be seperated by an OR operator. It stats that after the `#`, the following code to provide the hex value, it will be either 3 or 6 characters long.


### Flags

This regular expression does not contain any flags!


### Character Escapes

This regular expression does not contain any character escapes!


## Author

Hello, my name is Sami Khawja! While creating this gist, I'm a current student at UC Berkeley's full stack coding bootcamp learning what will be the beginning of my career! What I know and understand is only the tip of the iceberg and Mars is the limit! Below, I've attached a link to my GitHub profile:

Check it out!
[GitHub](https://github.com/samikhawja)