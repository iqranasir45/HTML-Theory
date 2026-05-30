# HTML Theoretical Questions

## Question 0: What is HTML and what is the difference between HTML and HTML5?

## Answer:
HTML stands for Hyper Text Markup Language. It is the standard language used to create web pages. It uses elements like headings, paragraphs, images, links, and tables to create a webpage's structure.

### Difference between HTML and HTML5:
- HTML is the older version mainly used to structure the web page content.
- HTML5 is the latest and improved version of HTML with new features.
- HTML doesn't support multimedia tags like `<video>` and `<audio>` without the plugins. On the other hand, HTML5 has the built-in multimedia tags.
- HTML5 has the new semantic tags like `<header>`, `<nav>`, `<article>`, `<footer>`, and `<section>` instead of just `<div>` and `<span>` tags, which makes it easier to organize and understand the web pages.
- The initial line in old HTML was long and difficult. HTML5 made it short and simple:
`<!DOCTYPE html>`
- HTML only uses cookies to store temporary data. HTML5 uses SQL databases and application cache to store offline data.

#### HTML Layout (Non-Semantic Tags):

| Header |
|---------|
| `div id="header"` |

| Sidebar | Content |
|----------|----------|
| `div id="sidebar"` | `div class="post"` |
| | `div class="post"` |

| Footer |
|---------|
| `div id="footer"` |

#### HTML5 Layout (Semantic Tags):

| Header |
|---------|
| `<header>` |

| Navigation | Content |
|------------|----------|
| `<nav>` | `<article>` |
| | `<article>` |

| Footer |
|---------|
| `<footer>` |


## Question 1: What are semantic HTML tags? Why are they important in web development?

## Answer:
Semantic HTML tags clearly describe the meaning and purpose of their content, making the webpage's structure easy for developers and browsers to understand. 
Examples of semantic tags are:
- `<header>` : Top section of page include logo, nav, banner etc.
- `<nav>` : Navigation links
- `<main>` : Main content of the page
- `<section>` : Grouped section of content
- `<figure>` : Image + caption content
- `<article>` : A self-contained piece of content (like blog post)
- `<aside>` : Side content (like a sidebar)
- `<footer>` : Bottom section of a page

### Importance:
- It provides better readability. Developers can easily identify different sections of webpage content. For example, when you see the `<nav>` tag, you can easily understand that this section is of navigation links.
- It makes maintenance easier because the well-structured code is easier to modify, debug and maintain.
- Search engines can easily understand the structure and content of webpage. which helps in higher ranking of website.

## Question 2: What is the difference between `<div>` and `<span>` tags?

## Answer:
- `<div>` is block-level element and `<span>` is an inline element.
- `<div>` occupy the whole available width and on the other side `<span>` just used the required width.
- `<div>` used to organize and group large blocks of content and on the other side `<span>` is used to style and group small blocks of content within the line.
- `<div>` starts on a new line and on the other side `<span>` remains to the same line.
- `<div>` used to create layouts, and divide the page sections and on the other side `<span>` is used to style specific words and parts of the text.

### Examples: 

#### Use of `<div>`:
`<div style="background-color: pink;">This is a section</div>`
`<div style="background-color: blue; color: white;">It starts a new line</div>`

#### Output: 
<div style="background-color: pink;">This is a section</div>
<div style="background-color: blue; color: white;">It starts a new line</div>

#### Use of `<span>`:
`<p>This is a <span style="color:red;">red</span> word. This is a paragraph with <span>span</span>, it doesn't starts on a new line.</p>`

#### Output: 
<p>This is a <span style="color:red;">red</span> word. This is a paragraph with <span>span</span>, it doesn't starts on a new line.</p>

## Question 3: Explain the difference between block-level elements and inline elements.

## Answer: 
### Block-level Elements:
Block-level elements always start on a new line. They take the whole available width and browser automatically add some space (padding/margin) before, after or within the element. We can set the width and height of the block-level elemnts with the help of CSS.
Block-level elements are `<div>`, `<p>`, `<h1>` to `<h6>`, `<section>`, and `<article>` etc.

