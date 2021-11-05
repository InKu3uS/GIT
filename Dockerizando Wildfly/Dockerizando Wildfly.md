## **Ejercicio Practico**

**Neftalí Rodríguez Rodríguez**

[**Github**](https://github.com/InKu3uS/)

![](imagenes/docker.png)



**Indice**

[Ejercicio Practico](#id1)

[1. Primera parte](#id1)

[2. Segunda parte](#id2)

[3. Tercera parte](#id3)

[4. Cuarta parte](#id4)

[5. Quinta parte](#id5)




## **1. Primera parte**<a name="id1"></a>

Crearemos un directorio con el nombre **“wildfly-config”** y accederemos a este.


![](imagenes/1.png)



Dentro del nuevo directorio creamos el archivo **“Dockerfile”** y añadimos el contenido que se ve en la siguiente imagen.

![](imagenes/2.png)





## **2. Segunda parte**<a name="id2"></a>

Construimos la imagen. Con el atributo **“--tag=”** le pondremos un nombre.

![](imagenes/3.png)


## **3. Tercera parte**<a name="id3"></a>

Verificamos todas las imagenes de docker que tenemos en nuestro equipo y comprobamos que aparece la última imagen que acabamos de crear.


![](imagenes/4)



## **4. Cuarta parte**<a name="id4"></a>

A continuación, ejecutamos la imagen .

![](imagenes/5.png)

Accedemos desde el navegador a **Wildfly** a través del puerto **8080** que es el que especificamos en la imagen anterior al ejecutar la imagen.

![](imagenes/6.png)



Accedemos a la consola de administración, nos pedirá el usuario y contraseña. Introducimos **“admin-admin”** que es el usuario que especificamos en el archivo **“Dockerfile”**

![](imagenes/7.png)

Como se puede observar en la siguiente imagen, mediante dicho usuario tenemos acceso a la consola de administración de **Wildfly**

![](imagenes/8.png)


