---
title: HTML Template Tag
author: Sudarshan
---

### What is a HTML Template?<br/>
The HTML template element is a mechanism to hold client-side content,so that the content is not rendered when a page is loaded but it may subsequently be instantiated during the runtime using JavaScript.<br/>

### Syntax of template tag:
    {% highlight html %}
    <template>
    
    </template>
    {% endhighlight %}

### Why to use template? <br/>
Template is an inert HTML tag.<br/>
Template content is not rendered by the browser, and anything inside it is not executed,So resources like script files,styles,images,videos etc., enlosed inside it will not be fetched when intially a page is loaded which increases the performance of your site as it decreases the burden on the onload event Handler of the javascript.<br/>

Template tag is an inactive tag so the code that is enclosed inside the template will not run unless we use javascript to insert the content inside the DOM i.e., Intially template content is not a part of the DOM but later we use Javascript to load the content in to the DOM thus giving out the life to the content inside the template. <br/>

### Where templates are useful?<br/>
Templates enriches website performance widely when we implement carousel effects or other CSS Animations,where we require the content to be loaded first before the loading the rich media and other animations.Templates are also used for many other purposes checkout the references included at the end of the page.<br/>

### Support of Browssers:<br/>
Currently template element is supported by Chrome, Opera, Safari and Firefox.IE & Edge doesn't support the template tag.<br/>

Javascript code to load content inside the content:
{% highlight html %}

var template = document.querySelector('template');    
var temp_parent = template.parentNode;    
var temp_content = template.innerHTML;    
temp_parent.removeChild(template);    
temp_parent.innerHTML += temp_contents;
    
 {% endhighlight %}

Here is the [demo](http://jsbin.com/qaxiw/7/edit?html,js,output)<br/>

### More References : <br/>
1)Post by Christian Heilman : [USING TEMPLATE TO DELAY LOADING OF IMAGES](https://www.christianheilmann.com/2015/09/08/quick-trick-using-template-to-delay-loading-of-images/?utm_content=bufferdda9b&utm_medium=social&utm_source=facebook.com&utm_campaign=buffer) <br/>
2) [Introduction To Template Element](http://webcomponents.org/articles/introduction-to-template-element/) by Web Components.


