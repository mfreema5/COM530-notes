#22 Oct 14

```HTML
<label for="FOO">Username</label>
<input type="text" name="username" id="BAR" />
```

`FOO` must *exactly* match some `BAR`.


[formalize.me](http://formalize.me/)

* Get all agents to display the same

```HTML
<head>
<link rel="stylesheet" href="formalize.css" />
<script src="jquery.formalize.js"></script>
</head>
```

"CDN" - Content Delivery Network

```HTML
<script src="//ajax.googleapis.com/ajax/libs/jquery/2.1.1/jquery.min.js"></script>
```

```HTML
<script src="/assets/js/jquery.formalize.js"></script>
```

"[Attribute selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors)"

>Attribute selectors select an element using the presence of a given attribute or attribute value.

----

`[attr]` &ndash;
Represents an element with an attribute name of attr.

`[attr=value]` &ndash;
Represents an element with an attribute name of attr and whose value is exactly "value".

`[attr|=value]` &ndash;
Represents an element with an attribute name of attr whose value is a whitespace-separated list of words, one of which is exactly "value".

`[attr~=value]` &ndash;
Represents an element with an attribute name of attr. Its value can be exactly “value” or can begin with “value” immediately followed by “-” (U+002D). It can be used for language subcode matches.

`[attr^=value]` &ndash;
Represents an element with an attribute name of attr and whose value is prefixed by "value".

`[attr$=value]` &ndash;
Represents an element with an attribute name of attr and whose value is suffixed by "value".

`[attr*=value]` &ndash;
Represents an element with an attribute name of attr and whose value contains at least one occurrence of string "value" as substring.

----

sidebar: [Accessible Rich Internet Applications (ARIA)](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA)

----


[MDN &ndash; JavaScript Reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference)



```
html.no-js label { display: block; }
html.has-js label { display: FOO; }
```

```
<html lang="en" class="no-js">
```

Document Object Model &ndash; "DOM"

Evented language &ndash; "Nothing ever happens until something happens"


| Objects                | Events |
|------------------------|--------|
| have properties        |
| have methods/functions |


HTML is the document object.

There is also the window object:
```JavaScript
window.innerHeight;
```

`onLoad` bad.  `ready` good. &ndash; [api.jquery.com/ready](http://api.jquery.com/ready/)

"`$`" gets aliased to the jquery object

```JavaScript
$(document).ready(handler);
```

after document is ready, go after "no-js" class

```
$('html')
```

Equivilent to `CSS` selecting `html` elements.

Anyway, then you can manipulate the object you've found.


[api.jquery.com/category/forms](http://api.jquery.com/category/forms/)

Querying form info.




getters vs. setters







