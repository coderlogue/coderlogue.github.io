---
title:  "Javascript Use Strict"
author: Sanjay
layout: post
---

Javascript being a loosely typed language we always have a privilege mode to ensure our code is syntactically correct.
This can be done by using  an expresssion called "Use Strict" which helps to throw and catch errors where ever needed.


How to use ??

Adding “use strict” as the first statement¹ in your JavaScript code will enforce Strict Mode over the entire source…


// declared globally 

"use strict";

var x =" coderlogue";

You can use it either globally or within a function. 

How to use in function ?

function doSomething() {

    "use strict";
    // this runs in strict mode
    
}


The expressions which declared globally or locally  helps in following ways 

* Using a variable (property or object) without declaring it, is not allowed.

* Defining a property more than once, is not allowed.

* Duplicating a parameter name is not allowed.

