## **Despliegue App Hola Mundo**

**Neftalí Rodríguez Rodríguez**

[**Github**](https://github.com/InKu3uS/)

![](imagenes/Tomcat.png)

**"Indice**


[1. Primera parte	2](#id1)

[2. Segunda parte	3](#id1)

[3. Tercera parte	4](#id1)

[4. Cuarta parte	5](#id1)

[5. Quinta parte	6](#id1)

[6. Sexta parte	7](#id1)

[7. Septima parte	7](#id1)

[8. Octava parte	8](#id1)

[9. Novena parte	9](#id1)

[10. Decima parte   9](#id10)





## **1. Primera parte**

Creamos un nuevo proyecto Maven en VSCode.

Pulsamos **CTRL+MAYUS+P** y pulsamos en **Create Java Project**

![](imagenes/1.png)










## **2. Segunda parte**

Pulsamos en **Maven from archetype**

![](imagenes/2.png)











## **3. Tercera parte**

Por ultimo en **maven-archetype-webapp**

![](imagenes/3.png)










## **4. Cuarta parte**

Y le ponemos un nombre al proyecto, en nuestro caso será **“demo”**

![](imagenes/4.png)








## **5. Quinta parte**

El resto de opciones las dejaremos por defecto ya que se trata de un proyecto de prueba y no nos haran falta.

Esperamos a que Maven termine de crear el proyecto, nos aparecerá una pantalla siguiente.


![](imagenes/5.png)








## **6. Sexta parte**

Creamos el siguiente archivo **web.xml** que aparece en la imagen.

![](imagenes/6.png)

## **7. Septima parte**
Modificamos el **index.jsp** y colocamos el mensaje que queramos que se muestre al inicio

![](imagenes/7.png)











## **8. Octava parte**

Ejecutamos **mvn clean install** desde la terminal de VSCode para compilar la App

![](imagenes/8.png)

En la carpeta target del proyecto veremos que ha aparecido el paquete en formato WAR con el nombre del proyecto.


![](imagenes/9.png)











## **9. Novena parte**

Lo siguiente que haremos será copiar el archivo WAR al directorio ***opt*/tomcat/apache-tomcat/webapps**

![](imagenes/10.png)


## **10. Decima parte**

Por último, accederemos desde el navegador para comprobar que la app se ha desplegado correctamente.

![](imagenes/11.png)
