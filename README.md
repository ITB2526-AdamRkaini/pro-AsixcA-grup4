# pro-AsixcA-grup4
# Proyecto Transversal ASIXc1 — InnovateTech
**Grupo:** pro-AsixcA-grupo4  
**Miembros:** Erik Pandales, Steven Ramirez, Aleix Ramon, Adam Rkaini  
**Curso:** 25/26 · Instituto Tecnológico de Barcelona

## Índice
- [Fase 1 — Arquitectura CPD](./fase1-cpd.md)
- [Fase 2 — Servicios de Audio y Vídeo](./fase2-audio-video.md)
- [Fase 3 — Base de Datos](./fase3-bbdd.md)
- [Fase 4 — Servidor Web](./fase4-servidor-web.md)
- [Fase 5 — Comprobación funcionamiento](./fase5-comprobaciones.md)

# FASE 1: ARQUITECTURA DEL ESPACIO FÍSICO, DISEÑO ESTRUCTURAL Y SEGURIDAD

**Objetivo:** Modernizar nuestra infraestructura informática para que sea rápida, segura, consuma poca energía y no nos cueste una fortuna.

A continuación, explicamos de forma sencilla cómo vamos a montar nuestro nuevo Centro de Datos y la nube.

## 1.1. Organización Física de la Sala

### 1.1.1. Los Armarios (Racks)
Vamos a arrancar con dos armarios grandes estándar. Para tenerlo todo ordenado, los vamos a dividir así:
* **Armario 1 (Comunicaciones):** Aquí pondremos todo lo que conecta a la empresa con el mundo (routers, los sistemas de seguridad y los cables de red).
* **Armario 2 (Cerebro y Memoria):** Aquí irán los servidores (donde se procesa la información) y los discos duros gigantes donde guardaremos los datos.

### 1.1.2. Nuestra Estructura: Suelo Técnico y Techo Técnico
Para que la sala no sea un caos de cables y sea fácil hacer reparaciones, vamos a separar las cosas por "carreteras" distintas:
* **Por debajo (Suelo técnico elevado):** Solo van a pasar los cables de la luz eléctrica y, lo más importante, el aire frío para refrescar los equipos.
* **Por arriba (Techo técnico):** Colgaremos unas bandejas del techo por donde irán todos los cables de datos (los de internet y fibra). Así, si un técnico necesita cambiar un cable de red, lo tiene a mano arriba y no se mezcla con la electricidad (lo que además evita interferencias).

## 1.2. Ubicación y Parámetros Atmosféricos

### 1.2.1. El Local ideal
Hemos elegido una habitación en una planta intermedia del edificio que no tiene ventanas. ¿Por qué?
Porque si nos ponemos en la planta baja nos podemos inundar, y en el tejado podemos tener goteras. Al no tener ventanas, nadie de fuera puede ver qué hay dentro, es más seguro y, sobre todo, no nos entra el calor del sol, lo que nos ahorra muchísimo dinero en aire acondicionado.

### 1.2.2. Parámetros Atmosféricos y Climatización
Los servidores son como estufas, así que el clima de la sala es vital para que no se rompan:
* **Temperatura (Pasillos fríos y calientes):** Vamos a hacer que el aire frío salga por el suelo justo delante de los equipos. Los equipos lo "respiran", se enfrían, y sueltan el aire caliente por la parte de atrás, que sube al techo y se extrae. Así no se mezcla el aire frío con el caliente y enfriamos la sala gastando mucha menos luz.
* **Humedad controlada (45%-55%):** Esto es súper importante. Si el aire de la sala es muy seco, se genera electricidad estática y un chispazo puede freír un servidor. Si es muy húmedo, se crea agua (condensación) y los equipos se oxidan o hacen cortocircuito. Mantendremos la humedad siempre a la mitad exacta.
* **Calidad del aire:** Usaremos filtros antipolvo potentes para que no entre suciedad que pueda atascar los ventiladores de los servidores.

## 1.3. Los Equipos Informáticos (Hardware)
* **Servidores "Virtuales":** En lugar de comprar 20 ordenadores normales para 20 tareas distintas, vamos a comprar unos pocos servidores súper potentes. Usando un programa especial, vamos a dividirlos internamente para que cada uno funcione como si fueran muchos ordenadores pequeños. Ahorramos mucho espacio físico, dinero y electricidad.
* **Cables cortos y rápidos:** Para no tener cables kilométricos cruzando la sala, pondremos el enchufe principal de la red en la parte de arriba de cada armario. Usaremos cables de cobre modernos (muy rápidos y baratos) para distancias cortas, y cables de fibra óptica para conectar los armarios entre sí a la velocidad de la luz.

