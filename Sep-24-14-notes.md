#Class Notes 24 Sep 2014



(First half of class: many presentations of drafts of Project 2.)

###Project 2 due date pushed back to Oct 8.

(Aside: how to merge forks?) 





* Device pixels ("physical pixels")
* Reference pixels (the pixels that the device believes it's rendering)

* For old hardware:
  * device pixel = reference pixel

* For new high-desity displays
  * (device pixels) x F = (reference pixel)
  * E.g., F = 2 for some iPhones
  * 


###[Creative Commons](https://creativecommons.org/)

* Licensing options
  * Attribution 
  * Attribution-ShareAlike 
  * Attribution-NoDerivs 
  * Attribution-NonCommercial 
  * Attribution-NonCommercial-ShareAlike 
  * Attribution-NonCommercial-NoDerivs 

* [Flicker - Creative Commons licensed images](https://www.flickr.com/creativecommons/)



3000x1996  -->  Looks like 1500x998 on Retina display.

300x200  -->  On iPhone it gets expanded to use 600x400 physical pixels.


Use `html` comments as a reminder to give attribution.

----

###Resize image to match window

```CSS
/* Responsive Images */
img {
  display: block;
  max-width: 100%;
}
```

##Media queries


###Break points

```CSS
@media screen and (min-width: 800px) {
 img { width: 60% }
 figcaption {width: 30%}
 }
```

But ems are better: 

```CSS
@media screen and (min-width: 50em) {
 img { width: 60% }
 figcaption {width: 30%}
 }
```

* Often
  * `16px = 1em`

72pt/inch
321px/inch
math?






