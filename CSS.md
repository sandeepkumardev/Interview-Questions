<div align="center">
  <img height="60" src="https://img.icons8.com/ultraviolet/80/000000/css--v2.png"/>
  <h1>CSS Questions</h1>
  
  From basic to advanced: test how well you know CSS, refresh your knowledge a bit, or prepare for your coding interview! 💪 🚀
</div>
  
###### 1. What is CSS and what is its purpose?

<details><summary><b>Answer</b></summary>

CSS, or Cascading Style Sheets, is a stylesheet language used for describing the look, formatting, and layout of documents written in HTML (Hypertext Markup Language) or XML (Extensible Markup Language). Its primary purpose is to separate the presentation and design of a web page from its content, making it easier to maintain, update and modify the visual appearance of a website.

The main benefits of CSS include:

- Consistency: By using a single CSS file to control the styles for multiple pages, you can create a consistent look and feel across an entire website.
- Efficiency: CSS reduces code duplication and makes it easier to manage and update styles. This leads to faster page-load times and lower bandwidth usage.
- Modularity: With CSS, you can break courses down into modules that can be easily reused, combined, and updated independently of each other.
- Accessibility: CSS helps create accessible web pages by allowing developers to apply specific styles for different types of devices or user preferences.
- Flexibility: CSS offers a wide range of styling properties and techniques that can be used to achieve various effects, catering to diverse design requirements.

</details>

###### 2. What are the different ways to include CSS in a web page?

<details><summary><b>Answer</b></summary>
There are three main ways to include CSS in a web page:

- Inline CSS: Adding the style directly to an HTML element using the "style" attribute.
- Internal CSS: Placing the CSS code within the < style > tags in the < head > section of an HTML document.
- External CSS: Linking an external CSS file to the HTML document using the < link > tag in the < head > section.
</details>

###### 3. How do you select an element with a specific class in CSS?

<details><summary><b>Answer</b></summary>
To select an element with a specific class in CSS, you use the dot (.) followed by the class name. For example, to select all elements with the class "example-class", the CSS selector would be ".example-class".
</details>

###### 4. What is the box model in CSS?

<details><summary><b>Answer</b></summary>
The Box Model in CSS refers to the concept that organizes and structures HTML elements on a web page in the form of rectangular boxes. Every element in a page is comprised of a rectangular box, which includes content, padding, border, and margin. These components contribute collectively to the element's dimensions and positioning.

- Content: The actual text or images inside the element.
- Padding: The space between the content and the border, working as a cushion around the content.
- Border: The line enclosing the padding and content, which visually defines the boundaries of the element.
- Margin: The space surrounding the border, which helps to space out elements from each other and other sections of the page.

Together, these elements determine the total dimensions and layout of an HTML element on a web page. The Box Model is crucial for controlling the placement and appearance of content when designing a web page using Cascading Style Sheets (CSS).

</details>

###### 5. How do you center an element horizontally in CSS?

<details><summary><b>Answer</b></summary>
To center an element horizontally in CSS, you can use one of the following methods:

- Set the left and right margins to "auto" and specify a width for the element.
- Use the flexbox layout by setting the parent container's "display" property to "flex" and using the "justify-content" property with a value of "center".
</details>

###### 6. How do you change the background color of an element in CSS?

<details><summary><b>Answer</b></summary>
To change the background color of an element in CSS, you use the background-color property and set it to the desired color. You can use color names, hexadecimal values, RGB, or HSL values as the color value. Here's an example of how to set the background color of an element with a class name "example":

```css
.example {
  background-color: red; /* color name */
  /* or */
  background-color: #ff0000; /* hexadecimal value */
  /* or */
  background-color: rgb(255, 0, 0); /* RGB value */
  /* or */
  background-color: hsl(0, 100%, 50%); /* HSL value */
}
```

Apply the class to an HTML element:

```html
<div class="example">This element's background color is red.</div>
```

</details>

###### 7. What is the difference between padding and margin in CSS?

<details><summary><b>Answer</b></summary>
In CSS, padding and margin are properties that control the space around an element, but they serve different purposes:

- Padding: This property defines the space between the content of an element and its border. It is usually used to create extra space around the content inside an element. Padding is included within the background color or background image of the element and holds the border outside the actual content.
- Margin: This property defines the space around the outside of an element, between the element and its surrounding elements. It is used for creating space between elements, and it is transparent. Margin is situated outside the border, so if an element has a background color or image, it won't influence the margin.
</details>

###### 8. How do you add a border to an element in CSS?

<details><summary><b>Answer</b></summary>
To add a border to an element in CSS, you need to set the border property, which is a shorthand for three individual properties: border-width, border-style, and border-color. You can specify all three properties in a single declaration or set them individually.

Here's an example of how to add a border using the shorthand property:

```css
.box {
  border: 2px solid red; /* border-width, border-style, and border-color */
}
```

Or you can set the properties individually:

```css
.box {
  border-width: 2px;
  border-style: solid;
  border-color: red;
}
```

Both of these examples will result in a red, solid border with a width of 2 pixels around an element. To apply the style, add the class to an HTML element:

```html
<div class="box">This element has a solid red border of 2 pixels width.</div>
```

The border property allows you to style borders with different widths, styles (e.g., solid, dashed, dotted, etc.), and colors. You can also control the border for individual sides (top, right, bottom, and left) using specific properties like border-top, border-right, border-bottom, and border-left.

</details>

###### 9. What is the difference between inline and block-level elements in CSS?

<details><summary><b>Answer</b></summary>
In CSS, elements can be categorized as either inline or block-level based on their default display behavior within the HTML document. Here are the key differences:

<img src="https://d2mk45aasx86xg.cloudfront.net/Difference_between_inline_and_block_elements_c995170809.jpg" >
</details>

###### 10. How do you apply CSS styles to only the first letter of a paragraph?

<details><summary><b>Answer</b></summary>
To apply CSS styles to only the first letter of a paragraph, you can use the ::first-letter pseudo-element. It allows you to target and style the first letter of a text element without altering the HTML structure. Here's an example:

```css
p::first-letter {
  font-size: 2em;
  font-weight: bold;
  color: blue;
}
```

In this example, the first letter of every < p > (paragraph) element will be styled with a larger font size (2 times the normal font size), bold font-weight, and blue color.

</details>
