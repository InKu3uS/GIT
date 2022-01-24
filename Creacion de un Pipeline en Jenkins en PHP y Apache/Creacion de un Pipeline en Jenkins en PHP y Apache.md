## **Creación de un Pipeline en Jenkins en PHP y Apache**

**Neftalí Rodríguez Rodríguez**

![](imagenes/logo.png)


[](https://github.com/InKu3uS/)

[**Github**](https://github.com/InKu3uS/)

Indice

[Creación de un Pipeline en Jenkins en PHP y Apache	1](#id1)

[1. Parte 1](#id1)

[2. Parte 2](#id2)

[3. Parte 3](#id3)

[4. Parte 4](#id4)

[5. Parte 5](#id5)



## **1. Parte 1**<a name="id1"></a>

Creamos un nuevo repositorio en **GitHub** con el nombre **“hello-world-php-apache”**

![](imagenes/1.png)


## **2. Parte 2**<a name="id2"></a>

Clonamos el repositorio en nuestra maquina local. Dentro del directorio principal creamos el directorio **“src”** y dentro creamos un archivo **PHP** como el siguiente.

![](imagenes/2.png)



## **3. Parte 3**<a name="id3"></a>

En la raiz del directorio del repositorio creamos un archivo **Dockerfile** con el siguiente contenido

![](imagenes/3.png)


Posteriormente creamos el archivo **Jenkinsfile** que le indicará a **Jenkins** las fases y los pasos a seguir.

![](imagenes/4.png)


## **4. Parte 4**<a name="id4"></a>

El siguiente paso será dirigirnos a **Jenkins** y crear una nueva tarea **Pipeline**


![](imagenes/5.png)


En lugar de introducir el script directamente pulsamos sobre **“Pipeline script from SCM”**, luego configuramos el repositorio en el que se buscará el archivo **Jenkinsfile** y el nombre de usuario y contraseña para acceder a **GitHub**

![](imagenes/6.png)

## **5. Parte 5**<a name="id5"></a>

Una vez se haya creado la tarea, probamos a ejecutarla. Si todo va bien deberíamos ver una pantalla como la siguiente.


![](imagenes/7.png)


Comprobamos el **log** del **Pipeline** para comprobar que todo ha salido correctamente.

![](imagenes/8.png)


Por último, accedemos a la dirección **“localhost:8085”** y comprobamos que vemos el contenido del archivo **“index.php”** que creamos.


![](imagenes/9.png)


