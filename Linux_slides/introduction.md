name: inverse
layout: true
class: center, middle, inverse
---
name: Inicio
#Curso Básico de Linux
[Felipe de J. Muñoz González]

[fmunoz@lcg.unam.mx](mailto:fmunoz@lcg.unam.mx)
.footnote[Introducción<br>[Descargar Presentación](http://pipemg.github.io/Linux_slides/introducción.html)]
---
## Objetivo General
#### Ofrecer al participante los conocimientos básicos para la administración y utilización del sistema operativo Linux.

<br><br>

## Objetivos Particulares

 Desempeñarse en el entorno gráfico de Gnome y Unity

 Dar uso correcto de las utilidads básicas del entorno de Linux

 Realizar tareas de administrador para el manejo del sistema

 Conocer las bases de seguridad de linux

---
name: que_es
layout: false
.left-column[
  ## ¿Qué es Linux?
<br><br>
<image src="http://blog.capacityacademy.com/wp-content/uploads/2014/11/linux-tux.png" width="160px">
]
<br><br><br><br>

.right-column[
**Linux** es un **sistema operativo gratuito** y de **libre distribución** inspirado en el sistema Unix, escrito por **Linus Torvalds** con la ayuda de miles de **programadores en Internet.**

<br><br><br><br>


**Unix** es un sistema operativo desarrollado en 1970. Una de sus mayores ventajas es que es **fácilmente portable** (PC, Mac, estaciones de trabajo y superordenadores).
]

---
template: inverse

## ¿Que es un sistema operativo?
---
name: SO

.left-column[
  ## Sistema operativo

]
.right-column[
Son programas (Software) que aportan los mecanismos y las reglas básicas para la comunicación maquina-usuario.

El **sistema operativo** es el encargado de **controlar y dirigir la computadora**. Traduciendo las instrucciones del usuario a un lenguaje que la maquina (hardware) pueda comprender.

Es el responsable de brindar una forma de **operar**, **interpretar**, **codificar** y **emitir** ordenes al **procesador central de la computadora** para que realice las tareas necesarias y especificas para completar una orden.

 - Windows
 - Lion OS, Leopard OS, ... (Mac OS)
 - Ubuntu
 - UNIX
 - Fedora
 - CentOS
 - ...

]
---
name: Historia

.left-column[
  ## Historia del Software Libre
]
.right-column[ 

- **1983**: Richard Stallman crea GNU (GNU is not Unix)

- **1989**: Primera versión de la licencia GNU GPL.

- **1991**: El núcleo Linux es anunciado públicamente

- **1992**: Las primeras distribuciones Linux son creadas.

- **1993**: +100 desarrolladores trabajan sobre Linux. 

- **1994**: Linus Benedict Torvalds presenta la versión 1.0

- **1995**: Nueva rama estable de Linux en SUN SPARC.

- **1996**: Linux 2.0, Procesamiento en paralelo

- **1998**: IBM, Compaq y Oracle dan soporte para Linux. 

- **1998**: Se desarrolla la interfaz KDE para linux

- **1999**: Aparece 2.2 del núcleo Linux y GNOME

- **2000**: La Suite de oficina StarOffice

- **2001**: Núcleo Linux 2.4, Soporta hasta 64 Gb de RAM

]
---
name: Historia

.left-column[
  ## Historia del Software Libre
]
.right-column[ 

- **2002**: La comunidad libera OpenOffice.org  1.0 

- **2005**: El proyecto openSUSE es comenzado

- **2006**: Oracle publica su propia distribución de Red Hat

- **2007**: Dell llega a ser el primer fabricante en vender una computadora personal de escritorio con Ubuntu preinstalado.

<image src="https://4.bp.blogspot.com/-8nqDqfdHGvU/WBqaz19e-KI/AAAAAAAABBM/8O1CULTur8YIijWWDJ4ioqAtXXEy-BhpACLcB/s400/linux_distros.png">

]
---
name: instalacion3

.left-column[
  ## Instalación
### - Linux
]
.right-column[

Abrimos una terminal de linux (Ctrl + Alt + T) y dentro de esta, dependiendo del sistema operativo:

<image src="http://tuxylinux.com/wp-content/themes/images/logos/ubuntu-22.png" width="18px"> Ubuntu
```remark
$ sudo apt-get install r-base
```
<image src="http://tuxylinux.com/wp-content/themes/images/logos/fedora-22.png" width="18px"> Fedora
```remark
$ su -c 'yum install R'
```

<image src="http://tuxylinux.com/wp-content/themes/images/logos/archlinux-crystal-22.png" width="18px"> Arch Linux
```remark
$ sudo pacman -S r
```
]
---


.left-column[
  ## ¿Cómo funciona?
  ### - Ejecutar desde el cmd/terminal 
  ### - Entornos graficos
]
.right-column[
#### Desde Windows:

- Opcion A:

 Inicio > Simbolo del sistema

- Opcion B:

 Buscar > CMD


#### Desde MAC/Linux:
1. Se abre la terminal


## Se ejecuta:
```remark
$ R
```


]

---
.left-column[
  ## ¿Cómo funciona?
  ### - Entornos graficos
]
.right-column[
### Rstudio

Ambiente gráfico integrado, se basa en diversos compartimentos:
 - Consola para editar codigo
 - Ventana de datos e historial
 - Ventana de la Consola
 - Ventana de gráficas y archivos

Permite importar y ver los datos de una manera gráfica 

<image src="http://www.sthda.com/sthda/RDoc/images/rstudio.png" width="380px" align="middle">
]
---
.left-column[
<br>
<image src="https://www.rstudio.com/wp-content/uploads/2016/09/RStudio-Logo-Blue-Gray-250.png" width="150px" align="middle">
]
.right-column[
<br> <br>

Importando desde el ambiente grafico


<image src="https://support.rstudio.com/hc/en-us/article_attachments/206327917/data-import-environment.png" width="550" align="rigth">

]

---

.left-column[
  ## ¿Cómo funciona?
  ### - Entornos graficos
]
.right-column[
### R commander (Rcmdr)

Es una inferfaz gráfica que cuenta con botones y menus extensos, las caracteristicas son

 - Contiene codigos precargados (SPSS, SAS o Stata)
 - No provee acceso directo a la linea de comandos de R
 - No es enriquecido gráficamente, contiene 3 paneles:
   - Ventana del script (código ejecutandose)
   - Ventana de Salida (Imprime los resultados)
   - Ventana de Mensajes(Errores/advertencias/notas) 
  

<image src="http://www.unige.ch/ses/sococ/cl/r/rcommander.menu.png" width="380" align="left">
]
---
.left-column[
<br>
<image src="http://4.bp.blogspot.com/-bVDv8F9VdLY/T0yobXtHoEI/AAAAAAAADLk/QVue51r1Hbg/s1600/logo+Rcommander.png" width="100" align="left">
]
.right-column[
<br>
Utilizando las herramientas predefinidas


<image src="Images/rcomander_analysis.jpg" width="550" align="rigth">

]

---


template: inverse

## ¿Cuál usar y como instalarlo?
---
.left-column[
 ## Comparación
]
.right-column[
<br><br>
RStudio

- Provee acceso directo al codigo en R.

- Uso para proyectos que requieren interacción directa con el código o manipulacion de datos compleja

Rcmdr

- Simple y amable para el usuario sobre todo en analisis estadísticos y diagnósticos.

- Uso para analisis tradicionales, datos convencionales y tests estadísticos.

<br>
**NOTA:** Es posible ejecutar Rcmdr desde R-Studio.
]

---
.left-column[
  ## Instalación de R-Studio
]
.right-column[
RStudio tiene diferentes versiones:
 - Version gratis para escritorio
 - Version de paga para escritorio
 - Version gratis para servidor
 - Version pro para servidor

Para descargarlo entramos a 

```
https://www.rstudio.com/products/rstudio/download/
```
<image src="Images/Rstudio_instalador.png" width="550" align="rigth">
]
---
.left-column[
  ## Instalación de Rcmdr 
<br>
<image src="Images/r-seleccionar-repositorio.png" width="150">

]
.right-column[

Ejecutamos R

```remark
[usuario@equipo ~]$ R
```

Instalamos el paquete de Rcmdr

```remark
> install.packages("Rcmdr",dependencies=TRUE)
```

Seguimos las instrucciones de la salida

```remark
Aviso en install.packages("Rcmdr", dependencies = TRUE) :
'lib = "/usr/lib/R/library"' is not writable
Would you like to use a personal library instead? (y/n) y
Would you like to create a personal library
~/R/x86_64-unknown-linux-gnu-library/2.15
to install packages into? (y/n) y
```

Se abrirá una ventana para seleccionar el repositorio de dónde descargar los paquetes necesarios. Seleccionamos el que queramos y después de aceptar empezará a descargar los paquetes.

]

---
.left-column[
  ## Ejecutar Rcmdr 

]
.right-column[

Ejecutamos R

```remark
[usuario@equipo ~]$ R
```

Cargamos la libreria de Rcmdr

```remark
> library("Rcmdr")
```
<image src="http://www.tuxylinux.com/wp-content/uploads/2013/02/r-commander-gui.png" width="600">

]





---



.left-column[
  ## Markdown extensions
  ### - Slide properties
  ### - Content classes
]
.right-column[
Any occurences of one or more dotted CSS class names followed by square brackets are replaced with the contents of the brackets with the specified classes applied:

```remark
.footnote[.red.bold[*] Important footnote]
```

Resulting HTML extract:

```xml
<span class="footnote">
  <span class="red bold">*</span> Important footnote
</span>
```
]
---
.left-column[
  ## Markdown extensions
  ### - Slide properties
  ### - Content classes
  ### - Syntax Highlighting
]
.right-column[
Code blocks can be syntax highlighted by specifying a language from the set of [supported languages](https://github.com/gnab/remark/wiki/Configuration#highlighting).

Using [GFM](http://github.github.com/github-flavored-markdown/) fenced code blocks you can easily specify highlighting language:

.pull-left[

<pre><code>```javascript
function add(a, b)
  return a + b
end
```</code></pre>
]
.pull-right[

<pre><code>```ruby
def add(a, b)
  a + b
end
```</code></pre>
]

A number of highlighting [styles](https://github.com/gnab/remark/wiki/Configuration#highlighting) are available, including several well-known themes from different editors and IDEs.

]
---
.left-column[
  ## Presenter mode
]
.right-column[
To help out with giving presentations, a presenter mode comprising the
following features is provided:

- Display of slide notes for the current slide, to help you remember
  key points

- Display of upcoming slide, to let you know what's coming

- Cloning of slideshow for viewing on extended display
]
---
.left-column[
  ## Presenter mode
  ### - Inline notes
]
.right-column[
Just like three dashes separate slides,
three question marks separate slide content from slide notes:

```
Slide 1 content

*???

Slide 1 notes

---

Slide 2 content

*???

Slide 2 notes
```

Slide notes are also treated as Markdown, and will be converted in the
same manner slide content is.

Pressing __P__ will toggle presenter mode.
]
???
Congratulations, you just toggled presenter mode!

Now press __P__ to toggle it back off.
---
.left-column[
  ## Presenter mode
  ### - Inline notes
  ### - Cloned view
]
.right-column[
Presenter mode of course makes no sense to the audience.

Creating a cloned view of your slideshow lets you:

- Move the cloned view to the extended display visible to the audience

- Put the original slideshow in presenter mode

- Navigate as usual, and the cloned view will automatically keep up with the original

Pressing __C__ will open a cloned view of the current slideshow in a new
browser window.
]
---
template: inverse

## It's time to get started!
---
.left-column[
  ## Getting started
]
.right-column[
Getting up and running is done in only a few steps:

1. Visit the [project site](http://github.com/gnab/remark)

2. Follow the steps in the Getting Started section

For more information on using remark, please check out the [wiki](https://github.com/gnab/remark/wiki) pages.
]
---
name: last-page
template: inverse

## That's all folks (for now)!

Slideshow created using [remark](http://github.com/gnab/remark).