# Introduction to HTML and CSS layouts

## Topics

1. CSS Box Model
   - Content, padding, border, margin
   - Width and height
1. Flexbox: One-dimensional layout
1. Grid: Two-dimensional layout
1. Responsive Basics
   - Why websites must work on different screens
   - Relative sizing
   - Flexible layouts
   - Media queries

### Learning Goals

- explain what the CSS box model is
- use margin, border, padding, and width
- create simple layouts with Flexbox
- create simple two-dimensional layouts with Grid
- understand the basics of responsive design
- use a simple media query

## Starter HTML

This HTML code is used as a base for lecture examples. To try the examples, create a new directory for this lecture, and add an `index.html` file with the following content:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Layout Basics</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

  <h1>Layout Basics</h1>

  <section class="box-demo">
    <h2>Box Model</h2>
    <div class="box">This is a box.</div>
    <div class="box">This is another box.</div>
  </section>

  <section>
    <h2>Flexbox</h2>
    <div class="flex-container">
      <div class="card">Card 1</div>
      <div class="card">Card 2</div>
      <div class="card">Card 3</div>
    </div>
  </section>

  <section>
    <h2>Grid</h2>
    <div class="grid-container">
      <div class="grid-item">Cell 1</div>
      <div class="grid-item">Cell 2</div>
      <div class="grid-item">Cell 3</div>
      <div class="grid-item">Cell 4</div>
      <div class="grid-item">Cell 5</div>
      <div class="grid-item">Cell 6</div>
    </div>
  </section>

</body>
</html>
```

Add also an empty `styles.css` file to the same directory to add styles for the examples.

## The Box Model

**Every HTML element is a box!**

 ```mermaid