#### Usage Example of block-level elements:
`<p>This is a paragraph</p>`
`<h1>This is heading</h1>`
`<div>This is a div section</div>`
`<article>This is a blog post</article>`

#### Output:
<p>This is a paragraph</p>
<h1>This is heading</h1>
<div>This is a div section</div>
<article>This is a blog post</article>

### Inline Elements:
Inline Elements do not start on the new line. They take the only required width and they sit next to each other. They contain only horizontal margins, vertical margins don't affect the content. We can't set their width and height with CSS, they are ignored by default.
Inline elements are `<span>`, `<br>`, `<b>`, `<a>`, `<em>`, and `<strong>` etc.

#### Usage Example of Inline elements:
`<p>Lorem Ipsum is simply <span>dummy text</span> of the printing and typesetting industry. <em>Lorem Ipsum</em> has been the industry's standard dummy text ever since 1966, when designers at Letraset and James Mosley, the librarian at St <b>Bride Printing Library</b>, took a 1914 Cicero translation and scrambled it to make dummy text for Letraset's Body Type sheets.</p>`

#### Output:
<p>Lorem Ipsum is simply <span>dummy text</span> of the printing and typesetting industry. <em>Lorem Ipsum</em> has been the industry's standard dummy text ever since 1966, when designers at Letraset and James Mosley, the librarian at St <b>Bride Printing Library</b>, took a 1914 Cicero translation and scrambled it to make dummy text for Letraset's Body Type sheets.</p>

## Question 4: What is the purpose of the DOCTYPE declaration in HTML?

## Answer: 
All HTML documents starts with a `<!DOCTYPE html>` declaration. It is not an HTML tag, it is an instruction for the browser to tell in which version of HTML the page is written. Without it, the browser enters Quirks Mode, which may cause the page to appear inaccurately. CSS margins, padding, and widths may not work correctly wihout the DOCTYPE declaration. It ensures the consistency and informs the browser to render the website using new web standards instead of the old, outdated functionality. 

### Example of DOCTYPE declaration:

```
<!DOCTYPE html>
<html>
  <head>
    <title>My Page</title>
  </head>
  <body>
    Hello World
  </body>
</html>
```

## Question 5: What is the difference between id and class attributes?

## Answer:
The main difference between id and class is that `id` is unique; only one element can have it on a page. On the other hand, `class` can be reused by many elements on a page. `id` has a higher priority; it overrides the class styles, while the `class` has a lower priority. We use `id` when we need to identify a specific element, while we use the `class` when we need to style multiple elements in the same way.

### Example: 
```
<!-- ID: only one element can have it on a page (also only one id per element) -->
<div id="main-content">This is the main content of the web page</div>

<!-- Class: many elements can share it on a page (also one element can have multiple classes)  -->
<p class="highlight text bold main-passage">First passage</p>
<p class="highlight">Second passage</p>
<p class="highlight">Third passage</p>
```

## Question 6: How do you create a form in HTML? Which input types are commonly used?

## Answer:
A form can be created in HTML using the `<form>` tag. It is used to get the user input like name, email, and passwords etc., and store it to the server.

### Basic Form Structure:
```
<form action="/submit" method="POST">
  <label>Name:</label>
  <input type="text" name="name">
  <label>Email:</label>
  <input type="email" name="email">
  <button type="submit">Submit</button>
</form>
```

### Key attributes:
- action: Where the form data is sent (URL)
- method: How data is sent to the server (GET or POST)
- label: Describes what each input is for

Some commonly used inputs types in the form are:
- `type="text"`: used for name, username, and search etc.
- `type="password"`: used for passwords - hides the characters
- `type="email"`: used for email addresses
- `type="number"`: used for numeric input - age, quantity, price, mobile numbers etc.
- `type="radio"`: select only one option - yes/no
- `type="checkbox"`: select multiple options - like select preferences
- `type="submit"`: sends the form data to server - used in buttons

## Question 7: What are meta tags in HTML and why are they used?

## Answer:
Meta tags are HTML elements that provide metadata (data about data) about a webpage to the browsers, and search engines, but they are not visible on the webpage itself. `<meta>` tags are always written inside the `<head>` tag. 

