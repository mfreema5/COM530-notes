#Class notes &ndash; 19 Nov 2014

>Set up HAML & Less on your computer by running `$ npm install -g coffee-script haml-coffee less` in your terminal.

(ToDo: Make sure this is installed on rMBP)

##HAML &ndash; [HTML abstraction markup language](http://haml.info/)

Some metasyntactic examples (taken from [github.com/haml/haml](https://github.com/haml/haml)).

```Haml
%tagname(attr1='value1' attr2='value2') Contents

%tagname#id.class

%ul
  %li Salt
  %li Pepper

%p
  Hello,
  World!
```

**Indentation** can be tabs or spaces. However, it must be consistent. Tabs and spaces can't be mixed; the same number of tabs/spaces must be used for each level, through the document.

A tag without a name defaults to a `<div>`.

```Haml
#foo Hello!
```

becomes

```html
<div id='foo'>Hello!</div>
```

###HAML Coffee

>Haml Coffee is a JavaScript templating solution that uses Haml as markup, understands inline CoffeeScript and generates a JavaScript function that renders to HTML.  ([source](https://github.com/netzpirat/haml-coffee/blob/master/README.md))

Installing HAML Coffee:

```sh
$ npm install haml-coffee coffee-script less
$ mkdir bin
$ cd bin
$ ln -s $HOME/node_modules/coffee-script/bin/coffee coffee
$ ln -s $HOME/node_modules/haml-coffee/bin/haml-coffee haml-coffee
$ ln -s $HOME/node_modules/less/bin/lessc lessc
```

**index.haml**:
```Haml
!!! 5
%html{lang:"en"}
  <head>
    %title Let's write some HAML
    %meta{charset:"UTF-8"}
  %body
    %header#header
      %h1 Hello World!
    #content
      %p
        Hey I'm some paragraph content!
  %footer#footer
```

`$ haml-coffee -r -f xhtml -i index.haml`

`[Haml Coffee] Rendering file index.haml to index.html`

```HTML
<!DOCTYPE html>
<html lang='en'>
  <head>
    <title>Let's write some HAML</title>
    <meta charset='UTF-8' />
  <body>
    <header id='header'>
      <h1>Hello World!</h1>
    </header>
    <div id='content'>
      <p>
        Hey I'm some paragraph content!
      </p>
    </div>
  </body>
  <footer id='footer'></footer>
</html> 
```

[HAML HTML-elements reference](http://haml.info/docs/yardoc/file.REFERENCE.html#html_elements)

##Less

* [LESS CSS-preprocessor](http://lesscss.org/#)

**screen.less**:
```less
@primaryColor: white;
@secondaryColor: green;

body {
  color:           @primaryColor;
  bacground-color: @secondaryColor;
}

#footer {
  color:            @secondaryColor;
  background-color: @primaryColor;
}
```

`$ lessc screen.less`

```CSS
body {
  color: white;
  bacground-color: green;
}
#footer {
  color: green;
  background-color: white;
}
```

Also can build function-like substitution. ("[mix-in](http://lesscss.org/features/#mixins-feature)")

Streamlining:

`$ lessc -x screen.less`

`body{color:white;bacground-color:green}#footer{color:green;background-color:white}`

##Final Project

Using HAML is required.  LESS is not.



