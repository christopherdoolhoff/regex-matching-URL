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

Quantifiers are used to tell the engine reading the regex how many instances of a character or group should be present. The `?` is a quantifier that tells the engine a character or group is optional. In our URL matcher, it is saying the "s" in "https" is optional and might just be `http`. The next `?` is telling the engine that `https?:\/\/` is also optional. The final `?` is telling the engine that the last `/` is optional and may or may not be present as well. We just discussed `?`, now we will discuss `*`. Like `?`, the `*` character indicates that something may or may not be present. The difference between them is that `?` indicates the instance may occur once or not at all but `*` indicates that the instance may occur zero or more times. This tells the engine in our case that it can expect letters or numbers in any quantity but they may also not be present. The `+` character indicates an occurrence of an instance one or more times. In our regex, it is saying that we expect to see digits, letters, dots, and hyphens. The last quantifier in our expression is the `{m,n}` quantifier. It indicates the least or minimum number of occurrences and the most times an instance can occur. In our regex, it is saying that letters a to z and a dot should occur between two and six times `{2,6}`.
```
? Zero or one. * Zero or more. + One or more. {m,n} Minimum m, maximum n.
```

### Grouping Constructs

Our regex is grouped together with parentheses, splitting our expression into four groups. The first group is `(https?:\/\/)?` where it is saying this group is optional. The second group is the `([\da-z\.-]+)` indicating that we expect digits, letters, dots, and hyphens. The third group is `([a-z\.]{2,6})` indicating extensions with letters and dots. This third group is where our URLs usually have a ".com" or ",org". The fourth and final group in our regex is `([\/\w \.-]*)*\/?` indicating optional filepaths or directories.
```
Group 1: (https?:\/\/). Group 2: ([\da-z\.-]+). Group 3: ([a-z\.]{2,6}). Group 4: ([\/\w \.-]*).
```

### Bracket Expressions

Bracket Expressions can be used to match a group of characters. It is used multiple times in our regex for matching a URL. In `[\da-z\.-]`, we are saying that we expect to see digits, letters, dots, or hyphens. In `[a-z\.]`, we are saying that we expect to see letters and dots. In `[\/\w \.-]`, we are saying that we expect to see letters, numbers, slashes, hyphens, or dots.
```
Bracket Expressions:[\da-z\.-], [a-z\.], [\/\w \.-].
```

### Character Classes

You can use bracket expressions to indicate a character class. This makes the bracket expression an example of character classes. There are also other character classes that do not need brackets. our regex uses some of these others as well. The `\d` indicates a number between zero and nine, or a digit.\w indicates a lowercase letter, uppercase letter, or digit between zero and nine. 
```
Character Classes:  Bracket Expression Character Classes:[\da-z\.-], [a-z\.], [\/\w \.-]. Character Classes without Brackets: \d, \w.
```

### Character Escapes

## Author

