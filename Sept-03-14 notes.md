###Sept 03, 2014


browsing agent spoofer
  ID self as a google spider to get access to “locked” pages
----

* Grand-daddy:
  * SGML
    * Standard Generalized Markup Language
      * "Data serialization languages"?

----

Text/content: **XHTML**

Presentation layer: **CSS**

Behavior: **JavaScript**

`<meta charset="utf-8" />`
 ???  attribute=value

----

There is *always* a “root” element.
    <html></html>

Basic form is
    <html>
      <head></head>
      <body></body>
    </html>

----

"Quirks mode" - render pages as if it's 1998

To avoid quirks mode:
    <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">

----

Specify markup and language:
    <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">

Let's respecify what we're using:
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />

And then a title:
    <title>Title</title>

----

[validator.w3.org](http://validator.w3.org/)

----

¿ “xml preamble” ?

----

Errors cascade.

----

Old standard was 960 pixels wide (IE6 on 1024x768)

    <meta name="viewport" content="width=device-width,initial-scale=1.0" />

^(“need space before closing hash because IE sucks”)

Hard-coding scaling breaks usability (can't zoom)





