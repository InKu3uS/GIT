## **Instalación de Docker**

**Neftalí Rodríguez Rodríguez**

[**Github**](https://github.com/InKu3uS/)

![](imagenes/docker.png)



**Indice**

[Instalación de Docker](#id1)

[1. Primera parte](#id1)

[2. Segunda parte](#id2)

[3. Tercera parte](#id3)

[4. Cuarta parte](#id4)

[5. Quinta parte](#id5)

[6. Sexta parte](#id6)

[7. Séptima parte](#id7)

[8. Octava parte](#id8)


## **1. Primera parte**<a name="id1"></a>

Primero haremos un **“apt update”** para actualizar los repositorios.

A continuación, con el comando **“sudo apt install apt-transport-https ca-certificates curl software-properties-common”** para poder instalar paquetes a traves de HTTPS.

![](imagenes/1.png)
## **2. Segunda parte**<a name="id2"></a>
Luego, añadimos la clave **GPG** para el repositorio de **Docker**.

![](imagenes/2.png)

## **3. Tercera parte**<a name="id3"></a>
Agregamos el repositorio de **Docker** y ejecutamos un **“apt update”** para actualizar la lista de paquetes

![](imagenes/3.png)

## **4. Cuarta parte**<a name="id4"></a>
Comprobamos que el paquete **“docker -ce”** se va a descargar desde el repositorio de **Docker.**

![](imagenes/4.png)


## **5. Quinta parte**<a name="id5"></a>
Ejecutamos **“apt install docker-ce”** para instalar comenzar la instalación de **Docker**.

![](imagenes/5.png)
## **6. Sexta parte**<a name="id6"></a>
Una vez se haya completado la instalación, comprobamos que **Docker** esta activo con el comando **“systemctl status docker”**

![](imagenes/6.png)

## **7. Séptima parte**<a name="id7"></a>
Usamos el comando **“docker run hello-world”** para comprobar que podemos acceder y descargar imágenes de **Docker**.

![](imagenes/7.png)


## **8. Octava parte**<a name="id8"></a>
Mediante el comando **“docker ps”** podremos ver los contenedores activos.

![](imagenes/8.png)

Con el comando **“docker ps -a”** veremos los contenedores activos e inactivos.

![](imagenes/9.png)

Mediante el comando **“docker ps -l”** podremos comprobar cual fue el ultimo contenedor cargado.

![](imagenes/10.png)

Por último mediante el comando **“docker  images”** se nos mostrara todas las imágenes de Docker en nuestro equipo.

![](imagenes/11.png)

