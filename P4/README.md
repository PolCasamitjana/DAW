# P4: SERVIDORES VIRTUALES DE APACHE

1. Crea dos sitios web que compartirán IP y puerto, pero tendrán nombres DNS distintos 
para acceder a ellos. El nombre del primer dominio será daw.gimbernat.eug.es y el 
segundo tunombreyapellidos.gimbernat.eug.es, donde “tunombreyapellidos” contiene 
la inicial de tu nombre, el primer apellido, y la inicial de tu segundo apellido. De esta 
manera, si tu nombre es: Francisco Mesas Cervilla, el domino quedaría: 
fmesasc.gimbernat.eug.es.
• En el primer caso, daw.gimbernat.eug.es tendrá su directorio base en 
/var/www/daw/ conteniendo una página llamada index.html que ponga el 
nombre de la clase como título con un archivo css para aplicarle estilos al título.
• En el segundo caso, fmesasc.gimbernat.eug.es tendrá su directorio base en 
/var/www/fmesasc/ (el equivalente para vuestros nombres), conteniendo una 
página llamada index.html que contenga vuestro currículum aplicándole un 
estilo css para que se visualice correctamente.
Para ello, tendrás que crear un archivo de configuración (copiado de 000-default.conf) 
para cada uno de los dominios. Recuerda que con a2ensite puedes crear los enlaces 
simbólicos necesarios para añadir esta configuración a la ejecución de apache.

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/8ce30033-738a-4441-8c2c-1116e79d2fe7)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/612d656e-3ad7-4d04-8ed6-7db8eb74178d)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/a31706c9-83b1-414b-b356-b5adfbaf7495)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/68a5cdc6-658b-4901-a7be-198868531850)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/77e247cd-ccea-495b-b592-060ba87014eb)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/472ca38d-c238-4c21-9fce-731cd4f426e7)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/4466d439-f1c3-47ad-abb2-84dc2d87a9d1)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/c6fcf82d-4ecb-438f-9fa6-bc998c9e724b)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/8c6ad767-5b07-4ddc-b416-9e2f789e8646)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/b1bd5f34-b412-4aa8-b2a3-4276ebb12d06)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/3dcc0117-42e9-4f8f-bfcd-fc6824ad52f2)

![image](https://github.com/PolCasamitjana/DAW/assets/144775621/2633f026-04c1-45f5-ba68-b0d6bee712cb)

