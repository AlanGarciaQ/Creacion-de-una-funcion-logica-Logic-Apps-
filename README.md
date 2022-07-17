# Creación de una función lógica (Logic Apps) 
**Objetivo:** Crear una función lógica por medio del recurso logic apps de Azure.

![](/imagenes/Logic-Apps.png)

**Requisitos**
- Cuenta de Azure con una suscripción activa
- Equipo de cómputo con sistema operativo: Windows, Linux o MacOs
- En Google Sheet crear un archivo en Excel y guardarlo en una carpeta en Google drive. El archivo será como se muestra a continuación.
![](/imagenes/Imagen0.png)
 
**Pasos**  
inicia sesión en Portal.Azure.com  
En la barra de búsqueda escribimos “Logic Apps” y lo seleccionamos.  
Damos clic en el apartado agregar

En la pestaña datos básicos, llenamos lo siguiente:  
**En Detalles del proyecto**  
Suscripción: La suscripción que queramos utilizar.  
Grupo de recursos: Podemos crear uno o seleccionar uno ya existente.
![](/imagenes/Imagen1.png)

**En Detalles de Instancia**  
Nombre de la aplicación: Ponemos el que queramos.  
Región: Podemos escoger cualquiera, pero si no queremos que haya mucha latencia escogemos uno cercano a donde vivimos.  
Habilitar Log Analitycs: Seleccionamos no.

En Plan  
Tipo de plan: Seleccionamos la opción de consumo.

Por último, damos clic en el botón de revisar y crear, y luego en crear.
![](/imagenes/Imagen2.png)

Cuando se termine de crear nuestro recurso, daremos clic en el botón de ir al recurso.
Seleccionamos la plantilla de aplicación lógica en blanco

En la barra de búsqueda de la ventana que se abrió buscamos Twitter y lo seleccionamos. (Con esto lo que vamos a hacer es que cada vez que recibamos un tuit va a desencadenar una acción).

En el campo nombre de la conexión ponemos el nombre que queramos que tenga nuestra conexión, en tipo de autentificación la dejamos como esta e iniciamos sesión en nuestra cuenta de Twitter.

En la ventana siguiente que se nos muestra llenamos el campo de texto de búsqueda con el siguiente texto: #IAWizards, la frecuencia va a ser cada 5 segundos.  
Damos clic en el botón de Nuevo Paso.

En la barra de búsqueda de la ventana que se abrió buscamos “text” y seleccionamos la opción de azure cognitive.  
Seleccionamos la opción de sentimiento.
![](/imagenes/Imagen3.png)

A continuación, tendremos que llenar unos apartados, pero para poder llenarlos tendremos que abrir otro portal Azure y en la barra de búsqueda escribimos “Cognitive services” y lo seleccionamos.  
Seleccionamos la opción que dice servicio de lenguaje.  
Damos clic en el botón de Continuar con la creación del recurso.  
En la pestaña datos básicos, llenamos lo siguiente:  
**En Detalles del proyecto**  
Suscripción: La suscripción que utilizamos anteriormente.  
Grupo de recursos: Seleccionar el que creamos anteriormente.

**En Detalles de Instancia**  
Región: Ponemos la misma que seleccionamos anteriormente.  
Nombre: Ponemos el que queramos.  
Plan de tarifa: Seleccionamos el gratis 

Las casilla las marcamos con la palomita y le damos en revisar y crear, y luego en crear.
![](/imagenes/Imagen4.png)

Cuando se termine de crear nuestro recurso, daremos clic en el botón de ir al recurso.  
En el menú de la parte de la izquierda le damos clic en la opción de claves y puntos de conexión.  
Copiamos la clave 1 y la pegamos en clave de cuenta de donde nos habíamos quedado en el anterior portal azure y hacemos lo mismo con la URL. En la ventana donde se pegó la clave y la URL le pondremos el nombre de la conexión y le daremos en crear. 
![](/imagenes/Imagen5.png)

![](/imagenes/Imagen6.png)

Llenamos el apartado de documents id y text como se ve en la imagen y le damos en nuevo paso.
![](/imagenes/Imagen7.png)

En la barra de búsqueda de la ventana que se abrió buscamos “Google sheet” y lo seleccionamos.
Seleccionamos insertar fila e iniciamos sección en nuestra cuenta de Google Drive.  
En archivo en la imagen de la carpeta seleccionamos el archivo donde se guardará la información de los Tweet. Y seleccionamos la hoja de cálculo donde se guardará.
![](/imagenes/Imagen8.png)

Seleccionamos todos los parámetros de la hoja de Excel y nos pedirá que seleccionemos con lo que se van a llenar. En la siguiente imagen se muestra cómo se llenan. Cuando se terminen de llenar le daremos clic en nuevo paso.
![](/imagenes/Imagen9.png)

En la barra de búsqueda escribimos teams y buscamos la opción que dice publicar mensaje en un chat o canal y la seleccionamos e iniciamos sesión en Teams.  
En la siguiente pestaña llenamos los datos como se muestra a continuación. Cuando se rellenen le damos en guardar.
![](/imagenes/Imagen10.png)

Nos vamos a Twitter y escribimos #IAWizards que habíamos puesto antes, y escribimos lo que queramos a continuación. En el portal azure le damos a ejecutar desencadenador y en Twitter lanzamos el Tuit. 
![](/imagenes/Imagen11.png)

En nuestra hoja de cálculo se mirarán todos los datos de los tuits que se ejecuten, así como en Teams.  
![](/imagenes/Imagen12.png)  
![](/imagenes/Imagen13.png)