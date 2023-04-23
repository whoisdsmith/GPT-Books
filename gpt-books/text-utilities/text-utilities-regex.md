# Regular Expressions

Regular expressions, known as regex or regexp, are sequences of characters used to match and manipulate patterns in strings. They are a fundamental feature of programming languages, text editors, and command-line utilities, and have become a key tool for data cleaning, validation, and analysis.

## Syntax

The syntax of regular expressions is based on a set of metacharacters that represent classes of characters, repetition, alternation, and grouping. Here are some examples:

* `[a-z]`: matches any lowercase letter between a and z.
* `\d`: matches any digit character.
* `+`: matches one or more repetitions of the previous character or group.
* `|`: matches either the left or the right alternative.
* `( )`: groups expressions together and defines their scope.

## Examples

Let's see some examples of regular expressions in action:

### Matching

Given the string `"Hello world!"`, we can use the following regular expression to match any word starting with the letter H:

```
/H\w*/
```

This expression matches the word `"Hello"` in the string.

### Substitution

We can also use regular expressions to substitute parts of a string. For example, given the string `"John Smith <jsmith@example.com>"`, we can use the following regular expression to extract the email address:

```
/[\w.-]+@[\w.-]+/
```

This expression matches the email address `"jsmith@example.com"`. We can substitute it with the name `"John Smith"` by using the following code in Python:

```
import re

s = "John Smith <jsmith@example.com>"
pattern = re.compile(r"([\w\s]+) <([\w.-]+)>")
result = pattern.sub(r"\1", s)
print(result)
```

This code prints `"John Smith"`.

## Conclusion

Regular expressions are a powerful and flexible tool for working with text data. While their syntax can be complex and cryptic at first, mastering regular expressions can save countless hours of manual processing and manipulation. With practice and experimentation, you can become proficient in using regular expressions to match and manipulate the patterns in string data.
