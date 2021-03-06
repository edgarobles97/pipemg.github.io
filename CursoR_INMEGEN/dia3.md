name: inverse
layout: true
class: center, middle, inverse
---
name: Inicio
#Curso de R y estadística básica
[Felipe de J. Muñoz González]

[fmunoz@lcg.unam.mx](mailto:fmunoz@lcg.unam.mx)
.footnote[Introducción<br>[Descargar Presentación](http://pipemg.github.io/CursoR_INMEGEN/Presentacion3.pdf)]

---

layout: false
.left-column[
  ## Programación
   ### Operadores lógicos y comparativos
]
.right-column[

Relaciónes
- **>** Mayor que
- **<** Menor que
- **<=** Menor o igual que
- **>=** Mayor o igual que
- **==** Igual 
- **!=** Diferente

Lógicos
- **!x** Negación (no x)
- **x & z** Conjución (x y z)
- **x && z** Conjunción(*)
- **x|y** Disyuncion
- **==** Disyuncion(*) 
- **xor(x, y)** O exclusivo (∗∗)
- **identical()** Comparar dos objetos

<small><small>
(∗) Si se escriben dos símbolos repetidos, estos tienen el mismo significado que si apareciese uno,  la diferencia consiste en que se evalúa primero la parte de la izquierda y, si ya se sabe el resultado no se sigue evaluando, por lo que pueden ser mas rapidos y eliminar errores

(∗∗) Da como valor verdadero si uno y sólo un argumento es válido.
</small></small>
]


---

layout: false
.left-column[
  ## Programación
   ### Operadores lógicos y comparativos
]
.right-column[
<br><br>
```
> x<-10; x # Asignamos a x el valor 10
> x<5 # Le preguntamos si x es menor que 5
> x>=5 # Le preguntamos si x es mayor o igual que 5
> x==5 # Le preguntamos si x vale 5
> x!=5 # Le preguntamos si x es distinto de 5
```

```
> y<-1:3; z<-3:1 # Creamos dos vectores
> identical(y,z) # Le preguntamos si son iguales
> y==z # Vemos los elementos que coinciden
> x<-1:5 # Renombramos x e y
> y<-c(2,4,3,6,5)
```

```
> x==y
> x!=y
> x[x==y]
> x[x!=y]

```
]



---

name: last-page
template: inverse

## Probabilidad
---

layout: false
.left-column[
  ## Probabilidad
   ### Espacio muestral
]
.right-column[

**Espacio muestral**  (denotado S) consiste en el conjunto de todos los posibles resultados de un experimento aleatorio.

Moneda 

```
> S<-data.frame(pos=c("H","T"))

```
Espacio Muestral de una moneda que se lanza 3 veces

```
> expand.grid(t(S),t(S),t(S))
```

Dado

```
> S<-data.frame(pos=c(1:6))

```


```
>  sample(x=c("H","T"), size=5, replace=T)

```

Espacio Muestral de un dado

```
>  expand.grid(t(S),t(S),t(S))

```


]

---

layout: false
.left-column[
  ## Probabilidad
   ### Espacio muestral
]
.right-column[
<br><br>
Espacio Muestral de Cartas Inglesas 

```
> palos<-c("D","P","T","C")

> numeros<-c(1:10,"J","Q","R")

> cartas<-as.vector(outer(numeros, palos, paste, sep=""))

> cartas<-sample(cartas)

```

Espacio Muestral de Muestreo de urnas

```
> urna=c("roja","azul","amarilla","violeta","negra","blanca")

```

```
> urnsample<-sample(urna,size=20, replace=T)

> table(urnsample)
```

]


---
layout: false
.left-column[
  ## Probabilidad
   ### Subsets de datos
]
.right-column[
<br><br>

%in%  #busqueda por elementos

```
> x <- 1:10
> y <- 8:12
> y %in% x
> y[y %in% x]

```

isin 

```
> isin(x,y) #todo el vector

```

all 
```
> x <- 1:10
> y <- c(3, 3, 7)
> unique(c(y %in% x))


```

¿Por que isin y all tienen esos resultados?


]

---

layout: false
.left-column[
  ## Probabilidad
   ### Union, Interseccion y diferencia
]
.right-column[
<br><br>
Elementos que existen en el Evento A, en el Evento B o en ambos
union(A,B)

```
> S <- expand.grid(numeros, palos)
> colnames(S)<-c("numero", "palo")
> A <- subset(S, palo == "C")
> B <- subset(S, numero %in% as.character(7:9))

> union(apply(A,1,paste, collapse=""), apply(B,1,paste, collapse=""))
```
Elementos que existen en el Evento A y en el Evento B
intersect(apply(A,1,paste, collapse=""), apply(B,1,paste, collapse=""))

```
>  intersect(apply(A,1,paste, collapse=""), apply(B,1,paste, collapse=""))

```

Elementos que existen en el Evento A pero no en el Evento B


```
> setdiff(apply(A,1,paste, collapse=""), apply(B,1,paste, collapse=""))
```

**Nota** setdiff no es simetrico y podemos calcular el complemento de todos los eventos Ej. setdiff(S,A)

]

---
layout: false
.left-column[
  ## Probabilidad
   ### Probabilidades de frecuencias relativas
]

.right-column[

<br><br>
P(A) ≈ observados / posibles ≈ S_n/n


```
> S<-data.frame(pos=c(1:6))
> posibles<-expand.grid(t(S),t(S),t(S))
> posibles[which(posibles[,1] == posibles[,2] & posibles[,3] == posibles[,2]),]
> obsv<-length(which(posibles[,1] == posibles[,2] & posibles[,3] == posibles[,2]))
> prob= obsv/length(posibles)
```

Ej. Moneda no balanceada


```
> S<-c("H","T")
> p<-c(1/3,2/3)
> sample(S, prob=p, size=1, replace=T)
> sample(S, prob=p, size=200, replace=T)

```
**WARNING:** RAM memory y probabilidades infinitecimales 


]

---
layout: false
.left-column[
  ## Probabilidad
   ### Conteo con urnas
]
.right-column[
<br>

<img src="Images/Counting.png", width=500px>

Numeros Factoriales

```
> factorial(n) 
```

Coeficiente binomial (Combinaciones) 


```
> choose(n,k)

```

]
---
layout: false
.left-column[
  ## Probabilidad
   ### Probabilidad Condicional
]
.right-column[
<br><br><br>

```
> S<-1:6
> space <- sample(S, size=100, replace= TRUE) 
> head(S) # first few rows

```


```
> E <- expand.grid(t(S),t(S),t(S))
> A <- subset(E, Var1 == Var2)
> B <- subset(E, Var1 + Var2 >= 8)

```

```
> prob(A, given = B) #no Code
> prob(B, given = A) #no Code

```




]

---
layout: false
.left-column[
  ## Probabilidad
   ### Variables Aleatorias
]
.right-column[
<br><br><br>

Definición: Una variable aleatoria X es una función X:S -> R que asocia para cada w ∈ S exactamente X(ω) = x. 

Se define como S todos los posibles resultados de el evento E

**Ejemplo:**

Definimos la variable aleatoria X como "numero de aguilas cuando se tira una moneda".

Por lo tanto si **S** es nuestro espacio muestral y **w** los sucesos posibles 


<table border=1px align="center">
<tr align="center"><th> w∈ S</th><td> AA </td><td> AS </td><td> SA </td><td> SS </td></tr>
 
<tr align="center"  margin=10px><th> X(w) = x </th><td> 2 </td><td>  1 </td><td>  1 </td><td>  0 </td></tr>
</table>


]

---
layout: false
.left-column[
  ## Probabilidad
   ### Variables Aleatorias
]
.right-column[
<br><br><br>

Escribir una formula que define una variable aleatoria dentro de una función, agregando una columna a un data.frame.


Tiramos un dado de 4 lados 3 veces y definimos nuestra variable U = X1 - X2 + X3 


Ahora podemos preguntar, ¿Cual es la probabilidad de que U > 6?


]
---

name: last-page
template: inverse

## Distribuciones de datos
---
layout: false
.left-column[
  ## Distribuciones de datos
]
.right-column[
<br><br><br><br>

**Centroide:** Conjunto de datos está asociado con un número que representa una tendencia media o general de los datos.

La **Dispersión** de un conjunto de datos está asociada con su variabilidad; Los conjuntos de datos con una dispersión grande tienden a cubrir un gran intervalo de valores, mientras que los conjuntos de datos con dispersión pequeña tienden a agruparse fuertemente alrededor de un valor central.

**Forma:** Forma exhibida por una pantalla gráfica asociada. La forma puede decirnos mucho sobre cualquier estructura subyacente a los datos, y puede ayudarnos a decidir qué procedimiento estadístico debemos usar para analizar los.

]

---
layout: false
.left-column[
  ## Distribuciones de datos
  ### Forma
]
.right-column[

**Simetría** y **asimetría** 
   - **positivamente sesgada**
   - **negativamente sesgada**

<img src="Images/tipos-asimetria.jpg", width=500px>

La **curtosis** (o apuntamiento) es una medida de forma que mide cuán escarpada o achatada está una curva o distribución. 

<img src="Images/curtosis.jpg", width=500px>

]

---


layout: false
.left-column[
  ## Estadistica descriptiva 
   ### Medidas de Forma
]
.right-column[
<br><br><br><br>


La **asimetría** (Fisher) de la muestra, se define por la fórmula

<img src="http://www.universoformulas.com/imagenes/formulas/estadistica/descriptiva/coeficiente-asimetria-fisher.jpg" width=400px>

donde S es la desviación estandar (o tipica)

<img src="http://www.universoformulas.com/imagenes/estadistica/descriptiva/coeficiente-asimetria-fisher.jpg" width=400px>

]
---


layout: false
.left-column[
  ## Estadistica descriptiva 
   ### Medidas de Forma
]
.right-column[
<br><br><br><br>


La **curtosis**  de la muestra, se define por la fórmula

<img src="http://www.universoformulas.com/imagenes/formulas/estadistica/descriptiva/curtosis.jpg" width=400px>

donde S es la desviación estandar (o tipica)

<img src="http://www.universoformulas.com/imagenes/estadistica/descriptiva/curtosis.jpg" width=400px>

]

---



layout: false
.left-column[
  ## Estadistica descriptiva 
   ### Medidas de Forma
]
.right-column[
<br><br>

Asimetria
 
```
> library(e1071)
> skewness(discoveries)
```

```
> 2 * sqrt(6/length(discoveries))
```

**Nota** si 2 * sqrt(6/n) < skewness(x) => existe un sesgo dado el signo del calculo.


Curtosis
 
```
> kurtosis(UKDriverDeaths)
```

```
> 4 * sqrt(6/length(UKDriverDeaths))
```

**Nota** abs(4 * sqrt(6/n)) < kurtosis(x) => presenta curtosis


]

---

layout: false
.left-column[
  ## Estadistica descriptiva 
]
.right-column[
<br><br><br><br>

Utilizando R. Calcula las siguientes cosas del vector 

```
x<-round(runif(20, min=1, max=100))
```

- rango
- media
- mediana/media recortada
- quantiles/quintiles/septiles
- varianza
- desviación estandar


**Nota Rcmdr**

Statistics > Summaries > Numerical Summaries

calculamos los cuantiles automaticamente

]
---

layout: false
.left-column[
  ## Estadistica descriptiva 
  ### Rangos intercuantiles y MAD
]
.right-column[
<br><br><br><br>

```
> tr=c(3,4,5,3,4,5,4,3,2,3,12,11,3,4,89)
> quantile(tr)
> quantile(tr,.25)
> quantile(tr,.10)

```

suceptibilidad de la media, mediana a valores extremos.

Rango intercuartil (**IQR**) definido por IQR = q_{0.75} - q_{0.25}

Otro método más robusto que el IQR es la Media de la desviación absoluta (**MAD**).

1. Calculamos la media (prom) 
 
2. mediana(|x{i} - prom(X)|) , para toda i

]


---

layout: false
.left-column[
  ## Observaciones Extremas
]
.right-column[
<br><br><br><br>

Problemas que pueden implicar estimaciones exageradas e "inestabilidad" estadística. Podemos considerar que estos datos pueden ser:

 - Error tipográfico (typoo)

 - Observaciónes que no eran para el estudio. (Ej. Complicaciones medicas)

 - Indican un fenomeno o una tendencia más profunda

]



---


layout: false
.left-column[
  ## Estadistica descriptiva 
   ### Grafica de caja
]
.right-column[

Estas gráficas son buenas para visualizar mucha información descriptiva de nuestros datos al mismo tiempo:

**Centroide** (estimada por la mediana)

**Dispersión**

**Forma**

**Observaciones extremas**

**Outliers** Observaciones que pasan 1.5 veces el tamaño de la caja para cualquier extremo. 


Para observar los valores outliers

```
> boxplot.stats(rivers)$out #1.5 default
```
```
> boxplot.stats(rivers, coef = 3)$out #coef=3
```

```
> boxplot(rivers, horizontal=T)

```

]

---


layout: false
.left-column[
  ## Estadistica descriptiva 
   ### Z-value
]
.right-column[
<br><br>

Valor estandarizado, cuando queremos comparar datos en escala que es independiente a la medida.

Dado X=x[1], x[2], x[3], ... ,x[n] los z-scores son z[1], z[2],...z[n] se ven definidos como

z[i]=(x[i]-median(x))/s 

donde s es la sd()


```
> ?scale

```
]
---

layout: false
.left-column[
  ## Lectura y escritura de datos.
   ### Read table, View, fix
]
.right-column[

<br><br>
```
> # Leemos el archivo tabla.csv y lo nombramos misdatos
> misdatos <- read.table("Pathway", header=FALSE, sep="", na.strings="NA", dec=".")
```

Con la función “View” visualizamos los datos que hemos cargado en memoria anteriormente.

```
> View(Datos) #ver los datos

> fix(Datos) # editarlos datos
```
]

---

layout: false
.left-column[
  ## Lectura y escritura de datos.
   ### write
]
.right-column[

<br><br>
```
> Datos1 <- edit(as.data.frame(NULL)) # Creamos una tabla en blanco a la que nombramos como Datos1
```

```
> Datos1 # Vemos si realmente tenemos lo datos
> Datos1$var1->A # Vemos las columnas y las renombramos
> Datos1$var2->B
```

```
> A
> B
> A+B
> write(A*B,"sumaAyB.dat") # Lo guardamos en un fichero .dat que se llame sumaAyB
```
]
---

layout: false
.left-column[
  ## Ejemplos de funciones
   ### Funciones elementales
]
.right-column[
<br><br>

Calcular la media

```
> media<-function(x=NA)
+ {
+ x<-x[!is.na(x)]
+ sum(x)/length(x)
+ }
> media(c(2,4,1,3,6,7))
> media(c(2,4,1,3,6,NA))
```

Calcular la varianza 

```
> Varianza<-function(x=NA)
+ {
+ n<-length(x)
+ v<-sum((x-(sum(x)/n))^2)/n
+ return(v)
+ }
```

]

---

layout: false
.left-column[
  ## Ejemplos de funciones
    ### Funciones elementales
]
.right-column[
<br><br>

Calcular la desviación estandar

```
> DT<-function(x=NA)
+ {
+ n<-length(x)
+ v<-sqrt(sum((x-(sum(x)/n))^2)/n)
+ return(v)
+ }
> DT(1:3)
> DT(c(1,3,4,2,6,4))
```

Calcular la covarianza 

```
> Varianza<-function(x=NA)
+ {
+ n<-length(x)
+ v<-sum((x-(sum(x)/n))^2)/n
+ return(v)
+ }
```

Ejercicio. Crear una funcion llamada fact2 que genere el factorial de cualquier numero.
]
---
name: last-page
template: inverse

## That's all folks (for now)!

Slideshow created using [remark](http://github.com/gnab/remark).

