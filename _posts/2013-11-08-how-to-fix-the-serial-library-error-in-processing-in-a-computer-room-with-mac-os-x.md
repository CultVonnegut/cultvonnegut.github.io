---
id: 151
title: How to fix the serial library error in Processing in a computer room with MAC OS X
date: 2013-11-08T13:48:54+00:00
author: stephenchow
layout: post
guid: http://stephenchow.es/?p=151
permalink: /2013/11/how-to-fix-the-serial-library-error-in-processing-in-a-computer-room-with-mac-os-x/
categories:
  - BOFH
  - GNU/Linux
---
When an unprivileged user needs to use the serial port it is mandatory to run a script provided by Processing located in Tools->Fix Serial Library. This option just execute a call to osascript command in OS X to execute an applescript that will create a directory on root file and grant permission to the world. So the unprivileged user can't do it. So with Apple Remote Desktop or through a tool like <a href="http://sourceforge.net/projects/clusterssh/" title="cssh" target="_blank">cssh</a> the next command can be send to every computer.
  
`mkdir -p /var/lock &#038;& chmod 777 /var/lock`
  
Thanks to the <a href="https://code.google.com/p/processing/source/browse/trunk/processing/app/src/processing/app/tools/SerialFixer.java?spec=svn10290&#038;r=10290" title="Processing source code" target="_blank">processing source code</a> I was able to see what the hell was doing the script to adapt the process to my own needs. Now I can save tedious work from going machine to machine to just put the root user and password
  
Tested with versión 2.08b