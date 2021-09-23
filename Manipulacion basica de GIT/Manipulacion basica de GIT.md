## **Manipulación Básica de repositorios en Git**
 
 
 ![](https://github.com/InKu3uS/GIT/blob/main/Manipulacion%20basica%20de%20GIT/imagenes/git.jpeg)


**Indice**

[1. Explicación del ejercicio](#id1)

[2. Configuración de Git](#id2)

[3. Creación de un repositorio](#id3)

[4. Comprobar el estado del repositorio](#id4)

[5. Realizando Commit’s](#id5)

[6. Modificación de ficheros](#id6)

[7. Historial](#id7)


## **1. Explicación del ejercicio**<a name="id1"></a>


En este ejercicio vamos familiarizarnos con la creación y manipulación básica de repositorios **Git**

## **2. Configuración de Git**<a name="id2"></a>

Una vez hayamos terminado con la instalación que hicimos en el ejercicio anterior pasaremos a configurarlo:

Para establecer el nombre del usuario usaremos el parametro: **git config --global user.name "Your-Full-Name"**

Para establecer la dirección de correo usaremos: **git config --global user.email "your-email-address"**

Y con este activaremos el coloreado de la salida: **git config --global color.ui auto**

Por ultimo ejecutaremos **git config --list** para comprobar que los datos introducidos son correctos
![](https://github.com/InKu3uS/GIT/blob/main/Manipulacion%20basica%20de%20GIT/imagenes/1.png)

## **3. Creación de un repositorio**<a name="id3"></a>

A continuación crearemos una carpeta llamada dpl en nuestra carpeta personal, luego crearemos un repositorio dentro de dicha carpeta con el comando **git init** y comprobamos que nos ha generado el archivo **.git**

![](https://github.com/InKu3uS/GIT/blob/main/Manipulacion%20basica%20de%20GIT/imagenes/2.png)

## **4. Comprobar el estado del repositorio**<a name="id4"></a>

Para empezar creamos un archivo llamado **indice.txt** con el contenido que se ve en la imagen siguiente. Si usamos el comando **git status** veremos que nos indica que dicho archivo esta sin seguimiento, lo añadiremos con un **git add indice.txt**.

Si ahora volvemos a comprobar el estado con git status veremos que ahora **indice.txt** si tiene seguimiento y con cambios para ser confirmados

![](https://github.com/InKu3uS/GIT/blob/main/Manipulacion%20basica%20de%20GIT/imagenes/3.png)

## **5. Realizando Commit’s**<a name="id5"></a>

Una vez hayamos añadido nuestro archivo al repositorio y hecho los cambios pertinentes. Podremos hacer uso del comando **git commit -m “mensaje del commit”** para confirmar los cambios que hicimos en el paso anterior. Si ahora volvemos a realizar un **git status** git nos indicara que no hay archivos para hacer commit ya que todos los cambios los tenemos confirmados.

![](https://github.com/InKu3uS/GIT/blob/main/Manipulacion%20basica%20de%20GIT/imagenes/4.png)

## **6. Modificación de ficheros**<a name="id6"></a>

Ahora modificaremos el archivo **indice.txt** anterior para ver una comparación y realizar un commit con los nuevos cambios. Una vez hayamos hecho los cambios, ejecutaremos un **git –diff** veremos que hay diferencias entre ambos archivos.

Para guardar estos cambios haremos como en el paso anterior **git add indice.txt** para añadirlo y luego **git commit -m “mensaje del commit”** para confirmarlos

![](https://github.com/InKu3uS/GIT/blob/main/Manipulacion%20basica%20de%20GIT/imagenes/5.png)

## **7. Historial**<a name="id7"></a>

Para ver los ultimos cambios en nuestro repositorio usaremos el comando git show. Con este veremos (entre otras cosas) el autor, la fecha,los archivos afectados y el comentario del ultimo commit.

Si quisieramos modificar el comentario del último commit usariamos **git commid –ammend “nuevo mensaje del commit”** y luego nuevamente con un **git show** comprobariamos que se ha modificado correctamente el mensaje.

![](https://github.com/InKu3uS/GIT/blob/main/Manipulacion%20basica%20de%20GIT/imagenes/6.png)











