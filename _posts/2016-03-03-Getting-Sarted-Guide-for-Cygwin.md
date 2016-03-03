---
layout: post
published: true
title: "Getting-Sarted-Guide-for-Cygwin"
---

Windows Operating System is well known for Graphical User Interface and easy to work with. But the Problem is GUI based softwares doesn't provide the flexibility and the features that CUI based tools provides and there are wide range of reasons for that. Lets not dig deep into these reasons.<br/>

CUI based tools requires commands to be memorized as these provides great features its hard to remember these commands at first but once you get used to these then you will never leave your fingers from your terminals and it also improves your productivity.If you are a Windows user and you wanna get the Linux experience then Cygwin is for you.<br/>

## What is Cygwin?
Cygwin is a command line utility for windows. It compiles most UNIX software to run on the top of Windows i.e., it ports software running on POSIX systems to windows. In short it is a Linux shell for Windows.<br/>

## How to Install Cygwin?
[Cygwin Install](https://cygwin.com/install.html)
This install is similar other windows software install.During the install it downloads few packages based on the mirror site you opted to install. <br/>

## How to Install Packages using Cygwin?
You can use the power of linux by downloading the packages from cygwin on windows.To download the packages cygwin uses package managers like [apt-cyg](https://code.google.com/archive/p/apt-cyg/), [cyg-apt](http://www.lilypond.org/~janneke/software/cyg-apt) similar to apt-get used by Ubuntu, yum/dnf by Fedora, pacman by Arch, or brew by Mac OS X.  <br/>

apt-cyg is the widely used package manager.
To install apt-cyg Open Cygwin and then uses these commands to install: <br/>

lynx -source rawgit.com/transcode-open/apt-cyg/master/apt-cyg > apt-cyg   <br/>
install apt-cyg /bin <br/>


## Commonly used Commands

### To install packages:
{% highlight html %}
apt-cyg install package_name
{% endhighlight %}

Ex:
apt-cyg install git <br/>
apt-cyg install vim <br/>
apt-cyg install curl <br/>
apt-cyg install wget <br/>
apt-cyg install nano <br/>
apt-cyg install python <br/>
apt-cyg install bash-completion. <br/>



### To remove a package:
{% highlight html %}
apt-cyg remove package_name
{% endhighlight %}
Ex:
apt-cyg remove wget <br/>


### To update a package:
{% highlight html %}
apt-cyg update package_name
{% endhighlight %}
Ex:
apt-cyg update git <br/>


### To list all installed packages:
{% highlight html %}
apt-cyg list 
{% endhighlight %}


## To start a program or open a file or URL
cygstart is a command-line tool which allows you to let Windows start a program  or  open  a  file or URL in its associated application. <br/>

 
### To open a new bash window

{% highlight html %}
 cygstart bash 
{% endhighlight %}

###  To open a url in your default browser

{% highlight html %}
cygstart url
{% endhighlight %}
Ex: cygstart http://www.coderlogue.com 

### To open a file

{% highlight html %}
 cygstart --maximize path_to_the_file
{% endhighlight %} 
Ex: cygstart --maximize ~/projects/whatever/design.doc <br/>
 
### To opens a windows explorer window in the current directory

{% highlight html %}
cygstart . 
{% endhighlight %}
 
### Note:
ctrl+l clears the terminal    
















