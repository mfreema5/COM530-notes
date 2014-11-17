#Class notes for 12 Nov 2014

Checkout: [Firefox Developer Edition](https://www.mozilla.org/en-US/firefox/developer/)

[viewportify](http://viewportify.hawksworx.com/) &ndash; viewport sizes seen in the wild

----

##Pull Request Project

**DUE ANY TIME BEFORE DEC 10, 5:00PM**

1. Fork fellow student's project
1. Make improvements
1. Squash multiple commits into one commit, so that pull request is just for one commit.
1. Issue pull request to master branch

###Deliverables

* An email to the instructor by the due date containing:
  * The https:// link to your pull request on GitHub
  * A one-paragraph self-critique, including details of your improvement and your use of Git

More details next week.

----
##Tumblr Theme Project

Add blogging/social component to multi-page project

Layering CSS onto content from a server (Tumblr)

* Must handle "Text" post-type
* Plus three of:
  * Photo
  * Quote
  * Link
  * Chat
  * Audio
  * Video
  * Answer

* Examples of each post-type you support

* Must use HAML HTML preprocessor
  * May use LESS CSS preprocessor

##Deliverables

* An email to the instructor by the due date containing:
  * The https:// link to your project’s GitHub repository containing your HAML/preprocessed HTML and CSS files; and optionally also your compiled HTML file
  * The URL with your live, posted project on Tumblr (either at your own domain/subdomain or at username.tumblr.com)
  * A 1-2 paragraph self-critique, including details of your experiences working with HTML/CSS preprocessors (email to instructor by due date)

----

Intro to "[Scalable and Modular Architecture for CSS (SMACSS)](http://smacss.com/)"

(Read chapters 3, 4, 5 & 6)

Split CSS into:

1. Base &ndash; element selectors, e.g., "`html{}`", "`body{}`", "`p{}`", "`h1{}`", etcetcetc.
1. Layout rules &ndash; `#id` selectors
1. Modules &ndash; `.class` selectors
1. State &ndash; "`.wf-loafing`", "`.wf-active`", etcetcetc.

(WTF is `.wf-active`, etc?)

Read only chapters 3, 4, 5 & 6.

----

##Optimization

###Google

[Google Pagespeed Tool](https://developers.google.com/speed/pagespeed/) &ndash; analyzes site's load speed

Compress the page to reduce transmission time (can you specify different compression levels?)

Cache CSS and the like (set expiry dates)

###Minify

[Minify](http://coderaiser.github.io/minify/) &ndash; a minifier of js, css, html and img files, used in Cloud Commander project.






