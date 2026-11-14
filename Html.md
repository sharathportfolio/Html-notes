# HTML Notes

## 1. What is HTML?

**HTML** stands for **HyperText Markup Language**. It describes the
structure and content of a webpage.

-   **HyperText:** Text that can link to other pages or resources.
-   **Markup:** Tags that describe the role of content.
-   **Language:** A set of rules used to structure a document.

HTML is not a programming language; it is a markup language.

Example:

``` html
<h1>Hello, world!</h1>
<p>This is my first webpage.</p>
```

## 2. HTML document structure

A basic HTML page follows a standard structure called the **HTML
boilerplate**.

``` html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My First Website</title>
</head>
<body>
  <h1>Hello, world!</h1>
  <p>Welcome to my website.</p>
</body>
</html>
```

### `<!DOCTYPE html>`

-   Declares that the document uses HTML5.
-   Put it at the very top of the document.
-   It is a declaration, **not an HTML element**.
-   Helps the browser render the page in standards mode.

``` html
<!DOCTYPE html>
```

### `<html>`

-   The **root element** of the page.
-   All other HTML elements (except the doctype declaration) belong
    inside it.
-   Use the `lang` attribute to identify the page language.

``` html
<html lang="en">
  <!-- The head and body go here -->
</html>
```

### `<head>`

Contains information *about* the page, called metadata. It is not the
visible content area of the webpage.

Common contents include: - Page title - Character encoding - Viewport
settings - SEO description - CSS links - Some scripts and other metadata

``` html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="A beginner's personal portfolio website.">
  <title>My Portfolio</title>
</head>
```

### `<meta>`

Provides metadata about the document. It is placed inside `<head>` and does not display page content.

### **Common Attributes**

* `charset` → Defines character encoding.
* `name` → Specifies the type of metadata (e.g., description, keywords).
* `content` → Provides the actual metadata value.
* `viewport` → Controls layout on mobile devices.




Common examples:

``` html
<!-- Supports a wide range of characters -->
<meta charset="UTF-8">

<!-- Helps the page scale correctly on mobile devices -->
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- A short description of the page -->
<meta name="description" content="Projects and information about me.">

<!-- Identifies the author -->
<meta name="author" content="Your Name">
```

**Remember:** `name="viewport"` is the metadata name; the `content`
value controls the viewport settings.

### `<title>`

Sets the page title shown in the browser tab and used as the page title
in many search results.

``` html
<title>My Portfolio | Your Name</title>
```

## 3. Headings

HTML provides six heading levels, from `<h1>` (most important) to `<h6>`
(least important).

``` html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

### Element anatomy

``` html
<h1>Heading 1</h1>
```

-   `<h1>` --- opening tag
-   `Heading 1` --- content
-   `</h1>` --- closing tag
-   The complete line --- an HTML element

### Best practices

-   Use headings to describe the structure of the content, not just to
    make text look big.
-   A page usually has one clear main `<h1>` heading. HTML can
    technically have more, but one main heading is a useful beginner
    convention.
-   Nest heading levels logically: `<h1>` → `<h2>` → `<h3>`.
-   Do not choose a heading level only because of its default font size.
    Use CSS for appearance.

## 4. Paragraphs

The `<p>` element represents a paragraph of text.

``` html
<p>I am learning HTML and building my first website.</p>
<p>This is another paragraph.</p>
```

**Why use it?** Paragraph elements give text meaningful structure.
Browsers, search engines, and assistive technologies such as screen
readers can understand that the content is a paragraph.



## 5. Void elements

A **void element** cannot contain child content and does not have a
closing tag.

### Horizontal rule --- `<hr>`

Represents a thematic break between sections. Browsers usually display
it as a horizontal line.

``` html
<p>About me</p>
<hr>
<p>My projects</p>
```

### Line break --- `<br>`

Creates a line break inside text. Use it when the line break is part of
the content, such as an address or poem---not to create page spacing.

``` html
<p>
  Your Name<br>
  Chennai, India<br>
  your.email@example.com
</p>
```

**Note:** In HTML, `<hr>` and `<br>` are enough. The slash in `<hr />`
or `<br />` is optional.

## 6. Lists

Lists group related items together.

### Unordered list --- `<ul>`

Use when the order of items does not matter. Items usually appear with
bullet points.

``` html
<h2>My Skills</h2>
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ul>
```

### Ordered list --- `<ol>`

Use when the sequence or ranking matters. Items usually appear with
numbers.

``` html
<h2>My Learning Plan</h2>
<ol>
  <li>Learn HTML basics</li>
  <li>Practise CSS</li>
  <li>Build a small website</li>
</ol>
```

### Important list elements

-   `<ul>` --- unordered list container
-   `<ol>` --- ordered list container
-   `<li>` --- one list item

## 7. Nesting and indentation

**Nesting** means placing one element inside another element.

``` html
<ul>
  <li>Frontend
    <ul>
      <li>HTML</li>
      <li>CSS</li>
    </ul>
  </li>
  <li>Backend</li>
</ul>
```

The inner `<ul>` is nested inside the first list item.

### Indentation tips

-   Indent child elements consistently (two spaces is a common choice).
-   Make opening and closing tags easy to match.
-   Close elements in the reverse order in which they were opened.
-   Correct nesting makes code easier to read and maintain.

## 8. Anchor element --- links

The `<a>` element creates a hyperlink. Its `href` attribute specifies
the destination.

``` html
<a href="https://www.example.com">Visit Example</a>
```

A link to another page in your own website:

``` html
<a href="about.html">About Me</a>
```

A link that opens an email application:

``` html
<a href="mailto:hello@example.com">Email me</a>
```

**Remember:** Include `https://` for a full website URL. A value such as
`google.com` may be treated as a relative path rather than the intended
external website URL.

