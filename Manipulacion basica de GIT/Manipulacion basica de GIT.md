## **Manipulación Básica de repositorios en Git**

**Neftalí Rodríguez Rodríguez**

![](Aspose.Words.caae5e42-a1b6-4646-91df-53dcd48243ea.001.jpeg)[**Github**](https://github.com/InKu3uS/)


**TOC \o "1-10"Indice**

[1. Explicación del ejercicio	2](#__RefHeading___Toc5479_4026787900)

[2. Configuración de Git	2](#__RefHeading___Toc5481_4026787900)

[3. Creación de un repositorio	2](#__RefHeading___Toc5587_4026787900)

[4. Comprobar el estado del repositorio	3](#__RefHeading___Toc5589_4026787900)

[5. Realizando Commit’s	4](#__RefHeading___Toc5591_4026787900)

[6. Modificación de ficheros	5](#__RefHeading___Toc5593_4026787900)

[7. Historial	6](#__RefHeading___Toc5595_4026787900)









## **1. Explicación del ejercicio**

En este ejercicio vamos familiarizarnos con la creación y manipulación básica de repositorios **Git**




## **2. Configuración de Git**

Una vez hayamos terminado con la instalación que hicimos en el ejercicio anterior pasaremos a configurarlo:

Para establecer el nombre del usuario usaremos el parametro: **git config --global user.name "Your-Full-Name"**

Para establecer la dirección de correo usaremos: **git config --global user.email "your-email-address"**

Y con este activaremos el coloreado de la salida: **git config --global color.ui auto**

Por ultimo ejecutaremos **git config --list** para comprobar que los datos introducidos son correctos
![](Aspose.Words.caae5e42-a1b6-4646-91df-53dcd48243ea.002.png)





##





##
## **3. Creación de un repositorio**

A continuación crearemos una carpeta llamada dpl en nuestra carpeta personal, luego crearemos un repositorio dentro de dicha carpeta con el comando **git init** y comprobamos que nos ha generado el archivo **.git**

![](Aspose.Words.caae5e42-a1b6-4646-91df-53dcd48243ea.003.png)
## **4. Comprobar el estado del repositorio**

Para empezar creamos un archivo llamado **indice.txt** con el contenido que se ve en la imagen siguiente. Si usamos el comando **git status** veremos que nos indica que dicho archivo esta sin seguimiento, lo añadiremos con un **git add indice.txt**.

Si ahora volvemos a comprobar el estado con git status veremos que ahora **indice.txt** si tiene seguimiento y con cambios para ser confirmados

![](Aspose.Words.caae5e42-a1b6-4646-91df-53dcd48243ea.004.png)
##
## **5. Realizando Commit’s**

Una vez hayamos añadido nuestro archivo al repositorio y hecho los cambios pertinentes. Podremos hacer uso del comando **git commit -m “mensaje del commit”** para confirmar los cambios que hicimos en el paso anterior. Si ahora volvemos a realizar un **git status** git nos indicara que no hay archivos para hacer commit ya que todos los cambios los tenemos confirmados.

![](Aspose.Words.caae5e42-a1b6-4646-91df-53dcd48243ea.005.png)





























##
## **6. Modificación de ficheros**

Ahora modificaremos el archivo **indice.txt** anterior para ver una comparación y realizar un commit con los nuevos cambios. Una vez hayamos hecho los cambios, ejecutaremos un **git –diff** veremos que hay diferencias entre ambos archivos.

Para guardar estos cambios haremos como en el paso anterior **git add indice.txt** para añadirlo y luego **git commit -m “mensaje del commit”** para confirmarlos

![](Aspose.Words.caae5e42-a1b6-4646-91df-53dcd48243ea.006.png)






## **7. Historial**

Para ver los ultimos cambios en nuestro repositorio usaremos el comando git show. Con este veremos (entre otras cosas) el autor, la fecha,los archivos afectados y el comentario del ultimo commit.

Si quisieramos modificar el comentario del último commit usariamos **git commid –ammend “nuevo mensaje del commit”** y luego nuevamente con un **git show** comprobariamos que se ha modificado correctamente el mensaje.



![](Aspose.Words.caae5e42-a1b6-4646-91df-53dcd48243ea.007.png)











