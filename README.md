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
