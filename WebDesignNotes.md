Code{testing code type}
# Heading 1 is <h1></h1>
## Heading 2 is <h2></h2>
### Heading 3 is <h3></h3>

<p></p> is paragraph format

Regular elements require an ending

Void elements do NOT require an ending as they are discrete items already

<img> is a void element
to add images you need the relative path IF the image is in the same folder or inside a set of folders inside the folder where your html file is in.  

the attribute for this element is src = "path/to/file"

'''html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title> Code Block</title>
<img src = "path/to/file">
'''


notice the path to file *IS IN QUOTES*.  That is important and must be done

Giving an alternate text if the image fails is good practice AND follows Universal design requirements for disabilities

You add this attribute with the ' alt = "this is the alternate text" '
'''
html
<img src = "path/to/file" alt = "alternate text">
'''
