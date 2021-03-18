# Evadir IDS, firewalls y Honeypots

> Objetivos: Comprensión de IDS, Firewall y Concepto de Honeypot: Soluciones IDS, Firewall y Honeypot: Comprensión de diferentes técnicas para eludir IDS: Comprensión de diferentes técnicas para eludir firewalls, IDS / Herramientas para evadir firewall: Comprensión de diferentes técnicas para detectar honeypots: Descripción general de IDS y Prueba de penetración de cortafuegos

### Conceptos de IDS, firewall y Honeypot

* Un IDS inspecciona todo el tráfico de red entrante y saliente en busca de patrones sospechosos que puedan indicar una violación de la seguridad de la red.
  * Comprueba el tráfico en busca de firmas que coincidan con los patrones de intrusión conocidos
  * Detección de anomalías 
  * Detección de anomalías de protocolo
  * Indicaciones de intrusiones
  * Intrusiones del sistema
  * Presencia de nuevos archivos
  * Cambios en los permisos de archivos
  * Cambios inexplicables en el tamaño del archivo
  * Archivos deshonestos
  * Nombres de archivos desconocidos en directorios
  * Archivos perdidos
  * Intrusiones de red
  * Sondas repetidas de los servicios disponibles en sus máquinas
  * Conexiones desde ubicaciones inusuales
  * Intentos de inicio de sesión repetidos desde hosts remotos
  * Datos arbitrarios en archivos de registro
  * Arquitectura de firewall
  * Anfitrión de bastión
  * Sistema informático diseñado y configurado para proteger los recursos de red de ataques
  * Subred protegida
  * También conocido como DMZ contiene hosts que ofrecen servicios públicos. La zona DMZ solo responde a las solicitudes públicas y no tiene hosts a los que acceda la red privada
  * Cortafuegos de múltiples hogares
  * Un firewall con dos o más interfaces
  * Zona desmilitarizada 
  * Una red que sirve como un búfer entre la red interna segura e Internet insegura
  * Se puede crear usando un firewall con tres o más interfaces de red principales
  * Tipos de firewall
  * Filtros de paquetes: funciona en las capas de red de OSI. Puede descartar paquetes si es necesario
  * Pasarelas de nivel de circuito: funciona en la capa de sesiones. La información transmitida a una computadora remota a través de una puerta de enlace a nivel de circuito parece haberse originado en la puerta de enlace. Supervisan las solicitudes para crear sesiones y determinan si se permitirá la sesión. Permiten o evitan flujos de datos
  * Pasarelas de nivel de aplicación: los proxies de nivel de aplicación pueden filtrar paquetes en la aplicación más adelante del OSI
  * Cortafuegos de inspección multicapa con estado: combina los aspectos de los otros tres tipos de cortafuegos
  * Honeyot (tarro de miel)
  * Recurso del sistema de información que está configurado expresamente para atraer y atrapar a las personas que intentan penetrar en la red de una organización.
  * Honeypot puede registrar intentos de acceso al puerto, monitorear las pulsaciones de teclas del atacante, mostrar señales tempranas, etc.
  * Honeypots de baja interacción: simula solo un número limitado de servicios y aplicaciones. No se puede comprometer
  * Honeypots de alta interacción: simula todos los servicios y aplicaciones. Puede ser completamente comprometido por atacantes.  

## Evadir IDS

* Ataque de inserción: IDS cree ciegamente y acepta el paquete
  * Evasión: el sistema final acepta un paquete que un IDS rechaza. El atacante está explotando la computadora host
  * Ataque DoS: los intentos de intrusión de los atacantes no se registrarán
  * Ofuscación: codificar la carga útil del ataque de una manera que la computadora objetivo entienda, pero el IDS no lo hará
  * Generación de falsos positivos: los atacantes con conocimiento del IDS de destino, crean paquetes solo para generar alertas. Hace que IDS genere una gran cantidad de alertas de falsos positivos. Luego úselo para ocultar el tráfico de ataque real
  * Empalme de sesiones
  * Técnica de evasión Unicode: los atacantes pueden convertir cadenas de ataque en caracteres Unicode para evitar la coincidencia de patrones y firmas en el IDS
  * Ataque de fragmentación: los atacantes seguirán enviando fragmentos con retrasos de 15 segundos hasta que toda la carga útil del ataque se vuelva a ensamblar en el sistema objetivo.
  * Los ataques TTL requieren que el atacante tenga un conocimiento previo de la topología de la red de la víctima
  * Paquetes RST no válidos
  * Utiliza una suma de comprobación para comunicarse con el host a pesar de que el IDS cree que la comunicación ha terminado
  * Bandera de urgencia
  * Se utiliza una bandera URG en el encabezado TCP para marcar los datos que requieren procesamiento urgente
  * Muchos IDS no abordan el puntero URG
  * Shellcode polimórfico: la mayoría de los IDS contienen firmas para cadenas de uso común dentro de shellcode. Esto se puede evitar mediante el uso de shellcode codificado que contenga un stub que decodifique el código de shell
  * Ataques de capa de aplicación: IDS no puede verificar la firma de un archivo comprimido

## Evadir cortafuegos

* El escaneo de puertos se utiliza para identificar puertos abiertos y servicios que se ejecutan en estos puertos
  * Los puertos abiertos se pueden probar más a fondo para identificar la versión de los servicios, lo que ayuda a encontrar vulnerabilidades en estos servicios
  * Firewalking: una técnica que utiliza valores TTL para determinar los filtros ACL de la puerta de enlace
  * El atacante envía un paquete TCP o UDP al firewall objetivo con un TTL configurado en un salto mayor
  * Captura de pancartas: las pancartas son anuncios de servicios proporcionados por los servicios en respuesta a solicitudes de conexión y, a menudo, contienen información sobre la versión del proveedor.
  * Suplantación de direcciones IP a una máquina confiable
  * Enrutamiento de origen: permite al remitente de un paquete especificar parcial o completamente la ruta de un paquete a través de una red, pasando por un firewall
  * Tiny Fragments: Forzar parte de la información del encabezado del paquete TCP en el siguiente fragmento
  * ICMP Tunneling: permite tunelizar un shell de puerta trasera en la porción de datos de los paquetes de eco ICMP
  * Ack Tunneling: permite tunelizar una aplicación de puerta trasera con paquetes TCP con el bit ACK configurado
  * Método de túnel HTTP: permite a los atacantes realizar varias tareas de Internet a pesar de las restricciones impuestas por los firewalls. El método se puede implementar si la empresa de destino tiene un servidor web público con el puerto 80 utilizado para el tráfico HTTP

## Detectando Honeypots

* Los atacantes crean paquetes de sondeo maliciosos para buscar servicios como HTTP sobre SSL, SMTP sobre SSL e IMAP.
  * Los puertos que muestran un servicio en particular en ejecución pero niegan un protocolo de enlace de tres vías indican la presencia de un honeypot

