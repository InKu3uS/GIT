# **Clusterizando un Servicio Rest en Wildfly**

**Neftalí Rodríguez Rodríguez**

[**Github**](https://github.com/InKu3uS/)

![](imagenes/docker.png)




**Indice**

[Clusterizando un Servicio Rest en Wildfly](#id1)

[1. Primera parte](#id1)

[2. Segunda parte](#id2)

[3. Tercera parte](#id3)

[4. Cuarta parte](#id4)

[5. Quinta parte](#id5)

[6. Sexta parte](#id6)




## **1. Primera parte**<a name="id1"></a>


Descargamos el servicio “helloworld-rs”. En la raiz del proyecto creamos el archivo Dockerfile con el siguiente contenido.


![](imagenes/1.png)



## **2. Segunda parte**<a name="id2"></a>


En el mismo directorio creamos el archivo “docker-compose.yml” que contendra la información de todos los contenedores que vamos a crear y los puertos bajo los que van a funcionar.


![](imagenes/2.png)


![](imagenes/3.png)

## **3. Tercera parte**<a name="id3"></a>

A continuación, en el directorio “dump” del proyecto, crearemos el archivo “dbname.sql” que creará la base de datos contenida en el archivo en el contenedor de PHPMyAdmin.

![](imagenes/4.png)

Cuando hayamos completado los pasos anteriores, abriremos una terminal y pondremos el comando “mvn clean install” para compilar el proyecto y se cree el archivo “.war” que se desplegará en los 3 contenedores Wildfly.

Una vez termine de compilar el proyecto ejecutaremos el comando “sudo docker-compose up -d –buid” para crear los contenedores y arrancarlos.

## **4. Cuarta parte**<a name="id4"></a>

Una vez que hayan arrancado los contenedores, abrimos un navegador e introducimos la URL “localhost:8000”. El puerto 8000 se ha asignado a PHPMyAdmin. Tras loguearnos veremos el panel de control de PHPMyAdmin y veremos como la base de datos se ha creado con éxito.


![](imagenes/5.png)


## **5. Quinta parte**<a name="id5"></a>

Ahora probaremos los contenedores Wildfly, a los que les corresponden los puertos “8081-8082 y 8083”

![](imagenes/6.png)


![](imagenes/7.png)



![](imagenes/8.png)

## **6. Sexta parte**<a name="id6"></a>


Por ultimo, introducimos “localhost:puerto del contenedor/helloworld-rs/” para probar que el servicio se ha desplegado correctamente.



![](imagenes/9.png)


![](imagenes/10.png)