Most commonly used meta tags are:
- `charset="UTF-8"`: used for character encoding, tells the browser whch characters to support. UTF-8 covers all the languages and symbols in the world.
- `viewport`: used for mobile responsiveness.
- `description`: helps search engines understand the page content and improves webpage ranking on Google.
- `author`: used to provide the author name of the webpage.

### Example of meta tags:
```
<head>
  <meta charset="UTF-8">
  <meta name="description" content="Free Web tutorials">
  <meta name="keywords" content="HTML, CSS, JavaScript">
  <meta name="author" content="John Doe">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
```

## Question 8: Explain the purpose of the alt attribute in the <img> tag.

## Answer:
The alt attribute in the <img> tag provides alternative text for an image when it cannot be displayed. It helps search engines understand the image content and improving Google ranking. 

### Example without alt:
`<img src="img.png">`

### Example with alt:
`<img src="img.png" alt="This is the image of logo">`

This alt text will be shown to the users and search engines when the image is failed to load/link of image is broken. It will help them to understand the content of image.

## Question 9: How do you make an image clickable in HTML?

## Answer:
To make an image clickable, I just wrap the `<img>` tag inside the `<a>` tag. `<a>` makes anything inside it clickable - including images, texts etc. 

### Example:
```
<a href="/link" target="_blank">
    <img src="logo.png" alt="Company's logo">
</a>
```

- `href="/link"`: it is the link of page where we want to redirect
- `target="_blank"`: It will open the link in to the new tab.

## Question 10: What is the difference between JPG, PNG, SVG, and WebP image formats in web development?

## Answer:
- `JPG`: use for photos, it doesn't support transparency and file size is small.
- `PNG`: use for logos, screenshots, and icons. It supports the transparency, and file size is larger than JPG.
- `SVG`: use for icons, logos, charts, and illustrations. It supports transparency and file size is very small. It can also be styled and animated with the CSS. It is actually a math-based code to draw shapes, not a photo format.
- `WebP`: modern format of photos created by Google. It supports transoarency and file size is very smaller than the JPG and PNG with the same quality. It also supports animations like GIF.

## Question 11: What are semantic tags introduced in HTML5 such as `<header>`, `<footer>`, `<section>`, and `<article>`?

## Answer:
Semantic HTML tags clearly describe the meaning and purpose of their content, making the webpage's structure easy for developers and browsers to understand. 
Some examples of semantic tags that are introduced in HTML5:
- `<header>` : Top section of page include logo, nav, banner etc.
- `<nav>` : Navigation links
- `<main>` : Main content of the page
- `<section>` : Grouped section of content
- `<figure>` : Image + caption content
- `<article>` : A self-contained piece of content (like blog post)
- `<aside>` : Side content (like a sidebar)
- `<footer>` : Bottom section of a page

## Question 12: What is the difference between `<script>`, async, and defer in HTML?

## Answer:
The main difference between `<script>`, async, and defer in HTML is that how and when they execute the JavaSrcipt files, which affects the performance of the page.

- `<script>`: It stops the HTML parsing while downloading the script file. It executes the file immediately after downloading. It pserves the script order and useful for small scripts. It slow downs the performance of webpage.
- `async`: It doesn't stop the HTML parsing while downloading the script file. It downloads the script in the background. It executes the file immediately after downloading and stops the HTML parsing during the execution. It doesn't pserves the script order and useful for analytics and ads. It makes the loading of page faster.
- `defer`: It doesn't stop the HTML parsing while downloading the script file. It downloads the script in the background. It doesn't executes the file immediately after downloading, it waits for the execution until the entire HTML document has been parsed. It pserves the script order and useful for Main website scripts. It improves page performance while keeping script execution predictable.

## Question 13: How do you embed audio and video in HTML5?

## Answer:

### Audio Embedding:
```
<audio controls>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
  Your browser does not support the audio tag.
</audio>
```

### Video Embedding:
```
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
  Your browser does not support the video tag.
</video>
```

## Question 14: What is the difference between relative paths and absolute paths in HTML?

## Answer:

### Relative Path:
A relative path provides the location of a file in relation to the current HTML file. 

