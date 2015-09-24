---
title: Javascript Slice()
author: sudarshan
layout: post
---
# Javascript Slice() #

![cover-image](/img/jslice.png)


The slice() method is used to extract a section of an array.Selected elements of the original array are copied into a new array.


### Syntax: ###
slice(beginslice, endslice) 

### Parameters: ###
beginslice : Specifies where to begin the extraction.
endslice(optional): Specifies where to end the extraction.

### Note: ###
A negative index  indicates an offset from the end of the sequence
slice() extracts up to but not including endSlice. 
This method does not change the original array.

str.slice(3, 7) extracts the fourth character through the seventh character of an array.(where characters indexed 3,4, 5, and 6).


### Code Snippets: ###
{% highlight html %}
/*
var str1 = "Coder Logue is built using jekyll";
var slice1 = str1.slice(0);
var slice2 = str1.slice(0,-1);
var slice3 = str1.slice(4);
var slice4 = str1.slice(4, 8);
var slice5 = str1.slice(0,-8);

document.write(slice1 + "<br/>");
document.write(slice2 + "<br/>");
document.write(slice3 + "<br/>");
document.write(slice4 + "<br/>");
document.write(slice5); 
*/
{% endhighlight %}


### output: ### 
{% highlight html %}
/* 
Coder Logue is built using jekyll
Coder Logue is built using
Logue is built using jekyll
Coder Logue
Coder Logue is built using 
*/
{% endhighlight %}

