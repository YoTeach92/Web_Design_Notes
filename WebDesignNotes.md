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

`<li></li>` is the element for each item in either an ordered or unordered list

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

#### Meta Tags 
* Meta tags are Search Engine Optimization (Google)
* Best practice is one item per meta tag
* They are inside a `<meta>` tag and contain 2 parts
    * **name** which is the label for the tag and lets the search engine know what you are giving them
        * description = describes the site for the search engine
        * keywords = search engine key search terms, separated by commas
        * author = name of the author of the site (or company name)
        * viewport = sets scale and content resizing for mobile devices
    * **content** which is the actual information for the search engine to read and show
        * for description = describes what the website is
        * for keywords = list of keywords separated by commas
        * for author = name of the author or name of the company that is making the site
        * for viewport = `content="width=device-width, initial-scale=1.0"` will set the width of the content and scale it for mobile devices
```
  <meta charset="UTF-8">
  <meta name="description" content="Free Web tutorials">
  <meta name="keywords" content="HTML, CSS, JavaScript">
  <meta name="author" content="John Doe">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
```

#### Open Graph (OG) Tags
* Used for turning a simple link into a rich content for social media, text messaging etc.
* Put in a `<meta>` tag and contains 2 parts
    * **property** which operates like name but *must* start with "og:"
        * `og:title` Title of your object as it should appear
        * `og:type` defines the type of object
        * `og:image` gives the image that should appear with everything (thumbnail of a video etc)
        * `og:url` URL of the object, the place you want people to go if they click the object
    * **content** which gives the actual information that matches the property name
    * content information must be in quotes
        * for title `content="Title of the thing"`
        * for type this is where you use keywords to define what your content is
            * website
            * article
            * video.movie
            * book
            * profile
            * music.song
            * product
        * for image this is where you put the full URL to the image file
        * for URL this is where the full web address for your site goes
    * Optional metadata can be needed depending on type
        * for the audio file link to the file
            * `<meta property="og:audio" content="https://web_address.com/path/to/audio/file.mp3">`
        * for the video file link to the file
            * `<meta property="og:video" content="https://web_address.com/path/to/video/file.mp4">`
        * For location and language settings
        * `<meta property="og:locale" content="en_US">`
            * en_US is English for the US
            * en_GB is English for Great Britain (UK)
            * fr_FR is French for France
            * es_ES is Spanish for Spain
* Examples of basic metadata
```
    <html prefix="og: https://ogp.me/ns#">
    <head>
    <title>The Rock (1996)</title>
    <meta property="og:title" content="The Rock" />
    <meta property="og:type" content="video.movie" />
    <meta property="og:url" content="https://www.imdb.com/title/tt0117500/" />
    <meta property="og:image" content="https://ia.media-imdb.com/images/rock.jpg" />
```

* Examples of Optional metadata
```
    <meta property="og:audio" content="https://example.com/bond/theme.mp3" />
    <meta property="og:description" 
      content="Sean Connery found fame and fortune as the suave, sophisticated British agent, James Bond." />
    <meta property="og:determiner" content="the" />
    <meta property="og:locale" content="en_GB" />
    <meta property="og:locale:alternate" content="fr_FR" />
    <meta property="og:locale:alternate" content="es_ES" />
    <meta property="og:site_name" content="IMDb" />
    <meta property="og:video" content="https://example.com/bond/trailer.swf" />
```

     
# Main element
* main should wrap the core functionality and/or content
* One only visible
* Can **NOT** be inside the following: `<article>, <aside>, <footer>, <header>, or <nav>`
* Matches the coding concepts of Python, and especially C languages of having one main function


## Div element
* `<div></div>`
* Content division element
* A generic container or block for html elements that go together
* By default, it starts on a new line and takes up the full width available
* Group together elements that share the same CSS format
* No semantic meaning (generic purpose rather than having a structure based on what it is doing)

## Class attribute
* `<element class="something"> </element>`
* Class attribute can be used multiple times
* An element can be part of more than one class
* a space in the name creates two classes
    * `<elementName class="box boxes-blue"></elementName>`
    * This creates two classes: *box* and *boxes-blue* and places the element name in it
    * This is handy because of class inheritance (later)
* **Class is best used when you have multiple elements with the same styles**
```
<div class="box">stuff</div>
```
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

## Other Media Elements (Audio & Video)
* `<audio>` elements use mp3, wav, and ogg files in your website much like img
    * `<audio src="path/to/file.mp3> </audio>`
