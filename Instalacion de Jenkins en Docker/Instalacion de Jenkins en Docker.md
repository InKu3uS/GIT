## **Instalación de Jenkins en Docker**

**Neftalí Rodríguez Rodríguez**

![](imagenes/logo.png)


[](https://github.com/InKu3uS/)

[**Github**](https://github.com/InKu3uS/)

Indice

[Instalación de Jenkins en Docker	1](#id1)

[1. Creación de subdominio para Jenkins	1](#id1)

[2. Instalación de Jenkins con Docker	2](#id2)



## **1. Creación de subdominio para Jenkins**<a name="id1"></a>

Antes de comenzar el ejercicio, vamos a crear un dominio nuevo en el servidor apache con el nombre “[www.](http://www.neftaic.com/)[jenkins.](http://www.neftaic.com/)[nefta.com](http://www.neftaic.com/)” y lo añadimos a **/*etc/*hosts**


![](imagenes/1.png)


![](imagenes/2.png)

Luego creamos el directorio **“jenkinsnefta”** en **“/var/www/”**

![](imagenes/3.png)


## **2. Instalación de Jenkins con Docker**<a name="id2"></a>


Abrimos una terminal y descargamos la imagen de Jenkins desde los repositorios de Docker con el comando **“docker pull jenkins/jenkins:lts”**



![](imagenes/4.png)

Una vez terminada la descarga comprobaremos que esta en la lista de imágenes con el comando **“docker images”**

![](imagenes/5.png)

Arrancamos el contenedor de Docker que nos acabamos de descargar mediante el comando **“docker run -p 8080:8080 -p 50000:50000 -v /home/nefta:/var/jenkins\_home jenkins/jenkins:lts”**

![](imagenes/6.png)

Una vez arrancada, mediante el comando **“docker exec -it dockerjenkins\_pensive\_wu cat /var/jenkins\_home/secrets/initialAdminPassword”** obtendremos el código para desbloquear Jenkins

![](imagenes/7.png)

Introducimos la URL de nuestro dominio a través del puerto **8080** y veremos la pagina inicial de Jenkins donde se nos pedirá la contraseña que obtuvimos en el paso anterior. Una vez introducida veremos la siguiente pagina de bienvenida. En ella haremos click en **“Install suggested plugins”**.

![](imagenes/8.png)


Esperamos a que se instalen los **plugins.**

![](imagenes/9.png)

Una vez se hayan instalado los **plugins**, nos aparecerá la siguiente pagina en la que deberemos crear al usuario que usaremos para **Jenkins**

![](imagenes/10.png)

Una vez creado, estaremos en el **Panel de Control de Jenkins** y la instalación habrá terminado.

![](imagenes/11.png)



**3. Instalación de Jenkins con Docker y Docker-compose**<a name="id3"></a>

Creamos un directorio para guardar los archivos que crearemos a continuación, dentro de este crearemos otro al que llamaremos **“jenkins”** y dentro de este crearemos el archivo **Dockerfile** que se ve a continuación.

![](imagenes/12.png)

Dentro del directorio **“jenkins”** también crearemos el archivo **“plugins.txt”** que contendrá la lista de plugins que se instalarán en **Jenkins**.


![](imagenes/13.png)


En el directorio principal crearemos el archivo **“docker-compose.yml”** que se ve en la imagen siguiente.

![](imagenes/14.png)

Una vez tengamos estos tres archivos creados, ejecutamos en la terminal el comando **“docker-compose build”**. Si todo sale correctamente al final deberíamos ver el mensaje **“Successfully built”.**

![](imagenes/15.png)


Para arrancar el contenedor, usaremos el comando **“docker-compose up -d”**. Si el contenedor se arranca correctamente nos aparecerá en la terminal un mensaje en color verde diciendo **“done”**. Podremos comprobar que el contenedor está arrancado con el comando **“docker-ps”.**

**NOTA:** Durante este paso, el contenedor no podía arrancarse debido a que no se encontraban ciertos plugins incluidos en el archivo **“plugins.txt”**. Al borrar los cuatro plugins que no se encontraban en los repositorios, el contenedor arrancó sin mas problemas.

![](imagenes/16.png)

Ejecutamos en una consola el comando **“docker exec -it dockerjenkins\_master\_1 cat /var/jenkins\_home/secrets/initialAdminPassword”** para obtener la clave de desbloqueo de Jenkins.

![](imagenes/17.png)


Entramos al navegador con la dirección del subdominio. Nos aparecerá la pagina en la que deberemos introducir la clave de desbloqueo que obtuvimos en el paso anterior. Nos aparecerá la pagina siguiente, clickaremos en **“Install suggested plugins”** para continuar.

Esperamos a que se instalen los plugins. **Esta vez ya muchos se encontrarán instalados**.

![](imagenes/18.png)


Una vez instalados, crearemos al usuario que hará uso de **Jenkins**.

![](imagenes/19.png)


Cuando hayamos creado al usuario, nos encontraremos en el **Panel de Control** de **Jenkins** listo para usar.

![](imagenes/20.png)




