# Mensajeitor Tagboard v1.8.9 r4

¿Que es un tagboard?

Un tagboard ofrece a los visitantes de un sitio web la posibilidad de que expresen libremente opiniones, comentarios, inquietudes, hagan publicidad de sus webs, ayudar los visitantes, etc, todo de una forma rapida, sencilla, sin la complejidad que ofrece un servicio de foros u red social, pero con la velocidad en tiempo real de respuesta de los mensajes publicados.

El funcionamiento del servicio es muy sencillo, el TagBoard se modifica con cada comentario y se actualiza independientemente del resto de la página.

<img width="226" height="444" alt="imagen" src="https://github.com/user-attachments/assets/1c499fcb-d839-419b-8444-160ff255406b" />

Este es un respaldo de [Mensajeitor v1.8.9](https://web.archive.org/web/20111029051917/http://www.mensajeitor.com/index.php?pag=docs.php) creado en el 2006, 
para fines de estudio y arqueología digital. También revisar el [Tagboard de Mi Arroba](https://web.archive.org/web/20040904063552/http://miarroba.com/tagboard/index.php)

Entre sus funcionalidades se cuentan la opción de introducir nicks asociados a una url o e-mail, censurar palabras, cuenta con un sistema de smileys (caretos o emoticons), incluye compatibilidad con php-nuke (versión Mensajeitor Nuked) y emplea una hoja de estilos CSS (Cascade Style Sheet) lo que nos permite definir el diseño html en un archivo a parte.

<img width="475" height="207" alt="imagen" src="https://github.com/user-attachments/assets/02efda42-c9f8-44b2-a12d-c64a8bd89aab" />


Mensajeitor es un script en lenguaje PHP pensado para ser rápido de utilizar, de instalar y de cargar. Su creación se debe a los pocos tag boards que habia y que eran exclusivos de algunas webs ya que no se podian encotrar en ninguna página de scripts. El nombre fue idea de "Lowraider" en el canal #granaveria del irc-hispano y también inicialmente apoyado por webmasters de este canal. Al poco tiempo después se hizo esta web para publicarlo y se ha ido manteniendo la misma filosofía inicial, velocidad, facilidad y eficacia.

## Requerimientos

Obviamente Mensajeitor requiere un servidor con PHP funcionando, no lo he probado en versiones inferiores a la 4.0.4 pero probablemente funcione. La opción `register_globals` tiene que estar activada en versiones inferiores a la 1.8 y tiene que tener permisos para escribir en los ficheros de texto. Algunos servidores requieren permisos de ejecución para la función filesize.

## Licencia

La licencia es GPL v2, puedes distribuir y modificar el código libremente. Más detalles en el archivo LICENSE que trae el Mensajeitor 1.8 o superior.

```text
This program is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 2 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program; if not, write to the Free Software Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA 02111-1307 USA
```

## Créditos

Gracias a: willem, paharito, Jizu, perico, loading, a la gente del canal #granaveria, #ayuda_web y #php-developer y a todos los que han puesto Mensajeitor en su web.

## Instalación

La instalación del Mensajeitor es bastante sencilla.

1. Descomprime el archivo que te has bajado en un directorio llamado mensajeitor, por ejemplo.

2. Sube el directorio completo a tu servidor de forma que queden todos los archivos dentro de la carpeta mensajeitor

3. Si tu servidor necesita permisos (Iespana por ejemplo no los necesita y cualquier servidor windows tampoco) dale 666 a los archivos .txt y 776 a la carpeta smilies. Si aún así sigue dando errores de permisos dale 777 a todos los archivos.

4. Pon la url directa hacia el archivo mensajeitor.php en tu navegador para comprobar que funciona. Si ves el código en vez del Mensajeitor, quiere decir que tu servidor no tiene PHP funcionando. Ejemplo: http://www.miweb.com/mensajeitor/mensajeitor.php

5. Ahora tienes que editar el código de tu página y poner en algún lugar entre `<body>` y `</body>` el siguiente código:

```html 
<iframe marginwidth="0" marginheight="0" src="mensajeitor/mensajeitor.php" frameborder="0" width="175" height="325" scrolling="no"></iframe>
```

Dónde pone `src="mensajeitor/mensajeitor.php"` tendrás que poner la url absoluta o relativa al archivo del mensajeitor.

6. Solo te falta configurar el Mensajeitor. Abre el archivo `conf.php` con un editor de texto plano como el notepad o el nano y modifica las opciones. Una vez modificado, sube el archivo.

7. Ya tienes instalado el Mensajeitor! Si te sigue sin funcionar, vuelve a repasar los pasos a seguir y si aún no consigues que funcione, envía un mail desde aquí indicando el servidor, la url donde está el Mensajeitor, versión del Mensajeitor y el error que te da.
 

## Smileys

Lista completa de Smileys disponibles con Mensajeitor:

- ^_^ felicidad
- :) sonrisa
- :P lengua
- :| mustio
- ;) feliz
- :( triste
- xD carcajada
- -_- deprimido
- 8| sorprendido
- :D sonriente

## FAQ

¿Puedo borrar lo que sale justo debajo del Mensajeitor? 

Todo el mundo que pregunta eso es porque no ha configurado el mensajeitor. Edita el archivo `mensajeitor.php` (o usa el panel disponible en utilidades) con algún editor de texto y mira la opción $mostrar_features . Nada más simple que escribir un OFF en vez del ON.

¿Puedo poner Mensajeitor en un servidor sin php? 

No, Mensajeitor está programado en un lenguaje server-side, en este caso PHP y necesita estar en un servidor con php instalado. Ejemplos de estos servidores son: www.iespana.es y www.tripod.es

¿Tengo que borrar los mensajes de mi antiguo Mensajeitor para instalar una nueva versión? 

No, por ahora todas las versiones de Mensajeitor formatean el texto del mismo modo.

Acabo de instalar la versión 1.5 o superior y aún tengo el `muestra_mensajeitor.php` de otra versión. ¿Lo puedo Borrar? 

Si, el Mensajeitor 1.5 p superior no requiere el archivo `muestra_mensajeitor.php`, puedes borrarlo tranquilamente.

¿Cómo borro mensajes puestos en el Mensajeitor? 

Para hacer esto tienes que editar el archivo mensajeitor.txt con el riesgo de que si lo haces mal todos los mensajes se verán mal. Cada mensaje está separado por `#-#` No lo borres si quieres que funcione. También puedes usar el panel que hay por separado.

¿Cómo me identifico para usar mi nick protegido? 

Abre la dirección http://www.tuweb.com/mensajeitor/mensajeitor.php?status=administrator y te aparecerá un campo donde colocar tu contraseña

¿Cómo puedo hacer el campo de mensaje multilínea? 

Se pude cambiar el campo del mensaje abriendo el mensajeitor.php con un editor de texto plano, como por ejemplo el Bloc de Notas, buscando la línea:

```html
<input type="text" name="titulo" size="21" value="<?=$mensa_defecto;?>"
 class="form" onfocus="a1(this,'<?php echo $mensa_defecto; ?>');"
 onblur="a2(this,'<?php echo $mensa_defecto; ?>');" />
```

Y cambiándola por:

```html
<textarea name="titulo" cols="21" rows="2" class="form" 
onfocus="a1(this,'<?php echo $mensa_defecto; ?>');" 
onblur="a2(this,'<?php echo $mensa_defecto; ?>');">
<?=$mensa_defecto;?></textarea>
```


