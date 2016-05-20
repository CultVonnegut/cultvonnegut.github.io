---
id: 166
title: 'Activate or deactivate webcam&#8217;s led of Logitech c300 under linux'
date: 2014-12-10T10:23:57+00:00
author: stephenchow
layout: post
guid: http://stephenchow.es/?p=166
permalink: /2014/12/activate-or-deactivate-webcams-led-of-logitech-c300-under-linux/
categories:
  - GNU/Linux
---
If you need to activate or deactivate the webcam's led of a logitech c300 under linux it can be done with the software: uvcdynctrl
  
Under debian it can be installed using apt:
  
apt-get install uvcdynctrl
  
Later on terminal
  
Deactivate:
  
uvcdynctrl --device=video0 -s 'LED1 MODE' 0
  
To be always on, recording or not:
  
uvcdynctrl --device=video0 -s 'LED1 MODE' 1
  
To set it automatically, usually recording on, idle off:
  
uvcdynctrl --device=video0 -s 'LED1 MODE' 3
  
Let it blink:
  
uvcdynctrl --device=video0 -s 'LED1 MODE' 2
  
Usually the first video device is under video0, maybe you need to change that
  
In the file /usr/share/uvcdynctrl/data/046d/logitech.xml more functions can be found to be used with this or other logitech cam.
  
**Use with caution, I am NOT responsible for the harm you can cause to your cam**
  
After using the command you can check it out with cheese or any other software that make use of the webcam
  
Source: <a href="http://www.togaware.com/linux/survivor/Video_Camera.html" target="_blank">togaware.com</a> but the commands there doesn't work with this cam.