## 9. HTML attributes

Attributes provide extra information or settings for an element. They
are written in the opening tag.

General pattern:

``` html
<tag attribute="value">Content</tag>
```

Example:

``` html
<a href="https://www.example.com" target="_blank" rel="noopener">
  Open Example in a new tab
</a>
```

In this example: - `href` gives the link destination. -
`target="_blank"` requests a new tab or window. - `rel="noopener"`
prevents the new page from accessing the opener through `window.opener`.

Common attributes:

  Attribute   Typical use
  ----------- ---------------------------------------------------------
  `id`        Gives an element a unique identifier in the page
  `class`     Groups elements for CSS or JavaScript
  `href`      Sets a link destination
  `src`       Sets the source of an image or other embedded resource
  `alt`       Provides alternative text for an image
  `title`     Provides advisory information, often shown as a tooltip
  `lang`      Identifies the language of content

## 10. Image element --- `<img>`

The `<img>` element embeds an image. It is a void element.

``` html
<img src="images/profile.jpg" alt="Portrait of me smiling">
```

-   `src` --- path or URL of the image file.
-   `alt` --- text alternative describing the image's purpose or
    content.

### Good alt-text practices

-   Describe the useful information in the image.
-   If an image is decorative and adds no information, use `alt=""`.
-   Do not write "image of" or "picture of" unless that wording is
    genuinely useful.
-   Do not omit the `alt` attribute.

Example:

``` html
<img src="images/project-preview.png" alt="Screenshot of my weather app project">
```

## 11. File paths: absolute and relative

A file path tells the browser where to find a resource, such as an image
or another HTML file.

Imagine this project structure:

``` text
my-portfolio/
├── index.html
├── about.html
├── images/
│   └── profile.jpg
└── pages/
    └── contact.html
```

### Relative paths

A relative path is written from the location of the current file.

  -----------------------------------------------------------------------
  Path                                Meaning
  ----------------------------------- -----------------------------------
  `images/profile.jpg`                Open the `images` folder from the
                                      current directory

  `./index.html`                      `index.html` in the current
                                      directory

  `../index.html`                     Go up one directory, then find
                                      `index.html`

  `../images/profile.jpg`             Go up one directory, then open
                                      `images/profile.jpg`
  -----------------------------------------------------------------------

### Absolute paths

An absolute URL gives the complete web address of a resource.

``` html
<img src="https://example.com/images/profile.jpg" alt="Profile portrait">
```

A local absolute filesystem path (such as `C:\...`) is generally not
suitable for a website because it will not work for visitors on other
computers.

### Remember

-   `./` --- current directory
-   `../` --- parent directory (one level up)
-   `/` --- separates folders in a path; at the start of a URL path, it
    refers to the site's root

## 12. Special characters and HTML entities

Some characters have a special meaning in HTML. Use character references
(often called HTML entities) when you want to display them as text.

  Character   HTML entity   Meaning
  ----------- ------------- -----------------------
  `<`         `&lt;`        Less-than sign
  `>`         `&gt;`        Greater-than sign
  `&`         `&amp;`       Ampersand
  `"`         `&quot;`      Double quotation mark
  `'`         `&apos;`      Apostrophe (HTML5)
  `©`         `&copy;`      Copyright symbol
  `®`         `&reg;`       Registered trademark
  ``          `&nbsp;`      Non-breaking space

Example:

``` html
<p>In HTML, write &lt;h1&gt; to show the text &lt;h1&gt;.</p>
<p>Copyright &copy; 2026 Your Name</p>
```

## 13. Complete beginner example

This small page brings together the elements covered above.

``` html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="A simple beginner portfolio page.">
  <title>My First Portfolio</title>
</head>
<body>
  <header>
    <h1>Hello, I'm Your Name</h1>
    <p>A beginner learning web development.</p>
  </header>

  <hr>

  <main>
    <section>
      <h2>About Me</h2>
      <p>
        I enjoy learning how websites work and building small projects.
        This is my first HTML practice page.
      </p>
      <img src="images/profile.jpg" alt="My profile portrait">
    </section>

    <section>
      <h2>My Skills</h2>
      <ul>
        <li>HTML</li>
        <li>CSS</li>
        <li>Learning JavaScript</li>
      </ul>
    </section>

    <section>
      <h2>My Learning Goals</h2>
      <ol>
        <li>Understand HTML structure</li>
        <li>Learn CSS styling</li>
        <li>Build and publish a portfolio</li>
      </ol>
    </section>

    <section>
      <h2>Contact</h2>
      <p>
        <a href="mailto:hello@example.com">Send me an email</a>
      </p>
      <p>
        <a href="https://www.example.com">Example website</a>
      </p>
    </section>
  </main>

  <footer>
    <p>&copy; 2026 Your Name</p>
  </footer>
</body>
</html>
```

## 14. Semantic HTML elements to recognise

Semantic elements describe the purpose of the content they contain.

  Element       Purpose
  ------------- --------------------------------------------------
  `<header>`    Introductory content for a page or section
  `<nav>`       A group of navigation links
  `<main>`      The main content of the page
  `<section>`   A thematic section of content
  `<article>`   Self-contained content that can stand on its own
  `<aside>`     Related or supplementary content
  `<footer>`    Footer information for a page or section

Example:

``` html
<body>
  <header>
    <h1>My Website</h1>
  </header>

  <nav>
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
  </nav>

  <main>
    <section>
      <h2>My Projects</h2>
      <p>Here are some things I have built.</p>
    </section>
  </main>

  <footer>
    <p>&copy; 2026 Your Name</p>
  </footer>
</body>
```
