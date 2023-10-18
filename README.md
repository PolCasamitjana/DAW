1. Instale en una máquina virtual un sistema operativo con base Linux (se recomienda Debian o Ubuntu) e instale apache2.
   
En Debian:

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/cdebf043-7013-4a22-a239-b3ad86d93c95)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/97b80252-1003-4c9e-8639-247935126f96)

2. Explique con sus palabras que es una petición GET, POST, PUT y DELETE, remarcando sus diferencias. 

 

GET: Es una solicitud para obtener información del servidor. 

POST: Es una solicitud para enviar datos en el servidor, crear un recurso o actualizar uno que ya existe. Los cambios se pueden realizar en el servidor o en la base de datos. 

PUT: Es una solicitud para actualizar o reemplazar un recurso en concreto en el servidor. 

DELETE: Es una solicitud para eliminar un recurso en concreto del servidor. 

 

3. Cambie del puerto 80 al puerto 4444 el servidor apache2. Muestra desde el navegador su funcionamiento adjuntando una captura de pantalla.

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/71945460-40fc-41ad-b5f1-d23858ab01b8)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/2d196856-3c29-44e8-88b8-812c0b4d8c93)

4.Instale un certificado SSL y configure su Apache para servir contenido a través de HTTPS en el puerto 4444. Muestre desde el navegador cómo se muestra el sitio web como "seguro" (aunque sea un certificado autofirmado) 

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/884d640c-c1d8-4cf6-b6aa-df98f7eea8c8)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/04220812-38a9-4b02-b6ec-89495ddbde18)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/ddeead74-f061-4fc5-bf2f-02beb67b56db)

5. ¿Dónde se encuentran los ficheros de configuración de Apache2? 

• Ubicación principal. 

Se encuentran en /etc/apache2/apache2.conf 

• Explora el archivo apache2.conf. Identifica las secciones principales y describe su propósito. 

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/b5bbb7d4-5293-44f3-8a94-f49c3372b905)

• sites-available y sites-enabled: Explica la diferencia entre estos dos directorios y cómo funcionan juntos. 

“sites-available” contiene los archivos de configuración de los sitios web disponibles para ser utilizados. 

“sites-enabled” contiene enlaces simbólicos a los archivos de configuración de los sitios web que están activos. 

Cuando Apache2 se inicia o se reinicia, solo se cargan los archivos de configuación de los sitios web que se encuentran en el directorio sites-enabled. 

• mods-available y mods-enabled: Explica la diferencia entre estos dos directorios. 

La principal diferencia entre los dos es cómo se utilizan para administrar los módulos. 

“mods-available” contiene los archivos de configuración de los módulos disponibles para ser utilizados en Apache2. 

“mods-enabled” contiene enlaces simbólicos a los archivos de configuración de los módulos que están activos. 

 

6.¿Dónde se encuentran los ficheros de ejecución de Apache2? 

• Ubicación principal 

La ubicación principal es /etc/apache2/ 

• Control del servicio: Utiliza el binario de ejecución para iniciar, detener, recargar y reiniciar el servidor Apache2 explicando la diferencia entre cada uno de los comandos utilizados. 

sudo service apache2 start: Este comando inicia el servidor de Apache2. Inicia el proceso del servidor Apache2 y comienza a recibir las solicitudes. 

sudo service apache2 stop: Detiene el servidor Apache2. Deja de recibir las solicitudes entrantes. 

sudo service apache2 reload: Recarga el servidor Apache2. Recarga la configuración del servidor de Apache2 sin detener el proceso principal. 

sudo service apache2 restart: Reinicia el servidor Apache2. Lo detiene y luego lo inicia. 

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/ad9d7204-239a-479b-8035-f3c15806775a)

• Comprobación de sintaxis: Usa el binario de Apache para verificar la sintaxis de tu configuración. Esto es útil para asegurarse de que no haya errores antes de reiniciar el servidor.

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/64378c9a-89c9-4d39-935f-dabf31798e97)

7.¿Dónde se encuentran los ficheros de monitorización de Apache2? 

• Ubicación principal 

/etc/apache2/ 

• error.log y access.log: Explica la diferencia entre estos dos archivos. Abre y revisa las entradas recientes en cada uno de ellos. 

“error.log” registra los errores y advertencias relacionados con el servidor Apache2. 

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/d7f541cf-8d8b-41bf-acf9-442fcee51c63)

