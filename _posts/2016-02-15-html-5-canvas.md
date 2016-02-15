---
layout: post
published: true
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
If you have observed by getting the element id of the tag we can create lot stuff using the functions of javascript which looks even more cool .
The various functions which javascript provide is 
<ol>
<li>fillStyle -- Sets the style used when filling shapes.</li> 
<li>fillRect --Draws a filled rectangle.</li>
<li>strokeStyle --Sets the style for shapes' outlines.</li>
<li>strokeRect --Draws a rectangular outline.</li>
<li>clearRect --Clears the specified rectangular area, making it fully transparent.</li>
<li>beginPath --Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.</li>
</ol>


