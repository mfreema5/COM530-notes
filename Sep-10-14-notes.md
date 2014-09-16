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

----

##Modernizr is teh Awesome

[**Modernizr**](http://modernizr.com/): a JavaScript library that detects HTML5 and CSS3 features in the user’s browser.

Checks for HTML5 elements; if they aren't recognized, loads them into the browser's brain via Javascript.


```html
<script src="modernizr.custom.99475.js"></script>
````

Automatically adds class "js", *if the browser supports javascript.*

The existence (or non-existence) of class “`.js`” becomes a boolean for styles.

Now we can:
```html
.js .hamburger { display: block; }

.hamburger { display: none; }
```

----

##Reset CSS

###The foundational CSS Reset removes the inconsistent styling of HTML elements provided by browsers. This creates a dependably flat foundation to build upon. With CSS Reset loaded, write explicit CSS your project needs.

[http://yui.yahooapis.com/3.17.2/build/cssreset/cssreset-min.css](http://yui.yahooapis.com/3.17.2/build/cssreset/cssreset-min.css)

```html
/*
YUI 3.17.2 (build 9c3c78e)
Copyright 2014 Yahoo! Inc. All rights reserved.
Licensed under the BSD License.
http://yuilibrary.com/license/
*/

html{color:#000;background:#FFF}body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,code,form,fieldset,legend,input,textarea,p,blockquote,th,td{margin:0;padding:0}table{border-collapse:collapse;border-spacing:0}fieldset,img{border:0}address,caption,cite,code,dfn,em,strong,th,var{font-style:normal;font-weight:normal}ol,ul{list-style:none}caption,th{text-align:left}h1,h2,h3,h4,h5,h6{font-size:100%;font-weight:normal}q:before,q:after{content:''}abbr,acronym{border:0;font-variant:normal}sup{vertical-align:text-top}sub{vertical-align:text-bottom}input,textarea,select{font-family:inherit;font-size:inherit;font-weight:inherit;*font-size:100%}legend{color:#000}#yui3-css-stamp.cssreset{display:none}
```

----

[https://developer.mozilla.org/en-US/docs/Web/CSS/text-size-adjust](https://developer.mozilla.org/en-US/docs/Web/CSS/text-size-adjust)

On mobile devices, the `text-size-adjust` **CSS** property allows Web authors to control 	if and how the text-inflating algorithm is applied to the textual content of the element it is applied to.


----

Basic, grid-based design for the web.

Repeating, predictable grid.








