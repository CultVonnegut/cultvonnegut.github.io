---
id: 74
title: Error al actualizar la bios de un IBM Thinkpad T60
date: 2012-02-08T23:35:00+00:00
author: stephenchow
layout: post
guid: http://stephenchow.es/?p=74
permalink: /2012/02/error-al-actualizar-la-bios-de-un-ibm-thinkpad-t60/
dsq_needs_sync:
  - 1
categories:
  - Thinkpad
tags:
  - bios
  - ethernet
  - rom
  - T60
  - thinkpad
---
[You can see this post in english (or something very similar to)](http://stephenchow.es/2012/02/error-after-updating-bios-on-ibm-thinkpad-t60/ "Error after updating bios on IBM Thinkpad T60")
  
Tras actualizar la bios de la 1.07 a la 2.13 obtengo el siguiente error:
  
`[You can see this post in english (or something very similar to)](http://stephenchow.es/2012/02/error-after-updating-bios-on-ibm-thinkpad-t60/ "Error after updating bios on IBM Thinkpad T60")
  
Tras actualizar la bios de la 1.07 a la 2.13 obtengo el siguiente error:
  
` 
  
Tras esta pantalla aparece otra:
  
``[You can see this post in english (or something very similar to)](http://stephenchow.es/2012/02/error-after-updating-bios-on-ibm-thinkpad-t60/ "Error after updating bios on IBM Thinkpad T60")
  
Tras actualizar la bios de la 1.07 a la 2.13 obtengo el siguiente error:
  
`[You can see this post in english (or something very similar to)](http://stephenchow.es/2012/02/error-after-updating-bios-on-ibm-thinkpad-t60/ "Error after updating bios on IBM Thinkpad T60")
  
Tras actualizar la bios de la 1.07 a la 2.13 obtengo el siguiente error:
  
` 
  
Tras esta pantalla aparece otra:
  
`` 
  
Para arreglarlo hay que restaurar los valores a la rom de la tarjeta de red.
  
Procedemos a descargar la Intel ethernet boot utility:
  
http://downloadcenter.intel.com/Detail_Desc.aspx?agr=Y&DwnldID=19186&keyword=%22proboot.exe%22&DownloadType=Utilities%2c+Tools+and+Examples&OSFullname=OS+Independent&lang=eng
  
Yo la copie a un pendrive con arranque dos hay que ejecutar dos comandos:
  
1. para ver el puerto de la tarjeta
  
#BootUtil -p
  
2. Recargar los valores por defecto:
  
#bootutil -nic=X -defcfg
  
Sustituir x por el número de puerto que devuelve el comando anterior, normalmente el 1.
  
`Setting PXE EEPROM words back to defaults on NIC 1...done`
  
Everything smooth...
  
Otra forma más chapucera es entrar en la bios, config y en network desactivar la opción: "Read Network ROM on Startup".
  
<a href="http://notes.theorbis.net/2008/01/error-expansion-rom-not-initialized-pci.html" target="_blank">Fuente</a>
  
Mas info sobre actualización y configuración de este portátil y sobre IBM/Lenovo en<a href="http://thinkwiki.org" title="Wiki con información sobre uso de Linux en portátiles Lenovo" target="_blank">thinkwiki.org</a>

Disclaimer: Usa la información anterior bajo tu propia responsabilidad. Stepehnchow.es no se hace responsable de posibles daños causados al seguir dicha información.