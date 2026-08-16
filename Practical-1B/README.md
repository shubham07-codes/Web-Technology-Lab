# Practical No. 1(B)

## Aim
Study HTML tags and implement a basic web page.

## Problem Definition
To understand commonly used HTML tags and create a simple web page using headings, paragraphs, lists, nested lists, and hyperlinks.

## Theory
HTML stands for HyperText Markup Language. It is used to create and structure web pages. HTML uses different tags to display headings, paragraphs, lists, links, and other content in a browser. The head section contains information about the webpage, while the body section contains the visible content. Tags such as h1, p, ul, ol, li, and a are commonly used in basic webpages. By combining these tags, we can create a simple and organized webpage that can be opened and viewed in a web browser.

## Procedure and Execution

### Steps for Implementation
1. Open a text editor such as VS Code, Notepad, or Sublime Text.
2. Create a new file and save it as index.html.
3. Write the basic HTML document structure using html, head, and body tags.
4. Add headings using h1 and h2 tags.
5. Insert paragraph text using the p tag.
6. Create an unordered list using ul and an ordered list using ol.
7. Add nested lists inside the main list items.
8. Use the li tag to add individual list elements.
9. Add hyperlinks using the a tag.
10. Save the HTML file and open it in a web browser to check the output.

### Code

```html
<!DOCTYPE html>
<html>

<head>
    <title>My First Web Page</title>
</head>

<body>

    <h1>Welcome to My First Web Page</h1>

    <p>Hello! This is my first HTML practical.</p>

    <h2>Things I Am Learning</h2>

    <ul>
        <li>Programming
            <ul>
                <li>C</li>
                <li>C++</li>
                <li>Java</li>
            </ul>
        </li>

        <li>Web Technology
            <ul>
                <li>HTML</li>
                <li>CSS</li>
                <li>JavaScript</li>
            </ul>
        </li>
    </ul>

    <h2>Steps to Learn HTML</h2>

    <ol>
        <li>Learn basic HTML tags</li>
        <li>Practice different tags
            <ol>
                <li>Heading tag</li>
                <li>Paragraph tag</li>
                <li>List tag</li>
            </ol>
        </li>
        <li>Create a simple web page</li>
    </ol>

    <h2>Useful Links</h2>

    <p>
        <a href="https://www.youtube.com">Visit YouTube</a>
    </p>

    <p>
        <a href="https://www.wikipedia.org">Visit Wikipedia</a>
    </p>

</body>

</html>
```

## Output Analysis
The webpage was successfully created and displayed in the web browser. It shows headings, paragraphs, ordered lists, unordered lists, nested lists, and hyperlinks. The YouTube link opens the YouTube website, while the Wikipedia link opens the Wikipedia website. The output demonstrates how basic HTML tags can be combined to create a simple and organized webpage.

## Conclusion
In this practical, I learned the basic structure of an HTML document and how different HTML tags are used to create a simple webpage. I used headings, paragraphs, ordered lists, unordered lists, nested lists, and hyperlinks. I also learned how hyperlinks can be used to open external websites such as YouTube and Wikipedia.
