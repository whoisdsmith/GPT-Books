# JSON

JSON stands for JavaScript Object Notation which is a lightweight format for exchanging data. It is commonly used for transmitting data between a server and a web application, as an alternative to XML. JSON is easy to read and write, and it is almost like writing regular JavaScript objects.

## Syntax

JSON has a simple syntax, and it is written in key-value pairs, where the keys are strings, and the values can be any valid JSON data types such as string, number, boolean, null, array or another JSON object.

```
{
  "name": "John",
  "age": 30,
  "isAdmin": true,
  "hobbies": ["reading", "drawing", "coding"],
  "address": {
    "street": "123 Main St",
    "city": "Anytown",
    "state": "CA",
    "zip": "12345"
  }
}
```

## JSON data types

JSON supports the following data types:

- **String:** A sequence of characters, wrapped in double quotes.

```
{
  "name": "John Doe"
}
```

- **Number:** A numeric value, which can be integer, float or exponential.

```
{
  "age": 30,
  "score": 91.5,
  "e": 3.141e10
}
```

- **Boolean:** A value which can be either true or false.

```
{
  "isAdmin": true,
  "isActive": false
}
```

- **Null:** A value which represents null or empty.

```
{
  "middleName": null,
  "phone": ""
}
```

- **Array:** A collection of values, enclosed in square brackets and separated by commas.

```
{
  "hobbies": ["reading", "drawing", "coding"]
}
```

- **Object:** A collection of key-value pairs, enclosed in curly braces and separated by commas.

```
{
  "address": {
    "street": "123 Main St",
    "city": "Anytown",
    "state": "CA",
    "zip": "12345"
  }
}
```

## Parsing JSON

In JavaScript, JSON can be parsed into a JavaScript object using the `JSON.parse()` method:

```
const json = '{"name":"John","age":30,"isAdmin":true}';
const obj = JSON.parse(json);
console.log(obj.name); // Output: John
```

## Converting to JSON

In JavaScript, an object can be converted into a JSON string using the `JSON.stringify()` method:

```
const obj = { name: "John", age: 30, isAdmin: true };
const json = JSON.stringify(obj);
console.log(json); // Output: {"name":"John","age":30,"isAdmin":true}
```

## Conclusion

JSON is a lightweight, easy-to-read and easy-to-write data format, and it is widely used in web applications. It supports various data types, and it can be easily parsed and converted to other data formats.
