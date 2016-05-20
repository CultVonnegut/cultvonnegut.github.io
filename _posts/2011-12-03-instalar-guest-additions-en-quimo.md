---
id: 34
title: 'Instalar  guest additions en Quimo'
date: 2011-12-03T14:54:03+00:00
author: stephenchow
layout: post
guid: http://stephenchow.es/?p=34
permalink: /2011/12/instalar-guest-additions-en-quimo/
categories:
  - Virtualbox
tags:
  - linux
  - qimo
  - virtualbox
---
Tengo un niño de casi 3 años al que estoy introduciendo ya en el mundillo, para lo cual he instalado <a href="http://www.qimo4kids.com/" title="Qimo" target="_blank">Qimo</a>, que es una distribución orientada a niños que integra <a href="http://gcompris.net/-es-" title="Gcompris" target="_blank">gcompris</a>, <a href="http://tuxpaint.org/?lang=es" title="TuxPaint" target="_blank">tuxpaint</a> entre otros. Lo he instalado en <a href="https://www.virtualbox.org/" title="VirtualBox" target="_blank">Virtualbox</a>, para no tener que andar reiniciando y poder ponerlo en cualquier momento sin tener que cerrar lo que tengo abierto. He tratado de instalar las guest additions de Virtualbox, que dan soporte entre otras cosas a la gráfica para poder poner la máquina virtual a pantalla completa. He seguido los pasos de <a href="http://debiantotal.blogspot.com/2007/10/virtualbox-instalar-guest-additions.html" title="Debian total" target="_blank">DEBIAN TOTAL</a>

<pre>$ su -
Password:
# aptitude install gcc linux-headers-$(uname -r) make
.
.
.
La única diferencia con las instrucciones de la página es que he tenido que montar el cdrom primero:
#mkdir /media/cdrom
#mount /dev/cdrom /media/cdrom
# cd /media/cdrom
Por último ejecutamos el instalador:
# sh VBoxLinuxAdditions.run
</pre>

Si necesitáis más detalles podéis ver la fuente original: <a href="http://debiantotal.blogspot.com/2007/10/virtualbox-instalar-guest-additions.html" title="Debian total" target="_blank">DEBIAN TOTAL</a>