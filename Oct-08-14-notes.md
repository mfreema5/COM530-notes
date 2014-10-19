##08 Oct 14

----

For the 21st:

  Chapters  1-6, 12-14, 18 of [EloquentJavascript.net](http://eloquentjavascript.net/)

  Mozilla Developer Network's [HTML forms guide](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Forms)

----

Next project is redesigning a web login/sign-up page.

  (*Still need to send two pages to Karl.*)

----

#Laws of Simplicity

1. Reduced
2. Organize
3. Time


##Reduce

**SHE**

  * Shrink
  * Hide
  * Embody

How are these applied to the single-page web presence project?

#### Shrink
  * Design for mobile first
  * Have a specific, limited audience in mind

#### Hide
  * Hide the content that's not for the size of display being used
  * Hide source code
  * Hide the complexity, show the essential

#### Embody
  * "Embue this [page] with some kind of value"
  * Employ specific design choices
  * "Looks like you were thinking of exactly their screen!"
  * "You have to make other people care."
  * Value in having a nice URL.
  * "Source available on GitHub."


##Organize

*"Oragnizations makes a system of many appear to be fewer."*

**SLIP**

* Sort
* Label
* Integrate
* Prioritize

####Sort
  * Focus
  * Next
  * Base

####Label

####Integrate

####Prioritize


##Time

savings, speed, simplicity

----

HTML fallback: add `<p>some info</p>` into media element.

----

Layers of web pages

* Experience
* Behavior/Performance - javascript
* Presentation - css
* Structure - html

----

modernizer adds all kinds of classes to css based on browser capabilities

  call on those classes in order to only use css features supported by the browser

----


##HTML5

clone [github.com/karlstolley/html5-forms.git](https://github.com/karlstolley/html5-forms.git)


forms require actions, e.g., "`<form action="#null">`"


(project isn't just about the displayed form, but also the structure behind it)

````
<label for="firstname">First Name</label>
<input type="text" name="firstname" id="firstname" />
````

The property "for" specifically ties the label to the thing to which it belongs.

Label tag also warns of coming form elements.


```
<input type="submit" id="submit" value="Register" />
```

The "button" elment is not an html defined thing.


Do not accept strings for dates &ndash; no way to predict what a user will do.

Phone number: type "tel"

Input elements

  button

  checkbox

  radio-button

  date

  datetime
  

See MDN for details on styling form elements.

----

javascript

```
document.write("Hello world!");
```



