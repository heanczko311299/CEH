# Redes de exploración

## Descripción general del escaneo en red

* El escaneo de red se refiere a un conjunto de procedimientos para identificar hosts, puertos y servicios en una red.
* El escaneo en red es uno de los componentes de la recopilación de inteligencia y los usos del atacante para crear un perfil de la organización objetivo.
* Tipos de escaneo
  1. Exploración de puertos \ (enumere los puertos y servicios abiertos \)
  2. Escaneo de red \ (enumera las direcciones IP \)
  3. Análisis de vulnerabilidades \ (muestra la presencia de debilidades conocidas \)
* Banderas de comunicación TCP \ (controla la transmisión de datos \)
* URG \ (urgente \): los datos contenidos en el paquete deben procesarse inmediatamente
* PSH \ (push \): envía todos los datos almacenados en búfer inmediatamente
* FIN \ (Finish \): No habrá más transmisiones
* ACK \ (Reconocimiento \): reconoce los recibos de un paquete
* RST \ (Reset \): restablece una conexión
* SYN \ (Synchronization \): inicia una conexión entre hosts

## Técnicas para sistemas en vivo

1. Escaneo ICMP: Los escaneos de ping implican solicitudes ICMP ECHO a un host. Si el host está activo, devolverá una respuesta ICMP ECHO
2. Útil para localizar dispositivos activos y si ICMP atraviesa el firewall
3. El barrido de ping se utiliza para determinar los hosts en vivo a partir de un rango de direcciones IP
4. Los atacantes calculan las máscaras de subred con las calculadoras de máscaras de subred.
5. Luego, los atacantes usan el barrido de ping para crear un inventario de sistemas activos en la subred.

## Técnicas para puertos

1. El protocolo Simple Service Discovery \ (SSDP \) funciona junto con UPnP para detectar dispositivos plug and play en una red
2. Las vulnerabilidades en UPnP pueden permitir a los atacantes lanzar ataques de desbordamiento de búfer o DoS
3. El escaneo de redes IPv6 es computacionalmente menos factible debido al mayor espacio de búsqueda \ (128 bits \)
4. Los administradores de red pueden usar Nmap para el inventario de la red, administrar los programas de actualización del servicio y monitorear el tiempo de actividad del host o del servicio.
5. El atacante usa Nmap para extraer información como hosts en vivo en la red, servicios, tipo de filtros de paquetes / firewalls, sistemas operativos y versiones de SO
6. Hping2 / Hping3: herramientas de creación de paquetes y escaneo de red de línea de comandos para el protocolo TCP / IP
   1. Se puede utilizar para auditorías de seguridad de red, pruebas de firewall
7. El escaneo de conexión TCP detecta cuando un puerto está abierto al completar el protocolo de enlace de tres vías
   1. El escaneo de conexión TCP establece una conexión completa y la elimina enviando un paquete RST
   2. No requiere privilegios de superusuario.
8. Los atacantes envían paquetes de sondeo TCP con un conjunto de indicadores TCP \ (FIN, URG, PSH \) o sin indicadores. No hay respuestas significa que el puerto está abierto, RST significa que el puerto está cerrado
9. En el escaneo de Navidad, los atacantes envían un marco TCP a un dispositivo remoto con indicadores FIN, URG y PUSH configurados.
   1. No funcionará con ninguna versión actual de Microsoft Windows.
10. Los atacantes pueden sondear un paquete ACK con un número de secuencia aleatorio, si no hay respuestas significa que el puerto está filtrado \ (hay un firewall con estado presente \) y la respuesta RST significa que el puerto no está filtrado
11. Un puerto se considera abierto si una aplicación está escuchando en el puerto.
    1. La mayoría de los servidores web están en el puerto 80 y los servidores de correo en el 25.
    2. Una forma de determinar si un puerto está abierto es enviar un paquete "SYN" \ (establecimiento de sesión \) al puerto
       1. La máquina de destino enviará de vuelta un paquete SYN \ | ACK si el puerto está abierto, y un paquete RST \ (reset \) si el puerto está cerrado
    3. Escaneo IDLE
       1. Ataca una computadora zombi. Una máquina zombi es aquella que asigna paquetes IPID de forma incremental.
       2. Puede recuperar el número de IPID para la suplantación de direcciones IP
12. Escaneo UDP: Cuando el puerto UDP está abierto --- No hay protocolo de enlace TCP de tres vías para el escaneo UDP. El sistema no responde con un yo. El sistema no responde con un mensaje cuando el puerto está abierto. Cuando el puerto UDP está cerrado, el sistema responde con un mensaje de puerto ICMP inaccesible. Spywares, Trojan Horses y otras aplicaciones utilizan puertos UDP
13. También hay escáneres de puertos para dispositivos móviles.
14. Medidas contra el escaneo de puertos
    1. Configure el firewall, las reglas de IDS para detectar / bloquear sondas
    2. Ejecute herramientas de escaneo de puertos contra hosts para determinar que el firewall detecta correctamente la actividad de escaneo de puertos
    3. Asegúrese de que el mecanismo utilizado para el enrutamiento y el filtrado en los enrutadores y firewalls, respectivamente, no se pueda omitir.
    4. Asegúrese de que el firmware del enrutador, IDS y firewall estén actualizados
    5. Utilice un conjunto de reglas personalizado para bloquear la red y bloquear puertos no deseados
    6. Filtre todos los mensajes ICMP en los firewalls y enrutadores
    7. Realice un escaneo TCP y UDP
    8. Asegúrese de que estén configuradas las reglas anti-escaneo y anti-spoofing.
    
