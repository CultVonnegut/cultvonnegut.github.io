---
id: 96
title: Agregar extensiones a vim para activar el resaltado de sintaxis
date: 2012-04-27T17:07:44+00:00
author: stephenchow
layout: post
guid: http://stephenchow.es/?p=96
permalink: /2012/04/anadir-extensiones-a-vim-para-activar-el-resaltado-de-sintaxis/
categories:
  - GNU/Linux
  - Vim
---
Hoy en el trabajo he necesitado editar unos archivos bash que tenían como extensión .lib, con lo cual vim no resaltaba la sintaxis correctamente. Con estos comandos podemos arreglarlo:
  
Temporalmente:
  
`:set syn=sh`
  
o permanentemente editando .vimrc:
  
`au BufNewFile,BufRead *.lib set filetype=sh`
  
Ahora vim resaltará correctamente el resaltado de dichos archivos.