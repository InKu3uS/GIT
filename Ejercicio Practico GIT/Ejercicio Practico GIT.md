## **Ejercicio Practico**

**Neftalí Rodríguez Rodríguez**

![](/imagenes/git.jpeg)
[**Github**](https://github.com/InKu3uS/)


**Indice**

[Ejercicio Practico	1](#id1)

[1. Primera parte	2](#id2)

[2. Segunda parte	2](#id3)

[3. Tercera parte	3](#id4)

[4. Cuarta parte	3](#id5)

[5. Quinta parte	4](#id6)









## **1. Primera parte**<a name="id1"></a>

Creamos la carpeta “**ejercicio\_git\_neftali\_rodriguez\_rodriguez**”

Creamos el archivo **README.**

Inicializamos el repositorio con **git init**

Añadimos el **README** al repositorio usando **git add README**

Realizamos el primer **commit con git commit -m “Cambios en el README”**

Con el comando **git remote add origin “ruta del repositorio”** lo enlazamos con nuestro repositorio remoto.

![](imagenes/1.png)


## **2. Segunda parte**<a name="id2"></a>

Crearemos una nueva rama llamada f**eature-1** con el comando **git branch feature-1** y nos movemos a ella con **git checkout feature-1**

crearemos el archivo **hola.txt** con el siguiente contenido que se ve en la imagen. Modificamos el archivo para incluir nuestro nombre.

Añadimos los cambios con git add hola.html

Realizamos el commit con **git commit -m “Añadido el archivo hola.html”**


![](imagenes/2.png)






## **3. Tercera parte**<a name="id3"></a>

Nos movemos nuevamente a la rama master con **git checkout master**

creamos el archivo adios.html con **cat > adios.html**

![](imagenes/3.png)

## **4. Cuarta parte**<a name="id4"></a>

Añadimos los dos archivos a la zona de intercambio temporal con **git add .** (Lo haremos en ambas ramas).

Luego haremos los commits de ambos archivos con el comando **git commit -m “mensaje del commit”**

![](imagenes/4.png)







Luego nos movemos a la rama master y realizamos la mezcla con **git merge feature-1**

![](imagenes/5.png)

## **5. Quinta parte**<a name="id5"></a>

Por último, revisamos los cambios en el repositorio con **git log –graph –all --oneline**

![](imagenes/6.png)

