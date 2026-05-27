# pro-AsixcA-grup4

BLOQUE 1: ARQUITECTURA DEL ESPACIO FÍSICO, DISEÑO ESTRUCTURAL Y SEGURIDAD

1.1.Nuestra Ubicación Estratégica de la Sala e Integración Sostenible

Nuestro diseño del Centro de Procesamiento de Datos (CPD) para Innovate Tech parte de la premisa de que la seguridad física del mundo real es la base indispensable para la estabilidad del entorno digital. 
Aprovechando la disponibilidad de nuestro presupuesto sin restricciones y con el objetivo de alcanzar la máxima eficiencia ecológica, determinamos la implantación de la sala en la planta intermedia del edificio corporativo.
Con esta decisión arquitectónica responde a nuestra doble estrategia de mitigación de riesgos ambientales y optimización de recursos:
Aislamiento frente a desastres naturales: Nosotros descartamos por completo los sótanos y las plantas bajas, eliminando de raíz la vulnerabilidad ante inundaciones provocadas por roturas en las redes generales de agua o por lluvias torrenciales que pongan en peligro la integridad del hardware. Asimismo, al evitar el ático o la última planta, nosotros esquivamos las filtraciones de agua por cubiertas y la radiación térmica solar directa.
Eficiencia energética pasiva: Nosotros proyectamos el CPD en el núcleo geométrico de la planta, rodeado por zonas comunes de oficinas. Estas oficinas actúan como un colchón térmico natural que aísla los servidores de las fluctuaciones de temperatura del exterior del edificio. Al no sufrir el impacto directo del clima de la calle, hacemos que las necesidades de refrigeración disminuyan de manera drástica, reduciendo de forma directa la huella de carbono de nuestra empresa y logrando una infraestructura altamente sostenible.







# FASE 4. SERVER WEB

## 4.1. Configuración Técnica

* **SO:** Ubuntu Server 24.04
* **Software Web:** Nginx
* **Seguridad:** Implementación de acceso mediante usuarios guardados en server el LDP

Primero que todo creamos una máquina con los requisitos que queremos

![Página de AWS al crear la máquina virtual](images/image8.png)
![Página de AWS al crear la máquina virtual](images/image13.png)
![Página de AWS al crear la máquina virtual](images/image17.png)
![Página de AWS al crear la máquina virtual](images/image53.png)
![Página de AWS al crear la máquina virtual](images/image31.png)
![Página de AWS al crear la máquina virtual](images/image40.png)
![Página de AWS al crear la máquina virtual](images/image33.png)
![Página de AWS al crear la máquina virtual](images/image47.png)

IP Elastica

![Página de AWS al crear la máquina virtual](images/image48.png)
![Página de AWS al crear la máquina virtual](images/image9.png)
![Página de AWS al crear la máquina virtual](images/image43.png)
![Página de AWS al crear la máquina virtual](images/image7.png)
![Página de AWS al crear la máquina virtual](images/image21.png)
![Página de AWS al crear la máquina virtual](images/image16.png)


## 4.4. Procedimiento de Implementación

Antes de la instalación de cualquier servicio, hemos realizado una actualización inicial del sistema.

![Página de AWS al crear la máquina virtual](images/image4.png)
![Página de AWS al crear la máquina virtual](images/image41.png)

Ahora hemos creado un usuario administrativo nominal para evitar el uso del usuario ubuntu por defecto. El acceso se realiza exclusivamente mediante autenticación por clave pública RSA eliminando cualquier vulnerabilidad asociada a contraseñas.

![Página de AWS al crear la máquina virtual](images/image36.png)

Para eliminar la dependencia de contraseñas, hemos transferido las credenciales de acceso del usuario ubuntu al nuevo usuario nominal:
Creamos el directorio de configuración SSH para el nuevo usuario
Copiamos las llaves públicas autorizadas
Ajustamos los permisos y el propietario ( Para la seguridad SSH)

![Página de AWS al crear la máquina virtual](images/image34.png)
![Página de AWS al crear la máquina virtual](images/image23.png)

