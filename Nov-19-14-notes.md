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

```
$ haml-coffee
Usage: coffee /usr/local/lib/node_modules/haml-coffee/bin/haml-coffee

Options:
  -i, --input         Either a file or a directory name to be compiled          
  -o, --output        Set the output filename                                   
  -n, --namespace     Set a custom template namespace                             [default: "window.HAML"]
  -t, --template      Set a custom template name                                
  -b, --basename      Ignore file path when generate the template name            [default: false]
  -f, --format        Set HTML output format, either `xhtml`, `html4` or `html5`  [default: "html5"]
  -u, --uglify        Do not properly indent or format the HTML output            [default: false]
  -e, --extend        Extend the template scope with the context                  [default: false]
  -p, --placement     Where to place the template function; one of: global, amd   [default: "global"]
  -d, --dependencies  The global template amd module dependencies                 [default: "{ hc: 'hamlcoffee' }"]
  -r, --render        Render the template into static HTML                        [default: false]
  --preserve          Set a comma separated list of HTML tags to preserve         [default: "pre,textarea"]
  --autoclose         Set a comma separated list of self-closed HTML tags         [default: "meta,img,link,br,hr,input,area,param,col,base"]
  {…etc…}
```

The Haml parser knows different HTML formats. A given template must be rendered to one of:

* xhtml
* html4
* html5

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

###Filters in Haml

The colon character designates a filter. This allows you to pass an indented block of text as input to another filtering program and add the result to the output of Haml. The syntax is simply a colon followed by the name of the filter. For example:

```haml
%p
  :markdown
    # Greetings

    Hello, *World*
```

is compiled to:

```html
<p>
  <h1>Greetings</h1>

  <p>Hello, <em>World</em></p>
</p>
```

* Built-in filters
  * `:markdown` &ndash; Parses the filtered text with Markdown.
  * `:escaped` &ndash; Works the same as plain, but HTML-escapes the text before placing it in the document.
  * `:javascript` &ndash; Surrounds the filtered text with `<script>`. Useful for including inline Javascript. 
  * `:plain` &ndash; Does not parse the filtered text. This is useful for large blocks of text without HTML tags.

###Variables in Haml

```Haml
!!!
- foobar = "Practical impact"

%html{:lang => "en"}
  %head
    %title Index and abstract
    %meta{:charset => "utf-8"}/
    %meta{:content => "width=device-width, initial-scale=1.0", :name => "viewport"}/
    %link{:href => "css/screen.css", :rel => "stylesheet"}/
  %body
    %main
      %h1
        #{foobar}
      %article#abstract
        %h2
          The research value of tracking practical impact
        %p
          Bibliometric methods are well established and widely used, but…
    %footer
```

Renders to:

```HTML
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Index and abstract</title>
    <meta charset="utf-8">
    <meta content="width=device-width, initial-scale=1.0" name="viewport">
    <link href="css/screen.css" rel="stylesheet">
  </head>
  <body>
    <main>
      <h1>
        Practical impact
      </h1>
      <article id="abstract">
        <h2>
          The research value of tracking practical impact
        </h2>
        <p>
          Bibliometric methods are well established and widely used, but…
        </p>
      </article>
    </main>
    <footer></footer>
  </body>
</html>
```

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



