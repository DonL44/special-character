# Tutorial: Regex matching Hex value

Regular expressions are patterns used to match character combinations in strings. In a regular expression the metacharacter ^ means "not". So, while "a" means "match lowercase a", "^a" means "do not match lowercase a".

## Summary
I will be covering and breaking down the components of a regular expression used to match Hex Values. This is the regex code that we will be anaylizing today is:
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
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

## Regex Components

### Anchors

Anchors indicate a position to match strings.
`^` anchor matches at the beginning of a string.
`$` ancher matches at the end of a string.

### Quantifiers

Quantifiers indicate how many instances a character to match in a string and is appended to a character or an range of characters, e.g. `[...]`, more on that later. 
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```
In our example, we used:
1. `{2,6}` quantifier, we have set an range of 2 to 6 times to match what's denoted in `[...]`.
2. `+` quanifier at the end of `[...]`, this indicates we are matching between one and unlimited times. Both quantifiers matches as many time as possible giving back as needed.

### OR Operator

This specific regex does not have an "or" operator

### Character Classes

Character classes is a range of characters denoted in `[...]` of what we want to match.

### Flags

This specific regex does not have an "flag" operator

### Grouping and Capturing

Grouping is denoted by by parentheses, it unifies a pattern or string to be matched in a complete block. 
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```
In this example we have 3 groups `([a-z0-9_\.-]+)`, `([\da-z\.-]+)` and `([a-z\.]{2,6})`.

### Bracket Expressions

Brackets indicate a character class or range of characters that we want to match. 

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Example:
1. `[a-z0-9_\.-]` indicates we are looking for `lowercase "a-z" a through z, "0-9" 0 through 9, and we literal match special characters "_" underscore, "\." dot, and "-" hyphen`. 
2. `[\da-z\.-]` indicates we are looking for `"\d" 0 through 9, "a-z" a through z, "\." dot, and "-" hyphen`.
3. `[a-z\.]` indicates we are looking for `"a-z" a through z, and  "\." dot`.

### Greedy and Lazy Match

Greedy and Lazy Match
<br>![image](https://user-images.githubusercontent.com/85209802/136731575-ef79594b-faad-4f0a-9420-72d3bf72aa61.png)

Greedy and Lazy Match
Greedy and lazy matches. One of the easiest to understand to describe greedy and lazy matches was from the answer to a stack overflow question. A greedy match will look for the longest possible string, but a lazy match will look for the shortest one.
<https://stackoverflow.com/questions/2301285/what-do-lazy-and-greedy-mean-in-the-context-of-regular-expressions>
<https://javascript.info/regexp-greedy-and-lazy>
<https://www.w3docs.com/learn-javascript/greedy-and-lazy-quantifiers.html>

### Boundaries

![image](https://user-images.githubusercontent.com/85209802/136731835-4c20cdb5-65f1-4427-a047-18ee176cd68b.png)
Word boundary, exhibited with a (\b) it is equivalent to an anchor. It tells the user that this is a word boundary. It is a way to declare here a word/this is a word boundary. Example “fish” within the parenthesis is a word. If a particular regex declared, with anchors, “this is the first of a regex string,” using a ^ carrot, or the end of a string with the dollar sign, then a space or place is being declared. \b asks the programing language to look for that whole word. for example, if we said, please find the entire word “fish.” There are more complexities involved, but that’s a basic idea.
<https://www.javascripttutorial.net/regular-expression-word-boundaries/>

### Back-references

What does a back-reference look like? It is typically a \ followed by single-digit.
Back-reference is a command, which refers to something that already happened or a previous part of a matched regular expression. You could make a better preference by name or number; basically, what you are doing is you are referencing a named group, and you would have a bag/and a K then the name of that group, for example.

### Look-ahead and Look-behind

Look ahead and look behinds allows how matches get handled when using regular expressions.
I looked at the website regex buddy also says regular Dash expression .info, and Specifically, I looked at look-ahead and look-behind zero-length assertions on this website.
Look ahead and look behinds, also known as look around assertions, are similar to a start and end of the line or anchors. However, look around can match characters, and then they return a result of either a match or no match.

## Author

I'm DonL and I'm a full Stack Web Developer thats continuely furthering his knowledge in coding.   
GitHub: [DonL](https://github.com/DonL44)
