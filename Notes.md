**Cascading Style Sheet**:

CSS is the language we use to style a Web page.

**What is CSS?**
1. CSS stands for Cascading Style Sheets
2. CSS describes how HTML elements are to be displayed on screen, paper, or in other media
3. CSS saves a lot of work. It can control the layout of multiple web pages all at once
4. External stylesheets are stored in CSS files

**Why Use CSS??**

CSS is used to define styles for your web pages, including the design, layout and variations in display for different devices and screen sizes.

**Example**:

body {
  background-color: lightblue;
}

h1 {
  color: white;
  text-align: center;
}

p {
  font-family: verdana;
  font-size: 20px;
}

HTML was created to describe the content of a web page, like:

<h1>This is a heading</h1>

<p>This is a paragraph.</p>

When tags like <font>, and color attributes were added to the HTML 3.2 specification, it started a nightmare for web developers. Development of large websites, where fonts and color information were added to every single page, became a long and expensive process.

To solve this problem, the World Wide Web Consortium (W3C) created CSS.

CSS removed the style formatting from the HTML page!


**CSS Syntax**:

h1{
    color:red;
}

This styles text color of all h1 tag to red

h1:selector

color:attribute

red:value

1. The selector points to the HTML element you want to style.
2. The declaration block contains one or more declarations separated by semicolons.
3. Each declaration includes a CSS property name and a value, separated by a colon.
4. Multiple CSS declarations are separated with semicolons, and declaration blocks are surrounded by curly braces.


**Ways To Insert CSS**:

1. **Inline CSS**:

An inline style may be used to apply a unique style for a single element.

To use inline styles, add the style attribute to the relevant element. The style attribute can contain any CSS property.

Ex:

<body>
    <h1 style="color:blue;text-align:center;">This is a heading</h1>
    <p style="color:red;">This is a paragraph.</p>
</body>

2. **Internal CSS**:

    1. An internal style sheet may be used if one single HTML page has a unique style.
    2. The internal style is defined inside the <style> element, inside the head section.

    Example:

    <head>
        <style>

            body {
                background-color: linen;
            }

            h1 {
                color: maroon;
                margin-left: 40px;
            }
        </style>
    </head>


3. **External CSS**:

    1. With an external style sheet, you can change the look of an entire website by changing just one file!
    2. Each HTML page must include a reference to the external style sheet file inside the <link> element,      inside the head section.

    Example:

    <head>
        <link rel="stylesheet" href="mystyle.css">
    </head>

    3. An external style sheet can be written in any text editor, and must be saved with a .css extension.
    4. The external .css file should not contain any HTML tags.

    mystyle.css:

    body {
        background-color: lightblue;
    }

    h1 {
        color: navy;
        margin-left: 20px;
    }


**Cascading Order**:

What style will be used when there is more than one style specified for an HTML element?

So, an inline style has the highest priority, and will override external and internal styles and browser defaults.