*  `<video>` elements use mp4, ogg, and webm files in your websites
    * `<video src="path/to/file.mp4">  </video>`
    * You will want multiple formats of the video as sources and list them in order of preference
    * Text listed between `<video>` and `</video>` will appear if no formats were supported
 

### Attributes for Media
* Control attribute to any media element

| Attribute | Value | Description |
|:---|:---:|:---|
|autoplay | autoplay | starts playing as soon as it is ready |
|controls|controls|displays video controls|
|loop|loop|plays video in a loop until stopped|
|muted|muted|starts video with audio muted|
|poster|*URL*|URL of an image to display while the video loads|
|height|*pixels*|Size in pixels of the video player (video will fill up to aspect ratio)|
|width|*pixels*|Size in pixels of the video player (video will fill up to aspect ratio)|
|src|*URL*|URL of the video source|

## id attribute
* allows you to identify the item for future work in CSS and Javascript.
* This will create a global variable for every html item with an id tag
* each tag name must be unique for this reason
* No spaces in the name of the tag, no quotes just letters numbers underscores and dashes
* NOTE: explicitly select your labeled element by using `document.getElementById("name_of_attribute)`
* NOTE: when referencing from CSS the `#` at the beginning `#title { color: blue;}` is a keyword to target the id tagged element
* **ID is best used for only one element

## Section
* `<section></section>`
* Semantic container that works well for many devices
* Groups together elements

# Button Element
* `<button></button>`
* Creates a standard button with the text that is in the middle
* Can be used with class and id attributes for CSS and later Javascript
```
<button class="my-buttons" id="button-that-does-a-thing> Text In The Button </button>
```

# Footer element
`<footer>` stuff goes here `</footer>`
* used for Copyright notices: Legal ownership information for the site or content.Contact details: Phone numbers, physical addresses, or author information (often enclosed in an <address> tag).Important links: Privacy policies, terms of service, sitemaps, or FAQs.Navigation aids: Social media icons or "back to top" links.)


## HTML Entity, or character reference
* To show `<` and `>` which are normally parsed as code for HTML, you need a way to show the parser that it is a simple character
* Named references begin with an **&** and end with an **;**
* This prevents the parser from seeing it as an element
* Named references:
  | Character | Name | Reference |
  |:---:|:---|:---:|
  & | Ampersand | `&amp;` |
  < | Less-than | `&lt;` |
  `>` | Greater-than | `&gt;` |
  `"` | double quotes | `&quot;`|
  `'` | apostrophe or single quote | `&apps;`|

* There are others but this is a basic list

# Script Element
* `<script></script>`
* Used with source (src) to locate and load the .js file
```
<script> src="path-to-js-file.js"></script>
```
* Your script file ***should*** be in a separate file.
          
              
(----------------------)










# List of elements we know:
* img - img element
* src - source element
    * alt - alt text (attribute of src element)
 
        ```
        html
        Sample:
        <img src="path/to/file" alt="alternative text">
        breakdown:
        ```
        | image element | source element | alternative text element |
        | :--- | :---------------: | :----------- |
        |<img | src="path/to/file" | alt="alternative text"> |



* a - anchor element
    * href - hypertext reference: attribute of anchor element
    * target - attribute of anchor element, determines where hyperlink will open
        * "_self" opens in the current browser tab
        * "_blank" opens in a **new** browser tab or window
        * "_parent" opens in the parent context like inside of a frame or not (OR acts like _self)
        * "_top" opens the document in the full body of the window (breaks out of any frames)
        ```
        html
        sample 1 text link:
        <a href = "website/address/of/site" target = "_self"> Text to be hyperlinked blue </a>
        
        sample 2 image link:
        <a href = "website/address/of/site" target = "_self"> <img src="path/to/file" alt="alternative text"> </a>
        ```
        | opening anchor element | hyperlink reference address | how to open (new tab or same) | What is being linked | closing anchor element |
        | --- | --- | --- | --- | --- |
        | <a | href = "website/address/of/site" | target = "_self"> | Text to be hyperlinked blue | `</a>` |
        | <a | href = "website/address/of/site" | target = "_blank"> | `<img src="path/to/file" alt="alternative text">` | `</a>` |
            


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
* script - element used to embed executable code    
* div - division element sets up a container block of content
* section - separates logical sections of html
* footer - at the bottom of the website, usually contains author, copyright, terms of use etc
    * use special character references here for copyright etc `&reg;` for &reg;
* figure - used to group logical items together like images and captions, charts and graphs, code snippets, etc.
    * figcaption - adds the text to the figure group






