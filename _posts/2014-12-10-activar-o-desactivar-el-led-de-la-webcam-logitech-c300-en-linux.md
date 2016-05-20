---
id: 163
title: Activar o desactivar el led de la webcam logitech c300 en linux
date: 2014-12-10T10:23:57+00:00
author: stephenchow
layout: post
guid: http://stephenchow.es/?p=163
permalink: /2014/12/activar-o-desactivar-el-led-de-la-webcam-logitech-c300-en-linux/
categories:
  - GNU/Linux
---
Si necesitas activar o desactivar el led de la webcam logitech c300 en linux se puede hacer mediante el programa: uvcdynctrl
  
Bajo debian instálalo con apt:
  
apt-get install uvcdynctrl
  
Luego en línea de comandos usa:
  
para desactivarlo:
  
uvcdynctrl --device=video0 -s 'LED1 MODE' 0
  
Para activarlo permanentemente, grabe o no:
  
uvcdynctrl --device=video0 -s 'LED1 MODE' 1
  
Para dejarlo automático:
  
uvcdynctrl --device=video0 -s 'LED1 MODE' 3
  
y para que parpadee:
  
uvcdynctrl --device=video0 -s 'LED1 MODE' 2
  
Puede que necesites cambiar el dispositivo, habitualmente el primer dispositivo de video se encuentra en video0
  
En el fichero /usr/share/uvcdynctrl/data/046d/logitech.xml puedes encontrar más comandos que quizás funcionen con esta u otra cámara. **Úsalos con precaución, no me hago responsable del daño que puedas causar a tu cámara.**
  
Después de activarlo puedes comprobarlo con cheese o algún programa que haga uso de la webcam.
  
La idea la he sacado de <a href="http://www.togaware.com/linux/survivor/Video_Camera.html" target="_blank">togaware.com</a> aunque las instrucciones que vienen ahí no funcionan con esta cámara.