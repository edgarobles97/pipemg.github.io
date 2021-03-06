Distribuciones continuas de probabilidad

| Nombre | Funcion de densidad | Media(esperanza)|varianza | notacion|
|:-----:|:------------------:|:----------------:|:---------:|:---------:|
| Distribución Uniforme Continua |<img src="https://latex.codecogs.com/gif.latex?f%28x%3BA%2CB%29%20%3D%20%5Cleft%5C%7B%5Cbegin%7Bmatrix%7D%20%5Cfrac%7B1%7D%7BB-A%7D%2C%20A%5Cleq%20x%5Cleq%20B%20%5C%5C%200%2C%20para%20todo%20lo%20demas%20%5Cend%7Bmatrix%7D%5Cright."> |<img src="https://latex.codecogs.com/gif.latex?%5Cmu%20%3D%20%5Cfrac%7BA&plus;B%7D%7B2%7D">|<img src="https://latex.codecogs.com/gif.latex?%5Csigma%20%3D%20%5Cfrac%7B%28B-A%29%5E2%7D%7B12%7D">|<img src="https://latex.codecogs.com/gif.latex?X%20%5Csim%20unif%28x%3BA%2CB%29">| 
|Distribución Normal <br> (Gaussiana)|<img src="https://latex.codecogs.com/gif.latex?f%28x%3BA%2CB%29%3D%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%5Cpi%5Csigma%7D%7D%20e%5E%7B-%5Cfrac%7B1%7D%7B2%5Csigma%5E2%7D%20%28x-%5Cmu%29%5E2%7D"> | <img src="https://latex.codecogs.com/gif.latex?%5Cmu">|<img src="https://latex.codecogs.com/gif.latex?%5Csigma%5E2">|<img src="https://latex.codecogs.com/gif.latex?X%20%5Csim%20norm%28x%3B%5Cmu%2C%20%5Csigma%29%29">|
| Distribución Gamma |<img src="https://latex.codecogs.com/gif.latex?f%28x%3B%5Calpha%2C%5Cbeta%29%3D%20%28%5Calpha%29%20%5Cleft%5C%7B%5Cbegin%7Bmatrix%7D%20%5Cfrac%7B1%7D%7B%5Cbeta%5E%5Calpha%5CGamma%28%5Calpha%29%7Dx%5E%7B%5Calpha-1%7De%5E%7B-x%20/%20%5Cbeta%7D%2C%20x%3E0%20%5C%5C%200%20%5Cend%7Bmatrix%7D%5Cright."> |<img src="https://latex.codecogs.com/gif.latex?%5Cmu%20%3D%20%5Calpha%20%5Cbeta">|<img src="https://latex.codecogs.com/gif.latex?%5Csigma%5E2%3D%5Calpha%5Cbeta%5E2">|<img src="https://latex.codecogs.com/gif.latex?X%20%5Csim%20%5CGamma%28%5Calpha%2C%5Cbeta%29">
| Distribución exponencial |<img src="https://latex.codecogs.com/gif.latex?f%28x%3B%5Cbeta%29%3D%5Cleft%5C%7B%5Cbegin%7Bmatrix%7D%20%5Cfrac%7B1%7D%7B%5Cbeta%7D%20e%5E%7B-x/%5Cbeta%7D%2C%20x%3E0%20%5C%5C%200%20%7E%20para%20%7E%20otro%20%7E%20caso%20%5Cend%7Bmatrix%7D%5Cright.%20%5C%5C%20%7E%7E%7E%7E%7E%7E%7E%7E%7E%7E%7E%7E%7E%7E%7E%20para%20%7E%20%5Cbeta%3E0"> | <img src="https://latex.codecogs.com/gif.latex?%5Cmu%20%3D%20%5Calpha%20%5Cbeta">|<img src="https://latex.codecogs.com/gif.latex?%5Csigma%5E2%20%3D%20%5Calpha%20%5Cbeta%5E2">|<img src="https://latex.codecogs.com/gif.latex?X%20%5Csim%20%5CGamma%28%5Calpha%3D1%2C%5Cbeta%29">|
| Distribución Chi cuadrada <br> (Dist. de Pearson) |<img src="https://latex.codecogs.com/gif.latex?f%28x%3Bv%29%20%3D%20%5Cbegin%7Bcases%7D%20%5Cfrac%7B1%7D%7Bx%5E%7Bv/2%7D%20%5CGamma%28v/2%29%7Dx%5E%7Bv/%7B2-1%7D%20e%5E%7B-x/2%7D%7D%20%26%20%5Ctext%7Bcon%20%7D%20x%3E0%20%5C%5C%200%20%26%20%5Ctext%7B%20para%20todo%20lo%20demas%20%7D%20%5Cend%7Bcases%7D"> | <img src="https://latex.codecogs.com/gif.latex?%5Cmu%3Dv">|<img src="https://latex.codecogs.com/gif.latex?%5Csigma%5E2%3D2v">|<img src="https://latex.codecogs.com/gif.latex?X%20%5Csim%20%5CGamma%28%5Calpha%3D%5Cfrac%7Bk%7D%7B2%7D%2C%5Cbeta%3D%201/2%29">|
| Distribución Beta |<img src="https://latex.codecogs.com/gif.latex?B%28%5Calpha%2C%5Cbeta%29%20%3D%20%5Cleft%5C%7B%5Cbegin%7Bmatrix%7D%20%5Cfrac%7B1%7D%7BB%28%5Calpha%2C%5Cbeta%29%7Dx%5E%7B%5Calpha-1%7D%281-x%29%5E%7Bbeta-1%7D%26%200%3Cx%3C1%20%5C%5C%200%2C%20%26%20%5Ctext%7Bpara%20lo%20demas%7D%20%5Cend%7Bmatrix%7D%5Cright."> | <img src="https://latex.codecogs.com/gif.latex?%5Cmu%3D%5Cfrac%7B%5Calpha%7D%7B%5Calpha&plus;%5Cbeta%7D">|<img src="https://latex.codecogs.com/gif.latex?%5Csigma%5E2%3D%5Cfrac%7B%5Calpha%5Cbeta%7D%7B%28%5Calpha&plus;%5Cbeta%29%5E2%28%5Calpha&plus;%5Cbeta&plus;1%29%7D">|<img src="" > |
|Distribución logaritmica Normal| <img src="https://latex.codecogs.com/gif.latex?f%28x%3B%5Cmu%2C%5Csigma%29%20%3D%20%5Cbegin%7Bcases%7D%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%20%5Cpi%20%5Csigma%20x%7D%7D%20e%5E%7B-%5Cfrac%7B1%7D%7B2%20%5Csigma%5E2%7D%5Bln%28x%29-%5Cmu%5D%5E2%7D%20%26%20%5Ctext%7B%20donde%20%7D%20x%20%5Cgeq%200%20%5C%5C%200%2C%20%26%20%5Ctext%20%7Bdonde%20%7D%20x%20%3C%200%20%5Cend%7Bcases%7D" > |<img src="https://latex.codecogs.com/gif.latex?%5Cmu%3De%5E%7B%5Cmu&plus;%5Csigma%5E2/2%7D">| <img src="https://latex.codecogs.com/gif.latex?%5Csigma%5E2%20%3D%20e%5E%7B2%5Cmu&plus;%5Csigma%5E2%7D%28e%5E%7B%5Csigma%5E2%7D-1%29">|

### Distribución uniforme continua
1. Es una distribución rectangular con Base B-A y algura de 1/(B-A)
Ejemplo: Se tiene una sala de conferencias que se puede apartar maximo 4 horas en una empresa, esta tiene conferencias de tiempo X donde X es una distribucion uniforme en el intervalo [0,4]. ¿Cuál es la funcion de densidad de probabilidad? ¿Cual es la probabilidad de que una conferencia dure al menos  3 horas? 

Respuesta: 

<img src ="https://latex.codecogs.com/gif.latex?f%28x%29%20%3D%20%5Cfrac%7B1%7D%7B4%7D%20%5Ctext%7B%7E%7Epara%7E%7D%200%20%5Cgeq%20x%20%5Cgeq%204"> 

<img src="https://latex.codecogs.com/gif.latex?P%5BX%20%5Cgeq%203%5D%5Cint_3%5E4%201/4%20%7E%20dx%20%3D1/4">

Codigo en R
```
var1<-runif(100000)
density(var1)
plot(density(var1))
```



### Distribución 
