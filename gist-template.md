# Regex for Matching a URL

In this tutorial, I will explain how the regular expression, or regex, for matching a URL functions by breaking down each part of the expression and describing what it does. 

## Summary

The regex for matching a URL is `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`. I will discuss the regex components, what they do and how they are used in this regex.  
```
Regex for Matching a URL: /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
```

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components

There are a lot of regular expression components that make a regex work. I will discuss anchors, quantifiers, grouping constructs, bracket expressions, character classes, flags, character escapes and how they function in this regex for matching a URL. 

### Anchors

Anchors in regular expressions are tokens that assert something about the string such as teh beginning or the end of the line. In our regex for matching a URL, it uses the character `^` to indicate the beginning of the string. It is telling the engine that the string needs to start with http. Their are some other characters in their too but we will discuss those later. The `$` character tells teh engine that it is at the end of the string. It is telling the engine that this is the end of our URL matching regex. 
```
^ beginning, $ ending.
```

### Quantifiers

### Grouping Constructs

### Bracket Expressions

### Character Classes

### Character Escapes

## Author

