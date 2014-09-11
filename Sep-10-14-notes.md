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






