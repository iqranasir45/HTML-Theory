# HTML Theoretical Questions

### Question 0: What is HTML and what is the difference between HTML and HTML5?

### Answer:
HTML stands for Hyper Text Markup Language. It is the standard language used to create web pages. It uses elements like headings, paragraphs, images, links, and tables to create a webpage's structure.

#### Difference between HTML and HTML5:
- HTML is the older version mainly used to structure the web page content.
- HTML5 is the latest and improved version of HTML with new features.
- HTML doesn't support multimedia tags like &lt;video&gt; and &lt;audio&gt; without the plugins. On the other hand, HTML5 has the built-in multimedia tags.
- HTML5 has the new semantic tags like <header>, <nav>, <article>, <footer>, and <section> instead of just <div> and <span> tags, which makes it easier to organize and understand the web pages.
- The initial line in old HTML was long and difficult. HTML5 made it short and simple:
<!DOCTYPE html>
- HTML only uses cookies to store temporary data. HTML5 uses SQL databases and application cache to store offline data.

##### HTML Layout (non-semantic tags):
┌─────────────────────────────────┐
│        div id="header"          │
├──────────────┬──────────────────┤
│              │  div class="post"│
│ div          ├──────────────────┤
│ id="sidebar" │  div class="post"│
├──────────────┴──────────────────┤
│        div id="footer"          │
└─────────────────────────────────┘
##### HTML5 Layout (semantic tags):
┌─────────────────────────────────┐
│            <header>             │
├──────────────┬──────────────────┤
│              │    <article>     │
│    <nav>     ├──────────────────┤
│              │    <article>     │
├──────────────┴──────────────────┤
│            <footer>             │
└─────────────────────────────────┘