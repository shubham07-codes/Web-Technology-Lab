# Practical No. 3

## Aim

To develop and demonstrate the usage of inline, internal, and external style sheets using CSS.

## Problem Definition

To understand different methods of applying CSS to an HTML document and demonstrate inline CSS, internal CSS, and external CSS by creating simple web pages.

## Theory

CSS stands for Cascading Style Sheets. It is used to control the appearance and layout of HTML web pages. CSS can change properties such as text color, background color, font size, spacing, borders, and alignment. There are three main ways to apply CSS in HTML. Inline CSS is written directly inside an HTML element using the `style` attribute. Internal CSS is written inside the `<style>` tag in the `<head>` section. External CSS is written in a separate `.css` file and connected to HTML using the `<link>` tag. External CSS is useful when the same design is used on multiple pages.

## Procedure and Execution

### Step for Implementation

1. Open a text editor such as VS Code or Notepad.
2. Create an HTML file and save it as `index.html`.
3. Apply inline CSS using the `style` attribute inside an HTML tag.
4. Add internal CSS using the `<style>` tag inside the `<head>` section.
5. Create a separate file named `style.css` for external CSS.
6. Connect the external CSS file using the `<link>` tag.
7. Add headings, paragraphs, and buttons to the webpage.
8. Apply different styles using all three CSS methods.
9. Save both HTML and CSS files.
10. Open the HTML file in a web browser and observe the output.

### Code

#### HTML File – `index.html`

```html
<!DOCTYPE html>
<html>

<head>
    <title>CSS Example</title>

    <link rel="stylesheet" href="style.css">

    <style>
        h2 {
            color: green;
            text-align: center;
        }

        .internal {
            background-color: lightgray;
            padding: 10px;
        }
    </style>

</head>

<body>

    <h1 style="color: blue;">Inline CSS Example</h1>

    <p style="font-size: 18px;">
        This paragraph is styled using inline CSS.
    </p>

    <h2>Internal CSS Example</h2>

    <p class="internal">
        This paragraph is styled using internal CSS.
    </p>

    <h3>External CSS Example</h3>

    <p class="external">
        This paragraph is styled using external CSS.
    </p>

    <button>Click Me</button>

</body>

</html>
```

#### External CSS File – `style.css`

```css
h3 {
    color: purple;
}

.external {
    background-color: lightyellow;
    font-size: 18px;
}

button {
    background-color: black;
    color: white;
    padding: 8px;
}
```

## Output Analysis

The webpage was successfully displayed in the browser with different CSS styles. The first heading and paragraph were styled using inline CSS. The second heading and paragraph were styled using internal CSS defined inside the `<style>` tag. The third heading, paragraph, and button were styled using the external `style.css` file. This demonstrates that CSS can be applied to HTML using three different methods.

## Conclusion

In this practical, I learned how to use inline, internal, and external CSS in an HTML webpage. Inline CSS is useful for styling a single element, internal CSS can style multiple elements on one page, and external CSS helps maintain the same design across multiple web pages. This practical helped me understand different ways of applying styles to HTML elements.
