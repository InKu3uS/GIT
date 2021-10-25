## **Instalación de servicios REST/WS en Wildfly**

![](imagenes/wildfly.png)

**Neftalí Rodríguez Rodríguez**

[**Github**](https://github.com/InKu3uS/)


**Indice**

[Instalación de servicios REST/WS en Wildfly](#__RefHeading___Toc445_2750294972)

[1. Primera parte](#id1)

[2. Segunda parte](#id2)

[3. Tercera parte](#id3)

[4. Cuarta parte](#id4)

[5. Quinta parte](#id5)

[5. Sexta parte](#id6)




## **1. Primera parte**<a name="id1"></a>


Antes de empezar con la práctica, deberemos acceder a al enlace <https://github.com/wildfly/quickstart/> y descargarnos el repositorio.

Una vez descargado, descomprimimos los proyectos de pruebas que vamos a usar. En nuestro caso serán **“helloworld-ws”** y **“helloworld-rs”.**

![](imagenes/1.png)


## **2. Segunda parte<a name="id2"></a>

![](imagenes/2.png)



Una vez descomprimidos los proyectos, los abrimos con **VSCode**, abrimos un terminal dentro del proyecto **“helloworld-rs”.**


En la terminal ejecutamos el comando **“mvn clean install”**

y esperamos a que maven descargue las librerias necesarias y cree el archivo **war** del proyecto.

![](imagenes/3.png)



## **3. Tercera parte**<a name="id3"></a>

Cuando el proceso del paso anterior haya terminado, accederemos a Wildfly desde nuestro navegador mediante la url **“localhost:8083”** y abriremos la consola de administración de Wildfly. Luego nos moveremos a **“Deployments”**, pulsaremos sobre el boton **+** que aparece en la imagen y clickaremos en **“Upload Deployment”.**


![](imagenes/4.png)

En la nueva ventana que se abrirá, buscaremos el archivo **war** que queremos desplegar y pulsaremos en **Next**, luego Wildfly nos preguntará si queremos cambiar el nombre del proyecto y por ultimo pulsaremos en **Finish**.

![](imagenes/5.png)


## **4. Cuarta parte**<a name="id4"></a>

Una vez desplegado, si hacemos click sobre el proyecto podemos ver un breve resumen del estado del proyecto, así como un enlace para acceder a él.

![](imagenes/6.png)


Haremos click en el enlace y probaremos que el proyecto funciona correctamente

![](imagenes/7.png)

![](imagenes/8.png)


## **5. Quinta parte**<a name="id5"></a>

Ahora haremos lo propio con el proyecto **“helloworld-ws”**, abriremos una terminal dentro del proyecto desde **VSCode** e introducimos el comando **“mvn clean install”**. Esperaremos a que se complete el proceso.

![](imagenes/9.png)


## **5. Sexta parte**<a name="id6"></a>

Ahora volveremos a la consola de administración de Wildfly para repetir el proceso y desplegar el nuevo **war** que se nos ha generado.

![](imagenes/10.png)

Una vez se haya completado el despliegue, veremos la ventana de características del proyecto donde se nos indica que se ha completado el despliegue.

![](imagenes/11.png)

Haremos click en el enlace para comprobar que funciona correctamente.

![](imagenes/12.png)
