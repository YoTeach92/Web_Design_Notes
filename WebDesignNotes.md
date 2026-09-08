
```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title> Code Block</title>
    <img src = "path/to/file">
```

Code{testing code type}
# Heading 1 is `<h1></h1>`
## Heading 2 is `<h2></h2>`
### Heading 3 is `<h3></h3>`

``<p></p>`` is paragraph format

Regular elements require an ending

Void elements do NOT require an ending as they are discrete items already

`<img>` is a void element
to add images you need the relative path IF the image is in the same folder or inside a set of folders inside the folder where your html file is in.  

the attribute for this element is src = "path/to/file"



```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title> Code Block</title>
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



## Vocabulary
**Elements:** An element is an individual component of a webpage with a start tag, optional attributes, content, and most often an end tag  \ *Void Elements* like `<img>`don't have an end tag

**Attributes** A modifier placed *inside* an element (*between the opening and closing tags*) that configures behavior, appearance or gives extra information



```html
<element attribute="value"></element>
<a href="https://www.freecodecamp.org" target="_blank">Visit freeCodeCamp</a>
```

The ` href ` attribute specifies the URL of a link and the ` target ` attribute specifies where to open the link.
The ` <a> ` is the anchor element



``` html
<input type="checkbox" checked />
```

## Link Element
A link element is used to link to external resources like stylesheets and site icons. 

```
html
<link rel="stylesheet" href="./styles.css" />
```

*NOT* hyperlinking a website, that is `<a></a>`

### Attributes with it
p
`<rel>` - relationship defines how the document replated to a linked resource

    * stylesheets - connects external CSS file to style the webpage
    * nofollow - tells search engines to skip it (not strict)
    * noopener - improves security of `target="blank"` links by preventing new page from accessing original page window
    * sponsored - marks paid advertisement link
    * ugc - Marks user generated content (comments, forum posts, etc)
p

## List of elements we know:
* src - source element
    * alt - alt text (attribute of src element)
* a - anchor element
    * href - hypertext reference: attribute of anchor element
    * target - attribute of anchor element, determines where hyperlink will open
* h1 (and h2 h3 h4 h5 h6 respectively) - heading elements
* p - paragraph element
* input - element that takes input from the website user
    * checkbox - attribute of the input
        * checked or unchecked - boolean attribute of the checkbox
        * disabled or enabled - boolean attribute of an input
        * readonly - boolean attribute
        * required - boolean attribute
* link - link to outside sources (CSS & icons)
    * rel 





