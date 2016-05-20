---
id: 68
title: Crear un disco duro desde un USB para Virtualbox
date: 2012-02-08T15:56:52+00:00
author: stephenchow
layout: post
guid: http://stephenchow.es/?p=68
permalink: /2012/02/crear-un-disco-duro-desde-un-usb-para-virtualbox/
categories:
  - Virtualbox
tags:
  - discos
  - maquina virtual
  - usb
  - virtualbox
---
Con Virtualbox es posible crear un disco duro virtual que apunte fisicamente a un pendrive usb por ejemplo.
  
Para ello hay que usar el comando vboxmanage. El inconveniente es que es necesario ejecutar el comando y la máquina virtual en modo administrador si no da error al iniciar Virtualbox.
  
Probado en:
  
Windows 7 Pro 64 bits.
  
Oracle Virtualbox 4.1.8

Para ello hay que ejecutar una consola en modo administrador:
  
-En el menu inicio escribir cmd y pulsar `ctrl+shit+enter`
  
-Ir a c:\program files\oracle\virtualbox
  
Escribir:
  
`VBoxManage internalcommands createrawvmdk -filename "Ruta\de\guardado\nombre.vmdk" -rawdisk \\.\PhysicalDriveX`
  
Donde X es el número de tu disco usb. Lo puedes ver en el administrador de discos.
  
Luego puedes indicar en la creación de la máquina virtual la ruta hasta el archivo creado. Esto lo que hace es un enlace no clona el contenido del usb.
  
Hay que abrir la máquina como administrador.
  
Fuente y capturas: <a href="http://agnipulse.com/2009/07/boot-your-usb-drive-in-virtualbox/" title="Agnipulse" target="_blank">Agnipulse.com</a>