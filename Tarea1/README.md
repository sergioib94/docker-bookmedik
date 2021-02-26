# docker-bookmedik

Tarea 1: Ejecución de una aplicación web PHP en dockerPermalink

* Queremos ejecutar en un contenedor docker la aplicación web escrita en PHP: bookMedik (https://github.com/evilnapsis/bookmedik).

* Es necesario tener un contenedor con mariadb donde vamos a crear la base de datos y los datos de la aplicación. El script para generar la base de datos y los registros lo encuentras en el repositorio y se llama schema.sql. Debes crear un usuario con su contraseña en la base de datos. La base de datos se llama bookmedik y se crea al ejecutar el script.

* Ejecuta el contenedor mariadb y carga los datos del script schema.sql. Para más información. El contenedor mariadb debe tener un volumen para guardar la base de datos. El contenedor que creas debe tener un volumen para guardar los logs de apache2.

* Crea una imagen docker con la aplicación desde una imagen base de debian o ubuntu. Ten en cuenta que el fichero de configuración de la base de datos (core\controller\Database.php) lo tienes que configurar utilizando las variables de entorno del contenedor mariadb. (Nota: Para obtener las variables de entorno en PHP usar la función getenv. Para más infomación).

* La imagen la tienes que crear en tu máquina con el comando docker build.

* Crea un script con docker compose que levante el escenario con los dos contenedores.(Usuario: admin, contraseña: admin).

Entrega:

- Entrega la url del repositorio GitHub donde tengas la construcción (directorio build y el despliegue (directorio deploy))

- Entrega una captura de pantalla donde se vea funcionando la aplicación, una vez que te has logueado.

Tarea 2: Ejecución de una aplicación web PHP en dockerPermalink

* Realiza la imagen docker de la aplicación a partir de la imagen oficial PHP que encuentras en docker hub. Lee la documentación de la imagen para configurar una imagen con apache2 y php, además seguramente tengas que instalar alguna extensión de php.

* Crea esta imagen en docker hub.

* Crea un script con docker compose que levante el escenario con los dos contenedores.

Entrega:

- Entrega la url del repositorio GitHub donde tengas la construcción (directorio build y el despliegue (directorio deploy))

- Entrega una captura de pantalla donde se vea funcionando la aplicación, una vez que te has logueado.

Tarea 3: Ejecución de una aplicación PHP en dockerPermalink

* En este caso queremos usar un contenedor que utilice nginx para servir la aplicación PHP. Puedes crear la imagen desde una imagen base debian o ubuntu o desde la imagen oficial de nginx.

* Vamos a crear otro contenedor que sirva php-fpm.

* Y finalmente nuestro contenedor con la aplicación.

* Crea un script con docker compose que levante el escenario con los tres contenedores.

A lo mejor te puede ayudar el siguiente enlace: Dockerise your PHP application with Nginx and PHP7-FPM

Entrega:

- Entrega la url del repositorio GitHub donde tengas la construcción (directorio build y el despliegue (directorio deploy))

- Entrega una captura de pantalla donde se vea funcionando la aplicación, una vez que te has logueado.

Tarea 4: Ejecución de un CMS en dockerPermalink

* A partir de una imagen base (que no sea una imagen con el CMS), genera una imagen que despliegue un CMS PHP (que no sea wordpress).

* Crea los volúmenes necesarios para que la información que se guarda sea persistente.

* Elige un CMS PHP y crea la imagen que despliega la aplicación. Crea los contenedores necesarios para servir el CMS. Entrega una prueba de funcionamiento.

* Elimina los contenedores, vuelve a crearlos y demuestra que la información no se ha perdido.

Tarea 5: Ejecución de un CMS en dockerPermalink

* Busca una imagen oficial de un CMS PHP en docker hub (distinto al que has instalado en la tarea anterior, ni wordpress), y crea los contenedores necesarios para servir el CMS, siguiendo la documentación de docker hub.
 
* Explica el proceso que has seguido para realizar la tarea, pon alguna prueba de funcionamiento. ¿Se ha creado algún volumen para que la información sea persistente?
