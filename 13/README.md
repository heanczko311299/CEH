# Hackear servidores web

> Objetivos: comprender los conceptos del servidor web, comprender los ataques al servidor web, comprender la metodología de ataque al servidor web, las herramientas de ataque al servidor web, las contramedidas contra los ataques al servidor web, la descripción general de la gestión de parches, las herramientas de seguridad del servidor web, la descripción general de las pruebas de penetración del servidor web

### Conceptos de servidor web

* Un servidor web es un programa que aloja sitios web, los atacantes suelen apuntar a vulnerabilidades de software y errores de configuración para comprometer los servidores.
* Hoy en día, los ataques a nivel de red y de sistema operativo se pueden defender bien utilizando medidas de seguridad de red adecuadas, como firewalls, IDS, etc. Los servidores web son más vulnerables a los ataques ya que están disponibles en la web.
* ¿Por qué están comprometidos los servidores web?
* Permisos de archivo / directorio incorrectos
* Instalación del servidor con la configuración predeterminada
* Servicios innecesarios habilitados
* Conflictos de seguridad
* Falta de una política de seguridad adecuada
* Autenticación incorrecta
* Cuentas predeterminadas
* Configuraciones incorrectas
* Errores en el sistema operativo
* Certificados SSL mal configurados
* Uso de certificados autofirmados
* IIS \ (servicio de información de Internet \) es una aplicación de servidor web desarrollada por Microsoft para Windows.

## Ataques a servidores web

* Ataques DoS / DDoS: los atacantes pueden enviar numerosas solicitudes falsas al servidor web, lo que provoca que el servidor web se bloquee o deje de estar disponible
* Puede apuntar a servidores web de alto perfil
* Secuestro del servidor DNS: el atacante compromete el servidor DNS y cambia la configuración de DNS para que todas las solicitudes que llegan al servidor web de destino se redirijan a otro servidor malicioso
* Ataque de amplificación de DNS: el atacante aprovecha el método recursivo de DNS de redirección de DNS para realizar un ataque de amplificación de DNS
* El atacante utiliza PC comprometidas con IP falsificadas para amplificar el ataque DDoS explotando el método recursivo de DNS
* Ataque transversal de directorio: los atacantes usan ../ para secuenciar para acceder a directorios restringidos fuera del directorio raíz del servidor web \ (prueba y error \)
* Man-in-the middle Sniffing Attack: los ataques MITM permiten que un atacante acceda a información confidencial interceptando y alterando las comunicaciones
* Ataques de phishing: el atacante engaña al usuario para que envíe detalles de inicio de sesión para un sitio web que parece legítimo pero no lo es. Intentos de robar credenciales
* Defacetación del sitio web: el intruso altera maliciosamente la apariencia visual de una página web al insertar datos ofensivos. Variedad de métodos como la inyección MYSQL
* Configuración del servidor web: se refiere a las debilidades de configuración en la infraestructura, como el cruce de directorios
* Ataque de división de respuestas HTTP: implica agregar datos de encabezado en el campo de entrada para que el servidor divida la respuesta en dos respuestas. El ataque puede controlar la segunda respuesta para redirigir al usuario a un sitio web malicioso, mientras que la otra respuesta será descartada por el navegador.
* Envenenamiento de caché web: un atacante obliga a la caché del servidor web a vaciar su contenido de caché real y envía solicitudes especialmente diseñadas, que se almacenarán en la caché.
* SSH Bruteforce Attack: los protocolos SSH se utilizan para crear un túnel SSH cifrado entre dos hosts. Los atacantes pueden usar la fuerza bruta de las credenciales de inicio de sesión SSH
* Craqueo de contraseñas del servidor web: un atacante intenta aprovechar las debilidades para piratear contraseñas bien elegidas \ (ingeniería social, suplantación de identidad, phishing, etc.).
* Ataques de aplicaciones web: las vulnerabilidades en las aplicaciones web que se ejecutan en un servidor web proporcionan una amplia ruta de ataque para comprometer el servidor web
* Inyección SQL, Cruce de directorios, DoS, Alteración de cookies, Ataque XSS, Desbordamiento de búfer, ataque CSRF

## Metodología de ataque:

Recopilación de información, implantación de servidores web, creación de reflejo de sitios web, análisis de vulnerabilidades, secuestro de sesiones, piratería de contraseñas de servidores web

* Recopilación de información: el archivo Robots.txt contiene una lista del directorio del servidor web y los archivos que el propietario del sitio web desea ocultar de los rastreadores web
* .Utilice herramientas como burp suite para automatizar el secuestro de sesiones

## Herramientas de ataque de servidor web

* Metasploit: encapsula un exploit.
* Módulo de carga útil: lleva una mochila al sistema para descargar
* Módulo auxiliar Metasploit: Realización de acciones arbitrarias y únicas, como escaneo de puertos, DoS y fuzzing
* Módulo NOPS: genera instrucciones de no operación utilizadas para bloquear búferes
* Descifrado de contraseña: THC Hydra, Cain & Abel

## Contramedidas

* Se debe diseñar una red de alojamiento web ideal con al menos tres segmentos, a saber: el segmento de Internet, el segmento de seguridad del servidor seguro \ (DMZ \), la red interna
* Colocó el servidor web en DMZ de la red aislado de la red pública así como de la red interna
* Deben colocarse firewalls para la red interna, así como para el tráfico de Internet que se dirige hacia DMZ
* Parches y actualizaciones: asegúrese de que los paquetes de servicios, las revisiones y los niveles de los parches de seguridad sean consistentes en todos los controladores de dominio
* Protocolos: bloquee todos los puertos innecesarios, ICMP y protocolos innecesarios como NetBIOS y SMB. Desactive WebDav si no se utiliza
* Archivos y directorios: elimine archivos innecesarios, deshabilite el servicio de listados de directorios, deshabilite el servicio de ciertos tipos de archivos, evite los directorios virtuales
* Detección de intentos de piratería: ejecute scripts en el servidor que detecten cualquier cambio realizado en el archivo ejecutable existente. Compare los valores hash de los archivos en el servidor para detectar cambios en la base de código. Alerta al usuario sobre cualquier cambio en la detección
* Asegure el SAM \ (solo servidores independientes \)
* Defensa contra el secuestro de DNS: elija un registrador acreditado por ICANN. Instalar antivirus

## Gestión de parches

* Las revisiones son una actualización para solucionar un problema específico del cliente
* Un parche es una pequeña pieza de software diseñada para solucionar problemas
* Las revisiones y revisiones a veces se combinan para paquetes de servidor
* La gestión de parches es un proceso que se utiliza para garantizar que se instalen los parches adecuados en un sistema para ayudar a corregir las vulnerabilidades conocidas.
* Antes de instalar un parche, verifique la fuente.
* Herramientas de administración de parches: MBSA \ (Microsoft baseline Security Analyzer \): busca actualizaciones disponibles para el sistema operativo, SQL Server, .NET framework, etc.

Herramientas de seguridad del servidor web

* Syhunt ayuda a automatizar las pruebas y las protecciones de seguridad de las aplicaciones web. N Stalker es un escáner para buscar vulnerabilidades

Prueba de la pluma del servidor web

* Se utiliza para identificar, analizar y reportar vulnerabilidades.
