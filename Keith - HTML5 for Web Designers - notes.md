#Keith, [HTML5 for Web Designers](http://html5forwebdesigners.com/)

##[Chapter 4 – &ldquo;Web Forms 2.0&rdquo;](http://html5forwebdesigners.com/forms/index.html)

>PLACEHOLDER

>The placeholder text is usually displayed in a lighter shade than an actual form field value—either through CSS, JavaScript, or a combination of both.

>In an HTML5 document, you can simply use the placeholder attribute (FIG 4.01):

```HTML
<label for="hobbies">Your hobbies</label>
<input id="hobbies" name="hobbies" type="text"
placeholder="Owl stretching">
```

----

####Testing

>Here’s a generic little JavaScript function that tests whether an element supports a particular attribute:

```JavaScript
function elementSupportsAttribute(element,attribute) {
 var test = document.createElement(element);
 if (attribute in test) {
  return true;
 } else {
  return false;
 }
}
```

>Using this function, you can make sure that a JavaScript solution is only provided to browsers that don’t support placeholder:

```JavaScript
if (!elementSupportsAttribute('input','placeholder')) {
 // JavaScript fallback goes here.
}
```

----

>AUTOFOCUS

>HTML5 allows you to do this using the Boolean autofocus attribute:

```HTML
<label for="status">What's happening?</label>
<input id="status" name="status" type="text" autofocus>
```

>The only problem with this pattern is that it can be annoying as hell. When I’m surfing the web, I often hit the space bar to scroll down to content “below the fold.” On sites like Twitter that use the auto-focus pattern, I find myself filling up a form field with spaces instead.

----

>REQUIRED

>One of the most common uses of JavaScript is client-side form validation. Once again, HTML5 is moving this solution from scripting to markup. Just add the Boolean attribute required:

```HTML
<label for="pass">Your password</label>
<input id="pass" name="pass" type="password" required>
```

>Theoretically, this allows browsers to prevent form submissions if required fields haven’t been filled out. Even though browsers aren’t doing that yet, you can still make use of the required attribute in your JavaScript form validation. Instead of keeping a list of all the required fields in your script or adding class="required" to your markup, you can now check for the existence of the required attribute.


----

>AUTOCOMPLETE

>HTML5 allows you to disable auto-completion on a per-form or per-field basis. The autocomplete attribute isn’t Boolean, yet it can only take two possible values: “on” or “off”:

```HTML
&lt;form action="/selfdestruct" autocomplete="off"&gt;
```

>By default, browsers will assume an autocomplete value of “on,” allowing them to pre-fill the form.

----

>DATALIST

```HTML
<label for="homeworld">Your home planet</label>
<input type="text" name="homeworld" id="homeworld" list="planets">
<datalist id="planets">
 <option value="Mercury">
 <option value="Venus">
 <option value="Earth">
 <option value="Mars">
 <option value="Jupiter">
 <option value="Saturn">
 <option value="Uranus">
 <option value="Neptune">
</datalist>
```

----

###Input Types


>SEARCHING

>An input element with a type value of “search” will behave much the same way as an input element with a type value of “text”:

```
<label for="query">Search</label>
<input id="query" name="query" type="search">
```

>The only difference between “text” and “search” is… the styling of search fields….

----

>CONTACT DETAILS

>There are three new type values for specific kinds of contact details:

| contact detail    | example HTML                                     |
|-------------------|--------------------------------------------------|
| email addresses   | `<label for="email">Email address</label>`       |
|                   | `<input id="email" name="email" type="email">`   |
| websites          | `<label for="website">Website</label>`           |
|                   | `<input id="website" name="website" type="url">` |
| telephone numbers | `<label for="phone">Telephone</label>`           |
|                   | `<input id="phone" name="phone" type="tel">`     |

>Once again, these fields will behave in the same way as text inputs, but browsers now have a bit more information about the kind of data expected in the field.

> [Some browsers will display] a different on-screen keyboard depending on the value of the type attribute.

----

>SLIDERS

>In HTML5, thanks to `type="range"`, browsers can now offer a native control:

```HTML
<label for="amount">How much?</label>
<input id="amount" name="amount" type="range">
```

(“Slider” as in adjusting a setting from 0 to 10.)

>By default, the input will accept a range from 0 to 100. You can set your own minimum and maximum values using the min and max attributes:

```HTML
<label for="rating">Your rating</label>
<input id="rating" name="rating" type="range" min="1" max="5">
```


####Testing

>Testing for native support of input types requires a similar trick to the test for attribute support.

```JavaScript
function inputSupportsType(test) {
 var input = document.createElement('input');
 input.setAttribute('type',test);
 if (input.type == 'text') {
  return false;
 } else {
  return true;
 }
}
```

>You can then use this function to [check] support [for an] input type:

```JavaScript
if (!inputSupportsType('range')) {
 // JavaScript fallback goes here.
}
```

----

>SPINNERS

>Other kinds of data work best when the user can see and choose the numerical value. That’s where type="number" comes in:

```HTML
<label for="amount">How much?</label>
<input id="amount" name="amount" type="number" min="5" max="20">
```

>The `number` input type is a hybrid of `text` and `range`. It allows users to enter values directly, like a `text` field, but it also allows browsers to ensure that only numerical values are entered, like a `range` control.

###Dates and times