## 4.5. Aseguramiento de la Infraestructura (Firewall)

Hemos implementado una política de "denegación por defecto y solo permitimos el tráfico necesario para el funcionamiento del servidor
Configuramos la política por defecto

![Página de AWS al crear la máquina virtual](images/image42.png)

Permitimos solo los puertos necesarios
Puerto 22/TCP — Protocolo SSH
Puerto 80/TCP — Protocolo HTTP
Puerto 443/TCP — Protocolo HTTPS

![Página de AWS al crear la máquina virtual](images/image22.png)

Verificamos

![Página de AWS al crear la máquina virtual](images/image26.png)

Activamos el firewall

![Página de AWS al crear la máquina virtual](images/image29.png)

## Implementación del Servicio de Transferencia de Ficheros (SFTP)

Para cubrir el requerimiento de transferencia segura de archivos, hemos configurado un servicio SFTP con aislamiento (Chroot). Este diseño garantiza que los usuarios puedan subir y descargar archivos sin que tengan privilegios para navegar por las carpetas del sistema.
Editamos el archivo de configuración de SSH ya añadimos esta línea:

![Página de AWS al crear la máquina virtual](images/image52.png)
![Página de AWS al crear la máquina virtual](images/image6.png)

Hemos usado ChrootDirectory para crear una 'cárcel' lógica. Esto permite que cualquier persona  gestione archivos en el servidor con la total seguridad de que su acceso está limitado únicamente a los directorios autorizados, protegiendo la integridad del sistema operativo central.

## Instalación del servidor web

Hemos optado por Nginx debido a su arquitectura basada en eventos, la cual gestiona las peticiones de forma más eficiente que los servidores web tradicionales. Esto nos permite garantizar una alta disponibilidad.

![Página de AWS al crear la máquina virtual](images/image15.png)
![Página de AWS al crear la máquina virtual](images/image28.png)

Nginx no usa VirtualHost como Apache, usa lo que se llaman server blocks. Vamos a crear uno nuevo para la empresa.

![Página de AWS al crear la máquina virtual](images/image38.png)

Ahora creamos el índice el cual vamos a ver al acceder a la página y ponemos una frase de prueba

![Página de AWS al crear la máquina virtual](images/image2.png)

![Página de AWS al crear la máquina virtual](images/image51.png)

Por último crearemos y configuraremos el fichero de configuración y lo activaremos 

![Página de AWS al crear la máquina virtual](images/image37.png)

Comprobamos que no hay errores de sintaxis 

![Página de AWS al crear la máquina virtual](images/image19.png)

Añadimos el enlace lógico para que la configuración se active en la web y reiniciamos.

![Página de AWS al crear la máquina virtual](images/image54.png)

También eliminaremos los archivos por defecto para asegurar que solo pueda acceder a nuestra web.

![Página de AWS al crear la máquina virtual](images/image1.png)

Verfificacion:

![Página de AWS al crear la máquina virtual](images/image20.png)


## Conexión con la Base de Datos
Instalamos el cliente mariadb para que nos podamos conectar

![Página de AWS al crear la máquina virtual](images/image45.png)

Mostrem com el port de SQL és accessible.

![Página de AWS al crear la máquina virtual](images/image3.png)

I aquí podem veure com podem entrar a la BBDD desde el web server amb les dades que ens han proporcionat.

![Página de AWS al crear la máquina virtual](images/image55.png)

Una vegada comprovat que podem accedir a la Base de Dades creem un arxiu dins del directori creat anteriorment (/var/www/innovate_web) y configurem amb els paràmetres que hem vist anteriorment.

![Página de AWS al crear la máquina virtual](images/image46.png)


## 4.6. Página Web
Usaremos php ya que HTML es estático, el servidor web se limita a transmitir el archivo tal cual está almacenado en el disco duro hacia el navegador del cliente, el cual realiza el trabajo.

Como ahora vamos a usar formato php, tenemos que instalar los paquetes necesarios para que pueda trabajar sin problemas ya que si no los instalamos es como que el servidor no puede leer o traducir esos datos.

