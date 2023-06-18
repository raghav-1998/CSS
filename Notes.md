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

1. So, an inline style has the highest priority, and will override external and internal styles and browser defaults.

**Note:** If we want to apply Internal CSS over inline during conflict, then mark **!important** with 
the property in Internal CSS

2. Resolution of Conflict b/w the Internal & External CSS property depends upon whether style tag comes first or link:
    1. If style tag comes first, then value in internal CSS will dsiplay
    2. Otherwise, value in external CSS will display..


**CSS Selectors:**

A CSS selector selects(or find) the HTML element(s) you want to style.

We can divide CSS selectors into five categories:

1. Simple selectors (select elements based on name, id, class)
2. Combinator selectors (select elements based on a specific relationship between them)
3. Pseudo-class selectors (select elements based on a certain state)
4. Pseudo-elements selectors (select and style a part of an element)
5. Attribute selectors (select elements based on an attribute or attribute value)

1. Simple Selectors:

    1. **The CSS element Selector**:

        The element selector selects HTML elements based on the element name.

        Example:

        p {
            text-align: center;
            color: red;
        }

    2. **The CSS id Selector**:

        1. The id selector uses the id attribute of an HTML element to select a specific element.
        2. The id of an element is unique within a page, so the id selector is used to select one unique element!
        3. To select an element with a specific id, write a hash (#) character, followed by the id of the      element.

            Example:
            The CSS rule below will be applied to the HTML element with id="para1": 

            #para1 {
                
                text-align: center;
                color: red;

            }

    3. **The CSS class Selector**:

        1. The class selector selects HTML elements with a specific class attribute.
        2. To select elements with a specific class, write a period (.) character, followed by the class name.

            Example:
            Style all the HTML elements of class center

            .center {

                text-align: center;
                color: red;

            }

        3. You can also specify that only specific HTML elements should be affected by a class.

            Example:
            Style all the p elements of class center

            p.center {

                text-align: center;
                color: red;

            }

    4. **The CSS Grouping Selector**:

        The grouping selector selects all the HTML elements with the same style definitions.

        Example:
        h1,h2 & p will style in same manner

        h1, h2, p {

            text-align: center;
            color: red;

        }


**CSS Colors:**

Colors are specified using predefined color names, or RGB, HEX, HSL, RGBA, HSLA values.

1. **CSS Background Color:**

You can set the background color for HTML elements:

<h1 style="background-color:DodgerBlue;">Hello World</h1>
<p style="background-color:Tomato;">Lorem ipsum...</p>


2. **CSS Text Color:**

You can set the color of text:

<h1 style="color:Tomato;">Hello World</h1>
<p style="color:DodgerBlue;">Lorem ipsum...</p>
<p style="color:MediumSeaGreen;">Ut wisi enim...</p>


**CSS RGB Colors:**

An RGB color value represents RED, GREEN, and BLUE light sources.

1. **RGB color:**

In CSS, a color can be specified as an RGB value, using this formula:

rgb(red, green, blue)

Each parameter (red, green, and blue) defines the intensity of the color between 0 and 255.

For example, rgb(255, 0, 0) is displayed as red, because red is set to its highest value (255) and the others are set to 0.

To display black, set all color parameters to 0, like this: rgb(0, 0, 0).

To display white, set all color parameters to 255, like this: rgb(255, 255, 255).

2. **RGBA color:**

RGBA color values are an extension of RGB color values with an alpha channel - which specifies the opacity for a color.

An RGBA color value is specified with:

rgba(red, green, blue, alpha)

The alpha parameter is a number between 0.0 (fully transparent) and 1.0 (not transparent at all)..

**CSS Borders:**

- **CSS Border Types:**

    The border-style property specifies what kind of border to display.

    The following values are allowed:

    1. dotted - Defines a dotted border
    2. dashed - Defines a dashed border
    3. solid - Defines a solid border
    4. double - Defines a double border
    5. groove - Defines a 3D grooved border. The effect depends on the border-color value
    6. ridge - Defines a 3D ridged border. The effect depends on the border-color value
    7. inset - Defines a 3D inset border. The effect depends on the border-color value
    8. outset - Defines a 3D outset border. The effect depends on the border-color value
    9. none - Defines no border
    10. hidden - Defines a hidden border
    
    The border-style property can have from one to four values (for the top border, right border, bottom border, and the left border).

- **CSS Border Color:**

    The border-color property is used to set the color of the four borders.

    Ex:

    p{

        border-style: solid;
        border-color: red;

    }

    **Specific Side Colors:**

    The border-color property can have from one to four values (for the top border, right border, bottom border, and the left border). 

    Ex:

    p{

        border-style: solid;
        border-color: red green blue yellow; /* red top, green right, blue bottom and yellow left */

    }

- **Border Sides:**

    From previous examples, it is possible to assign different value of a border property for different side.

    p {
        border-style: dotted solid double dashed; 
    }

    In above example 1st value(dotted) belongs to top, 2nd value(solid) belongs to right, 3rd value(double) belongs to bottom, 4th value(dashed) belongs to left

    /* Three values */ 
    p {
        border-style: dotted solid double;
    }

    In above example 1st value(dotted) belongs to top, 2nd value(solid) belongs to right & left, 3rd value(double) belongs to bottom

    /* Two values */
    p {
        border-style: dotted solid;
    }

    In above example 1st value(dotted) belongs to top & bottom, 2nd value(solid) belongs to right & left

    /* One value */
    p {
        border-style: dotted;
    }

    In above example, all sides display dotted border.


- **CSS Rounded Borders:**

    The border-radius property is used to add rounded borders to an element:

    Ex:
    
    p{

        border-radius:5px;

    }


**CSS Padding:**

Padding is used to create space around an element's content, inside of any defined borders.

The CSS padding properties are used to generate space around an element's content, inside of any defined borders.

- **Padding - Individual Sides:**

    CSS has properties for specifying the padding for each side of an element:

    1. padding-top
    2. padding-right
    3. padding-bottom
    4. padding-left

    Ex:

    div {

        padding-top: 50px;
        padding-right: 30px;
        padding-bottom: 50px;
        padding-left: 80px;

    }

- **Padding Shorthand Properties:**

    1. 1st Case;

        div {

            padding: 25px 50px 75px 100px;

        }

        1. top padding is 25px
        2. right padding is 50px
        3. bottom padding is 75px
        4. left padding is 100px

    2. 2nd Case:

        div {

            padding: 25px 50px 75px;

        }

        1. top padding is 25px
        2. right and left paddings are 50px
        3. bottom padding is 75px

    3. 3rd Case:

        div {

            padding: 25px 50px;

        }

        1. top and bottom paddings are 25px
        2. right and left paddings are 50px

    4. 4th Case:

        div {

            padding: 25px;

        }

        - all four paddings are 25px


**Padding and Element Width:**

div {

  width: 300px;
  
  padding: 25px;

}

The CSS width property specifies the width of the element's content area. The content area is the portion inside the padding, border, and margin of an element (the box model).

So, if an element has a specified width, the padding added to that element will be added to the total width of the element.

Here, the div element is given a width of 300px. However, the actual width of the div element will be 350px (300px + 25px of left padding + 25px of right padding)

To keep the width at 300px, no matter the amount of padding, you can use the box-sizing property. This causes the element to maintain its actual width; if you increase the padding, the available content space will decrease.

div {

  width: 300px;

  padding: 25px;

  box-sizing: border-box;

}
