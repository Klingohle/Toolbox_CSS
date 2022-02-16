# CSS Highlights
## 1 Tipps and Tricks
## 2 More than basics
## 3 Good defaults
## 4 Core Topics
___
## 1 Tipps and Tricks
### <span style="color:grey">Using Variables</span>
#### In CSS you can use variable. Best is usually to give them a global scope and define them in the root section like so
``` CSS
:root {
    --green: #118320;
}

h1 {
    color: var(--green);
}
```
#### This can be extremely helpful if you have values like colors that are all over the place and need to match a certain color scheme.
## 2 More than basics
### <span style="color:grey">Specificity</span>
#### id > class > element
#### inline > referenced stylesheet
#### !important beats everything but should be rarely used 
[this specificity calculator can help](https://specificity.keegan.st/)
### <span style="color:grey">Pseudo-Classes</span>
### <span style="color:grey">Pseudo Elements</span>
### <span style="color:grey">attr()</span>

## 3 Good defaults

## 4 Core Topics
### Boxmodel
#### This concept explains how to size and layout elements. It is all about widht, height, padding, border and margin.
#### There are tons of webpages  out there showing the boxmodel concept. However there are some details that really matter:
##### As opposed the behaviour of the other elements mentioned above, margin will collapse if there are several adjacent elements. In this case whatever margin is the largest will be the margind between them.
##### as for the 'box' in boxmodel, there are usually these three to be taken into account: height&width, padding, border.MIND: that their values are usually added up which makes sizing very difficult, e.g. if you define a width and height each of 10px and then a padding of 10px and a border of 10px, the entire box will show up as 50px. You can prevent this by applying in you stylesheet 
``` CSS
* {
    box-sizing: border-box;
}
```
#### short forms regarding padding, margin
``` CSS
padding: 10px 5px 20px 15px;
```
##### this is going clockwise from top -> right -> bottom -> left, kind of trbl ;-)
##### you can apply this also to borders, but there you need to specify a general border element and then additionally a border-width like so
``` CSS
border: 10px solid black;
border-widht: 10px 5px 20px 15px;
```
#### MIND there is also a border-top-width element which may come in handy
##### as for padding, margin and border-width you can also define just 2 values, which then go into top&bottom and left&right
### CSS units
#### px -> can have different sizes depending on the screensize
#### % -> 50% means 50% of your screen size, it is adjusting, based on the size of their parent, in general it behaves like em
#### vw -> view width, based on the entire size of the screen, e.g. 100vw means 100% of the screen
#### vh -> view height, based on the entire size of the screen, e.g. 100vw means 100% of the screen
#### em -> based on the parents' font-size, typical use case: you need to give an object a padding that scales with the size of the element, in general it behaves like %
#### rem -> based on the root font-size which is typically 16px, e.g. 2rem means 200% of our root font-size; this is probably the best unit to use