![Página de AWS al crear la máquina virtual](images/image18.png)

![Página de AWS al crear la máquina virtual](images/image14.png)

Ahora para aplicarlo tenemos que editar el fichero de configuración de nginx que hemos utilizado anteriormente para cambiar a php 

IMPORTANTE QUE PONGAMOS LA VERSIÓN QUE ESTAMOS USANDO 

![Página de AWS al crear la máquina virtual](images/image44.png)


## Archivos Creados
Para la  web, se ha desplegado un árbol de archivos donde cada componente cumple una función específica dentro de la aplicación:

![Página de AWS al crear la máquina virtual](images/image11.png)

### config.php (Configuración): 
Este archivo es fundamental porque aquí es donde se configura la conexión a la base de datos. Guarda los datos clave como la dirección IP del servidor (54.205.31.97), el usuario, la contraseña y el nombre de la base de datos.

![Página de AWS al crear la máquina virtual](images/image39.png)

### funciones.php (Herramientas): 
Es como una caja de herramientas. Contiene funciones de ayuda que se usan en la web, como por ejemplo el código necesario para transformar los datos de las tablas en un archivo descargable de Excel o CSV.

![Página de AWS al crear la máquina virtual](images/image27.png)

### auth.php : 
Es el vigilante de la web. Su única función es revisar si alguien intenta entrar a la web escribiendo la dirección IP sin haberse identificado, este archivo lo detecta y lo envía directamente a la pantalla de login.

![Página de AWS al crear la máquina virtual](images/image25.png)

### login.php (Pantalla de Acceso): 
Es el formulario donde el usuario pone su nombre y contraseña. Este archivo habla con el servidor de la empresa (LDAP/Directorio Activo) para comprobar que el usuario realmente trabaja ahí y que sus datos son correctos. 

![Página de AWS al crear la máquina virtual](images/image30.png)

Aquí podemos ver la parte del archivo que hemos configurado para que se pueda conectar al Servidor LDAP

![Página de AWS al crear la máquina virtual](images/image32.png)

### dashboard.php (Panel de Bienvenida): 
Es la primera pantalla que se ve al poner bien su contraseña. Le da la bienvenida, le muestra su nombre de usuario le da acceso a la gestión de las tablas.

![Página de AWS al crear la máquina virtual](images/image5.png)

### index.php (Pantalla Principal de Gestión): 
Es la página central de nuestro proyecto donde se junta todo. Muestra el menú lateral con las 11 tablas de la base de datos, el buscador en tiempo real, la tabla con los datos de los empleados o alertas, y los botones para exportar o cerrar sesión.

![Página de AWS al crear la máquina virtual](images/image10.png)

### buscador.php (El Motor de Búsqueda): 
Trabaja en segundo plano. Cuando el usuario escribe una letra en el buscador del index.php, este archivo va a la base de datos, busca lo que coincide y lo devuelve al instante.

![Página de AWS al crear la máquina virtual](images/image24.png)

### logout.php (Cierre de Sesión): 
Su función es borrar de la memoria del servidor cuando este hace clic en "Cerrar Sesión". Limpia los accesos y bloquea la pantalla para que nadie pueda volver a entrar dándole al botón de "Atrás" del navegador.

![Página de AWS al crear la máquina virtual](images/image27.png)

### Editar (Modificar datos): 
Esta función permite al usuario cambiar la información de una fila que ya existe en la base de datos (por ejemplo, actualizar el departamento de un empleado o corregir una alerta de backup).

![Página de AWS al crear la máquina virtual](images/image35.png)

![Página de AWS al crear la máquina virtual](images/image12.png)


### Eliminar (Borrar datos): 
Esta función permite limpiar el sistema eliminando registros que ya no son necesarios o que son erróneos (por ejemplo, borrar un aviso viejo). 

![Página de AWS al crear la máquina virtual](images/image35.png)

Si le damos al botón de eliminar nos aparece este mensaje 

![Página de AWS al crear la máquina virtual](images/image49.png)














