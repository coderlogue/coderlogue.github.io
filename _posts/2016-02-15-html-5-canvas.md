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
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.fillStyle = "yellow";
ctx.fillRect(0,0,150,75);
{% endhighlight %}
### output
It looks like this rectangle of size 300x100 width and height respectively with the yellow color filled in it using function fillRect(0,0,150,75);
{% highlight html %}

![Untitled.png]({{site.baseurl}}/_posts/Untitled.png)

{% endhighlight %}
If you have observed by getting the element of the tag we can create lot stuff using the functions of javascript which looks even more cool .
The things which we can do with Canvas is the below list 
1. Drawing shapes
2.Animations
3.Playing with pixels of a Image
4.Text Formation 
5.Alphabets drawing
