## **LAMMP con Docker**



**Neftalí Rodríguez Rodríguez**

[**Github**](https://github.com/InKu3uS/)

![](imagenes/docker.png)


**Indice**

[LAMMP con Docker](#id1)

[1. Parte 1](#id1)

[2. Parte 2](#id2)

[3. Parte 3](#id3)

[4. Parte 4](#id4)

[5. Parte 5](#id5)

[6. Parte 6](#id6)

[7. Parte 7](#id7)

[8. Parte 8](#id8)




## **1. Parte 1**<a name="id1"></a>


Creamos el archivo **Dockerfile** en la raiz de nuestro proyecto con el siguiente contenido


![](imagenes/1.png)




## **2. Parte 2**<a name="id2"></a>

A continuacion, el archivo **“docker-compose.yml”** con el siguiente contenido


![](imagenes/2.png)




## **3. Parte 3**<a name="id3"></a>

Creamos el archivo sql en el directorio dump que creará nuestra base de datos en el contenedor **“db”**

![](imagenes/3.png)





Este será el contenido de **“dbname.sql”**


![](imagenes/4.png)




## **4. Parte 4**<a name="id4"></a>

Luego creamos el archivo **“index.php”** en el directorio www

![](imagenes/5.png)




Con el contenido que se ve en la siguiente imagen.

![](imagenes/6.png)




## **5. Parte 5**<a name="id5"></a>

Ejecutamos el comando **“docker-compose up -d”** para crear los contenedores

![](imagenes/7.png)

Ejecutaremos **“docker-compose ps”** y veremos que el contenedor **“conf\_db1”** no esta arrancado


![](imagenes/8.png)





Si revisamo el log de dicho contenedor, se nos avisa de que el usuario root ya existe y no puede crearse.

![](imagenes/9.png)

Paramos todos los contenedores mediante **“docker-compose down –volumes”** ya que será necesario hacer cambios en el archivo **“docker-compose.yml”**

![](imagenes/10.png)



## **6. Parte 6**<a name="id6"></a>

Una vez abierto el archivo, modificamos la linea **“MYSQL\_USER”** que anteriormente tenia el valor **“root”** por otro de nuestra elección.

![](imagenes/11.png)


## **7. Parte 7**<a name="id7"></a>

Volvemos a ejecutar **“docker-compose up -d”** para crear los contenedores de nuevo y vamos al navegador. Introducimos la dirección **127.0.0.1:8000** y nos deberá aparecer la pagina de inicio de sesión de **MySQL**. Nos logueamos con el usuario y la contraseña que aparece en el archivo **“docker-compose.yml”** y nos loguearemos en MySQL y deberemos tener la base de datos **“dbname”** creada.



![](imagenes/12.png)




## **8. Parte 8**<a name="id8"></a>

Ejecutamos de nuevo **“docker-compose down –volume”** para apagar y borrar los contenedores

![](imagenes/13.png)

Cogemos un archivo PHP nuestro y lo intercambiamos por el que creamos de inicio.




![](imagenes/14.png)

Volveremos a ejecutar **“docker-compose up -d”** para crear de nuevo los contenedores. Una vez arrancados abrimos el navegador y escribimos **“localhost”** y deberemos ver el php que hemos puesto en el paso anterior. En nuestro marca errores ya que el archivo que colocamos depende de otro archivo php.

![](imagenes/15.png)
