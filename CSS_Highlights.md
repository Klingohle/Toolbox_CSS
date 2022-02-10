# CSS Highlights
## 1 Tipps and Tricks
## 2 More than basics
## 3 Good defaults
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


## 3 Good defaults