## 1.4. Electricidad y Baterías de Respaldo
Queremos que el sistema nunca se apague por sorpresa, así que todo va por duplicado:
* **Doble enchufe:** Cada máquina importante tendrá dos cables de corriente conectados a fuentes eléctricas distintas (Línea A y Línea B). Si falla un lado, el otro sigue funcionando.
* **Baterías de emergencia (SAIs):** Tendremos unas baterías gigantes que nos darán entre 15 y 20 minutos de vida si hay un apagón general. Este tiempo es perfecto: nos da margen suficiente para que arranque nuestro generador de gasolina o, en el peor de los casos, para que los servidores se apaguen solitos con cuidado, sin que perdamos ningún archivo.

## 1.5. Seguridad: Nadie entra sin permiso
* **Seguridad Física:** A la sala de servidores solo entrará la gente autorizada. Hará falta usar una tarjeta de empleado y además teclear un PIN. Pondremos cámaras de seguridad en los pasillos, pero apuntando de forma que no puedan grabar qué estamos haciendo en las pantallas. Si hay un fuego, tenemos un gas especial que apaga las llamas de golpe pero que no deja manchas ni estropea los ordenadores (no podemos usar agua, obviamente).
* **Seguridad Digital:** Instalaremos un "portero de discoteca" virtual (Firewall) muy estricto para frenar ataques de internet. Dividiremos la red en compartimentos para que, si un virus entra por un ordenador de un usuario, no pueda saltar a los servidores. Además, guardaremos todos los datos valiosos por duplicado y haremos copias de seguridad usando la regla del 3-2-1 (tres copias, en dos formatos distintos, y una fuera de la oficina).

## 1.6. Cuidando a nuestro equipo - Riesgos Laborales
Queremos que quien trabaje en la sala esté a salvo y cómodo:
* Pondremos un suelo especial que evita calambres o descargas eléctricas.
* Como los servidores pesan muchísimo, compraremos unas pequeñas grúas elevadoras para meterlos en los armarios sin que nadie se destroce la espalda.
* En esa sala hay un zumbido constante por los ventiladores que, a la larga, daña los oídos. Para solucionarlo, forraremos las paredes con paneles que absorben el ruido y será obligatorio entrar con cascos de protección auditiva.

## 1.7. Trabajando con Internet - Nuestra Nube en Amazon
No todo tiene que estar en nuestra oficina. Vamos a ser prácticos y a repartir el trabajo entre nuestra sala y los servidores de Amazon (AWS):
* **Lo público fuera, lo privado en casa:** La web de la empresa y todo lo que tiene que estar expuesto a internet lo alojaremos en Amazon. Así, si recibimos muchas visitas o un ataque cibernético fuerte, los servidores gigantes de Amazon lo soportarán. Sin embargo, nuestros secretos, contraseñas y datos privados de clientes se quedan en nuestro cuarto de servidores.
* **Gestión segura y a distancia:** Para manejar los equipos que tenemos en Amazon, lo haremos de forma automática con pequeños programas (Ansible). Para conectarnos a ellos, no usaremos contraseñas normales que nos puedan robar, sino que entraremos por una única "puerta" súper vigilada (Bastion Host) usando llaves digitales (ficheros secretos) que solo tenemos nosotros.

## 1.8. Diseño inicial de nuestro CPD

<!-- ========================================== -->
<!-- HUECO PARA INSERTAR LA IMAGEN DEL DISEÑO -->
![Esquema del Diseño Inicial del CPD](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/modelo-final.jpg)
<!-- ========================================== -->

*(Leyenda de los componentes del diseño que aparecen en la imagen adjunta)*
* **Estructura del edificio:** Techo real, falso techo, suelo técnico elevado, baldosas perforadas y suelo real (forjado).
* **Climatización:** Zona de extracción de aire caliente, pasillo caliente, pasillo frío, impulsión de aire frío.
* **Cableado:** Bandeja de cableado de datos por el techo (Fibra y cobre CAT 6a), conductos eléctricos y PDU inteligentes por el suelo (Línea A y B).
* **Seguridad y Extinción:** Acceso doble factor (Card + PIN), gas Novec 1230.
* **Riesgos Laborales:** Avisos de ruido alto (uso de protección auditiva), suelo antiestático y mecanismo Server Lifter.
* **Rack 1 (Telecomunicaciones):** Routers, Switches, Firewalls, Switches ToR, cableado Cat 6a UTP.
* **Rack 2 (Servidores y Almacenamiento):** Clúster de virtualización denso, SAN/NAS arrays.


