# Computer Science - The Regex Tutorial!

You can think of Regex, or regular expression, as a text search that with the addidtion filters and Regex Components, to become quite soophisticated and focused. Regex is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string.

## Summary

The explantion of Regex in the Javascript environment, where all variable declarations and commands are written in Javascript. Its very important to not that Regex notation is a universal language and can be applied across various coding languages.
 
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

This regular expression identifies an email by utilizing the ^ anchor, indication the beginning of the string, and the $ anchor, indicating the end of the string. The regex concludes at $ unless multiline (m) mode is activated.

### Quantifiers

Quantifier are character that specify the frequency of occurrence for the preceding character ina a regular expression. The "?" symbol denotes that the characters before it may appear once or zero times. With the "+" symbol, the preceding characters can occur in any number of instances, while the "*" symbol signifies that the characters before it can occur zero or more times. The notation "{min, max}" tells you that the characters before it must appear at least "min" times and at most "max" times.

The regular expression /^[a-z0-9_.-]@([/da-z.-]+)([a-z]{2,6})$/ is analyzed in this context. The "+" quantifier implies that the characters preceding it can repeat one or more times. The expression concludes with a dollar sign ($) placed just before {2.6}, specifying that each segment preceding it must have a minimum length of two chaacters and a maximum length of six characters.

### OR Operator

When reading, between the "|"(pipe) and "[]"(square brackets), when "x" is followed by "y" or "z" in a string, it results in a match and gets both "y" and "z"(example like: "xy" or "xz"). This is distinct from the previously mentioned case where "x[yz]" cannot get "y" or "z" by itself. Instead it will captre "xy" or "xz" but not "xyz"

### Character Classes

The period"." symbolizes any character except for newline characters. "/w" is representative of words, while "/W" indicates non-word characters, and "\d" stands for numbers. "\D" represents non-numeric values. "\S" shows anything other than white space. "[abc]" tells either "a","b"," or "c" while "[^abc]" signifies the absense of "a","b" or "c""[a-z]" shows characters ranging from "a" to "z".

In the formula /^[a-z0-9_.-]@([/da-z.-]+)([a-z]{2,6})$/, character classes a-z and "\d" are utilized. This suggests that, along with digits and 0-9, the string may also include letters from a to z.

### Flags

The usage of "g" for global matching and "i" for case-insensitive matching is denoted by aappending these flags after the search pattern, as shown by the 2 slash letters. In the case of /xyz/g, after the first match, the search resumes at the end of the preceding match. To match the beginning and the end of a line, "m" is combined with ^ and $. For example, /xyz/i would match "XYZ" while /xyz/ would only match "xyz". The "i" flag makes the expression case-insensitive. The typical regex format is /abc/, where the search pattern is closed by two slash characters. These values can be put together to define a flag at the end.

### Grouping and Capturing

The focus of parenthesis within a regex pattern, is to close text, enabling the application of quantifiers and other operations to that specific content. In the formula /^([a-z0-9_.-]+)@([\da-z.-]+)([a-z.]{2,6})$/, there are 3 groups enclosed in paremtheses and seperated by brackets. The groups allow for the targeted application of regex operations to distinct portions of the matched text.

### Bracket Expressions

Bracket expression, also known as character classes, are conceptualized as longer or equivalent. For instance, [xyz] is the same as x|y|z. Inside brackets, groups of digits can be specified, and not all possibilities need to be spelled all the way out. Foe example, [x-z] is the same as [xyz], representing x,y, or z. A bracket group like [a-z1-9] will match a digit that is 1-9 or a-z. It's possible to include multiple sets of digits within a single bracket group. Following the brackets, characters can be specified, such as [xyz]#, where an x,y, or z string before a # will match. When the ^ symbole shows inside a bracket expression, it becomes a negation, as in [^xyz], meaning it matches any charcter that isn't x,y, or z. THe text within brackets [a-z0-9_-] indicates that the search term may be any character from a-z, a number between 0-9, and underscore, or a hyphen.

### Greedy and Lazy Match

This regex incorporates greedy matches, shows by the use of the + quantifier, which matches as many times as possible, returning as needed. THe final capture group also utilizes {} as another greedy quantifier with {{2,6}}. In a greedy expression, it matches as many occurences as possible, while in a lazy expression, it matches as few as possible. If the string end and the pattern isn't done, the search will backtrack one character as a time, attempting to complete the undone pattern expression. This process continues until the pattern is complete pr fails to validate, repeating as it needs.

### Boundaries

In the context of email validation, the inclusion of boundaries is sometimes unnecessary. This is because the whole email adresses need to be identified and the "@" symbol serves as a boundary for the given email adress. The components like username, domain, and extension are treated as entities with boundaries before and after the "@" symbol. Similar to the anchors $ and ^, "\b" serves as an anchor when one side is a word character and the other is not. It's worth mentioning that every point not matched by "\b" is matched by "\B". The email regex provided doesn't incorporate boundaries in its validation process.

### Back-references

I have the perspective that email validation usually does not really require back references. Back references are commonly employed for task like matching HTML elemants or referencing content between tags on an HTML page, where the regex looks for the exact same text again after identifying a group it previously matched. Notably, the email regular expression provided does not utilize back references for validation.

### Look-ahead and Look-behind

When using look-ahead or look-behind in regular expressions, there is a specific order in which they must match. However, in the email code provided, this order is not used. Look-ahead allows you to specify patterns that only match based on whether another pattern follows them, while look-behind lets you create patterns that only match when another pattern precedes or follows them. It's important to not that in the email regex mentioned, niether look-ahead or look-behind is employed.

## Author

Get to know me! @
https://github.com/jlonthegrea/
