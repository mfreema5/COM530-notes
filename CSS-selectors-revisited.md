#CSS selectors (re-visited)

##Basic selectors

(Quotes from: [Mozilla Developer Network: Selectors](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors).)

>In addition to tag names, you can use attribute values in selectors

>If more than one rule applies to an element and specifies the same property, then CSS gives priority to the rule that has the more specific selector. An ID selector is more specific than a class selector, which in turn is more specific than a tag selector.

|Kind of selector| example   | notes                                                     |
|----------------|-----------|-----------------------------------------------------------|
| *class*        | .foo      |  Classes can apply to multiple, *different* elements      |
| *ID*           | #foo      |  IDs are unique (on a page)                               |
| *pseudo-class* | :foo      |  These are pre-defined.  See list below                   |
| *descendant*   | foo bar   |  Only those “bar” that are a descendent of “foo”          |
| *child*        | foo > bar |  A child is an *immediate* descendant                     |
| *first-child*  | foo:first-child | The first child only                                |
| *sibling*      | bar+ baz  | The next child of the same parent                         |
| *unrelated*    | foo, bar  | The rule is applied to both “foo” and “bar” independently |

###Pseudo-class selectors

* :link
* :visited
* :active
* :hover
* :focus
* :first-child
* :last-child
* :nth-child
* :nth-last-child
* :nth-of-type
* :first-of-type
* :last-of-type
* :empty
* :target
* :checked
* :enabled
* :disabled

##Attribute selectors

Re: [Mozilla Developer Network: Attribute selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors)

* `[attr]` &ndash; Represents an element with an attribute name of attr.
  * `span[lang]` &ndash; Any span with an explicitly defined “lang” attribute
* `[attr=value]` &ndash; Represents an element with an attribute name of attr and whose value is exactly "value".
  * `span[lang="en-us"]` &ndash; Any span with a “lang” attribute of exactly “en-us”
* `[attr|=value]` &ndash; Represents an element with an attribute name of attr whose value is a whitespace-separated list of words, one of which is exactly "value".
  * `span[lang|="en-us"]` &ndash; Any span with one or more “lang” attributes, at least one of which is “en-us”
* `[attr~=value]` &ndash; Represents an element with an attribute name of attr. Its value can be exactly “value” or can begin with “value” immediately followed by “-” (U+002D). It can be used for language subcode matches.
  * `span[lang~="zh"]` &ndash; Any span with a “lang” that attribute matches “zh(-.)*” (e.g., “zh”, “zh-TW”, etc.)
* `[attr^=value]` &ndash; Represents an element with an attribute name of attr and whose value is prefixed by "value".
  * `a[href^="#"]` &ndash; All links to urls starting with “#”
* `[attr$=value]` &ndash; Represents an element with an attribute name of attr and whose value is suffixed by "value".
  * `a[href$=".cn"]` &ndash; All links to urls ending in “.cn”
* `[attr*=value]` &ndash; Represents an element with an attribute name of attr and whose value contains at least one occurrence of string "value" as substring.