# FASE 2. IMPLANTACIÓN DE LOS SERVICIOS DE AUDIO-VÍDEO Y VIDEOCONFERENCIA
## 2.5. Server-Videoconferencias
 
Creación de usuario de administración:
 
![Creación de usuario de administración](images.Adam/image43.png)
 
ip a de la máquina:
 
![ip a de la máquina](images.Adam/image24.png)
 
Generación clave SSH:
 
![Generación clave SSH](images.Adam/image37.png)
 
Cambiamos el hostname de la máquina de videoconferencia.
 
![Cambio de hostname](images.Adam/image20.png)
 
Descargamos la firma de Jitsi para verificar que vamos a descargar el auténtico y no uno falso o un virus.
 
![Descarga firma Jitsi](images.Adam/image42.png)
 
Añadimos el repositorio de descarga de la página web de Jitsi.
 
![Repositorio Jitsi](images.Adam/image1.png)
 
Actualizamos los repositorios una última vez e instalamos ya el jitsi-meet:
 
![sudo apt update](images.Adam/image35.png)
 
![sudo apt install jitsi-meet](images.Adam/image41.png)
 
Ponemos la IP pública de la máquina como el dominio para más tarde usarla y poder acceder a la página mediante la IP.
 
![Configuración dominio Jitsi](images.Adam/image22.png)
 
Generamos un certificado nuevo.
 
![Generación certificado](images.Adam/image19.png)
 
Añadimos este bloque de configuración en el archivo localizado en `/etc/jitsi/videobridge/jvb.conf` con la IP pública y privada de la máquina AWS:
 
![Configuración jvb.conf](images.Adam/image6.png)
 
Reiniciamos el servicio para aplicar bien los cambios:
 
![Reinicio de servicios](images.Adam/image10.png)
 
Buscamos la web por la IP pública de la máquina:
 
![Acceso web Jitsi](images.Adam/image31.png)
 
Saldrá una pantalla roja. **Esto es correcto y esperado**, ya que configuramos un certificado *autofirmado*. Hacemos clic en "Configuración avanzada" y luego en "Acceder a... (no seguro)").
 
Iniciamos la conferencia correctamente; cualquiera puede acceder poniendo la IP en el buscador:
 
![Videoconferencia funcionando](images.Adam/image28.png)
 
---
 
## 2.6. Server-logs-Adam
 
Creación de usuario de administración:
 
![Creación de usuario de administración](images.Adam/image9.png)
 
![Creación de usuario de administración](images.Adam/image29.png)
 
Generación clave SSH:
 
![Generación clave SSH](images.Adam/image26.png)
 
Cambiamos el hostname de la máquina:
 
![Cambio de hostname](images.Adam/image44.png)
 
Buscamos las líneas siguientes y las descomentamos en el archivo `/etc/rsyslog.conf`:
 
![Descomentamos líneas en rsyslog.conf](images.Adam/image25.png)
 
Además, al final del archivo añadimos estas tres líneas que nos permitirán organizar mejor los logs:
 
![Líneas añadidas al final de rsyslog.conf](images.Adam/image23.png)
 
Reiniciamos los servicios para aplicar bien los cambios:
 
![Reinicio de rsyslog](images.Adam/image15.png)
 
Comprobamos que el servidor está escuchando ya a internet:
 
![Comprobación de puertos](images.Adam/image46.png)
 
Añadimos líneas específicas con las IPs de las máquinas del grupo en la sección de Security Group de la máquina de logs para limitar el acceso a otras máquinas.
 
![Security Group](images.Adam/image14.png)
 
Además, añadimos estas dos líneas con las IPs en el documento `/etc/rsyslog.conf`:
 
![AllowedSender en rsyslog.conf](images.Adam/image2.png)
 
En los equipos de los integrantes del equipo de los que vayamos a recibir logs vamos al archivo de configuración `/etc/rsyslog.conf` y al final añadimos la configuración correspondiente.
 
Hacemos un restart del servicio para aplicar cambios:
 
![Restart rsyslog](images.Adam/image12.png)
 
Comprobamos con la prueba desde el equipo de un integrante con el comando `logger -t PROYECTO "Hola Adam, esto es un log de prueba de Eric"`:
 
![Prueba de log remoto](images.Adam/image4.png)
 
### Montar servicio web de logs para ver gráficamente
 
