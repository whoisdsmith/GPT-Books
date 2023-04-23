# Text Manipulation

Text manipulation is the process of changing or modifying the content of a text document. This process is important in many scenarios such as data processing, text analysis, and file parsing. There are several text manipulation techniques that can be used to achieve different goals, which are discussed in detail below.

## String Operations

String operations are used to change the content of a text document by manipulating its characters. Some of the most common string operations include:

* **Concatenation**: Joining two or more strings together to form a new string. For example, `"hello"+"world"` will result in `"helloworld"`.
* **Substring**: Extracting a portion of a string based on its position or length. For example, `"hello world"[0:5]` will result in `"hello"`.
* **Replace**: Replacing a portion of a string with another string. For example, `"hello world".replace("world","python")` will result in `"hello python"`.
* **Split**: Dividing a string into multiple strings based on a separator. For example, `"hello,world".split(",")` will result in `["hello", "world"]`.

## Regular Expressions

Regular expressions are a powerful tool for text manipulation that allows you to search for and match specific patterns in a text document. Regular expressions are comprised of a combination of characters, symbols, and words that define a pattern. Some of the most common regular expression symbols include:

* **Dot (".")**: Matches any character except for a line break.
* **Asterisk ("\*")**: Matches zero or more occurrences of the preceding character.
* **Plus ("+")**: Matches one or more occurrences of the preceding character.
* **Question Mark ("?")**: Matches zero or one occurrence of the preceding character.
* **Pipe ("|")**: Matches either the preceding or the following character.
* **Square Brackets ("\[]")**: Matches any character within the brackets.
* **Parentheses ("()")**: Used to group expressions together.

## Examples

Here are some examples of text manipulation:

*   **Counting Words**: Count the number of words in a text document.

    ```
    text = "Hello, world! This is a sample text document."
    word_count = len(text.split())
    print(word_count)  #Output: 8
    ```
*   **Removing Punctuation**: Remove all punctuation from a text document.

    ```
    import re
    text = "Hello, world! This is a sample text document."
    cleaned_text = re.sub(r'[^\w\s]','',text)
    print(cleaned_text)  #Output: Hello world This is a sample text document
    ```
*   **Extracting Email Addresses**: Extract all email addresses from a text document.

    ```
    import re
    text = "My email is john.doe@example.com and my friend's email is jane.smith@example.com"
    email_addresses = re.findall(r'\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b', text)
    print(email_addresses)  #Output: ['john.doe@example.com', 'jane.smith@example.com']
    ```
*   **Replacing Text**: Replace certain words in a text document with another word.

    ```
    text = "Hello World! This is a sample text document."
    replaced_text = text.replace("Hello", "Hi")
    print(replaced_text)  #Output: Hi World! This is a sample text document.
    ```
