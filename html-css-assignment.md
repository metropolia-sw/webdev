# Assignment 1: HTML + CSS Company website

**Make your version of [the provided layout](assets/assignment-1-layout.pdf). Note: multiple pages!**

- In the provided layout you'll find the plans for three pages: Home, Products and Contact.
- Your task is to make a simple website using the provided layout.
- The result does not have to be pixel-perfect. It's enough that the visual structure is close to the provided layout.
- You can have the three pages in one document, or you can put each page into its own document.
- You should make up your own color palette and choose a font (or fonts) for your version.
- Also add your own images to the page(s).
- You can use [lorem ipsum](https://en.wikipedia.org/wiki/Lorem_ipsum) as text content. Any text will do.
  - [lipsum generator](https://www.lipsum.com/)
- You don't have to consider copyrights, since this is an educational assignment.
- More detailed description in the video provided in Oma.
- Web page(s) don't need to be responsive in this assignment, but in the second assignment you will make a responsive website, so you can start thinking about how to make the layout responsive already now.

### How to submit

In Oma, provide a `clickable` link to the folder where your assignment is. Also provide a `clickable` link to the html document where you have the screenshots and the css example of your font. See the [video](https://www.youtube.com/watch?v=u7mjd5Vi6lk&list=PLKenVLUxjmH-y89AiiI2xcXDy5QG83D4K&index=6) for details.

Example submission:

[Site](https://users.metropolia.fi/~username/foldername)

[Screenshots](https://users.metropolia.fi/~username/foldername/screenshots.html)

### Evaluation

Evaluation will be done on scale **pass/fail**. The assignment is considered passed if the following requirements are mostly met:

- Your version resembles the provided layout.
- CSS is in use
- Navigation works
- Images are visible on page
- Contrast check is passed
  - _UPDATE_: https://color.a11y.com/Contrast/ is no longer available. Use https://wave.webaim.org/ instead. [Example screenshot here](assets/wave.png).
  - Contrast errors needs to be 0. Other items are checked with validation and Lighthouse below.
- Validation is passed
  - No errors
  - Warnings, like no heading in `<article>` or `<section>` etc. are allowed
- Lighthouse check score must be at least 90 or 3/4 or 4/5 depending on the Browser
  - Update: If you use `<iframe>` to add Google map, Lighthouse will deduct points. That will not affect evaluation. you should however consider just using an image of the map.
- Do not use the default font (Times New Roman)
- Enough padding is used (text not too close to edges or other elements)

**Note! Test your assignment on a different computer to make sure all files are loaded!**

Screenshot page example html:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Results</title>
  </head>
  <body>
    <h2>Font</h2>
    <p>
      Font is from
      <a href="https://fonts.google.com/specimen/Whatever"
        >Google Fonts. Name: Whatever</a
      >
    </p>
    <pre>
    @font-face {
      font-family: whatEver;
      src: url(sansation_light.woff) format(woff);
    }

    body {
       font-family: whatEver;
    }
</pre
    >
    <h2>Validation</h2>
    <p>
      <img src="img/validator.png" alt="valid" />
    </p>
    <h2>Lighthouse</h2>
    <p>
      <img src="img/lighthouse.png" alt="lighthouse" />
    </p>
    <h2>Contrast</h2>
    <p>
      <img src="img/contrast.png" alt="contrast" />
    </p>
  </body>
</html>
```
