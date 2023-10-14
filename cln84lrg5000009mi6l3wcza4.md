---
title: "An Introduction to HTML Tags"
datePublished: Sun Oct 01 2023 16:51:00 GMT+0000 (Coordinated Universal Time)
cuid: cln84lrg5000009mi6l3wcza4
slug: an-introduction-to-html-tags
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1696203409110/fd8b23e5-e16b-460f-8046-d4e8860c9e33.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1696203527911/4d3aa191-e8e5-4ece-9821-ad3501393c75.jpeg
tags: web-development, html5, frontend-development, technical-writing-1, html-tags

---

### Introduction

HTML (HyperText Markup Language), as the name implies, is a markup language used to create the layouts of web pages within a website. Various tags are used to organize and instruct the web browser on how to handle different contents and how they should be displayed on the web browser.

## Prerequisite

To make sense of this guide, you should know the basics of how websites function, don't need much previous programming know-how, and have a laptop with a code editor and a web browser.

## i) Introduction to HTML5

HTML5 is the fifth major version of HTML (HyperText Markup Language) used on the internet. It was first created and published in January 2008 and became widely used between 2008 and 2012. It was officially recommended by W3C in 2014. Before HTML5, there were earlier versions of HTML (1-4).

You can tell you're using HTML5 by starting your document with the `<!DOCTYPE html>` declaration. This tells the web browser that you're using HTML5 for your code. Read more about HTML on [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML)[.](https://www.w3schools.com/html/default.asp)

```abap
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Tags</title>
</head>
<body>
    
</body>
</html>
```

| HTML VERSION | YEAR OF PUBLICATION |
| --- | --- |
| HTML | 1991 |
| HTML+ | 1993 |
| HTML 2.0 | 1995 |
| HTML 3.2 | 1997 |
| HTML 4.01 | 1999 |
| HTML 5.0 | 2012 |

## ii) HTML Tags

HTML tags serve as directives that provide instructions to a web browser regarding the rendering of content within a web page. These tags enable the web browser to discern and format diverse elements, including images, paragraphs, headings, hyperlinks, tables, lists, and additional components.

### A) Opening and closing tags in HTML

Most HTML tags have both an opening and a closing tag. These tags are denoted by the use of angle brackets, '&lt;' and '&gt;', with the tag command enclosed within for the opening tag, and the same symbols with a '/' (forward slash) before the command followed by '&gt;' for the closing tag.

For example, `<head>` represents an opening tag, and `</head>` represents a closing tag. Any content enclosed between the opening and closing 'head' tags is treated as a 'head' element and is not displayed on the web page by the browser.

```xml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Tags</title>
</head>
<body>
    <p>Hello, World!</p>
</body>
</html>
```

Output:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696204158430/e56bafcf-f813-4229-bb19-d04337fdb0a3.png align="center")

Observe that the content within the head tag remains invisible on the browser, as will be elucidated later. Conversely, the content within the body tag, such as 'Hello, World!', is visible and displayed. This underscores the significance of HTML tags, as the browser renders them according to their intended purpose and relevance on the web page.

### B) Self-closing tags in HTML

These tags don't require separate opening and closing parts. They work as a single tag enclosed in angle brackets, and the content goes inside the tag, like this: &lt;img src="image.png&gt;.

```xml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Tags</title>
</head>
<body>
    <p>Hello, World!</p>
        <figure>
            <img src="https://shorturl.at/pvGI8" alt="A male programmer working on a workstation">
            <figcaption>I am a developer</figcaption>
        </figure>
</body>
</html>
```

Output:

