# Semantic HTML

## Introduction to Semantic HTML

* Semantics is the meaning of words
* Semantic HTML is giving meaning to the labels of different HTML elements
  * Div elements do **NOT** have semantic meaning
  * All other elements do

--------------------------------------

* Using headers in the right order (outline style) helps your website make sense
  * `<h1>` There is usually only one per page and should come before the content
    * `<h2>` Is your first subheading: Use this to separate different sections of your website
      * `<h3>` Comes after an h2 and should never be directly under an h1

**Example:**
```
<section>
  <h1>freeCodeCamp</h1>
    <h2>Learn Front-End Development</h2>
      <h3>First steps in Front-End Development</h3>
      <h3>Second steps in Front-End Development</h3>
    <h2>Learn Back-End Development</h2>
      <h3>First steps in Back-End Development</h3>
      <h3>Second steps in Back-End Development</h3>
</section>
```
* Use CSS to style larger sized text for effects you want to see; keep headers for organization

## Semantic vs Presentational
* Presentational HTML was based on how it looked and most of these tools have been deprecated (gotten rid of)
* Semantic HTML is more flexible and powerful for SEO and Adaptive technologies (which are required often by ADA)
* Rules:
  * *FONT SIZES, COLOR, and JUSTIFICATION should ALWAYS be set with CSS!!*
* Basic Summary:
  * Presentational HTML was about looks
  * Semantic HTML is about describing the content

## Examples of Semantic HTML
* header - for defining the header of the document, or section
* nav - for sections with navigation links
* section - for grouping related information
* figure - for illustrations and diagrams
    ```
    <header>
      <nav>
        <a href="#">Home</a>
        <a href="#">About</a>
        <!--Add the products link here-->
    
        <a href="#">Contact</a>
      </nav>
    </header>
    ```

### Use of Emphasis for Semantic Meaning
* `<em></em>` will make text *italicized*
 * This should be used to add meaning to the *text* rather than as a style decision
 * It can also be used to set apart a different language *s'il vous plaît* (if you please)
* Another way is to do the following: `i lang="fr">je ne sais quoi</i>` which creates a small element with a different language
 * i element is an idiomatic expression element used to set apart words but **not** give them additional meaning
  * That is the job of *emphasis* discussed above: `<em>`*important words*`</em>`

### Use of B vs Strong
* `<b></b>` is used to "*bring attention*" to text but does NOT demonstrate it's importance
* `<strong></strong>` emphasizes the **importance** of the text

### Description Lists
* Used like a term and definition pair and indents appropriately
* `<dl>` Creates the Description List `</dl>`
 * `<dt>` Is the description term `</dt>`
 * `<dd>` Is the description definition and is indented automatically `</dd>`
```
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>
  <dt>CSS</dt>
  <dd>Cascading Style Sheets</dd>
</dl>
```
* Output will look something like this: 

```
HTML

    HyperText Markup Language

CSS

    Cascading Style Sheets
```

### Quotations
#### Block Quotes
* Block quotes element is used to set apart a section quoted from another source
 * This is just like in your papers you write for school
* `<blockquote>` Quotation from the source `</blockquote>`
* If you have a url source you add it to the opening of the element with the `cite` attribute
 * `<blockquote cite="https://www.website.com/path/to/quotation>` Quotation from the source `</blockquote>`
* If you have multiple paragraphs to quote you simply use the `<p></p>` element for each paragraph

  ```
   <blockquote cite="https://www.website.com/path/to/quotation>
    <p> Quotation from the source </p>
    <p> More quotation </p>
    <p> you get the point </p>
   </blockquote>
  ```
* If you want to show the citation you use `<cite></cite>` as its own element instead of an attribute of blockquote
 * This works best within a div element or some other element to keep them together


```
<div>
  <blockquote cite="https://www.freecodecamp.org/news/learn-to-code-book/">
    Can you imagine what it would be like to be a successful developer? To have built software systems that people rely upon?
  </blockquote>
  <p>—Quincy Larson, <cite>How to Learn to Code and Get a Developer Job [Full Book].</cite></p>
</div>
```

#### Inline Quotes
* used for shorter quotes from sources within the paragraph.
* `<q>` words from the source `</q>`
* Just like blockquote, you can cite within the opening

```
<p>
  As Quincy Larson said,
  <q cite="https://www.freecodecamp.org/news/learn-to-code-book/">
    Momentum is everything.
  </q>
</p>
```


#### Abbreviation Element `<abbr></abbr>`
* Terms like HTML (which is an acronym) need explaining behind the scenese
* By itself `<abbr>` will identify that an acronym or abbreviation has been used
* Along with `title` it will define its meaning
```
<p>
 <abbr title="HyperText Markup Language">
  HTML
 </abbr>
 is the foundation of the web
</p>
```

#### Address Element `<address></address>`
* Works like a div element but with semantic meaning and specific formatting
* `<br>` or the line break element shows the division between the parts of the address
* for phone numbers create an anchor element with the href starting with "tel:+" then the number
* for email contact create an anchor element with the href starting with "mailto:" then the email
```
<address>
  <h2>Company Name</h2>
  <p>
    1234 Elm Street<br />
    Springfield, IL 62701<br />
    United States
  </p>
  <p>Phone: <a href="tel:+15555555555">+1 (555) 555-5555</a></p>
  <p>Email: <a href="mailto:contact@company.com">contact@company.com</a></p>
</address>
```


#### Dates and Times `<time></time>`
* Time element is used to represent time for display
 * Operating solo it just alerts screen readers and gives semantic meaning to the text you input
* `datetime` attribute shares the time value in a machine readable format
 * must be a valid year, valid month, valid time, local date, global date, or valid duration string
 * ISO 8601 format. ISO 8601 is an international standard to represent dates and times.
  * The first part of that value is the year, month and day. The capital T in the value is a separator between the date and time.
  * `2025-11-18T08:53` or YYYY-MM-DD (T separator for time)


|year|-|month|-|day|time separator|hour|:|minute|:|second|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|yyyy|-|mm|-|dd|t|hh|:|mm|:|ss|
|2026|-|01|-|25|t|12|:|03|:|00|



```
<p>The reservations are for <time datetime="20:00">20:00 PM</time> </p>
<p>The graduation will be on <time datetime="2024-06-15T15:00">June 15</time> </p>
```


## Special Situations

### Subscript <sub></sub>
* 
