## **NodeJS con Docker**

**Neftalí Rodríguez Rodríguez**

[**Github**](https://github.com/InKu3uS/)

![](imagenes/node.jpg)


**Indice**

[NodeJS con Docker](#id1)

[1. Primera parte](#id1)

[2. Segunda parte](#id2)

[3. Tercera parte](#id3)

[4. Cuarta parte](#id4)

[5. Quinta parte](#id5)




## **1. Primera parte**<a name="id1"></a>


Creamos un nuevo proyecto y en su interior creamos el archivo **“package.json”** con el contenido que aparece a continuación.


![](imagenes/1.png)

Si intentamos ejecutar el comando **“npm install”** nos daremos cuenta de que npm no se encuentra instalado, asi que lo instalamos mediante **“apt npm install”**.

![](imagenes/2.png)


Una vez completada la instalación ejecutamos el comando **“npm install”**

![](imagenes/3.png)

Al acabar debería mostrar una salida similar a esta


![](imagenes/4.png)

Se deberá haber creado el siguiente archivo **“package-lock.json”**

![](imagenes/5.png)



## **2. Segunda parte**<a name="id2"></a>

Una vez completado el paso anterior, creamos el archivo **“server.js”** con el contenido que se muestra en la siguiente imagen

![](imagenes/6.png)



## **3. Tercera parte**<a name="id3"></a>

A continuación creamos el archivo **“Dockerfile”**

![](imagenes/7.png)

Y el archivo **“.dockerignore”**

![](imagenes/8.png)



## **4. Cuarta parte**<a name="id4"></a>

Luego abrimos una terminal dentro del directorio del proyecto y ejecutamos el comando **“docker build . t ‘etiqueta del contenedor’/nodeweb-app”** y esperamos a que se descargue y se cree el contenedor

![](imagenes/9.png)



## **5. Quinta parte**<a name="id5"></a>

Por ultimo, lanzamos el contenedor con el comando **“docker run p ‘puerto’:8080 ‘etiqueta del contenedor’/node-web-app”**

![](imagenes/10.png)


Abrimos un navegador y en la URL introducimos **“0.0.0.0:5555”** y comprobamos que vemos el mensaje **“Hello World”**

![](imagenes/11.png)


















