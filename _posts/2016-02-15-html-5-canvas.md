---
layout: post
published: false
author: Sanjay
title: "Html 5 Canvas "
---


## HTML 5 CANVAS
With the recent development of HTML language  the new tag called CANVAS has changed the way the graphics has been used , with the help of this tag we can draw shapes of anykind like rectangle,circle and triangle and this tag is implemented by using Javascript .All you need to know is Basic understanding of HTML and Javascript below is an example on how to use canvas Tag 

### In Html 
{% highlight html %}
<canvas id="myCanvas" width="200" height="100" >
</canvas>
{% endhighlight %}
### In Javascript
{% highlight html %}
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.fillStyle = "yellow";
ctx.fillRect(0,0,150,75);
</script>
{% endhighlight %}

![alt text]https://github.com/coderlogue/coderlogue.github.io/blob/master/_posts/Untitled.png
If you have observed by getting the element id of the tag we can create lot stuff using the functions of javascript which looks even more cool .
The various functions which javascript provide is 
1.
2.

