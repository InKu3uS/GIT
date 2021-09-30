## **Ejemplos en GIT**

**Neftalí Rodríguez Rodríguez**

![](Aspose.Words.0e9d9988-e72b-481c-8a33-a5694a5a8fbc.001.jpeg)[**Github**](https://github.com/InKu3uS/)


**TOC \o "1-10"Indice**

[Ejemplos en GIT	1]

[1. Pasos previos	2]

[2. Ejercicio 1	3]

[3. Ejercicio 2	4]

[4. Ejercicio 3	5]

[5. Ejercicio 4	6]

[6. Ejercicio 5	7]

[7. Ejercicio 6	7]

[8. Ejercicio 7	8]

[9. Ejercicio 8	9]

[10. Ejercicio 9	10]








## **1. Pasos previos**

Creamos un directorio para realizar el ejercicio y dentro de este clonaremos el repositorio mediante el comando: **git clone https://github.com/jpexposito/libro.git**

Una vez hecho accedemos al nuevo directorio.


![](Aspose.Words.0e9d9988-e72b-481c-8a33-a5694a5a8fbc.002.png)
##
















## **2. Ejercicio 1**

Mostramos el historial de cambios del repositorio con **git log**

luego creamos un nuevo directorio llamado **capitulos**, y dentro de este un archivo con el nombre **capitulo1.txt** con el contenido que se ve en la imagen.

Añadimos los cambios a la zona de intercambio temporal con **git add .** Y luego realizamos un commit con el comando **git commit -m “Añadido capitulo 1”**

Volvemos a revisar el historial y veremos que aparece el commit que acabamos de realizar.

![](Aspose.Words.0e9d9988-e72b-481c-8a33-a5694a5a8fbc.003.png)






##


## **3. Ejercicio 2**

Creamos el archivo capitulo2.txt dentro del directorio capítulos con el contenido que aparece en la imagen siguiente.

Añadimos los cambios a la zona de intercambio temporal con **git add .**

Realizamos un nuevo commit con **git commit -m “Añadido capitulo 2”**

Por ultimo mostramos las diferencias entre esta version y dos versiones anteriores mediante el comando **git diff HEAD~2..HEAD**


![](Aspose.Words.0e9d9988-e72b-481c-8a33-a5694a5a8fbc.004.png)
##


##
##

## **4. Ejercicio 3**

Creamos un nuevo archivo dentro del directorio **capitulos** llamado **capitulo3.txt** con el texto que aparece en la imagen.

Añadimos los cambios a la zona de intercambio temporal con **git add .**

Realizamos un nuevo commit con **git commit -m “Añadido capitulo 3”**

![](Aspose.Words.0e9d9988-e72b-481c-8a33-a5694a5a8fbc.005.png)

Mosramos las diferencias entre la primera y la última versión del repositorio con el comando

git diff <codigo hash de la primera version>..HEAD

![](Aspose.Words.0e9d9988-e72b-481c-8a33-a5694a5a8fbc.006.png)
## **5. Ejercicio 4**

Creamos el archivo **indice.txt** en la raiz del repositorio con el contenido que se ve en la siguiente imagen.

Se añaden los cambios a la zona de intercambio temporal con **git add .**

Hacemos un commit **git commit -m "Añadido el índice ."**

Usamos el comando **git annotate indice.txt** para ver quien ha hecho los ultimos cambios en el archivo indice.txt


![](Aspose.Words.0e9d9988-e72b-481c-8a33-a5694a5a8fbc.007.png)


## **6. Ejercicio 5**

Lo siguiente que haremos será crear una nueva rama llamada bibliografia con **git branch bibliografia** y luego mostraremos las ramas del repositorio con **git branch -av**

![](Aspose.Words.0e9d9988-e72b-481c-8a33-a5694a5a8fbc.008.png)


## **7. Ejercicio 6**

Creamos el archivo **capitulo4.txt** con el contenido que se aprecia en la imagen.

Añadimos los cambios a la zona de intercambio temporal con **git add .**

Hacemos un commit **git commit -m "Añadido el capitulo 4 ."**

Mostramos la historia del repositorio incluyendo todas la ramas que se han creado con **git log –graph –all --oneline**


![](Aspose.Words.0e9d9988-e72b-481c-8a33-a5694a5a8fbc.009.png)
















## **8.** **Ejercicio 7**

Creamos la rama **bibliografia** con el comando **git branch bibliografia** y nos movemos a ella.

Creamos el archivo **bibliografia.txt** con el contenido que aparece en la imagen.

Añadimos los cambios a la zona de intercambio temporal con **git add .**

Realizamos el commit **con git commit – m “mensaje de commit”**

Por último, mostramos la historia del repositorio con el comando **git log –graph –all – oneline**

![](Aspose.Words.0e9d9988-e72b-481c-8a33-a5694a5a8fbc.010.png)











## **9. Ejercicio 8**

Nos movemos a la rama main con **git checkout main**

Fusionamos la rama main con la rama bibliografia con **git merge bibliografia**

Mostramos la historia del repositorio con el comando **git log –graph –all – oneline**

Luego, eliminamos la rama bibliografia con el comando **git branch -d bibliografia**.

Volvemos a mostrar la historia del repositorio para comprobar que la rama bibliografia se ha eliminado.

![](Aspose.Words.0e9d9988-e72b-481c-8a33-a5694a5a8fbc.011.png)





## **10. Ejercicio 9**

Creamos nuevamente la rama bibliografia con **git branch bibliografia** y nos movemos a ella con **git checkout bibliografia**

Modifocamos el archivo **bibliografia.txt** para que contenga lo que aparece en la imagen

Volvemos a la rama main mediante **git checkout main**

Desde esta rama modificamos nuevamente el archivo **bibliografia.txt** con el contenido de la imagen.

Realizamos el commit con **git commit -m “mensaje del commit”**

Intentamos fusionar la rama bibliografia con la main mediante **git merge bibliografia** y veremos que nos aparecerá un conflicto ya que en las dos ramas, bibliografia contiene elementos diferentes.

![](Aspose.Words.0e9d9988-e72b-481c-8a33-a5694a5a8fbc.012.png)







Si abrimos **bibliografia.txt** con un editor de texto (en este caso nano) veremos que git nos ha indicado con **“HEAD”** el contenido que tenemos en la rama main y a continuacion lo que contiene la rama bibliografia.

![](Aspose.Words.0e9d9988-e72b-481c-8a33-a5694a5a8fbc.013.png)Realizamos los cambios que aparecen en la imagen para resolver el conflicto

![](Aspose.Words.0e9d9988-e72b-481c-8a33-a5694a5a8fbc.014.png)

Una vez hayamos resuelto el conflicto, añadimos los cambios a la zona de intercambio temporal con **git add .** y realizamos el commit mediante **git commit -m “mensaje del commit”**

Por ultimo revisamo la historia del repositorio mediante el comando **git log –graph –all – oneline**

![](Aspose.Words.0e9d9988-e72b-481c-8a33-a5694a5a8fbc.015.png)
