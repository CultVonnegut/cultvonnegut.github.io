---
id: 135
title: Añadir un usuario a un grupo
date: 2013-04-09T16:19:43+00:00
author: stephenchow
layout: post
guid: http://stephenchow.es/?p=135
permalink: /2013/04/anadir-un-usuario-a-un-grupo/
categories:
  - Crunchbang
  - GNU/Linux
tags:
  - administración
  - debian
  - grupos
  - linux
  - root
  - terminal
---
`sudo usermod -a -G <em>nombredelgrupo</em> <em>usuario</em>` **Importante**: Si no se añade la opción -a al comando borrará todos los grupos y le asignára unicamente el nuevo grupo.