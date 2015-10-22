---
title: Converting Media formats using ffmpeg
author: Sudarshan
layout: post
---

Around the web we have seen many websites full of rich media it may be either audio,video or image to grab the user interaction.You might have come across the websites with the animated backgrounds have you ever wondered how they produce these perfect gifs format images & use them as background. <br/>
Some developers use the videos as background removing controls and audio from it.And to achieve these many developers use a simpe,open source,command-line tool ffmppeg.It converts one media format to other format losslessly with out much effort and it requires almost no code except few commads to create those.
<br/> 

Download latest_buids of [ffmpeg](http://ffmpeg.zeranoe.com/builds/) <br/> 

### Procedure to install ffmpeg in windows<br/> 
Let say I have extracted ffmpeg file in c folder **c:\ffmpeg**<br/> 
Go to Control Panel->System->Advanced System systems then Click on Environment Variables.Then a windows popsup here under User variables for Admin section add the "**path**" variable if it doesn't exist and give its value as **c:\ffmpeg\bin;**<br/> 

Open Command Prompt and type ***ffmpeg -version*** to checkout the proper installation of ffmpeg.<br/> 
To know the formats it supports type ***ffmpeg -formats***<br/> 
For help type ***ffmpeg -h***<br/> 

### Here are the commands for various conversions:<br/> 
Lets say I have a folder media it has selena.mp4 video <br/> 

{% highlight html %}

Job1:
  To extract Mp3 from video  
Command:
  ffmpeg -i selena.mp4 selena.mp3
Explanation:
  -i := it specifies that the next token is input 
   last token is the output 
{% endhighlight %}

{% highlight html %}


Job2:
  To copy audio from video
Command:
  ffmpeg -i selena.mp4 -vn -c:a copy selena.aac
Explanation: 
  -vn := video none(Drop out the video from selena.mp4) 
  -c means codec
  a means audio 
  -c:a copy :=copy audio from the input codec
  An audio file selena.aac is the output.
{% endhighlight %}

{% highlight html %}

Job3:
  To reduce audio bitrate 
Command:
  ffmpeg -i selena.aac -ab 96k selena.aac 
Explanation: 
  -ab 96k :=audio bitrate 96kbps(kilo bits per second)

{% endhighlight %}

{% highlight html %}

Job4:
  To copy a  clip 
Command:
  ffmpeg -i selena.mp4 -ss 01:38 -t 02:00 -c copy selenaclip.mp4
Explanation: 
  -ss 01:38 := It specifies the start time of the clip 
  -t 02:00 := It specifies the duration of the clip 
  -c copy :Codec copy (It copies both audio & video) 

{% endhighlight %}

{% highlight html %}

Job5:
  To take video snapshots 
Command:
  ffmpeg -i selena.mp4 -r .01 selenapic_%04d.png 
Explanation:  
  -r .01 :=It process the input at rate of 0.1hz

{% endhighlight %}

{% highlight html %}

Job6:
  Reducing Resolution (1080pixels to 720pixels)
Command:
  ffmpeg -i selena.mp4 -vf scale=-1:720 selena720.mp4 
Explanation:
  -vf scale=-1:720 
  v :=video  
  f :=filter 
  scale :=scale filter used to change dimensions
{% endhighlight %}

{% highlight html %}

Job7:
  To generate animated gif 
Command:
  ffmpeg -i selena.mp4 selenabasic.gif
Explanation: 
  It converts a video to gif.
  The duration of the gif file is the entire duration of the video
Command:
  ffmpeg -i selena.mp4 -ss 00:00:02  -t 3 selenashort.gif
Explanation:   
  gif image is created from the video for time starting at 2seconds
  & ending at 5 seconds  

Command:
  ffmpeg -i selena.mp4 -r 2 selena.gif
Explanation: 
  -r 2 :=It takes frames at 2hz (i.e., for every 0.5 seconds)
  It also converts entire video to gif.
{% endhighlight %}

{% highlight html %}

Job8:
  To convert gifs to video
Command:
  ffmpeg -f gif -i selena.gif selenagif.mp4
Explanation: 
  -f :=force format 
  It is used to convert gif to video 
{% endhighlight %}

{% highlight html %}
Job9:
  To concatenate videos
Command:
  ffmpeg -f concat -i file_list.txt -c copy selenaconcat.mp4
Explanation: 
  concat := adds one file at the end of other files 
            in the file_list.txt file
  Inside the file_list.txt files are listed as below: 
  file 'selena.mp3'
  file 'selena720.mp3' 
{% endhighlight %}

{% highlight html %}
Job10:
  To merge Audio & Video 
Command:
  ffmpeg -i selena.mp4 -i selena.mp3 -c:v copy -c:a copy output.mp4 
Explanation: 
  It takes selena.mp4 and selena.mp3 as input files and 
merges both audio and video into output.mp4 
{% endhighlight %}

Hope you followed the post.Here is little task for you. comment out the commands giving the solutions for <br/> 
1)How to remove audio from video?<br/> 
2)How to add subtitles to the video?<br/> 