flowchart TB
    subgraph Margin["Margin"]
        style Margin fill:#ffe6e6,stroke:#000,stroke-width:2px,color:#000

        subgraph Border["Border"]
            style Border fill:#fff2cc,stroke:#000,stroke-width:2px,color:#000

            subgraph Padding["Padding"]
                style Padding fill:#e6ffe6,stroke:#000,stroke-width:2px,color:#000

                Content["Content"]
                style Content fill:#e6f0ff,stroke:#000,stroke-width:2px,color:#000
            end
        end
    end

    %% Force text color to black
    classDef default fill:#ffffff,color:#000,stroke:#000;
 ```

- Content: The actual text or image inside the element.
- Padding: Space inside the element, between content and border.
- Border: The visible line around the element.
- Margin: Space outside the element, between this element and others.

Example, add to `styles.css` and try modifying the values:

```css
.box {
  width: 200px;
  padding: 20px;
  border: 4px solid black;
  margin: 20px;
  background-color: lightblue;
}
```

This controls all elements having the class `box` (in this case, the div in the Box Model section). You can change the values to see how they affect the layout.

By default, `width` only controls the content area. So, in the example above, the total width of the box is: 200px + 20px + 4px + 20px = 244px (content + padding + border + margin). If you want the total width to be 200px, including padding and border, you can use `box-sizing: border-box;` which makes the width include padding and border.

You can set this rule for all elements by using the universal selector `*`:

```css
* {
  box-sizing: border-box;
}
```

The `body` element is a box too, and it has default margin (browser default). You can remove it with:

```css
body {
  margin: 0;
}
```

And add any (cascading) styles you want to make your page looking better:

```css
body {
  margin: 0;
  font-family: Arial, sans-serif;
  line-height: 1.5;
  background-color: #f9f9f9;
  color: #333;
  padding: 20px;
} 
```

### Different types of boxes

- Block elements
  - Start on a new line
  - Take full width by default
  - Respect width, height, margin, padding
  - Examples: `<div>`, `<p>`, `<section>`
- Inline elements
  - Stay on the same line
  - Only take as much width as needed
  - Behave differently with spacing
  - Examples: `<span>`, `<a>`, `<strong>`
  - Note: Inline elements are boxes, but: They do NOT behave like block boxes, for inline elements:
    - width and height properties usually do not apply
    - vertical padding and margins do not affect layout (but horizontal do)
- Note: some elements can be both block and inline depending on CSS (e.g., `<img>` is inline by default but can be made block)
- Special case: inline-block (set: `display: inline-block;`) is a hybrid that behaves like inline (stays on the same line) but also respects width and height like block elements.

---

## Flexbox

Flexbox is used for arranging items in one direction:

- either in a row
- or in a column

It is useful for:

- navigation bars
- card rows
- centering content
- spacing items evenly
- aligning items inside a container

### Example of adding flexbox styles to HTML document

First, make a flex container:

```css
.flex-container {
  display: flex;
  gap: 10px;
}
```

This makes the **child elements** flexible and adds some space between them. By default, they will be arranged in a row. If you want to change the direction to column, you can add: `flex-direction: column;`.

With flexbox, you can control how the child elements are aligned and spaced. For example, to center the items horizontally, you can use: `justify-content: center;`. To align items vertically in the center, you can use: `align-items: center;`. Try using different values for these properties to see how they affect the layout.

Next, style the child elements, using the `card` class:

```css
.card {
  padding: 20px;
  background-color: peachpuff;
  border: 1px solid #333;
}
```

Read more about flexbox: <https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox>

---

## Grid

Grid is used for two-dimensional layouts using both rows and columns.

Grid is useful for:

- galleries
- dashboard layouts
- page sections
- card layouts
- larger layout structures

### Example of adding grid styles to HTML document

Add the following styles to make a grid container:

```css
.grid-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 10px;
}
```

- `display: grid` turns the container into a grid
- `grid-template-columns: 1fr 1fr` creates 2 equal columns
- `gap: 10px` adds space between items

Next, add some styling for grid items:

```css
.grid-item {
  padding: 20px;
  background-color: lightgreen;
  border: 1px solid #333;
}
```

Read more about grid: <https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout>.

---

## Responsive Design Basics

A website should work well on different kind of platforms, like desktops, tablets and mobile devices. This is called responsive design.

People use websites on many screen sizes. A layout that looks good on a laptop may break on a phone. Common problems when a site is not designed responsively for smaller screens include:

- Content overflowing the screen
- Text becoming too small to read
- Buttons and links becoming too small to tap
- Layout breaking and elements overlapping
- Images not resizing properly

Mobile screens are the most popular way to access the web today. The common design practice is to design websites with a "mobile-first" approach, which means designing for mobile devices first and then enhancing the layout for larger screens. This ensures that the website is usable and looks good on mobile devices, which are often more challenging to design for due to their smaller screen size.  

### Basic responsive principles

1. Use flexible widths: Avoid giving everything a fixed width, e.g.:
   - Use relative units: Use percentages, ems, rems instead of pixels for sizing.
   - Instead of this: `width: 800px;` use: `width: 100%; max-width: 800px;`
1. Use Flexbox or Grid: These tools help layouts adjust more easily.
1. Make images flexible, this prevents images from overflowing their container:

    ```css
    img {
      max-width: 100%;
      height: auto;
    }
    ```

1. Use media queries, they let you change styles for smaller screens. For example, if the screen is 600px wide or smaller, the cards will stack vertically:

    ```css
    @media (max-width: 600px) {
      .flex-container {
        flex-direction: column;
      }
    }
    ```

    Grid example, for large screen 2 columns and for small screen: 1 column:

    ```css
    .grid-container {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 10px;
    }

    @media (max-width: 600px) {
      .grid-container {
        grid-template-columns: 1fr;
      }
    }
    ```

1. Include viewport meta tag in html `head` to make responsive styles to work correctly on mobile devices: `<meta name="viewport" content="width=device-width, initial-scale=1.0">`

### Note about CSS units

Simple rules for beginners:

- Use `px` for precise sizes when you want fixed, exact control. Good for:
  - borders
  - small spacing
  - shadows
  - fine adjustments
- Use relative units (`%`, `rem`, `em`) for layout and text
  - `%` (percentage, e.g. `width: 100%;`) is based on parent element size and is good for example:
    - layouts
    - containers
    - images
  - `rem` is based on root font size (e.g. `font-size: 1.2rem;`) and predictable
  - `em` is based on parent element font size and can be more confusing because it stacks

---

<!-- add mermaid support for gh pages -->
<script type="module">
    Array.from(document.getElementsByClassName("language-mermaid")).forEach(element => {
      element.classList.add("mermaid");
    });
    import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@11/dist/mermaid.esm.min.mjs';
    mermaid.initialize({startOnLoad: true});
</script>