“access.log” registra los detalles de las solicitudes de acceso al servidor Apache2. Cada vez que se realiza una solicitud al servidor, se registra en este archivo. Incluye la direccion IP del cliene, la fecha y hora de la solicitud, el método de solicitud, la URL solicitada, el código de estado HTTP. 

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/3c6c9877-2f4a-4485-8f3b-3dc042419de3)

•  Rotación de logs: Investiga cómo funciona la rotación de logs en Apache2. ¿Por qué es importante? ¿Cómo se configura? 

Es importante por diferentes motivos: 

Ahorra espacio en disco. 

Mantenimiento de registros históricos. 

Mejora del rendimiento. 

Se configura de la siguiente manera: 

sudo nano /etc/logrotate.d/apache2 

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/671ea2db-c78d-4d47-818f-12bb6b2c34d8)

• Monitorización en tiempo real: Utiliza herramientas como tail -f para monitorear en tiempo real los accesos a tu servidor web y posibles errores. 

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/f803f987-5ed9-4123-af7f-8d7f197f440f)

• Análisis de logs: Instala y usa herramientas como goaccess para analizar y obtener estadísticas visuales a partir de tus logs de Apache2 

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/bb2585ce-28b9-41fa-a831-963534928875)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/e06317f7-2519-44ed-9a15-68f751e413b6)

8. ¿Qué es un Firewall? ¿Para qué sirve? ¿Por qué es necesario? Instale y configure un Firewall en la máquina virtual para que solo permita tráfico HTTP y HTTPS. Bloquee todo el resto de los puertos y demuestre su funcionamiento 

 

Es una barrera de seguridad que se utiliza para proteger una red de amenazas. 

También tiene la función de filtrar el tráfico de información que entra y sale de la misma red. 

Es necesario para tener una red segura en todo momento contra ataques / malwares. 

Vamos a instalar un firewall para Debian 11; ufw 

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/ff711305-2352-4cb8-8228-827879d8ad0f)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/05e6778e-f88f-42b4-888c-51264c304013)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/f7ea4301-52ef-4165-82e3-ff0c971192fa)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/673c0da6-1a5e-41e9-800b-8ee86458a0da)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/9f3f13fd-eed0-4b04-85ce-7ef9da0bf99b)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/30cd3cb9-762c-4b43-a06d-5475d9cb01fa)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/094ebbb6-39d9-49e5-886e-6c7a23806e7f)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/eeacaefa-af3b-4c97-ac29-7975c7a23ff9)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/ff4bde52-6408-4ffd-8514-0a73e1913284)

9. Explica con tus palabras las diferentes partes de una URL. 

 

Una URL tiene varias partes: 

Protocolo: Indica el protocolo que se utiliza, como HTTP o HTTPS. 

Dominio: Es el nombre del sitio web al que queremos acceder. 

Ruta: Ubicación concreta del recurso dentro del web. 

Parámetros: Elementos opcionales que transmiten info adicional. 

Fragmento: Referencia a una sección específica del recurso que se ha solicitado. 

 

10. Explica el funcionamiento del protocolo HTTP con tus palabras. 

 

El protocolo HTTP se utiliza para la comunicación entre cliente y servidor web. Funcionamiento: 

El cliente envía una solicitud HTTP al servidor. La solicitud incluye un método como GET, POST, PUT, DELETE, etc. 

El servidor web recibe dicha solicitud y la procesa. Si la solicitud es válida, el servidor envía la respuesta al cliente. La respuesta enviada incluye un código de estado. 

El cliente recibe la respuesta del servidor y la procesa. Dependiendo el código de estado, el cliente puede hacer diferentes acciones. 

El cliente y el servidor pueden continuar intercambiando más solicitudes y respuestas. 

 

11. ¿Qué es un archivo .htaccess? Proporcione un ejemplo de cómo se puede utilizar para reescribir URL o restringir el acceso a ciertas partes de su sitio web. 

 

Es un archivo de configuración utilizado en servidores web basados en Apache. 

Este archivo permite definir reglas para la configuración del servidor. 

EJEMPLO: 

Tenemos la siguiente URL: http://www.ejemploURL.com/index.php?id=1 

Queremos que los usuarios puedan acceder a ella mediante: http://www.ejemploURL.com/pagina1 

Agregamos las siguientes líneas al archivo .htaccess: 

RewriteEngine On 

RewriteRule ^pagina1$ index.php?id=1 [L] 

 

Para restringir el acceso podemos hacer lo siguiente: 

AuthType Basic 

AuthName "Acceso restringido" 

AuthUserFile /ruta/a/.htpasswd 

Require valid-user 