![Instalación dependencias Grafana](images.Adam/image36.png)
 
![Añadir repositorio Grafana](images.Adam/image40.png)
 
Instalamos el Grafana:
 
![Instalación Grafana](images.Adam/image13.png)
 
Activamos los servicios:
 
![Activación servicios Grafana](images.Adam/image38.png)
 
Instalamos Loki y Promtail de los repositorios de GitHub:
 
![Descarga Loki](images.Adam/image3.png)
 
![Descarga Promtail](images.Adam/image34.png)
 
![Instalación Loki y Promtail](images.Adam/image11.png)
 
![Instalación Loki y Promtail](images.Adam/image8.png)
 
Configuramos el archivo `/etc/promtail/config.yml` y añadimos este bloque:
 
![Configuración promtail config.yml](images.Adam/image30.png)
 
Arrancamos los dos servicios:
 
![Arranque Loki y Promtail](images.Adam/image7.png)
 
Entramos a la web:
 
![Login Grafana](images.Adam/image5.png)
 
Nos solicita cambiar la contraseña después del primer inicio de sesión; la cambiamos por "pirineus".
 
En el apartado Connections del menú izquierdo, añadimos exactamente `http://localhost:3100` en el campo Connection URL y guardamos los cambios.
 
![Conexión Loki en Grafana](images.Adam/image21.png)
 
![Data source conectado correctamente](images.Adam/image39.png)
 
Vamos a Explore, seleccionamos Loki y en el apartado Code escribimos exactamente la línea `{job="rsyslog-remote"}` y le damos al botón azul de Run query. Ahora podemos ver los logs en tiempo real y los hechos anteriormente.
 
![Logs en tiempo real en Grafana](images.Adam/image16.png)
 
---
 
### ANSIBLE
 
Actualización de los repositorios:
 
![Actualización repositorios](images.Adam/image32.png)
 
Instalación de Ansible:
 
![Instalación Ansible](images.Adam/image33.png)
 
Configuración del playbook:
 
![Configuración del playbook](images.Adam/image17.png)
 
Ejecución del playbook exitosa:
 
![Ejecución del playbook](images.Adam/image18.png)
 
Comprobación de que funciona correctamente:
 
![Comprobación Grafana](images.Adam/image45.png)
 
Creación de dashboard personalizado:
 
![Dashboard personalizado](images.Adam/image27.png)

# FASE 3. CREACIÓN DE LA BASE DE DATOS

## 3.1. Preparación del entorno

El primer paso fue verificar la conectividad de la máquina y preparar el usuario de administración.

