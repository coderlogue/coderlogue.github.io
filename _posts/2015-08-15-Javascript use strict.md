---
title:  "Javascript Use Strict"
author: Sanjay
layout: post
---

Javascript being a loosely typed language we always have a privilege mode to ensure our code is syntactically correct.
This can be done by using  an expresssion called "Use Strict" which helps to throw and catch errors where ever needed.


<h2>How to use it Globally ?</h2>

Adding “use strict” as the first statement¹ in your JavaScript code will enforce Strict Mode over the entire source…

{% highlight html %}

    // declared globally 
    
    "use strict";
    
    var x =" coderlogue";
    
{% endhighlight %}

You can use it either globally or within a function. 

<h2>How to use it Locally (In Functions) ?</h2>
{% highlight html %}

    function doSomething() {
    
        "use strict";
        // this runs in strict mode
        
    }
    
{% endhighlight %}


<h3> The expressions which declared globally or locally  helps in following ways </h3>
        Using a variable (property or object) without declaring it, is not allowed.
        Defining a property more than once, is not allowed.
        Duplicating a parameter name is not allowed.
        

    
