---
id: 145
title: Cómo reparar el error de processing para usar la librería serie en muchos ordenadores en MAC OS X
date: 2013-11-08T13:48:54+00:00
author: stephenchow
layout: post
guid: http://stephenchow.es/?p=145
permalink: /2013/11/como-reparar-el-error-de-processing-para-usar-la-libreria-serie-en-muchos-ordenadores-en-mac-os-x/
categories:
  - Bofh
  - GNU/Linux
---
Cuando un usuario no tiene privilegios para usar el puerto serie con Processing es necesario ejecutar un script que te proporciona el propio Processing que está en Tools->Fix Serial Library. Esta opción lo único que hace es ejecutar una llamada a osascript para que ejecute un applescript que a su vez va a crear un directorio en la raíz y le va a conceder todos los permisos. Como el usuario no tiene permisos para ello no puede hacerlo. Así que a través de Apple Remote Desktop o mediante la herramienta <a href="http://sourceforge.net/projects/clusterssh/" title="cssh" target="_blank">cssh</a> podéis mandar el siguiente comando a todas las máquinas:
  
`mkdir -p /var/lock &#038;& chmod 777 /var/lock`
  
Gracias al <a href="https://code.google.com/p/processing/source/browse/trunk/processing/app/src/processing/app/tools/SerialFixer.java?spec=svn10290&#038;r=10290" title="Código fuente de Processing" target="_blank">código fuente de processing</a> he podido ver lo que hacía el script para adaptar el proceso a mis necesidades. Y ahorrarme el tedioso trabajo de ir una a una cada máquina para poner solo el root y el password.
  
Se ha probado con la versión 2.08b