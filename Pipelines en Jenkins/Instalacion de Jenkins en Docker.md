## **Pipelines en Jenkins**

**Neftalí Rodríguez Rodríguez**

![](imagenes/logo.png)



[**Github**](https://github.com/InKu3uS/)

Indice

[Pipelines en Jenkins](#id1)

[2. Parte 1](#id1)

[2. Parte 2](#id2)

[3. Parte 3](#id3)

[4. Parte 4](#id4)

[5. Parte 5](#id5)

[6. Parte 6](#id6)

[7. Parte 7](#id7)

[8. Parte 8](#id8)




## **2. Parte 1**<a name="id1"></a>

Antes de empezar a crear nuevas tareas en Jenkins nos aseguraremos de tener los plugins necesarios instalados. Para ello nos dirigiremos a **“Administrar Jenkins”**, luego a **“Administrar plugins”** y en dicha pantalla buscaremos **“docker”** en el cuadro de busqueda. Necesitaremos los plugins **“docker plugin”** y **“docker pipeline”**. Marcamos ambos y pulsamos en instalar.

![](imagenes/0.png)

Marcaremos la opcion de que se reinicie Jenkins al acabar la instalación y esperamos a que se instalen los plugins



## **2. Parte 2**<a name="id2"></a>

Accedemos al panel de control de Jenkins y pulsamos sobre **“Nueva tarea”**. Nos llevará a la siguiente pantalla en la que le pondremos un nombre a la tarea y luego pulsamos sobre la opcion **“Pipeline”**


![](imagenes/1.png)


En la siguiente ventana que nos aparecerá a continuación, nos desplazamos al final de esta y pegamos el script que vamos a usar dentro del cuadro de texto “Pipeline script”

![](imagenes/2.png)

Una vez se haya creado la tarea pulsamos sobre **“Construir ahora”** y esperamos a que se ejecute la tarea.

![](imagenes/3.png)


Si la tarea se ha ejecutado con éxito, debemos ver una pantalla como la siguiente.

![](imagenes/5.png)


![](imagenes/6.png)

Si miramos la salida de la tarea, veremos la versión de que se ha ejecutado el comando **“mvn –version”** y se muestra la salida correctamente.


**3. Parte 3**<a name="id3"></a>

Creamos otra nueva tarea Pipeline, esta vez para **NodeJS**. Tal y como lo hicimos en el paso anterior pero cambiaremos el script por uno que descargue un **contenedor Docker de NodeJS** y ejecute el comando **“node –version”**.

![](imagenes/7.png)


Seguimos completando la tarea y esperamos a que se ejecute, si se ejecuta correctamente deberá mostrar la versión de **NodeJS** del contenedor.

![](imagenes/9.png)


## **4. Parte 4**<a name="id4"></a>

Repetimos el proceso, esta vez para un contenedor Docker de **Ruby**

![](imagenes/10.png)


Al ejecutarse la tarea correctamente, nos mostrará la versión de **Ruby** del contenedor.

![](imagenes/11.png)


## **5. Parte 5**<a name="id5"></a>

Crearemos otro Pipeline para un contenedor Docker de **Python** mediante el script que se muestra en la imagen.


![](imagenes/12.png)

Al finalizar la tarea nos mostrará la versión de **Python** del contenedor.

![](imagenes/13.png)


## **6. Parte 6**<a name="id6"></a>

Esta vez haremos lo mismo para un contenedor de **PHP** usando el siguiente scrtipt

![](imagenes/14.png)

Al finalizar podremos ver que se nos muestra la versión de **PHP** del contenedor.

![](imagenes/15.png)


## **7. Parte 7**<a name="id7"></a>

Por último, crearemos otro Pipeline para un contenedor **Go** usando el siguiente script

![](imagenes/16.png)

Al completarse la tarea, veremos la versión de **Go** del contenedor Docker.

![](imagenes/17.png)


## **8. Parte 8**<a name="id8"></a>

Si todas las tareas se han ejecutado con éxito, la pagina principal de Jenkins debería mostrarse de una manera similar a esta. Donde vemos con el tick verde que la ultima ejecución de los contenedores fue exitosa, el sol indica que las dos últimas ejecuciones no produjeron errores, el tiempo que ha pasado desde la última ejecución exitosa de la tarea, el último fallo (N/D en nuestro caso ya que ninguno falló), y la duración de la última ejecución.

![](imagenes/18.png)
