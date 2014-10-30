#Oct-29-14 in-class notes


* Check boxes are so small
  * The label tag becomes part of what can be checked (if you use the html element correctly)

(formalize css)

----

"Tonight is the beginning of the end."

* Expanded web-presence project
* Quick refresher on media queries
  * "`min-width` is the only one you need"
* Web-fonts, font-stacks & JS-loading fonts
  * [Butterick’s Practical Typography](http://practicaltypography.com/)

----

#Project 4

* Due on Nov. 19th.
* Expand single-page website into multi-page website
* "Creative ways to present your work."
* "Mobile-first design techniques"

* Deliverables
  * Link to github
  * Link to live page
  * Self-critique
    * Optional: detailed list o' improvements.

* Requirements (among others)
  * Valid HTML
  * The same, single-CSS file for *every* webpage in project
  * Media-queries, em-based units
  * JS that doesn't throw errrors

----

* 05-Nov &ndash; work in class.
* 12-Nov &ndash; (drifted)
* 26-Nov &ndash; no class (T-day)
* 03-Dec &ndash; last class

----

##Mobile-first design

Block-elements default to 100% width (of containing block).  So, making anchor (`<a>`) element "`display: block`", you get a clickable area that's the width of the containing block.

Ideal: when you cross media-query width, the length of lines shouldn't visibly change, but just stop expanding.

Use min-width only.  In "em" units.

##Using fonts from Google

"`@fonts`"



Copy "css" link from google-font webpage
* Loads CSS file, but isn't responsive.
* "Web-font loader"
 * Lets us track if fonts get loaded or not, etc. (see below)





##[Web-font loader](https://github.com/typekit/webfontloader)

### Events

>Web Font Loader provides an event system that developers can hook into. It gives you notifications of the font loading sequence in both CSS and JavaScript.

  * `loading` - This event is triggered when all fonts have been requested.
  * `active` - This event is triggered when the fonts have rendered.
  * `inactive` - This event is triggered when the browser does not support linked fonts *or* if none of the fonts could be loaded.
  * `fontloading` - This event is triggered once for each font that's loaded.
  * `fontactive` - This event is triggered once for each font that renders.
  * `fontinactive` - This event is triggered if the font can't be loaded.

>CSS events are implemented as classes on the `html` element. The following classes are set on the `html` element:

```css
.wf-loading
.wf-active
.wf-inactive
.wf-<familyname>-<fvd>-loading
.wf-<familyname>-<fvd>-active
.wf-<familyname>-<fvd>-inactive
```

etcetcetc&ellipsis;

##Progressive enhancement

* Being aware of what happens when various things fail
 * Fail to load fonts, etc.



Is it just in your post that you have:  "&#x96; &#x2d;encrypted" (the first two characters as html-hex: "&amp;#x96;&amp;#x2d;")?  As opposed to "&#x2d;&#x2d;encrypted" ("&amp;#x2d;&amp;#x2d;")





----

(aside: [Web Open Font Format (WOFF)](https://developer.mozilla.org/en-US/docs/Web/Guide/WOFF))
