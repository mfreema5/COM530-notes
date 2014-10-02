##Layout mode

[developer.mozilla.org/CSS/Layout_mode](https://developer.mozilla.org/en-US/docs/Web/CSS/Layout_mode)

A CSS layout mode, sometimes abbreviated as layout, is an algorithm determining the position and the size of boxes based on the way they interact with their sibling and ancestor boxes. There are several of them:

The block layout, designed for laying out documents. The block layout contains document-centric features, like the ability to float elements or to lay them out over multiple columns.

*  The inline layout, designed for laying out text.
*  The table layout, designed for laying out tables.
*  The positioned layout, designed for positioning elements without much interaction with other elements.
*  The flexible box layout, designed for laying out complex pages that can be resized smoothly.
*  The grid layout, designed for laying out elements relative to a fixed grid.


##Visual Formatting Model

[developer.mozilla.org/CSS/Visual_formatting_model](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Visual_formatting_model)

###Block-level

An element is said to be block-level when the calculated value of its CSS display property is one of:

* block
* list-item
* table

###Box model

A box is rendered relative to the edge of its containing block.

Usually a box establishes the containing block for its descendants.

  (Note that a box is not constrained by its containing block; when its layout goes outside it, it is said to overflow.)


The layout of each box is defined by:
* its box dimensions: precisely defined or constrained, or not;
* its box type: an inline, inline-level, atomic inline-level, block box;
* the positioning scheme: in the normal flow, a float or absolute positioning;
* the other elements in the tree: its children and neighbors;
* the viewport size and position;
* intrinsic dimensions of contained images;
* other external information.

Each block-level element generates at least one block-level box, which is its “*principal* block-level box”.

Block-level boxen are *intended to be vertically stacked*. (Within what?)

**Types of boxen:**
* block-level box
* block container box
  * A block container box contains:
    * only other block-level boxes, or
    * only inline boxes (by creating an inline formatting context)
* block box (a block-level box that is also a block container box)

Also:
* “anonymous boxes”
  * Created on the fly by the browser to deal with unboxed text, etc. (mixes of inline and block-level boxes inside a block container box).
  * Inherits some properties, others are set to the page's(?) “initial” value.

¿¿¿
Another case which leads to the creation of anonymous block boxes is when an inline box contains one or several block boxes. In that case, the box containing the block box is split in two inline boxes - one before and one after the block box. All the inline boxes before the block box are then enclosed into an anonymous block box, so are the inline boxes following the block box. Therefore the block box becomes the sibling of the two anonymous block boxes containing the inline elements.
???


###Inline-level

An element is said to be inline-level when the calculated value of its display CSS property is:

* inline
* inline-block or
* inline-table

Visually, an inline-level element does *not* constitute blocks of contents, but is distributed in lines with other inline-level content.

Typically, the content of a paragraph, being text with different formatting such as “emphasis”, is made from inline-level elements.

  (Ah, yes!  So, for example, &lt;em&gt; is an *element*, whose visual properties we define in `css`.  It would almost never make sense to make &lt;em&gt; a block-level element.)

* “atomic inline-level boxes” - cannot be split between lines or boxen.
  * atomic
    * `display:inline-block;`
  * non-atomic (the default)
    * `display:inline;`

###Model-induced boxes

Beside the inline and block formatting contexts, CSS specifies several additional content models that may be applied to elements. These additional models, used to describe specific layouts, may define additional box types:

* The table content model may create a table wrapper box and a table box, but also specific boxes like caption boxes.
* The multi-column content model may create column boxes between the container box and the content.
* The experimental grid or flex-box content models also create additional types of boxes.

###Positioning schemes

The CSS engine positions boxen using one of the following methods:

1. normal flow
  * lay each box one after the other.
2. floats algorithm
  * extract box from normal flow
  * put it to the side of the containing box
3. absolute positioning scheme
  * box is positioned within a coordinate system
    * coordinate system is established by containing element.
  * Note: absolutely positioned element can cover other elements

(So, I'm thinking what I want to do is: &lt;section&gt; defines the coordinate system, and the &lt;div&gt; blocks it contains are positioned *absolutely* within that &lt;section&gt; block.  Meanwhile, the &lt;article&gt; and &lt;section&gt; elements just flow on the page.)

####Normal flow

In normal flow boxen are laid out one after the other.

* block formatting context ➜ laid out vertically
* inline formatting context ➜ laid out horizontally

normal flow triggered by:

* CSS position is set to static or relative, and
* CSS float is set to none.

####Floats

In float positioning, specific boxen are positioned at the beginning or end of the current line.

Text (and anything with normal flow) flows along the edge of the floating box

float positioning selected when:

* CSS float set different from “none”, and
* CSS position set to static or relative

float left ➜ at beginning of line box

float right ➜ at end of line box

  In either case, the line box is shrunk to fit alongside the float.


###Absolute positioning

In the absolute positioning, boxen:

* are removed from the flow and
* don't interact with flow elements
* are positioned relative to their containing block, using CSS properties:
    * top
    * bottom
    * left
    * right

An element is absolutely positioned when:

* CSS position is set to absolute or fixed.


*Note*: A “fixed positioned element” is an absolutely positioned element whose containing block is the *viewport*.

Such element will be *fixed on the screen* when scrolling as the viewport is not moving.

(Might be useful for page header?  Maybe stick something off to the right? Like a contact-info link?)


##Using multi-column layouts

[developer.mozilla.org/CSS/Using_multi-column_layouts](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Using_multi-column_layouts)

Bloody hell!  Why have I been futzing around with semantically-named &lt;div&gt; elements?

`<div style="column-count:2;">`

`<div style="column-width:20em;">`
