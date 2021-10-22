## **Instalación de Wildfly**

**Neftalí Rodríguez Rodríguez**

[**Github**](https://github.com/InKu3uS/)

![](imagenes/wildfly.png)

**"Indice**

[Instalación de Wildfly	1]

[1. Parte 1](#id1)

[2. Parte 2](#id2)

[3. Parte 3](#id3)

[4. Parte 4](#id4)

[5. Parte 5](#id5)

[6. Parte 6](#id6)

[7. Parte 7](#id7)

[8. Parte 8](#id8)

[9. Parte 9](#id9)

[10. Parte 10](#id10)

[11. Parte 11](#id11)

[12. Parte 12](#id12)

[13. Parte 13](#id13)

[14. Parte 14](#id14)

[15. Parte 15](#id15)








## **1. Parte 1**<a name="id1"></a>


Antes de comenzar la instalación, realizaremos un “sudo apt update && apt update” para actualizar el sistema y los repositorios.

Ahora ejecutaremos el comando “  wget <https://github.com/wildfly/wildfly/releases/download/25.0.0.Final/wildfly-25.0.0.Final.tar.gz>”

Con esto, nos descargaremos la ultima versión de Wildfly desde su Github oficial.


![](imagenes/1.png)





## **2. Parte 2**<a name="id2"></a>

Creamos el usuario y el grupo Wildfly

![](imagenes/2.png)






## **3. Parte 3**<a name="id3"></a>


Descomprimimos el paquete que nos descargamos con **“tar -xvzf wildfly-25.0.0.Final.tar.gz”** y lo movemos a **/*opt*/wildfly**

![](imagenes/3.png)

## **4. Parte 4**<a name="id4"></a>

Creamos un enlace simbolico al directorio.

![](imagenes/4.png)

## **5. Parte 5**<a name="id5"></a>

Posteriormente haremos propietario del directorio al usuario wildfly que creamos en pasos anteriores.

![](imagenes/5.png)










## **6. Parte 6**<a name="id6"></a>

Creamos el directorio **/*etc*/wildfly** y hacemos una copia del archivo de configuración de wildfly a este nuevo directorio.

![](imagenes/6.png)


Este es el contenido de el archivo **wildfly.conf** que acabamos de copiar

![](imagenes/7.png)


## **7. Parte 7**<a name="id7"></a>

Lanzamos los comandos que aparecen en la siguiente imagen para preparar el arranque del servicio

![](imagenes/8.png)







## **8. Parte 8**<a name="id8"></a>

Ejecutamos un **“sudo systemctl start wildfly”** y comprobamos que esta arrancado con **“sudo systemctl status wildfly”**

![](imagenes/9.png)


Si wildfly esta activo y sin problemas ejecutaremos **“sudo systemctl enable wildfly”** para que arranque con el sistema.

![](imagenes/10.png)











## **9. Parte 9**<a name="id9"></a>


El siguiente paso será modificar el archivo **standalone.xml** que se encuentra en la ruta  **/opt/wildfly/standalone/configuration/**

En este archivo modificaremos la linea en la que aparece el cursor en la imagen, para indicar en que puerto accederemos a Wildfly. En nuestro caso será el **8083**




![](imagenes/11.png)



Tambien deberemos permitir el tráfico a través del puerto 8083 con el comando **“ufw allow 8083/tcp”**


![](imagenes/12.png)











## **10. Parte 10**<a name="id10"></a>


El siguiente paso será crear un usuario administrador para Wildfly.

Para ello ejecutaremos el script **“/opt/wildfly/bin/add-user.sh”**

Veremos un asistente que nos guiará en el proceso. Marcaremos la opcion **“a”** para crear un usuario administrador, luego tendremos que indicar el **nombre del usuario**, **contraseña** y nos preguntará si queremos añadir a dicho usuario al grupo **“ManagementRealm”**, indicamos que si y el usuario quedará creado.



![](imagenes/14.png)




## **11. Parte 11**<a name="id11"></a>

El siguiente paso será abrir el script **“/*opt/wildfly/bin/launch.sh”*** con un editor de texto*** y comprobar que el contenido es igual al de la siguiente imagen.

![](imagenes/15.png)


## **12. Parte 12**<a name="id12"></a>
Luego abriremos el archivo **“/etc/systemd/system/wildfly.service”** y comprobamos que el contenido es el mismo que en la siguiente imagen.

En nuestro caso, hubo que añadir **“$WILDFLY\_CONSOLE\_BIND”** al final de la linea **“ExecStart….”**

![](imagenes/16.png)



## **13. Parte 13**<a name="id13"></a>

Tras realizar las modificaciones en ambos archivos reiniciaremos los servicios para asegurarnos que los nuevos cambios se han cargado.

![](imagenes/17.png)



## **14. Parte 14**<a name="id4"></a>

Si queremos activar la consola de administración, bastaría con comentar o eliminar las lineas de las etiquetas **inet-address** en el archivo **“/opt/wildfly/standalone/configuration/standalone.xml”**

![](imagenes/18.png)




## **15. Parte 15**<a name="id15"></a>


Una vez hayamos completado la instalación y configuración de **Wildfly**, accederemos a él desde nuestro navegador introduciendo **“localhost:8083”**

![](imagenes/19.png)

