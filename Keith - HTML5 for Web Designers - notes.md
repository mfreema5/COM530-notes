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

if (!elementSupportsAttribute('input','placeholder')) {
 // JavaScript fallback goes here.
}

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
<form action="/selfdestruct" autocomplete="off">
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






