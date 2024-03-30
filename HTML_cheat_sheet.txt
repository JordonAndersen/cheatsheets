## Basic HTML Page Cheat Sheet

**Getting Started:**

* **Text Editor:**  Use a simple text editor like Notepad (Windows) or TextEdit (Mac) to write your HTML code. Avoid using word processors that add extra formatting.

**Building the Structure:**

1. **Document Declaration:**  Start your code with `<!DOCTYPE html>` which tells the browser you're using HTML5.
2. **HTML Root:**  Create the main container with `<html>` and `</html>` tags.
3. **Head Section:**  Enclose information about the page (not displayed) using `<head>` and `</head>` tags. Here you can add:
   - **Page Title:** `<title>Your Page Title Here</title>` 
   - **Character Encoding:** `<meta charset="UTF-8">` (for proper text display)
   - **Link to External CSS:**  Use `<link rel="stylesheet" href="style.css">`  to link a separate CSS file for styling your page. Replace "style.css" with your actual filename.
4. **Body Section:**  Everything the user sees goes between `<body>` and `</body>` tags. This is where you add content and structure.

**Common Element Types:**

* **Headings:**  Use `<h1>` (largest) to `<h6>` (smallest) tags to create headings and subheadings.
* **Paragraphs:**  Define paragraphs with `<p>` and `</p>` tags. 
* **Links:**  Create links to other pages or websites with `<a href="URL">Link Text</a>`. Replace "URL" with the actual web address.
* **Images:**  Insert images using `<img src="image.jpg" alt="Image Description">`. Replace "image.jpg" with your image file name and add a description in the "alt" attribute.
* **Lists:**  Create ordered lists with `<ol>` and `</ol>` tags, and unordered lists with `<ul>` and `</ul>` tags. Use `<li>` for each list item.
* **Bold and Italics:**  Make text bold with `<strong>` and `</strong>` or `<b>` and `</b>` tags. Italicize with `<em>` and `</em>` or `<i>` and `</i>` tags.

**Linking External Files:**

* **CSS:** Link a CSS file in the `<head>` section using `<link rel="stylesheet" href="style.css">`. 
* **JavaScript:** You can link JavaScript in two ways:
    - **In the `<head>`:**  `<script src="script.js"></script>` to load the script before the page content.
    - **Before the `</body>` tag:**  `<script src="script.js"></script>`  to load the script after the content has loaded (often preferred).

**Snippet Example:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My Basic Page</title>
  <link rel="stylesheet" href="style.css">  </head>
<body>
  <h1>Welcome to My Page!</h1>
  <p>This is a basic HTML page with some content.</p>
  <a href="https://www.example.com">Visit an Example Site</a>
  <img src="banner.jpg" alt="Banner Image">
  <script src="script.js"></script>  </body>
</html>
```

**Resources:**

* **W3Schools HTML Tutorial:** [https://www.w3schools.com/html/](https://www.w3schools.com/html/) 
* **HTML Dog Tutorial:** [https://www.htmldog.com/guides/html/beginner/](https://www.htmldog.com/guides/html/beginner/)
* **Codecademy Learn HTML:** [https://www.codecademy.com/catalog/language/html-css](https://www.codecademy.com/catalog/language/html-css) 

**Remember:**

*  Always close your tags properly (e.g., `<h1>` needs a `</h1>`).
*  Indent your code for better readability.
*  There are many more HTML elements to explore as you learn more!
*  Separate CSS and JavaScript files keep your HTML code cleaner and easier to maintain.