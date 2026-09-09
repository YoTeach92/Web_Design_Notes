# Text elements and formatting

# Heading 1 is `<h1></h1>`
## Heading 2 is `<h2></h2>`
### Heading 3 is `<h3></h3>`

`<p></p>` is paragraph format

`<em></em>` is the emphasis element and <em> italicizes </em> in between them

`<strong></strong>` is the strong element and <strong> bolds </strong> in between them

`<ul></ul>` is an unordered list

<ul>
    <li>cheddar</li>
    <li>swiss</li>
    <li>gouda</li>
</ul>

`<ol></ol>` is an ordered (numbered list)
<ol>
    <li>frosted flakes</li>
    <li>cheerios</li>
    <li>granola</li>
</ol>

## Elements vs Attributes
**Elements:** An element is an individual component of a webpage with a start tag, optional attributes, content, and most often an end tag  \ *Void Elements* like `<img>`don't have an end tag

**Attributes** A modifier placed *inside* an element (*between the opening and closing tags*) that configures behavior, appearance or gives extra information

```html
<element attribute="value"></element>
<a href="https://www.freecodecamp.org" target="_blank">Visit freeCodeCamp</a>
```

The ` href ` attribute specifies the URL of a link and the ` target ` attribute specifies where to open the link.
The ` <a> ` is the anchor element


Inputs are also available to allow user input directly on the HTML
``` html
<input type="checkbox" checked />
```

Regular elements require an ending

Void elements do NOT require an ending as they are discrete items already

# Image elements
`<img>` is a void element
to add images you need the relative path IF the image is in the same folder or inside a set of folders inside the folder where your html file is in.  

the attribute for this element is src = "path/to/file"

```html

    <img src = "path/to/file">
```

notice the path to file ***IS IN QUOTES***.  That is important and must be done

Giving an alternate text if the image fails is good practice AND follows Universal design requirements for disabilities

You add this attribute with the ` alt = "this is the alternate text" `
```
html
<img src = "path/to/file" alt = "alternate text">
```
It looks like this: <img src="path/to/file" alt="alternative text"> when it needs to appear

#### Figure with images
The `<figure>` element is an HTML semantic tag used to group self-contained content like images, diagrams, code snippets, or charts
```
<figure>
  <img src="flower.jpg" alt="A close-up of a red flower">
  <figcaption>Figure 1: A red flower in the spring garden.</figcaption>
</figure>
```
The `<figcaption>` element goes with it to add the text as a single unit 


# Link Element
A link element is used to link to external resources like stylesheets and site icons. 

```
html
<link rel="stylesheet" href="./styles.css" />
<link rel="icon" href="icon_file_name.ico" />
```
**./** in the href means to look in a folder inside the current directory

Link elements should be placed inside the `<head>` element

*NOT* hyperlinking a website, that is `<a></a>`

### Attributes with it

`<rel>` - relationship defines how the document is related to a linked resource
* stylesheets - connects external CSS file to style the web page
* nofollow - tells search engines to skip it (not strict)
* noopener - improves security of `target="blank"` links by preventing new page from accessing original page window
* sponsored - marks paid advertisement link
* ugc - Marks user generated content (comments, forum posts, etc)

# Head element
Example:
```
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Examples of the link element</title>
  <link rel="stylesheet" href="./styles.css" />
</head>
```
More about the head later

### Boilerplate in the head
Standard set of information you can often copy and paste, changing a few things along the way
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta
       name="viewport"
       content="width=device-width, initial-scale=1.0" />
    <title>Title of the Webpage</title>
    <link rel="stylesheet" href="./styles.css" />
  </head>
  <body>
  </body>
</html>
```
* DOCTYPE HTML defines the document type
* `<HTML lang="en">  </HTML>` defines the language as English and ***everything*** on the page goes in between the opening and closing HTML brackets
* charset - standard today is UTF-8 or Unicode version 8.  It includes multiple languages, emojis, accented letters etc.
    * other options:
        * US-ASCII - old school 7 bit English only
        * UTF-16 or UTF-32 - used in programming environments (16 and 32 bit sizes)
        * ISO-8859 Series - legacy international standards for non-English languages
     
# Main element
* main should wrap the core functionality and/or content
* One only visible
* Can **NOT** be inside the following: `<article>, <aside>, <footer>, <header>, or <nav>`
* Matches the coding concepts of Python, and especially C languages of having one main function

# Footer element
`<footer>` stuff goes here `</footer>`
* used for Copyright notices: Legal ownership information for the site or content.Contact details: Phone numbers, physical addresses, or author information (often enclosed in an <address> tag).Important links: Privacy policies, terms of service, sitemaps, or FAQs.Navigation aids: Social media icons or "back to top" links.)

# List of elements we know:
* src - source element
    * alt - alt text (attribute of src element)
* a - anchor element
    * href - hypertext reference: attribute of anchor element
    * target - attribute of anchor element, determines where hyperlink will open
* h1 (and h2 h3 h4 h5 h6 respectively) - heading elements
* p - paragraph element
* em - emphasis element (italicizes the text in between the open and close)
* strong - strong element (bolds the text between open and close)
* * ul - unordered list
    * li - bulleted list item (requires open and close), must be nested in a `<ul>` element
* ol - ordered list (numbered list of items) uses the `<li>` element for each item
* input - element that takes input from the website user
    * checkbox - attribute of the input
        * checked or unchecked - boolean attribute of the checkbox
        * disabled or enabled - boolean attribute of an input
        * readonly - boolean attribute
        * required - boolean attribute
* link - link to outside sources (CSS & icons)
    * rel - relationship attribute of link
        * alternate - alternate representations of the current document
        * icon - icon image file.  Usually also contains alternate versions/sizes for different devices
        * stylesheet - references the CSS stylesheet file
            * best practice is to keep the HTML and CSS files separate from each other
    * href - used to give the link to the resource (CSS file)
* head - invisible information needed for the computer to accurately show your webpage (one per page ONLY)
    * link - CSS file is referenced here
    * title - the title that shows on the browser tab
    * meta - meta data
        * charset - declares the character encoding scheme used by the page
    * script - runs first JavaScript code snippets
    * style - local page only CSS information
    * base - sets base directory for the page all assets are referenced relative to the base rather than the full address
* main - wrapper around the core content
* section - separates logical sections of html
* footer - at the bottom of the website, usually contains author, copyright, terms of use etc
* figure - used to group logical items together like images and captions, charts and graphs, code snippets, etc.
    * figcaption - adds the text to the figure group