[![Preparación entorno](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-000.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-000.png)

Creamos el usuario de administración `adminitb`, le damos permisos `sudo` y creamos la carpeta SSH para el nuevo usuario, copiando las claves autorizadas y ajustando permisos:

```bash
sudo adduser adminitb --disabled-password --gecos ""
sudo usermod -aG sudo adminitb
sudo mkdir -p /home/adminitb/.ssh
sudo cp ~/.ssh/authorized_keys /home/adminitb/.ssh/
sudo chown -R adminitb:adminitb /home/adminitb/.ssh
sudo chmod 700 /home/adminitb/.ssh
sudo chmod 600 /home/adminitb/.ssh/authorized_keys
sudo apt update && sudo apt upgrade -y
```

## 3.2. Instalación MariaDB

Instalamos MariaDB y verificamos que el servicio arranca correctamente:

[![Estado servicio MariaDB](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-001.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-001.png)

La versión instalada es **MariaDB 11.8.6**. A continuación creamos también el usuario de administración y la carpeta SSH.

[![Creación usuario adminitb](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-002.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-002.png)

### Securización de MariaDB

Como `mysql_secure_installation` no funcionaba, lo hicimos manualmente entrando directamente como root. Pusimos contraseña a root, eliminamos usuarios anónimos, bloqueamos el acceso remoto de root, borramos la BD de test y recargamos privilegios.

[![Securización manual MariaDB](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-003.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-003.png)

## 3.3. Creación de la base de datos

### Creación de la BD

Creamos la base de datos del proyecto con charset `utf8mb4` y verificamos que se ha creado:

[![CREATE DATABASE y SHOW DATABASES](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-004.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-004.png)

Entramos a la base de datos:

[![USE innovatetech_db](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-005.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-005.png)

### Creación de tablas

Creamos todas las tablas del proyecto — bloque de Gestión del Personal (departaments, empleats) y bloque de Sistema de Comunicación (grups_qualitat, usuaris_comunicacio):

[![CREATE TABLE departaments y empleats](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-006.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-006.png)

### Inserción de datos de prueba

Insertamos datos iniciales en todas las tablas: departamentos, empleados, grupos de calidad y usuarios de comunicación:

[![CREATE TABLE grups_qualitat y usuaris_comunicacio](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-007.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-007.png)

### Creación de roles

Creamos cuatro roles (`admin`, `vendes`, `administracio`, `treballador`) con permisos diferenciados sobre las tablas de la base de datos:

[![INSERT datos de prueba](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-008.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-008.png)

### Creación de triggers

**Trigger 1 — Bloqueo de usuario:** impide hacer llamadas si el originador o el destinatario están bloqueados, y registra el intento en la tabla `avisos`.

**Trigger 2 — Quota de llamadas diarias (máx. 10):**

[![CREATE ROLE y GRANT privilegios](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-009.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-009.png)

### Evento de backup automático

Activamos el planificador de eventos y creamos un evento diario que exporta las tablas principales a ficheros CSV y registra el resultado en `control_backups`:

[![Triggers de bloqueo y quota diaria](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-010.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-010.png)

### Script de automatización de creación de usuarios

Creamos el script `crear_usuari.sh` que solicita nombre, contraseña y rol, valida que el rol sea correcto, comprueba que el usuario no exista, lo crea en MariaDB y genera un fichero `.sql` con el registro:

[![Evento ev_backup_diari](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-011.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-011.png)

Lo ejecutamos y mostramos la salida del SQL generado automáticamente:

[![Script crear_usuari.sh en nano](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-012.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-012.png)

## 3.4. Comprobaciones

### Tablas creadas

Verificamos que las 11 tablas se han creado correctamente:

[![Ejecución script y SQL generado](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-013.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-013.png)

### Roles y usuarios

Comprobamos los roles asignados y que la tabla `avisos` está vacía (aún sin eventos):

[![SHOW TABLES — 11 tablas](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-014.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-014.png)

### Prueba del trigger de bloqueo

Primero bloqueamos un usuario:

[![roles_mapping y avisos vacío](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-015.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-015.png)

Ahora intentamos hacer una llamada con el usuario bloqueado — como se puede ver, da error:

[![UPDATE estado bloqueado](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-016.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-016.png)



[![INSERT trucada con usuario bloqueado — ERROR 45000](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-017.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-017.png)

Comprobamos las llamadas que tiene el usuario 2 hoy:

[![SELECT COUNT trucadas usuario 2](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-018.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-018.png)

### Trigger de auditoría

Modificamos la tabla `empleats` y comprobamos que se ha registrado en `avisos`:

[![UPDATE empleats y SELECT avisos con registro de auditoría](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-019.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-019.png)

### Verificación de roles y datos de tablas

Comprobamos que los roles se han creado correctamente y vemos cómo se ha creado el usuario después de ejecutar `./crear_usuari.sh`:

[![roles_mapping con Steven creado](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-020.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-020.png)

Aquí podemos ver todas las tablas creadas correctamente con los inserts iniciales:

[![cat usuaris_creats.sql](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-021.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-021.png)

### Automatización con Ansible

Primeramente hemos instalado el servicio de ansible:

[![SELECT * FROM empleats, departaments, trucades y videos_streaming](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-022.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-022.png)


Automatizamos todo el despliegue con un playbook de Ansible que incluye instalación de MariaDB, configuración personalizada, arranque del servicio y creación del directorio de backups:

[![Playbook Ansible en nano](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-023.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-023.png)

El playbook se ejecutó correctamente sin errores:

[![Ejecución ansible-playbook — PLAY RECAP OK](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-024.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-024.png)

### Usuario webappuser y reglas de firewall

Algo que no habíamos tenido en cuenta antes fue crear el usuario `webappuser`, específico para el servidor web. Le damos permisos completos sobre la base de datos desde su IP:

[![CREATE USER webappuser y GRANT](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-025.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-025.png)

Añadimos la regla UFW que permite el puerto 3306 únicamente desde el servidor web:

[![UFW status verbose — puerto 3306 restringido](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-026.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-026.png)

## 3.5. Diagrama E/R

[![Diagrama E/R innovatetech_db](https://github.com/ITB2526-AdamRkaini/pro-AsixcA-grup4/raw/main/images/fase3-029.png)](/ITB2526-AdamRkaini/pro-AsixcA-grup4/blob/main/images/fase3-029.png)

## 3.6. Modelo Relacional

```
departaments (codi_dept PK, nom, telefon)

empleats (dni PK, nom, cognoms, adreca, telefon,
          codi_dept FK→departaments.codi_dept)

grups_qualitat (id_grup PK, nom_grup, qualitat,
                max_resolucio, max_bitrate_kbps)

usuaris_comunicacio (id_usuari PK, nom_complet, email,
                     extensio, estat, tipus, rol,
                     id_grup FK→grups_qualitat.id_grup,
                     data_bloqueig, bloqueig_temporal, data_fi_bloqueig)

trucades (id_trucada PK,
          id_originador FK→usuaris_comunicacio.id_usuari,
          id_destinatari FK→usuaris_comunicacio.id_usuari,
          data_inici, data_fi, durada_minuts,
          qualitat_usada, enllac_videotrucada)

valoracions_trucades (id_valoracio PK,
                      id_trucada FK→trucades.id_trucada,
                      puntuacio, comentari, data_valoracio)

videos_streaming (id_video PK, titol, descripcio,
                  categoria, durada_segons, data_publicacio,
                  enllac_streaming, paraules_clau)

mesures_amplada_banda (id_mesura PK, data_hora,
                       equip_mesurat,
                       id_operari FK→usuaris_comunicacio.id_usuari,
                       velocitat_baixada_mbps, velocitat_pujada_mbps,
                       latencia_ms, resultat, notes)

avisos (id_avis PK, usuari_bd, taula_afectada,
        operacio, data_hora, descripcio)

control_backups (id_backup PK, data_hora,
                 taules_incloses, resultat, notes)

configuracio_servidor (id_config PK, parametre, valor,
                       protocol, port, descripcio)
```


# FASE 4. SERVER WEB

## 4.1. Configuración Técnica

El primer paso es la creación de la máquina virtual que contendra la aplicación. En lugar de utilizar un servidor físico local, lo hemos hecho a traves de la nube mediante la plataforma Amazon Web Services (AWS). Esto nos garantiza que nuestro servidor esté operativo las 24 horas del día con una excelente estabilidad de red.

A nivel de especificaciones, seleccionamos una configuración estandarizada y eficiente para nuestro entorno:

* **SO:** Ubuntu Server 24.04 LTS. Elegimos una versión LTS (Soporte Extendido) porque nos asegura actualizaciones de seguridad y estabilidad durante varios años, lo cual es vital en cualquier entorno.
  
* **Tipo de Instancia:** t2.micro. Esta configuración nos aporta 1 vCPU (procesador virtual) y 1 GiB de memoria RAM, recursos perfectamente optimizados y suficientes para ejecutar con ligereza nuestro servidor web.

* **Nombre del Nodo:** Server-Web (SFTP), lo que nos permite identificarlo rápidamente dentro de nuestra red virtual de AWS.

![Página de AWS al crear la máquina virtual](images/image8.png)

![Página de AWS al crear la máquina virtual](images/image13.png)

Como se puede observar en la captura superior de la consola de AWS, el proceso de lanzamiento de la instancia requiere definir con precisión el hardware virtual. Al elegir Ubuntu Server como base, nos aseguramos de trabajar sobre un entorno Linux limpio, sin interfaz gráfica pesada, lo que permite aprovechar al máximo cada megabyte de la memoria RAM disponible para procesar las peticiones de los usuarios.



## 4.2. Elección del Software Web

Un cambio crítico que realizamos en la infraestructura durante el desarrollo del proyecto fue la elección del motor del servidor web. Aunque inicialmente se planificó utilizar Apache, finalmente decidimos instalar y configurar Nginx.

Esta decisión se justifica por motivos puramente técnicos y de rendimiento:

* **Consumo mínimo de memoria:** Apache consume mucha memoria RAM porque abre un proceso independiente por cada usuario que entra a la web. En una máquina con 1 GiB de RAM como la nuestra, esto podría saturar el sistema. Nginx, en cambio, utiliza un diseño avanzado basado en eventos que le permite atender a miles de usuarios simultáneamente usando poquísima memoria.

* **Velocidad en consultas en segundo plano:** Como nuestra web utiliza funciones que consultan continuamente las tablas de llamadas y transmisiones en segundo plano, Nginx es capaz de enviar y recibir estos datos de una forma muchísimo más rápida y fluida, evitando que la página web se quede congelada.



## 4.3. Mecanismos de Seguridad: Llaves SSH y Grupos de Seguridad

Para garantizar que nuestro servidor no sea interceptado o controlado por terceros en el entorno digital de Amazon Web Services, la plataforma nos obliga a establecer dos barreras de protección obligatorias durante la creación de la instancia: el cifrado por par de llaves y el aislamiento  mediante un firewall lógico.



### 4.3.1. Autenticación Criptográfica: El Par de Llaves (Key Pair)

El uso de contraseñas tradicionales (como 1234 o admin) está completamente descartado porque son vulnerables a ataques de fuerza bruta. En su lugar, implementamos un sistema de Cifrado  mediante la generación de un par de llaves criptográficas (un archivo con extensión .pem).

Este mecanismo funciona  como un candado y su llave:

* **La Llave Pública:** Se queda guardada dentro del propio servidor en la nube. Actúa como el candado.

* **La Llave Privada:** Es el archivo  que nos descargamos a nuestra computadora física. Actúa como la llave para abrir el candado
  

![Página de AWS al crear la máquina virtual](images/image17.png)



### 4.3.2. Aislamiento de Red: El Grupo de Seguridad (Security Group)

Mientras que el par de llaves controla quién puede entrar al servidor, el Grupo de Seguridad controla qué tipo de tráfico tiene permitido viajar por la red hacia nuestra máquina. El Grupo de Seguridad es como un firewall virtual

Por defecto, AWS aplica una política de seguridad estricta: todo lo que intente entrar desde el exterior está prohibido. Para que nuestra aplicación web y nuestros servicios de transmisión puedan funcionar, tuvimos que definir "reglas de entrada" específicas.


![Página de AWS al crear la máquina virtual](images/image53.png)

![Página de AWS al crear la máquina virtual](images/Captura de pantalla 2026-05-27 223817.png)

* **Puerto TCP 22 (SSH):** Destinado a la administración remota, gestión del sistema operativo Ubuntu Server y tareas de despliegue por consola mediante terminal segura.

* **Puerto TCP 80 (HTTP):** Habilitado para permitir el acceso público y la navegación de los usuarios a la plataforma web a través de peticiones HTTP estándar.

* **Puerto TCP 443 (HTTPS):** Configurado para canalizar de forma segura el tráfico web cifrado mediante la implementación de certificados SSL/TLS.

* **Puerto TCP 3306 (MySQL):** Apertura técnica que permite la comunicación y las consultas relacionales  de la aplicación con el motor de la Base de Datos.

* **Protocolo ICMP IPv4 (Todos los ICMP):** Permite comprobar de forma inmediata el estado y la latencia entre las instancias del entorno (ping).


## 4.5. Configuración de una IP Elástica (Elastic IP)

Tras haber configurado los puertos de entrada de nuestra máquina virtual, el último paso indispensable en la configuración de la infraestructura  fue estabilizar una IP estatica. Por defecto, las instancias de Amazon EC2 reciben una dirección IP pública dinámica. Esto significa que si el servidor se reinicia por mantenimiento o actualizaciones, la IP cambia automáticamente, lo que rompería de inmediato los enlaces del proyecto y las conexiones de los usuarios.

Para evitar este problema y asegurar que nuestro Server-Web mantenga siempre la misma IP, procedimos a reservar y asociar una IP Elástica. Una IP Elástica es una dirección IP pública estática.

A continucaion explicaremos como lo hemos configurado:

Primero seleccionamos Elastic IP's en ajustes de Network ans Security 

![Página de AWS al crear la máquina virtual](images/image48.png)

Creamos la IP Elástica dandole al boton naranja 
![Página de AWS al crear la máquina virtual](images/image43.png)
![Página de AWS al crear la máquina virtual](images/image7.png)

Ahora desde la seccion de "Instancias" seleccionamos nuestra maquina y le daremos a seleccionar la IP Elástica que hemos creado

![Página de AWS al crear la máquina virtual](images/image9.png)
![Página de AWS al crear la máquina virtual](images/image21.png)
![Página de AWS al crear la máquina virtual](images/image16.png)



## 4.6. Procedimiento de Implementación

Una vez que la infraestructura física y el direccionamiento de red quedaron completamente estabilizados gracias a la IP Elástica,lo siguiente que harmeos del proyecto consistira en la preparación interna del sistema operativo. El objetivo de esta fase es instalar y configurar las herramientas de software necesarias  para que el servidor sea capaz de procesar las peticiones web y conectarse con el exterior.

Para llevar a cabo este procedimiento de forma limpia y ordenada, ejecutamos una secuencia de comandos estructurada directamente desde la consola de administración de Ubuntu Server.


### 4.6.1. Actualización de los Repositorios del Sistema

Antes de la instalación de cualquier servicio, hemos realizado una actualización inicial del sistema.

![Página de AWS al crear la máquina virtual](images/image4.png)
![Página de AWS al crear la máquina virtual](images/image41.png)

## 4.6.2. Creación y Configuración del Usuario

Trabajar directamente con el usuario administrador absoluto (root) o que crea AWS por defecto (ubuntu) es una práctica de alto riesgo. Si un atacante consiguiera interceptar la sesión, tendría el control total e inmediato de toda nuestra infraestructura.

Para Eliminar este peligro, procedimos a crear un usuario administrador personalizado dentro del sistema operativo, el cual cuenta con contraseñas seguras y permisos supervisados.

![Página de AWS al crear la máquina virtual](images/image36.png)

Para eliminar la dependencia de contraseñas, hemos transferido las credenciales de acceso del usuario ubuntu al nuevo usuario:

* **Creamos el directorio de configuración SSH para el nuevo usuario**
* **Copiamos las llaves públicas autorizadas**
* **Ajustamos los permisos y el propietario ( Para la seguridad SSH)**

![Página de AWS al crear la máquina virtual](images/image34.png)
![Página de AWS al crear la máquina virtual](images/image23.png)



## 4.6.3. Configuración del Cortafuegos Interno del Sistema Operativo (UFW)

Aunque previamente configuramos el Grupo de Seguridad externo en la consola web de AWS (el cual actúa como un firewall en la nube).
Necessitamos un firewall interno porque si el firewall de Amazon llegara a fallar, el propio sistema operativo Ubuntu debe tener su propia armadura interna activa para detener conexiones no deseadas.

Para levantar este segundo firewall, configuramos UFW

Primero pondremos por defecto todos los puertos desabilitados

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

A partir de este momento, cualquier intento de conexión hacia un puerto que no hayamos autorizado explícitamente será descartado en el mismo instante en que toque la interfaz de red del Server-Web.

## 4.7. Implementación del Servicio de Transferencia de Ficheros (SFTP)

Para cubrir el requerimiento de transferencia segura de archivos, hemos configurado un servicio SFTP con aislamiento (Chroot). Este diseño garantiza que los usuarios puedan subir y descargar archivos sin que tengan privilegios para navegar por las carpetas del sistema.
Editamos el archivo de configuración de SSH ya añadimos esta línea:

![Página de AWS al crear la máquina virtual](images/image52.png)
![Página de AWS al crear la máquina virtual](images/image6.png)

Hemos usado ChrootDirectory para crear una 'cárcel' lógica. Esto permite que cualquier persona  gestione archivos en el servidor con la total seguridad de que su acceso está limitado únicamente a los directorios autorizados, protegiendo la integridad del sistema operativo central.

## 4.8. Instalación del servidor web

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


## 4.9. Conexión con la Base de Datos
Instalamos el cliente mariadb para que nos podamos conectar

![Página de AWS al crear la máquina virtual](images/image45.png)

Mostrem com el port de SQL és accessible.

![Página de AWS al crear la máquina virtual](images/image3.png)

I aquí podem veure com podem entrar a la BBDD desde el web server amb les dades que ens han proporcionat.

![Página de AWS al crear la máquina virtual](images/image55.png)

Una vegada comprovat que podem accedir a la Base de Dades creem un arxiu dins del directori creat anteriorment (/var/www/innovate_web) y configurem amb els paràmetres que hem vist anteriorment.

![Página de AWS al crear la máquina virtual](images/image46.png)


## 4.10. Página Web
Usaremos php ya que HTML es estático, el servidor web se limita a transmitir el archivo tal cual está almacenado en el disco duro hacia el navegador del cliente, el cual realiza el trabajo.

Como ahora vamos a usar formato php, tenemos que instalar los paquetes necesarios para que pueda trabajar sin problemas ya que si no los instalamos es como que el servidor no puede leer o traducir esos datos.

![Página de AWS al crear la máquina virtual](images/image18.png)

![Página de AWS al crear la máquina virtual](images/image14.png)

Ahora para aplicarlo tenemos que editar el fichero de configuración de nginx que hemos utilizado anteriormente para cambiar a php 

IMPORTANTE QUE PONGAMOS LA VERSIÓN QUE ESTAMOS USANDO 

![Página de AWS al crear la máquina virtual](images/image44.png)


## 4.11. Archivos Creados
Para la  web, se ha desplegado un árbol de archivos donde cada componente cumple una función específica dentro de la aplicación:

![Página de AWS al crear la máquina virtual](images/image11.png)



## config.php (Configuración):

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














