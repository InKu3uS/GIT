## **Instalación de Jenkins en Ubuntu**

**Neftalí Rodríguez Rodríguez**

![](imagenes/logo.png)


[**Github**](https://github.com/InKu3uS/)

Indice

[Instalación de Jenkins en Ubuntu](#id1)

[1. Parte 1](#id1)

[2. Parte 2](#id2)

[3. Parte 3](#id3)

[4. Parte 4](#id4)

[5. Parte 5](#id5)

[6. Parte 6](#id6)



## **1. Parte 1** <a name="id1"></a>

Antes de comenzar el ejercicio, vamos a crear un dominio nuevo en el servidor apache con el nombre **“www.neftaic.com”** y lo añadimos a /*etc/*hosts

![](imagenes/0.png)

![](imagenes/00.png)

## **2. Parte 2** <a name="id2"></a>


Antes de empezar añadiremos los repositorios de Jenkins al sistema.

![](imagenes/1.png)

Luego añadimos la dirección del repositorio al archivo **“sources.list”**

![](imagenes/2.png)

Luego realizamos un **“apt update”**

![](imagenes/3.png)

Una vez termine ejecutamos **“apt install jenkins”**

![](imagenes/4.png)

## **3. Parte 3** <a name="id3"></a>

Arrancamos el servicio de jenkins

![](imagenes/5.png)


Luego introducimos **“systemctl status jenkins”** para comprobar que el servicio se encuentra activo.

![](imagenes/6.png)

## **4. Parte 4** <a name="id4"></a>
Permitimos las conexiones  desde el puerto 8080 y OpenSSH en el Firewall. Luego guardamos los cambios con **“sudo ufw enable”.**

![](imagenes/7.png)

Luego ejecutamos **“sudo ufw status”** para comprobar que se han guardado los cambios.

![](imagenes/8.png)


## **5. Parte 5** <a name="id5"></a>


Accedemos al dominio que creamos anteriormente y deberiamos ver la pagina de inicio de Jenkins.

Luego introducimos el comando **“sudo cat /var/lib/jenkins/secrets/initialAdminPassword”** para ver la contraseña de desbloqueo de Jenkins, la copiamos y pegamos en dicha pagina

![](imagenes/9.png)


Al introducir la contraseña veremos la siguiente pagina, en ella haremos click en **“install suggested plugins”.** De esa manera, se instalaran los plugins necesarios para usar Jenkins


![](imagenes/10.png)

Esperamos a que terminen de instalarse los plugins.

![](imagenes/11.png)

## **6. Parte 6** <a name="id6"></a>

Una vez termine el proceso de instalación de los plugins veremos la siguiente pagina. En esta crearemos un usuario con el que haremos uso de Jenkins.

![](imagenes/12.png)

Una vez creado el usuario, ya podremos hacer uso de Jenkins.

![](imagenes/13.png)
