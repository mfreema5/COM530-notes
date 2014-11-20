#Class notes &ndash; 19 Nov 2014

Install HAML

```bash
$ npm install haml-coffee coffee-script less
$ mkdir bin
$ cd bin
$ ln -s $HOME/node_modules/coffee-script/bin/coffee coffee
$ ln -s $HOME/node_modules/haml-coffee/bin/haml-coffee haml-coffee
$ ln -s $HOME/node_modules/less/bin/lessc lessc
```


```haml
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