## Varias técnicas de evasión de IDS

1. Técnicas de evasión: paquetes IP fragmentados, falsificación de direcciones IP, enrutamiento de origen, conexión a servidores proxy
2. Reducir la frecuencia de los paquetes, dividir en partes

## Comprensión del agarre de banners

1. Un atacante utiliza técnicas de captura de banners para identificar hosts de red que ejecutan versiones de aplicaciones y sistemas operativos con vulnerabilidades conocidas.
2. La captura de pancartas o la toma de huellas digitales del sistema operativo es el método para determinar el sistema operativo que se ejecuta en un sistema de destino remoto. Hay dos tipos
   1. Captura activa de pancartas: los paquetes diseñados específicamente se envían al sistema operativo remoto y se anotan las respuestas, luego se comparan con una base de datos para determinar el sistema operativo.
   2. Captura pasiva de pancartas: olfatear el tráfico de la red. Captura de banner de mensaje de error y captura de banner de extensiones de página \ (sigiloso \)
3. La identificación de los sistemas operativos permite que un ataque descubra las vulnerabilidades que se ejecutan en un sistema de destino remoto
4. Un atacante usa la captura de pancartas para identificar el sistema operativo utilizado en el host de destino y así determinar las vulnerabilidades del sistema.
5. Herramientas como Netcat leen y escriben datos a través de conexiones de red.
6. Contramedidas para agarrar pancartas
   1. Mostrar pancartas falsas
   2. Apague los servicios innecesarios
   3. Utilice ServerMask
7. Ocultar extensiones de archivo de páginas web

## Escaneo de vulnerabilidades

1. El análisis de vulnerabilidades identifica vulnerabilidades y debilidades de un sistema.
2. Nessus es el producto de evaluación de vulnerabilidades y configuración

## Mapeo de red

1. Un diagrama de red ayuda a analizar la topología de red completa.
2. Dibujar el diagrama de red del objetivo muestra la ruta lógica o física a un objetivo potencial. Muestra la red y su arquitectura al atacante.

## Comprensión de los proxies

1. Los servidores proxy sirven como intermediarios para conectarse con otras computadoras
   1. Oculta la IP de origen
   2. Encadene varios proxies para evitar la detección
2. Muchos piratas informáticos utilizan proxies para ocultar su identidad para que no puedan ser rastreados. Los registros registran la dirección del proxy en lugar de la del atacante.
3. La suite Burp incluye un proxy de interceptación, que le permite inspeccionar y modificar el tráfico entre su navegador y la aplicación de destino. Popular.
4. Los anonimizadores eliminan toda la información de identificación de la computadora de un usuario mientras el usuario navega por Internet
5. Tails es un sistema operativo en vivo, que el usuario puede iniciar en cualquier computadora desde un DVD, memoria USB o tarjeta SD
6. Puede usar HPING2 a IPSpoof
7. Medidas contra la suplantación de propiedad intelectual
   1. Cifre todo el tráfico de la red
   2. Utilice varios cortafuegos
   3. No confíe en la autenticación basada en IP
   4. Utilice un número de secuencia inicial aleatorio
   5. Filtrado de entrada: use enrutadores y firewalls en el perímetro de la red para filtrar los paquetes entrantes que parecen provenir de una dirección IP interna
   6. Filtrado de salida: filtre todos los paquetes salientes con una dirección IP local no válida como dirección de origen

## Prueba de penetración: escaneo

1. La prueba de lápiz de una red determina la postura de seguridad de la red identificando sistemas activos, descubriendo puertos abiertos, asociando servicios y capturando pancartas del sistema para simular un intento de pirateo de la red.
2. A continuación se explica cómo realizar una prueba de penetración de una red de destino
   1. Descubrimiento de host: detecta hosts en vivo en la red de destino. Es difícil detectar hosts en vivo detrás de un firewall \ (Nmap, Angry IP scanner, colasoft \)
   2. Escaneo de puertos: busque puertos abiertos \ (Nmap, Netscan \)
   3. Captura de banner o huella digital del SO: determina el SO que se ejecuta en el host de destino
   4. Escanee la red en busca de vulnerabilidades \ (nessus \)
   5. Dibuje diagramas de red que le ayuden a comprender la conexión lógica
   6. Prepare Proxies: se esconde de la detección
   7. Documente todos los hallazgos.
