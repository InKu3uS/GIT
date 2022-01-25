## **Creación de los Pipeline Java en Apache Tomcat**

**Neftalí Rodríguez Rodríguez**

![](imagenes/logo.png)


[**Github**](https://github.com/InKu3uS/)

Indice

[Creación de los Pipeline Java en Apache Tomcat	1](#id1)

[1. Parte 1](#id1)

[2. Parte 2](#id2)

[3. Parte 3](#id3)

[4. Parte 4](#id4)

[5. Parte 5](#id5)

[6. Parte 6](#id6)



## **1. Parte 1**<a name="id1"></a>

Creamos un nuevo repositorio en **GitHub** con el nombre **“hello-world-java-apache-tomcat”.**

![](imagenes/0.png)


## **2. Parte 2**<a name="id2"></a>

Clonamos el repositorio en nuestra maquina local.

![](imagenes/1.png)


## **3. Parte 3**<a name="id3"></a>

En la raiz del directorio del repositorio creamos un archivo **Dockerfile** con el siguiente contenido

![](imagenes/2.png)



Posteriormente creamos el archivo **Jenkinsfile** que le indicará a **Jenkins** las fases y los pasos a seguir.

![](imagenes/3.png)


## **4. Parte 4**<a name="id4"></a>

Modificamos el archivo **“index.jsp”** dentro del directorio **“src”** para incluir nuestro nombre

![](imagenes/4.png)



## **5. Parte 5**<a name="id5"></a>

El siguiente paso será dirigirnos a **Jenkins** y crear una nueva tarea **Pipeline**

![](imagenes/5.png)


En lugar de introducir el script directamente pulsamos sobre **“Pipeline script from SCM”**, luego configuramos el repositorio en el que se buscará el archivo **Jenkinsfile** y el nombre de usuario y contraseña para acceder a **GitHub**

![](imagenes/6.png)



## **6. Parte 6**<a name="id6"></a>

Una vez se haya creado la tarea, probamos a ejecutarla. Si todo va bien deberíamos ver una pantalla como la siguiente.

![](imagenes/7.png)


Comprobamos el **log** del **Pipeline** para comprobar que todo ha salido correctamente.

![](imagenes/8.png)


Por último, accedemos a la dirección **“localhost:8082”** y comprobamos que vemos el contenido del archivo **“index.jsp”** que creamos.

![](imagenes/9.png)