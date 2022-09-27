# P1: Protocolo HTTP

1. Crea un repositorio para subir **todas las actividades de esta asignatura** con el nombre *despliegue-de-aplicaciones-web*.

    - Para crear un repositorio en GitHub tendremos que ir a la esquina superior derecha donde se encuentra un símbolo + y 
      luego una vez el menú se a desplegado le daremos a la opción de *new repository*.
   


2. Crea una carpeta en tu repositorio llamada "Actividad 1" y dentro crea un archivo README.md con la solución a los siguientes ejercicios.

    - Para crear carpetas dentro de un repositorio, lo que tendremos que hacer es acceder al menú del repositorio y le daremos a la etiqueta *Add File*,
      cuando estemos creando el nuevo documento escribiremos el nombre de la carpeta (Actividad 1) y luego pondremos una / para poner el nombre del archivo.



3. Analiza los headers de las peticiones cuando inicias sesión en el Moddle y comprende cómo se obtiene un token. 
   Para ello, necesitamos saber de dónde es salen **TODOS** los datos sensibles que se envían.

    - Para analizar las peticiones tendremos que ir a la página de inicio de sesión y luego hacer clic derecho "Inspeccionar" y dentro de este ir al apartado de "Red".
      Dentro de red vemos que la primera petición que hacemos al servidor "index.php", en esta petición se encuentra el **token**, este token es exclusivo para el 
      entorno Moodle y es que *logintoken* contiene el nombre del usuario y la contraseña. Esta información se obtiene de la llamada:
   
      -Nombre de la llamada: \core\session\manager::get_login_token()



4. ¿A qué puerto se reciben normalmente las peticiones del protocolo HTTP? ¿A qué capa del modelo TCP/IP se encuentra el protocolo HTTP?
    ¿Y los protocolos TCP, UDP e IP?
    
    - Las peticiones normalmente se reciben en el puerto 80 en TCP.
    - La capa del modelo TCP/IP donde se encuentra el protocolo HTTP, es la capa de aplicación.
    - La capa de modelo de TCP es una capa de Interfaz de red, el UDP proporciona una interfaz entre la capa de red y la capa de aplicación, finalmente 
      la IP se encuentra en la capa de interfaz de red.



5. ¿Cuál es el significado de la siguiente respuesta de un servidor? **HTTP/1.1 302 Found Location: http://www.example.com/test/index2.php**

    - Esta respuesta del servidor la hace cuando no encuentra el recurso solicitado donde solía estar y que este a sido movido temporalmente,
      a la URL dada por las cabeceras.


6. Utilizando el filtro de captura para la interfaz de red Wireshark, analiza la petición al host: www.google.com. Mostrando la cabecera IP, la dirección IP de tu ordenador y la del servidor. Comprueba que, poniendo esa IP en el navegador, accedas a Google. 

   - Viendo en el WireShark, y haciendo un filtrado de los Portocolos (TCP) comprobamos que "Destination" sea nuestra IP.
     Dirección de Google: **142.250.184.13**
   
   ![IP google](\Users\ramon\OneDrive\Escriptori\GIMBE 21-22\2nd Curso\IP google.jpg)
   
   

