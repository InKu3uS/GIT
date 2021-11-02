## **Instalación de Docker**

**Neftalí Rodríguez Rodríguez**

[**Github**](https://github.com/InKu3uS/)

![](Aspose.Words.18e8054f-54a1-4211-acca-97cec00511cb.001.png)









**TOC \o "1-10"Indice**

[Instalación de Docker	1](#__RefHeading___Toc445_2750294972)

[1. Primera parte	2](#__RefHeading___Toc5479_4026787900)

[2. Segunda parte	2](#__RefHeading___Toc5481_4026787900)

[3. Tercera parte	3](#__RefHeading___Toc5587_4026787900)

[4. Cuarta parte	3](#__RefHeading___Toc5589_4026787900)

[5. Quinta parte	4](#__RefHeading___Toc5591_4026787900)

[6. Sexta parte	4](#__RefHeading___Toc507_1893921560)

[7. Séptima parte	5](#__RefHeading___Toc509_1893921560)

[8. Octava parte	6](#__RefHeading___Toc511_1893921560)






##
##
##


##
## **1. Primera parte**

Primero haremos un **“apt update”** para actualizar los repositorios.

A continuación, con el comando **“sudo apt install apt-transport-https ca-certificates curl software-properties-common”** para poder instalar paquetes a traves de HTTPS.

![](Aspose.Words.18e8054f-54a1-4211-acca-97cec00511cb.002.png)
## **2. Segunda parte**
Luego, añadimos la clave **GPG** para el repositorio de **Docker**.

![](Aspose.Words.18e8054f-54a1-4211-acca-97cec00511cb.003.png)
##
##
##
##
##



## **3. Tercera parte**
Agregamos el repositorio de **Docker** y ejecutamos un **“apt update”** para actualizar la lista de paquetes

![](Aspose.Words.18e8054f-54a1-4211-acca-97cec00511cb.004.png)

## **4. Cuarta parte**
Comprobamos que el paquete **“docker -ce”** se va a descargar desde el repositorio de **Docker.**

![](Aspose.Words.18e8054f-54a1-4211-acca-97cec00511cb.005.png)







## **5. Quinta parte**
Ejecutamos **“apt install docker-ce”** para instalar comenzar la instalación de **Docker**.

![](Aspose.Words.18e8054f-54a1-4211-acca-97cec00511cb.006.png)
## **6. Sexta parte**
Una vez se haya completado la instalación, comprobamos que **Docker** esta activo con el comando **“systemctl status docker”**

![](Aspose.Words.18e8054f-54a1-4211-acca-97cec00511cb.007.png)
##
##

##
## **7. Séptima parte**
Usamos el comando **“docker run hello-world”** para comprobar que podemos acceder y descargar imágenes de **Docker**.

![](Aspose.Words.18e8054f-54a1-4211-acca-97cec00511cb.008.png)


















##
## **8. Octava parte**
Mediante el comando **“docker ps”** podremos ver los contenedores activos.

![](Aspose.Words.18e8054f-54a1-4211-acca-97cec00511cb.009.png)

Con el comando **“docker ps -a”** veremos los contenedores activos e inactivos.

![](Aspose.Words.18e8054f-54a1-4211-acca-97cec00511cb.010.png)

Mediante el comando **“docker ps -l”** podremos comprobar cual fue el ultimo contenedor cargado.

![](Aspose.Words.18e8054f-54a1-4211-acca-97cec00511cb.011.png)

Por último mediante el comando **“docker  images”** se nos mostrara todas las imágenes de Docker en nuestro equipo.

![](Aspose.Words.18e8054f-54a1-4211-acca-97cec00511cb.012.png)

