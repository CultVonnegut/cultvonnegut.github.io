---
id: 121
title: Tmux atajos de teclado
date: 2013-03-21T10:00:30+00:00
author: stephenchow
layout: post
guid: http://stephenchow.es/?p=121
permalink: /2013/03/tmux-atajos-de-teclado/
categories:
  - GNU/Linux
  - tmux
---
Recientemente he empezado a utilizar tmux para hacer las cosas habituales de mi trabajo. Obviamente podría hacerlo en varias terminales. Pero hacerlo con tmux tiene varias ventajas, están todas las tareas que necesites en un sitio, puedes desconectarte de la sesión de tmux y recuperarla más tarde sin perder lo que estabas haciendo, otros usuarios pueden conectarse a una sesión de tmux y ver lo que estás haciendo. He traducido <a href="http://blog.niklasottosson.com/?p=574" title="Tmux cheat sheet" target="_blank">este post (tmux cheat sheet)</a> sobre tmux ya que comprende un resumen de atajos de teclados más usados.

<div id="attachment_127" style="width: 560px" class="wp-caption alignleft">
  <a href="http://stephenchow.es/wp-content/uploads/2013/03/tmux.png" target="_blank"><img src="http://stephenchow.es/wp-content/uploads/2013/03/tmux-1024x640.png" alt="Tmux" width="550" height="343" class="size-large wp-image-127" /></a>
  
  <p class="wp-caption-text">
    Multiplexador de terminal
  </p>
</div>

Iniciar tmux
  
`tmux`

Iniciar una sesión salvada
  
`tmux attach`

Listar sesiones
  
`tmux ls`

Iniciar una sesión compartida
  
`tmux -S /tmp/shared_session<br />
chmod 777 /tmp/shared_session #Cualquiera puede conectarse a tu sesión`

Conectarse a una sesión compartida
  
`tmux -S /tmp/shared_session attach`

Modo comando (prefijo/prefix)
  
`ctrl + b`
  
Todos los comandos siguientes empiezan con esta combinación. Hace que tmux espere un comando para ejecutarlo

Desconectar de sesión (la sesión se guarda automaticamente)
  
`ctrl + b + d`

Pantalla de ayuda
  
`ctrl + b + ?`
  
Esto mostrará todos los comandos disponibles. Si haces cambios en el archivo de configuración se verán reflejados. Pulsa q para salir de la ayuda.

Crear nueva ventana
  
`ctrl + b + c`

Renombrar la ventana actual
  
`crtl + b + , (coma)`

Cambiar entre ventanas. Las ventanas se pueden ver en la parte inferior de la ventana de tmux
  
``Recientemente he empezado a utilizar tmux para hacer las cosas habituales de mi trabajo. Obviamente podría hacerlo en varias terminales. Pero hacerlo con tmux tiene varias ventajas, están todas las tareas que necesites en un sitio, puedes desconectarte de la sesión de tmux y recuperarla más tarde sin perder lo que estabas haciendo, otros usuarios pueden conectarse a una sesión de tmux y ver lo que estás haciendo. He traducido <a href="http://blog.niklasottosson.com/?p=574" title="Tmux cheat sheet" target="_blank">este post (tmux cheat sheet)</a> sobre tmux ya que comprende un resumen de atajos de teclados más usados.

<div id="attachment_127" style="width: 560px" class="wp-caption alignleft">
  <a href="http://stephenchow.es/wp-content/uploads/2013/03/tmux.png" target="_blank"><img src="http://stephenchow.es/wp-content/uploads/2013/03/tmux-1024x640.png" alt="Tmux" width="550" height="343" class="size-large wp-image-127" /></a>
  
  <p class="wp-caption-text">
    Multiplexador de terminal
  </p>
</div>

Iniciar tmux
  
`tmux`

Iniciar una sesión salvada
  
`tmux attach`

Listar sesiones
  
`tmux ls`

Iniciar una sesión compartida
  
`tmux -S /tmp/shared_session<br />
chmod 777 /tmp/shared_session #Cualquiera puede conectarse a tu sesión`

Conectarse a una sesión compartida
  
`tmux -S /tmp/shared_session attach`

Modo comando (prefijo/prefix)
  
`ctrl + b`
  
Todos los comandos siguientes empiezan con esta combinación. Hace que tmux espere un comando para ejecutarlo

Desconectar de sesión (la sesión se guarda automaticamente)
  
`ctrl + b + d`

Pantalla de ayuda
  
`ctrl + b + ?`
  
Esto mostrará todos los comandos disponibles. Si haces cambios en el archivo de configuración se verán reflejados. Pulsa q para salir de la ayuda.

Crear nueva ventana
  
`ctrl + b + c`

Renombrar la ventana actual
  
`crtl + b + , (coma)`

Cambiar entre ventanas. Las ventanas se pueden ver en la parte inferior de la ventana de tmux
  
`` 
  
Ejemplo: ctrl + b + 1 te lleva a la ventana 1 (nota: la primera ventana es la 0)

Cambiar entre paneles (ctrl + b + teclas dirección)
  
Ahora esto tiene una particularidad, al menos en la versión que yo tengo.
  
si pulsamos ctrl+b soltamos y luego la tecla de dirección va hacia ese panel, superior, inferior etc.
  
Pero si pulsamos ctrl+b mantenemos control pulsado, soltamos la b, y pulsamos repetidamente la tecla de dirección redimensiona el panel actual.

Modo desplazamiento. Te permite hacer scroll en la ventana o panel usando RePag/AvPag.
  
`ctrl + b + PageUp`

Salir modo desplazamiento
  
`Esc o tecla q`

Los siguientes comandos están en la configuración de <a href="http://blog.niklasottosson.com/" title="Niklas Ottosson" target="_blank">Niklas</a>

Partir la ventana horizontalmente
  
`ctrl + b + h<br />
ctrl + b + % # por defecto`

Partir la ventana verticalmente
  
`ctrl + b + v<br />
ctrl + b + " # por defecto`

Aumentar panel horizontalmente
  
`ctrl +b + + (más)`

Disminuir panel horizontalmente
  
`ctrl + b + - (minus)`

Aumentar panel verticalmente
  
`ctrl + b + *`

Disminuir panel verticalmente
  
`ctrl + b + /`

El archivo de configuración de <a href="http://blog.niklasottosson.com/" title="Niklas Ottosson" target="_blank">Niklas</a>(colócalo en tu directorio home con el nombre .tmux.conf para usarlo)
  
Yo, personalmente, solo he cambiado el prefijo de ctrl + b por ctrl + a, pero lo voy a cambiar porque me da conflicto con el mismo atajo de consola ir al principio de la línea.

\# Splitting windows into panes with h and v
  
bind-key h split-window -v
  
bind-key v split-window -h

\# Set up resize-pane keys
  
bind-key + resize-pane -D 3
  
bind-key / resize-pane -L 3
  
bind-key - resize-pane -U 3
  
bind-key * resize-pane -R 3

Por otro lado la barra de estado se puede personalizar. Podéis encontrar más archivos de <a href="https://github.com/search?q=tmux&#038;ref=commandbar" title="Tmux dotfiles." target="_blank">configuración de tmux en github</a>.

Enlace al artículo original: <a href="http://blog.niklasottosson.com/?p=574" target="_blank">http://blog.niklasottosson.com/?p=574</a>