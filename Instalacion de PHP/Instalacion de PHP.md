## **Instalación de PHP**

**Neftalí Rodríguez Rodríguez**

![](imagenes/php.png)

[**Github**](https://github.com/InKu3uS/)


**Indice**

[Instalación de PHP	1](#id0)

[1. Primera parte	2](#id1)

[2. Segunda parte	2](#id2)

[3. Tercera parte	3](#id3)

[4. Cuarta parte	4](#id4)

[5. Quinta parte	5](#id5)



## **1. Primera parte**<a name="id1"></a>


Antes de empezar haremos un **“apt update”** para actualizar la lista de paquetes.

![](Aspose.Words.1ede9667-352e-4edd-956c-49390d4b3f46.002.png)



## **2. Segunda parte**<a name="id2"></a>

Luego instalaremos PHP usando **“apt install -y php”**

![](Aspose.Words.1ede9667-352e-4edd-956c-49390d4b3f46.003.png)



## **3. Tercera parte**<a name="id3"></a>

Luego instalaremos **PHP-fpm** que es el que usaremos para Nginx


![](Aspose.Words.1ede9667-352e-4edd-956c-49390d4b3f46.004.png)



## **4. Cuarta parte**<a name="id4"></a>

Lo siguiente será dirigirnos al archivo **“/etc/nginx/sites-available/defaul”**, descomentar la linea donde aparece **“location”**, **“fastcgi”** y por último descomentaremos tambien el corchete de cierre y guardamos los cambios.

![](Aspose.Words.1ede9667-352e-4edd-956c-49390d4b3f46.005.png)

Una vez realizados los cambios, recargamos el servicio de Nginx

![](Aspose.Words.1ede9667-352e-4edd-956c-49390d4b3f46.006.png)



## **5. Quinta parte**<a name="id5"></a>

Para probar que tenemos PHP funcionando correctamente en Nginx creamos el siguiente archivo en **“var/www/html/”**


![](Aspose.Words.1ede9667-352e-4edd-956c-49390d4b3f46.007.png)

Por último, abriremos el navegador e introduciendo la dirección **“localhost:8084/info.php”** nos deberá aparecer la pagina de información de PHP.



![](Aspose.Words.1ede9667-352e-4edd-956c-49390d4b3f46.008.png)






















