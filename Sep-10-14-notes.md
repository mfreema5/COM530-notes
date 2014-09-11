Polyfill

Mobilefirst design

Typographic scales (font size; typographic grids)

----

style declarations in css

----

###Cascading style sheets

```HTML
   <p class="important">  </p>

   <p> </p>
```

```HTML
   p {
   color:red
   }

   p.important {
   font-weight:bold
   }
```
(Does bold red)

```HTML
   p.important {
   font-weight:bold
   color:white
   }
```
(Does bold white)


----

If you specify things like "font" in the `html`, it "breaks the cascade".

----

###Scoring for styling precedence:

| entity   | score | example           |
|----------|-------|-------------------|
| Elements | 1     | `<p>`             |
| Class    | 10    | `<p class="foo">` |
| ID       | 100   | `<p id="bar">`    |

----


##Units of measure in CSS

* Fixed
  * points/pica
  * pixel

* Fluid/relative
  * %
  * em  (width of lower-case ‘m’)
  * rem (root ‘em’ units)


To determine the attribute value you want:

```target / context = result```


----

Much wailing and gnashing of teeth over `git`.

----

Old:  `<div id="page">`
Old:  `<div id="header">`


Useful reference: [developer.mozilla.org/Web/Guide/HTML5_element_list](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5/HTML5_element_list)


Some new elements for HTML5

| element     | Description |
|-------------|-------------|
| `<article>` | Defines self-contained content that could exist independently of the rest of the content. |
| `<aside>`   | Defines some content loosely related to the page content. If it is removed, the remaining content still makes sense. |
| `<main>`    | Defines the main or important content in the document. **There is only one `<main>` element in the document.** |
| `<data>`    | Associates to its content a machine-readable equivalent . (This element is only in the WHATWG version of the HTML standard, and not in the W3C version of HTML5). |






















