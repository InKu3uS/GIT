## **Balanceo de Carga con Apache**

**Neftalí Rodríguez Rodríguez**

[**Github**](https://github.com/InKu3uS/)

![](imagenes/índice.png)






**Indice**

[Balanceo de Carga con Apache](#id1)

[1. Primera parte](#id1)

[2. Segunda parte](#id2)

[3. Tercera parte](#id3)

[4. Cuarta parte](#id4)

[5. Quinta parte](#id5)

[6. Sexta parte](#id6)

[7. Septima parte](#id7)





## **1. Primera parte**<a name="id1"></a>



Activamos los nodos necesarios para hacer balanceo de carga en Apache


![](imagenes/1.png)


![](imagenes/2.png)





## **2. Segunda parte**<a name="id2"></a>


Despues de activar todos los modulos necesarios, reiniciamos el servicio de Apache2




![](imagenes/3.png)



## **3. Tercera parte**<a name="id3"></a>

Editamos /etc/apache2/sites-available/000-default.conf y añadimos las siguientes lineas al archivo

![](imagenes/4.png)



## **4. Cuarta parte**<a name="id4"></a>

Creamos el archivo **Dockerfile** en el directorio raiz del proyecto con el contenido que aparece en la imagen.

![](imagenes/8.png)



## **5. Quinta parte**<a name="id5"></a>

Por ultimo creamos el archivo **“docker-compose.yml”** con 4 contenedores de **Wildfly** en los que se desplegará la app


![](imagenes/9.png)



## **6. Sexta parte**<a name="id6"></a>

Por último ejecutamos **“docker-compose up -d”** y esperamos a que se desplieguen los 4 contenedores

## **7. Septima parte**<a name="id7"></a>

Por último, abrimos el navegador e introducimos en la URL **“localhost:8081/app-web-demo/”** y comprobamos que funciona

![](imagenes/5.png)

![](imagenes/6.png)

![](imagenes/7.png)
