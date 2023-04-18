# A Tutorial on the Regular Expression for Matching Email Addresses

Regular expressions or regexes match patterns in text. It's like a set of rules that you can use to search for specific patterns in a block of text. This can be helpful when you want to find something specific in a chunk of text such as an email address. In this tutorial, I will explain a regular expression that can be used to match email addresses. 

## Summary

The regular expression we will be explaining is:
^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$
You can use this set of special characters, called a regular expression, to find email addresses that look similar to most other email addresses. The regular expression has different parts that help it recognize certain patterns in the text, like the "@" symbol and the ".com" at the end. By putting these parts together in a certain way, the regular expression can match many different types of email addresses that follow a common format.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)

## Regex Components

### Anchors
This pattern I am using for matching has special characters called ^ and $, which act as markers that show where the text should begin and end. With this regex, I can make sure that I match the entire string, not just part of it. It's important because I want to make sure I am only matching strings that completely fit the pattern I am looking for.
### Quantifiers
The symbols + and {2,} are like counters that determine how many times the preceding character or group should occur in the text. In this regular expression, they help ensure that there are at least one or more characters before the @ symbol, and two or more characters after the last dot in the email address.

### Character Classes
This regular expression uses character classes, which are sets of characters that can match any character within that set. The [a-zA-Z0-9._%+-] character class matches any letter (upper or lower case), number, or special character in the brackets, including the dot (.), plus (+), and percent (%) symbols. These symbols are used in email addresses, so they are included in the character class to allow for matching them. The second character class, [a-zA-Z0-9.-], matches letters, numbers, and the dash (-) symbol, as it is commonly used in domain names.

### Grouping and Capturing
The parentheses () are a special symbol used in regular expressions for grouping and capturing. In this specific regular expression, they group together the domain name and top-level domain (TLD). This grouping allows the quantifier to apply to both parts of the domain name, ensuring that there are at least two characters after the final dot. By doing this, we can match email addresses with domain names that have a minimum length of two characters after the dot.

### Greedy and Lazy Match
In this regex, we are using greedy matching by default.

### Boundaries
In regular expressions, boundaries are special characters that allow us to match specific positions in the text. For example, we can match the beginning or end of a word. In this particular regex, we are using the ^ and $ anchors as boundaries to match the start and end of the email address string.

## Author

I am a Software Development Certification student at the UW. You can find my Github profile at [https://github.com/silvam22?tab=repositories]