![A male programmer working on a workstation](https://cdn.hashnode.com/res/hashnode/image/upload/v1696188731050/5326d76d-a6c3-41f9-8ff7-9277b1183127.png align="center")

Image: [unsplash.com](https://shorturl.at/pvGI8)

Take note that the image tag lacks distinct opening and closing tags; it integrates both actions into one, encompassing the content within the tag. Remarkably, the browser successfully renders this as an image. Now, let's compare this behavior to when the image tag is explicitly opened and closed to observe the differences in functionality.

```xml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Tags</title>
</head>
<body>
    <p>Hello, World!</p>
        <figure>
            <img>
                 "https://shorturl.at/pvGI8" alt="A male programmer working on a workstation"
            </img>
            <figcaption>I am a developer</figcaption>
        </figure>
</body>
</html>
```

Output:

![A webpage showing the output of opening and closing an img tag](https://cdn.hashnode.com/res/hashnode/image/upload/v1696189050007/abb9b7f0-fb17-4057-a956-3a05ccc054e4.png align="center")

### C) Semantic HTML tags

Semantic HTML tags are specific elements within HTML that convey meaningful information about a web page's structure and content. They offer contextual clues to web browsers and assist in clarifying the purpose of various web page sections. By using semantic HTML tags, web content becomes more accessible and is better comprehended by search engines. Some common semantic HTML tags include:

1. `<header>`: Represents the introductory section of a page or a section, typically containing the site logo, navigation menus, and other top-level content.
    
2. `<nav>`: Defines a container for navigation links, such as menus or navigation bars.
    
3. `<main>`: Signifies the main content of a webpage and should be unique to each page.
    
4. `<article>`: Encloses a self-contained, independent piece of content, such as a blog post, news article, or forum post.
    
5. `<section>`: Represents a distinct thematic grouping of content within a webpage, helping to organize content into meaningful blocks.
    
6. `<footer>`: Represents the footer of a webpage or a section, typically containing copyright information, contact details, or other relevant information.
    
7. `<figure>` and `<figcaption>`: Used to associate a caption with an image or multimedia content.
    
8. `<time>`: Specifies a date and/or time within the content, providing machine-readable information.
    

Employing these tags not only enhances website accessibility and SEO but also aids developers and designers in grasping the page's layout. Ultimately, it improves the overall user experience by making content more meaningful and navigable.

## iii) Types of HTML tags

There are more than a hundred HTML tags, but we will categorize them into various groups as listed below and focus on the most significant and practical ones among them.

### A) Basic HTML tags

Basic HTML tags are fundamental elements used in Hypertext Markup Language (HTML) to structure and format web content. These tags provide the building blocks for creating a web page. Some essential basic HTML tags include:

* `<html>`: Defines the root element of an HTML document.
    
* `<head>`: Contains metadata about the document, such as the title and links to external resources.
    
* `<title>`: Specifies the title of the web page, which appears in the browser's title bar or tab.
    
* `<meta>`: Provides information about the character encoding, author, and other metadata.
    
* `<link>`: Establishes relationships between the current document and external resources like stylesheets.
    
* `<style>`: Contains CSS (Cascading Style Sheets) code for styling the document.
    
* `<script>`: Embeds JavaScript code for interactivity and functionality.
    
* `<body>`: Contains the visible content of the web page, including text, images, and other elements.
    
* `<heading>`: Define headings of varying levels, with `<h1>` being the highest level and `<h6>` the lowest.
    
* `<p>`: Represents a paragraph of text.
    

These basic HTML tags form the core structure of a web page and are essential for creating web content. Developers use a combination of these tags, along with more advanced elements, to design and structure web pages as needed. Let’s practice using the aforementioned tag to create a simple web page.

```xml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Tags</title>
    <link rel="stylesheet" href="style.css">
    <script src="myscript.js"></script>
</head>
<body>
    <p>Hello, World!</p>
    <h1>This is a heading</h1>
    <h2>This is a heading</h2>
    <h3>This is a heading</h3>
    <h4>This is a heading</h4>
    <h5>This is a heading</h5>
    <h6>This is a heading</h6>
</body>
</html>
```

Output:

![Illustrations of various headings in HTML](https://cdn.hashnode.com/res/hashnode/image/upload/v1696191669582/0cb9b70f-2310-431a-b2e2-03b93787a698.png align="center")

### B) Formatting tags

Formatting tags in HTML are used to apply various styles, formatting, and visual effects to text and content on a web page. They help control the appearance of the content presented to users. Here are some common formatting tags in HTML:

1. The bold tag: `<b>` Makes text bold `</b>`
    
2. Emphasis tag: `<em>` Emphasizes text by adding emphasis, typically displayed as italics.`</em>`
    
3. Underline tag: `<u>` Underlines text. `</u>`
    
4. Subscript tag: Displays text as `<sub>` subscript `</sub>` (below the baseline).
    
5. Superscript tag: Displays text as `<sup>` superscript `</sup>` (above the baseline).
    

These formatting tags allow web developers to style text and content in various ways to enhance readability and the user experience. When combined with CSS (Cascading Style Sheets), HTML formatting tags provide extensive control over the visual presentation of web content.

Now let’s use the following tag to format a web page by repeating the same sentences and commands as code.

```xml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Tags</title>
 </head>
<body>
   <h2>Formatting Tags</h2>
   <p>The bold tag: <b>Makes text bold.</b></p>
   <p>Emphasis tag: <em>Emphasizes text by adding emphasis, typically displayed as italics.</em></p>
   <p>Underline tag: <u>Underlines text.</u></p>
   <p>Subscript tag: Displays text as <sub>subscript</sub> (below the baseline).</p>
   <p>Superscript tag: Displays text as <sup>superscript</sup> (above the baseline).</p>
</body>
</html>
```

Output:

![Formatting Tags](https://cdn.hashnode.com/res/hashnode/image/upload/v1696193354062/c477c752-a062-4b04-b7be-8dd5d159e31a.png align="center")

### C) Link tag

The anchor tag denoted as `<a> </a>` serves the purpose of connecting different web pages. When it wraps around text, it transforms that text into a clickable hyperlink, providing the ability to navigate to another web page or a specific section within the same web page. An example of this functionality is demonstrated below.

```xml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Tags</title>
 </head>
<body>
   <h2>Link Tags</h2>
    <p>This is a <a href="https://www.google.com" target="_blank">link</a> to Google's search engine</p>
</body>
</html>
```

Output:

![Link tag demonstration](https://cdn.hashnode.com/res/hashnode/image/upload/v1696194088472/46d6cc55-2367-49a7-9ffe-02e4382612da.png align="center")

Observe that the text link is encompassed by the anchor tag in the code editor, and on the web page it was rendered as a clickable hyperlink.

### D) List tags

The `<li>` tag displays the content of a list nested within one of two HTML list types: the unordered list `<ul>` and the ordered list `<ol>`. The unordered list, as the name suggests, is unstructured and represented by bullet points. In contrast, the ordered list is organized in ascending order, using Arabic numerals (1-9).

Please refer to the illustration below for a visual example.

```xml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Tags</title>
</head>
<body>
   <h2>List Tags</h2>
    <h3>Unordered List</h3>
    <ul>
        <li>Code</li>
        <li>Eat</li>
        <li>Learn</li>
    </ul>

    <h3>Ordered List</h3>
    <ol>
        <li>Code</li>
        <li>Eat</li>
        <li>Learn</li>
    </ol>
</body>
</html>
```

Output:

![List tag demonstration](https://cdn.hashnode.com/res/hashnode/image/upload/v1696194735642/c0ab2c95-e2c4-4cef-97cd-8cd0bc8e46d0.png align="center")

### E) Table tags

We're now going to talk about the last tag in this guide, which is the table tag. The `<table>` tag is used in HTML to create tables on web pages. It works together with other elements like `<thead>`, which stands for the table's heading. Inside `<thead>`, we use `<th>` tags to define the actual content of the table's header.

Both `<thead>` and `<th>` are contained within the main `<table>` tag. Next, we have the `<tr>` tag, which represents rows in the table, and the `<td>` tag, which represents the actual data in those rows. These tags are all placed inside the `<table>` tag to structure the table properly.

To be more specific, the `<th>` tag goes inside the `<thead>` tag, which is nested within the `<table>` tag. Similarly, the `<td>` tag, representing the data, is inside the `<tr>` tag, which, in turn, is nested within the `<table>` tag. For a clearer picture, take a look at the example below and practice to better understand.

```xml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Tags</title>
</head>
<body>
   <h2>The Table Tag</h2>
        <table style="border: 1px solid black;">
            <thead>
                <tr>
                    <th style="border: 1px solid black;">Heading 1</th>
                    <th style="border: 1px solid black;">Heading 2</th>
                </tr>
            </thead>
            
            <tr>
                <td style="border: 1px solid black;">Data 1</td>
                <td style="border: 1px solid black;">Data 2</td>
            </tr>
        
            </tr>
                <td style="border: 1px solid black;">Data 3</td>
                <td style="border: 1px solid black;">Data 4</td>
            </tr>
            
        </table>
</body>
</html>
```

Output:

![Table tag ](https://cdn.hashnode.com/res/hashnode/image/upload/v1696195644759/e1e70be1-f257-40fb-a333-2cced8bff99c.png align="center")

## Conclusion

In this guide, you have gained a solid understanding of HTML tags, their purpose, and their usage. To enhance your comprehension, continue practicing and consult the [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML) and [W3Schools](https://www.w3schools.com/html/default.asp) for comprehensive information on these concepts. Additionally, explore further aspects of HTML for a deeper understanding.

Is this interesting? Read my next article by clicking on this [link](https://nezer.hashnode.dev/mastering-responsive-web-design-for-seamless-user-experiences-media-query-clng3nw11000908lg4dcvci5c).