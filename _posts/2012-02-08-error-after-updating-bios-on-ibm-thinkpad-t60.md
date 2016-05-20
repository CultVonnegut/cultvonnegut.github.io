---
id: 81
title: Error after upgrading bios on IBM Thinkpad T60
date: 2012-02-08T23:45:02+00:00
author: stephenchow
layout: post
guid: http://stephenchow.es/?p=81
permalink: /2012/02/error-after-updating-bios-on-ibm-thinkpad-t60/
categories:
  - English Post
  - Thinkpad
tags:
  - bios
  - lenovo
  - linux
  - T60
  - thinkpad
---
[Ver este post en español](http://stephenchow.es/2012/02/error-al-actualizar-la-bios-de-un-ibm-thinkpad-t60/ "Error al actualizar la bios de un IBM Thinkpad T60")
  
After updating bios from 1.07 to 2.13 I got the error:
  
`[Ver este post en español](http://stephenchow.es/2012/02/error-al-actualizar-la-bios-de-un-ibm-thinkpad-t60/ "Error al actualizar la bios de un IBM Thinkpad T60")
  
After updating bios from 1.07 to 2.13 I got the error:
  
` 
  
After another screen show:
  
``[Ver este post en español](http://stephenchow.es/2012/02/error-al-actualizar-la-bios-de-un-ibm-thinkpad-t60/ "Error al actualizar la bios de un IBM Thinkpad T60")
  
After updating bios from 1.07 to 2.13 I got the error:
  
`[Ver este post en español](http://stephenchow.es/2012/02/error-al-actualizar-la-bios-de-un-ibm-thinkpad-t60/ "Error al actualizar la bios de un IBM Thinkpad T60")
  
After updating bios from 1.07 to 2.13 I got the error:
  
` 
  
After another screen show:
  
`` 
  
To fix we have to set default values to NIC's rom.
  
Download the Intel ethernet boot utility:
  
http://downloadcenter.intel.com/Detail_Desc.aspx?agr=Y&DwnldID=19186&keyword=%22proboot.exe%22&DownloadType=Utilities%2c+Tools+and+Examples&OSFullname=OS+Independent&lang=eng
  
I copied to a DOS usb boot pendrive. Two commands must be run:
  
1. To see NIC's Port
  
#BootUtil -p
  
2. To set default data:
  
#bootutil -nic=X -defcfg
  
Change X with the number that is returned by previous command, usually 1.
  
`Setting PXE EEPROM words back to defaults on NIC 1...done`
  
Everything smooth...
  
Another workaround is going to bios and set "Read Network ROM on Startup" disabled under Config-network.
  
<a href="http://notes.theorbis.net/2008/01/error-expansion-rom-not-initialized-pci.html" target="_blank">Source</a>
  
More info about updating and configuring Linux on this laptop and about IBM/Lenovo can be found in <a href="http://thinkwiki.org" title="Wiki with information about IBM/Lenovo laptop running Linux" target="_blank">thinkwiki.org</a>

Disclaimer: Use the above information under your own responsabilty. Stephenchow.es is not responsible of possible damages caused due to the use of this information.