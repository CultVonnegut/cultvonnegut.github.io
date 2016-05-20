---
id: 61
title: Escritorio borroso en Lenovo Thinkcentre Serie M
date: 2012-01-18T14:32:46+00:00
author: stephenchow
layout: post
guid: http://stephenchow.es/?p=61
permalink: /2012/01/escritorio-borroso-en-lenovo-thinkcentre-serie-m/
categories:
  - Crunchbang
  - GNU/Linux
tags:
  - chrunchbang
  - intel
  - lenovo
  - linux
  - sandy bridge
---
En el trabajo tengo que cambiar de pc bastante a menudo y por lo tanto no tengo un pc fijo. Para no tener que andar reconfigurando cada poco tiempo un nuevo equipo me instalé, en un pendrive, hace tiempo una distro llamada Crucnhbang (<a href="http://crunchbanglinux.org/" title="Sitio web de #!" target="_blank">#!</a>), con la cual estoy muy contento y me siento muy cómodo trabajando con ella. A pesar de ser un pendrive de los baratos, y que tenía por ahí tirado, funciona muy bien y ahora estoy planteándome pasarla a un pendrive con mayor capacidad y mejor rendimiento en lectura/escritura, antes de que casque el pendrive, aunque he hecho una copia del mismo.
  
Crunchbang es minimalista y ligera y tiene un montón de atajos de teclados. Está basada en Debian y usa Openbox como sistema de escritorio. Trae integrado conky en el escritorio y tras la instalación nos ofrece un script de configuración donde nos permite instalar paquetes como LibreOffice, herramientas de desarrollo, pila LAMP etc.
  
La <a href="http://crunchbang.org/download/" title="Descarga Crunchbang" target="_blank">nueva versión</a> integra el nucleo 2.6.39. Pero la anterior llevaba el 2.6.32.
  
El problema ha sido que en un pc Lenovo Thinkcentre Serie M con el controlador de VGA: "Intel Corporation Sandy Bridge Integrated Graphics Controller" se veía muy borrosa la pantalla una Philips 191V. Indagando en el foro he encontrado <a href="http://crunchbanglinux.org/forums/topic/15050/solved-intel-hd-graphics-3000-sandy-bridge-incorrect-resolution" title="Foro" target="_blank">la solución</a> y era justamente actualizar al nuevo nucleo.
  
Los pasos que he seguido han sido:
  
Editar el archivo /etc/apt/source.list y activar el repositorio linux backports siguiendo <a href="http://backports-master.debian.org/Instructions/" target="_blank">las istrucciones</a>.
  
Cuando se configura el repositorio. Ya se puede actualizar el kernel nuevo
  
En mi caso he usado el kernel para la arquitectura i686
  
`En el trabajo tengo que cambiar de pc bastante a menudo y por lo tanto no tengo un pc fijo. Para no tener que andar reconfigurando cada poco tiempo un nuevo equipo me instalé, en un pendrive, hace tiempo una distro llamada Crucnhbang (<a href="http://crunchbanglinux.org/" title="Sitio web de #!" target="_blank">#!</a>), con la cual estoy muy contento y me siento muy cómodo trabajando con ella. A pesar de ser un pendrive de los baratos, y que tenía por ahí tirado, funciona muy bien y ahora estoy planteándome pasarla a un pendrive con mayor capacidad y mejor rendimiento en lectura/escritura, antes de que casque el pendrive, aunque he hecho una copia del mismo.
  
Crunchbang es minimalista y ligera y tiene un montón de atajos de teclados. Está basada en Debian y usa Openbox como sistema de escritorio. Trae integrado conky en el escritorio y tras la instalación nos ofrece un script de configuración donde nos permite instalar paquetes como LibreOffice, herramientas de desarrollo, pila LAMP etc.
  
La <a href="http://crunchbang.org/download/" title="Descarga Crunchbang" target="_blank">nueva versión</a> integra el nucleo 2.6.39. Pero la anterior llevaba el 2.6.32.
  
El problema ha sido que en un pc Lenovo Thinkcentre Serie M con el controlador de VGA: "Intel Corporation Sandy Bridge Integrated Graphics Controller" se veía muy borrosa la pantalla una Philips 191V. Indagando en el foro he encontrado <a href="http://crunchbanglinux.org/forums/topic/15050/solved-intel-hd-graphics-3000-sandy-bridge-incorrect-resolution" title="Foro" target="_blank">la solución</a> y era justamente actualizar al nuevo nucleo.
  
Los pasos que he seguido han sido:
  
Editar el archivo /etc/apt/source.list y activar el repositorio linux backports siguiendo <a href="http://backports-master.debian.org/Instructions/" target="_blank">las istrucciones</a>.
  
Cuando se configura el repositorio. Ya se puede actualizar el kernel nuevo
  
En mi caso he usado el kernel para la arquitectura i686
  
` 
  
Tras el reinicio todo se ve más claro 😛