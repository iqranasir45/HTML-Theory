# HTML Theoretical Questions

### Question 0: What is HTML and what is the difference between HTML and HTML5?

### Answer:
HTML stands for Hyper Text Markup Language. It is the standard language used to create web pages. It uses elements like headings, paragraphs, images, links, and tables to create a webpage's structure.

#### Difference between HTML and HTML5:
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


### Question 1: What are semantic HTML tags? Why are they important in web development?

### Answer:
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

#### Importance:
- It provides better readability. Developers can easily identify different sections of webpage content. For example, when you see the `<nav>` tag, you can easily understand that this section is of navigation links.
- It makes maintenance easier because the well-structured code is easier to modify, debug and maintain.
- Search engines can easily understand the structure and content of webpage. which helps in higher ranking of website.

### Question 2: What is the difference between `<div>` and `<span>` tags?

### Answer:
- `<div>` is block-level element and `<span>` is an inline element.
- `<div>` occupy the whole available width and on the other side `<span>` just used the required width.
- `<div>` used to organize and group large blocks of content and on the other side `<span>` is used to style and group small blocks of content within the line.
- `<div>` starts on a new line and on the other side `<span>` remains to the same line.
- `<div>` used to create layouts, and divide the page sections and on the other side `<span>` is used to style specific words and parts of the text.

#### Example: 

#### Use of `<div>`:
<div style="background-color: pink;">This is a section</div>
<div style="background-color: blue; color: white;">It starts a new line</div>

#### Use of `<span>`:
<p>This is a <span style="color:red;">red</span> word.</p>