#### Example: 
```
<img src="images/logo.png" alt="Logo"> 
```
The browser looks for the `images` folder in the same directory as the HTML file.

### Absolute Path:
An absolute path provides the complete URL or full location of a file. 

#### Example: 
``` 
<img src="https://www.example.com/images/logo.png" alt="logo">
<img src="C:/Users/Iqra/project/images/logo.png" alt="logo">
```
The browser loads the image directly from the specified website/location.

## Question 15: What are data attributes in HTML (data-*)? Where are they used?

## Answer:
Data attributes are custom attributes that can be used to store additional information within HTML elements. They always begin with `data-`.

### Syntax:
```
<button data-user-id="145" data-role="admin">Click Me</button>
```
- `data-user-id="145"`: stores a user ID.
- `data-role="admin"`: stores user's role.

### Where are they used?:
- Used to store additional custom information without affecting the page layout.
 e.g., `<button data-user-id="145" data-role="admin">Click Me</button>`
- Used to access data with JavaScript
 e.g., `<button id="btn" data-message="Hello World">Click Me</button>`
 ```
 const button = document.getElementById("btn");
 console.log(button.dataset.message);
 ```
 #### Output:
 Hello World
- Data attributes are commonly used in Dropdown menus, Tabs, Modals (pop-up windows), Product cards, and User profiles.

## Question 16: What is the purpose of the viewport meta tag in responsive web design?

## Answer:
The viewport is the user's visible area of a web page. The viewport varies with the device. It gives the browser instructions on how to control the page's dimensions and scaling. 

`<meta name="viewport" content="width=device-width, initial-scale=1.0">`
- `width=device-width`: sets the width of the page following the device's screen-width (it will vary depending on the device).
- `initial-scale=1.0`: sets the initial zoom level when the page is first loaded by the browser.

Without the viewport tag, mobile browsers may show the page as a desktop version that has been zoomed out to 100%.

## Question 17: How can you improve SEO using HTML?

## Answer:
SEO helps search engines to rank and understand your website. HTML plays an important role to improve SEO. Some key points to improve SEO using HTML are:
- Use the semantic tags, because they help search engines to better understand your structure.
- Add a proper `Title` tag, it appears in the search results as a clickable link on the browsers and includes the keywords for improving SEO.
- Write a good meta description, it helps search engines understand the page content and improves webpage ranking on Google.
- Use Correct Heading tags
- Write `alt` text for images, audios, videos, and files. If google can't see those file, it will help to understand the content of those files through `alt` text.
- Use proper, clean, and descriptive URLs
- Set the language, it tells Google the language of your page, and rank your page in the right region.

## Question 18: What are accessibility best practices in HTML?

## Answer:
Accessibility refers to developing online pages so that they are usable and understandable to everyone, including those with disabilities.
- Use semantic tags, it helps the screen readers to understand your webpage content.
- Write `alt` text for images, audios, videos, and files. If users can't see those file, it will help to understand the content of those files through `alt` text.
- Use labels for forms input, so users can easily understand the purpose of the input field.
- Use proper heading structure for better understanding webpage content structure.
- Ensure that all interactive features may be accessible via keyboard (Tab, Enter, Space).
- Use Descriptive Link Text like Read the HTML file. Avoid links like "Click Here."
- Use Lists for Related Items
- Use Tables for Tabular Data Only
- Use sufficient Color Contrast because low contrast text is hard to read for everyone

## Question 19: What is the difference between `<strong>` vs `<b>` and `<em>` vs `<i>` tags?

## Answer:
The main difference is that `<strong>` and `<em>` have semantic meaning (they convey importance/emphasis to screen readers), while `<b>` and `<i>` are just visual styling (they only change how text looks).

- The `<strong>` tag is used to define text with strong importance. The content inside is typically displayed in bold.
- The `<b>` tag specifies bold text without any extra importance.
- The `<em>` tag is used to define emphasized text. The content inside is typically displayed in italic. A screen reader will pronounce the words in `<em>` with an emphasis, using verbal stress.
- The `<i>` tag defines a part of text in an alternate voice or mood. The content inside is typically displayed in italic. It is often used to indicate a technical term, a phrase from another language, a thought, a ship name, etc.