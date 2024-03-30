## CSS Cheat Sheet

**Structure:**

* CSS uses selectors to target HTML elements and style them with declarations.
* A declaration consists of a property (e.g., font-size) and a value (e.g., 16px).
* Separated by a colon (:), property-value pairs are enclosed in curly braces ({ }).
* Selectors and declarations are separated by a comma (,).

**Example:**

```
h1 {  /* Targets all h1 elements */
  font-size: 2em;  /* Sets font size to 2 times the parent element's font size */
  color: blue;  /* Sets text color to blue */
}
```

**Common Selectors:**

* **Element Selector:** `h1, p, a` (targets specific elements)
* **Class Selector:** `.important` (targets elements with a specific class)
* **ID Selector:** `#banner` (targets an element with a specific ID)
* **Universal Selector:** `*` (targets all elements)
* **Descendant Selector:** `div p` (styles paragraphs within divs)
* **Pseudo-Classes:** `a:hover` (styles links on hover)

**Common Properties:**

* **Font:** `font-family`, `font-size`, `font-weight`, `color`
* **Text:** `text-align`, `line-height`
* **Background:** `background-color`, `background-image`
* **Borders:** `border-style`, `border-width`, `border-color`
* **Margins & Padding:** `margin`, `padding` (with specific directions like `margin-top`)
* **Dimensions:** `width`, `height`
* **Display:** `display` (control element display type like `display: none` to hide)

**Commonly Included CSS:**

* **Reset Styles:** Often used to normalize default browser styles for a consistent starting point.
* **Typography:** Styles for headings, paragraphs, links, and overall font appearance.
* **Layout:** Defines the overall page structure, margins, and positioning of elements.
* **Colors:** Defines a color palette for text, backgrounds, and borders.
* **Responsiveness:** Uses media queries to adjust styles for different screen sizes.

**Resources:**

* **CSS Cheat Sheet - W3Schools:** [https://www.w3schools.com/css/css_syntax.ASP](https://www.w3schools.com/css/css_syntax.ASP)
* **A Practical CSS Cheat Sheet by Toptal Developers:** [https://www.toptal.com/css](https://www.toptal.com/css)
* **Interactive CSS Cheat Sheet:** [https://www.codecademy.com/resources/cheatsheets/language/html-css](https://www.codecademy.com/resources/cheatsheets/language/html-css)

**Remember:**

* Specificity is important - more specific selectors override less specific ones.
* Use comments (`/* comment here */`) to explain your code.
* There are many more properties and values to explore as you learn more about CSS!
