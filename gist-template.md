# Title (replace with your title)

In this guide, I'll provide an overview of Regular Expressions (Regex). Regex is a powerful tool for pattern matching in text. Here, we'll focus on using regex to match hexadecimal color codes. The regex we'll explore is /^#?([a-f0-9]{6}|[a-f0-9]{3})$/, which matches both 3-digit and 6-digit hexadecimal color codes, optionally preceded by a "#" symbol.

## Summary
Regex, or Regular Expressions, is a powerful tool used in programming and text processing for pattern matching within strings. It allows you to search, match, and manipulate text based on specific patterns. Regex can be used for a variety of tasks, such as validating input formats, extracting substrings, replacing text, and parsing complex text structures.
Regular expressions consist of various components such as anchors, quantifiers, operators, character classes, flags, grouping and capturing, bracket expressions, greedy and lazy matches, boundaries, back-references, and look-ahead and look-behind assertions. This tutorial will cover these essential elements.

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
Regex components are the building blocks of regular expressions, working together to define search patterns. Key components include anchors, character classes, quantifiers, the OR operator, flags, grouping and capturing, bracket expressions, greedy and lazy matches, boundaries, back-references, and look-ahead/look-behind assertions. Each component serves a specific function in pattern matching.

### Anchors
Anchors are special characters that match positions within a string. They are crucial for constructing precise regex patterns. The most common anchors are the caret ^ and the dollar sign $. The caret ^ denotes the start of a string, while the dollar sign $ denotes the end. For example, in the regex /^#?([a-f0-9]{6}|[a-f0-9]{3})$/, the caret ^ and dollar sign $ indicate the beginning and end of the string, respectively.


### Quantifiers
Quantifiers specify how many instances of a character, group, or character class must be present for a match.They frequently include the minimum and maximum number of characters that your regex is looking for. Common quantifiers include:

*: 0 or more times
+: 1 or more times
?: 0 or 1 time
{n}: exactly n times
{n,}: at least n times
{n,m}: between n and m times
For example, the regex /^[a-z0-9_-]{3,16}$/ is looking for any string between 3 and 16 characters that starts and ends with a combination of lowercase characters, the numbers 0–9, and the special characters of an underscore and a hyphen.

### OR Operator
The OR operator (|) allows matching one pattern or another. For instance, the regex #21ECF3|#21F1E2 matches either of the two specified color codes. Similarly, #([A-Fa-f0-9]{3}|[A-Fa-f0-9]{6}) matches hex codes of either 3 or 6 digits.

### Character Classes
Character classes are predefined sets of characters represented with shorthand notations. Common classes include:

\d: any digit (0-9)
\D: any non-digit
\w: any word character (letters, digits, and underscores)
\W: any non-word character
\s: any whitespace character
\S: any non-whitespace character
These notations make regex more concise and readable.

### Flags
Regex flags modify the search behavior. Common flags include:

i: ignore case
g: global search
m: multiline mode
s: dot all (matches newline characters)
u: unicode support
y: sticky mode (matches from the last match position)
For example, the i flag makes regex case-insensitive.

### Grouping and Capturing
Parentheses () are used for grouping and capturing. Grouping treats multiple characters as a single unit, allowing for complex patterns. Capturing saves matched text for later use. For example, ([A-Fa-f0-9]{6}) captures a 6-digit hex code.


### Bracket Expressions
Bracket expressions [ ] match any character inside the brackets. For example, [0-8] matches any digit between 0 and 8.

### Greedy and Lazy Match
Greedy matches (using *) capture as much text as possible, while lazy matches (using *?) capture as little as possible. For example, #([0-9A-Fa-f]{6}).* is greedy, while #([0-9A-Fa-f]{6}).*? is lazy.

### Boundaries
Boundaries include word boundaries (\b), start of string (^), and end of string ($). For instance, \b#[0-9A-Fa-f]{6}\b matches a hex code as a whole word.

### Back-references
Back-references use captured groups for further matching. For example, #([0-9A-Fa-f]{2})\1\1 matches hex codes with repeating characters like #FFFFFF.


### Look-ahead and Look-behind
Look-ahead and look-behind assertions match patterns based on surrounding text. Positive look-ahead ((?=...)) and negative look-ahead ((?!...)) are used for forward assertions. Positive look-behind ((?<=...)) and negative look-behind ((?<!...)) are used for backward assertions. For example, #[0-9A-Fa-f]{6}(?=\s|$) matches a hex code followed by whitespace or end of string, while #[0-9A-Fa-f]{6}(?!\S) ensures it is not followed by a non-whitespace character.

## Author
I am Gaganjit Singh Virdi, Second year Computer science student at Sacramento State Univercity. 
You can find more of my work on my GitHub profile at https://github.com/gaganjitV