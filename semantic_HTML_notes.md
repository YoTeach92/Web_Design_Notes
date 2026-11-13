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
* 
