

#Notes on “[Easy Responsive CSS Grid Layouts: 4 Methods](http://www.sitepoint.com/css/)”
##[Nick Salloum](http://www.sitepoint.com/author/nsalloum/)

>I’m going to present four different techniques for developing your own CSS grid, and each of them are easily extendable. Here are the four methods:

1. Responsive grid layout, v1 (using negative margins)
2. Responsive grid layout, v2 (using `box‐sizing:border‐box`)
3. Responsive grid layout using table display
4. Responsive grid layout using flexbox


###CSS Common to all methods

```HTML
/* resets */
*,
*:before,
*:after {
  box-sizing: border-box;
}
.clearfix:after {
  content: "";
  display: table;
  clear: both;
}```



##Responsive gridlayout,v1(using negative margins)

HTML:

```HTML
<div class="row-2 clearfix">
  <div class="col-1-2"></div>
  <div class="col-1-2"></div>
</div><!-- /.row -->

<div class="row-4 clearfix">
  <div class="col-1-4"></div>
  <div class="col-1-4"></div>
  <div class="col-1-4"></div>
  <div class="col-1-4"></div>
</div><!-- /.row -->
```

CSS:

```html
/* grid */
[class*="row-"] {
  margin-bottom: 20px;
}
[class*="row-"]:last-child {
  margin-bottom: 0;
}
[class*="col-"] {
}

@media all and ( min-width: 768px ) {

  /* all cols margin */
  [class*="col-"] {
    margin-right: 20px;
  }
  [class*="col-"]:last-child {
    margin-right: 0;
  }

  /* make the columns responsive */
  .col-1-2 {
    float: left;
    width: 50%;
  }
  .col-1-4 {
    float: left;
    width: 25%;
  }

  /* 2 span rows */
  .row-2 {
    padding-left: 20px;
  }
  .row-2 [class*="col-"]:first-child {
    margin-left: -20px;
  }

  /* 4 span rows */
  .row-4 {
    padding-left: 60px;
  }
  .row-4 [class*="col-"]:first-child {
    margin-left: -60px;
  }
}

@media all and ( min-width: 1200px )  /* responsive changes follow */

```




##Responsive grid layout, v2 (using `box‐sizing:border‐box`)

Syntax of `margin` element:
```
margin: style                  /* One-value syntax   */  E.g. margin: 1em;
margin: vertical horizontal    /* Two-value syntax   */  E.g. margin: 5% auto;
margin: top horizontal bottom  /* Three-value syntax */  E.g. margin: 1em auto 2em;
margin: top right bottom left  /* Four-value syntax  */  E.g. margin: 2px 1em 0 auto;

margin: inherit
```



HTML:
```html
<div class="row clearfix">
  <div class="col-1-2"></div>
  <div class="col-1-2"></div>
</div><!-- /.row -->

<div class="row clearfix">
  <div class="col-1-4"></div>
  <div class="col-1-4"></div>
  <div class="col-1-4"></div>
  <div class="col-1-4"></div>
</div><!-- /.row -->

<div class="row clearfix">
  <div class="col-1-8"></div>
  <div class="col-1-8"></div>
  <div class="col-1-8"></div>
  <div class="col-1-8"></div>
  <div class="col-1-8"></div>
  <div class="col-1-8"></div>
  <div class="col-1-8"></div>
  <div class="col-1-8"></div>
</div><!-- /.row -->
```

CSS:
```html
/* grid */
.row {
  margin: 0 -10px;
  margin-bottom: 20px;
}
.row:last-child {
  margin-bottom: 0;
}
[class*="col-"] {
  padding: 10px;
}

@media all and ( min-width: 600px ) {

  .col-2-3 {
    float: left;
    width: 66.66%;
  }
  .col-1-2 {
    float: left;
    width: 50%;
  }
  .col-1-3 {
    float: left;
    width: 33.33%;
  }
  .col-1-4 {
    float: left;
    width: 25%;
  }
  .col-1-8 {
    float: left;
    width: 12.5%;
  }

}
```

##Responsive grid layout using table display

(Don't care for now.)



##Responsive grid layout using flexbox


(Don't care for now.)




