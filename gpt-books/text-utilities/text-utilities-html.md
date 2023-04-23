# HTML

HTML stands for Hypertext Markup Language, which is the standard markup language used to create web pages. HTML provides the basic structure of sites and web applications, while Cascading Style Sheets (CSS) and JavaScript are used to enhance the appearance and functionality of those web pages.

## Basic Structure of HTML

HTML is composed of elements, which are identified by tags. A tag is enclosed in angle brackets, like this:

```
<tagname>content</tagname>
```

An HTML element usually consists of a start tag and an end tag, with the content between them. For example, the basic structure of an HTML document looks like this:

```
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <h1>This is a Heading</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```

Let's break down the components of this HTML document:

* The `<!DOCTYPE html>` declaration defines this document to be HTML5.
* The `<html>` element is the root element of an HTML page.
* The `<head>` element contains meta information about the HTML document, such as the title of the page.
* The `<title>` element specifies a title for the HTML document, which is displayed in the browser's title bar or tab.
* The `<body>` element defines the document's body, which is where we put all the content that we want to display on the web page.
* The `<h1>` element defines a large heading, and the `<p>` element defines a paragraph.

## HTML Tags

HTML tags are used to create the structure and content of a web page. Here are some common HTML tags:

* `<a>`: defines a hyperlink to another web page or location.
* `<img>`: displays an image on the web page.
* `<ul>`: defines an unordered list.
* `<ol>`: defines an ordered list.
* `<table>`: defines a table.
* `<form>`: defines a form for user input.

## HTML Attributes

HTML attributes are used to provide additional information about an HTML element. Here are some common HTML attributes:

* `src`: specifies the URL of an image to be displayed with the `<img>` tag.
* `href`: specifies the URL of the page to be linked with the `<a>` tag.
* `alt`: provides alternative text for an image, in case it cannot be displayed.
* `class`: specifies one or more class names for an element, which can be used with CSS to style the element.
* `id`: specifies a unique identifier for an element, which can be used to target the element with JavaScript or CSS.

## Example

Here's an example of an HTML code that uses tags and attributes to create a simple web page:

```
<!DOCTYPE html>
<html>
  <head>
    <title>My Website</title>
    <style>
      .red-text {
        color: red;
      }
    </style>
  </head>
  <body>
    <h1>Welcome to My Website</h1>
    <img src="my-image.png" alt="My Image">
    <p>This is my <a href="http://example.com">website</a>.</p>
    <ul>
      <li>List Item 1</li>
      <li>List Item 2</li>
    </ul>
    <table>
      <tr>
        <th>Name</th>
        <th>Age</th>
      </tr>
      <tr>
        <td>John Doe</td>
        <td>35</td>
      </tr>
      <tr>
        <td>Jane Smith</td>
        <td>28</td>
      </tr>
    </table>
    <form>
      <label>Name:</label>
      <input type="text" name="name"><br>
      <label>Email:</label>
      <input type="email" name="email"><br>
      <input type="submit" value="Submit">
    </form>
    <p class="red-text">This text is red.</p>
    <p id="my-paragraph">This is my paragraph.</p>
  </body>
</html>
```

In this example, we've used various HTML elements and attributes to display text, images, lists, tables, and forms. We've also used CSS to style the text and provide a red color to a specific paragraph using the `.red-text` class. Finally, we've given the paragraph with the text "This is my paragraph." an `id` attribute of `my-paragraph`, which can be used to target that paragraph with JavaScript or CSS.
