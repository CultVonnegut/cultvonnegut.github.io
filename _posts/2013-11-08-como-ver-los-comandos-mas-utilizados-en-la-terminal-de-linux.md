---
id: 132
title: Cómo ver los comandos más utilizados en la terminal de linux
date: 2013-11-08T10:05:42+00:00
author: stephenchow
layout: post
guid: http://stephenchow.es/?p=132
permalink: /2013/11/como-ver-los-comandos-mas-utilizados-en-la-terminal-de-linux/
categories:
  - GNU/Linux
---
 

Con el siguiente comando podemos ver la cuenta de los 10 comandos más usados en la terminal de linux:
  
`history | awk '{CMD[$2]++;count++;}END { for (a in CMD)print CMD[a] " " CMD[a]/count*100 "% " a;}' | grep -v "./" | column -c3 -s " " -t | sort -nr | nl |  head -n10`

vía [How do I see what my most used linux command are? - Super User](http://superuser.com/questions/250227/how-do-i-see-what-my-most-used-linux-command-are).

<a href="http://linux.byexamples.com/archives/332/what-is-your-10-common-linux-commands/" title="Una explicación más detallada" target="_blank"></a>