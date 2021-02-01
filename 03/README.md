# Escaneo de Redes

## Concepto

* El escaneo de red se refiere a un conjunto de procedimientos para identificar hosts, puertos y servicios en una red
* El escaneo en red es uno de los componentes de la recopilación de inteligencia y los usos del atacante para crear un perfil de la organización objetivo

* Tipos de escaneo
1. Exploración de puertos
2. Escaneo de red
3. Análisis de vulnerabilidades
* Banderas de comunicación TCP
1. URG: los datos contenidos en el paquete deben procesarse urgentemente
2. PSH: envía todos los datos almacenados en búfer inmediatamente
3. FIN: finaliza transmisiones
4. ACK: reconoce los recibos de un paquete
5. RST: restablece una conexión
6. SYN: inicia una sincronizacion entre hosts

## Técnicas para sistemas en vivo

1. Escaneo ICMP: Los escaneos de ping implican solicitudes ICMP ECHO a un host. Si el host está activo, devolverá una respuesta ICMP ECHO
2. Útil para localizar dispositivos activos y si ICMP atraviesa el firewall
3. El barrido de ping se utiliza para determinar los hosts en vivo a partir de un rango de direcciones IP
4. Los atacantes calculan las máscaras de subred con las calculadoras de máscaras de subred.
5. Luego, los atacantes usan el barrido de ping para crear un inventario de sistemas activos en la subred.

## Técnicas para puertos

1. El protocolo Simple Service Discovery funciona junto con UPnP para detectar dispositivos plug and play en una red
2. Las vulnerabilidades en UPnP pueden permitir a los atacantes lanzar ataques de desbordamiento de búfer o DoS
3. El escaneo de redes IPv6 es computacionalmente menos factible debido al mayor espacio de búsqueda (128 bits)
4. Los administradores de red pueden usar Nmap para el inventario de la red, administrar los programas de actualización del servicio y monitorear el tiempo de actividad del host o del servicio.
5. El atacante usa Nmap para extraer información como hosts en vivo en la red, servicios, tipo de filtros de paquetes/firewalls, sistemas operativos y versiones de SO
6. Hping3: herramientas de creación de paquetes y escaneo de red de línea de comandos para el protocolo TCP/IP
> Se puede utilizar para auditorías de seguridad de red, pruebas de firewall
7. El escaneo de conexión TCP detecta cuando un puerto está abierto al completar el protocolo de enlace de tres vías
8. Los atacantes envían paquetes de sondeo TCP con un conjunto de indicadores TCP (FIN, URG, PSH) o sin indicadores. No hay respuestas significa que el puerto está abierto, RST significa que el puerto está cerrado
9. En el escaneo de Navidad, los atacantes envían un marco TCP a un dispositivo remoto con indicadores FIN, URG y PUSH configurados.
> No funcionará con ninguna versión actual de Microsoft Windows.
10. Los atacantes pueden sondear un paquete ACK con un número de secuencia aleatorio, si no hay respuestas significa que el puerto está filtrado \ (hay un firewall con estado presente \) y la respuesta RST significa que el puerto no está filtrado
11. Un puerto se considera abierto si una aplicación está escuchando en el puerto.
12. Escaneo UDP cuando el puerto UDP está abierto
13. También hay escáneres de puertos para dispositivos móviles.
14. Medidas contra el escaneo de puertos
- Configure el firewall, las reglas de IDS
- Ejecute herramientas de escaneo de puertos contra hosts para determinar que el firewall detecta correctamente la actividad de escaneo de puertos
- Asegúrese de que el mecanismo utilizado para el enrutamiento y el filtrado en los enrutadores y firewalls, respectivamente, no se pueda omitir.
- Asegúrese de que el firmware del enrutador, IDS y firewall estén actualizados
- Utilice un conjunto de reglas personalizado para bloquear la red y bloquear puertos no deseados
- Filtre todos los mensajes ICMP en los firewalls y enrutadores
- Realice un escaneo TCP y UDP
- Asegúrese de que estén configuradas las reglas anti-escaneo y anti-spoofing.
    
## Técnicas de evasión de IDS

1. Técnicas de evasión: paquetes IP fragmentados, falsificación de direcciones IP, enrutamiento de origen, conexión a servidores proxy
2. Reducir la frecuencia de los paquetes y dividir en partes

## Comprensión de Banner Grabbing

1. Un atacante utiliza técnicas de captura de banners para identificar hosts de red que ejecutan versiones de aplicaciones y sistemas operativos con vulnerabilidades conocidas.
2. La captura de pancartas o la toma de huellas digitales del sistema operativo es el método para determinar el sistema operativo que se ejecuta en un sistema de destino remoto. Hay dos tipos
 > Captura activa y pasiva
3. La identificación de los sistemas operativos permite que un ataque descubra las vulnerabilidades que se ejecutan en un sistema de destino remoto
4. Un atacante usa la captura de pancartas para identificar el sistema operativo utilizado en el host de destino y así determinar las vulnerabilidades del sistema.
5. Herramientas como Netcat leen y escriben datos a través de conexiones de red.
6. Contramedidas
- Mostrar banners falsos
- Apague los servicios innecesarios
- Utilice ServerMask
7. Ocultar extensiones de archivo de páginas web

## Mapeo de red

1. Un diagrama de red ayuda a analizar la topología de red completa.
2. Dibujar el diagrama de red del objetivo muestra la ruta lógica o física a un objetivo potencial. Muestra la red y su arquitectura al atacante.

## Comprensión de los proxies

1. Los servidores proxy sirven como intermediarios para conectarse con otras computadoras
- Oculta la IP de origen
- Encadene varios proxies para evitar la detección
2. Muchos piratas informáticos utilizan proxies para ocultar su identidad para que no puedan ser rastreados. Los registros registran la dirección del proxy en lugar de la del atacante
3. Burpsuite incluye un proxy de interceptación, que le permite inspeccionar y modificar el tráfico entre su navegador y la aplicación de destino
4. Los anonimizadores eliminan toda la información de identificación de la computadora de un usuario mientras el usuario navega por Internet
5. Tails es un sistema operativo en vivo, que el usuario puede iniciar en cualquier computadora desde un DVD, memoria USB o tarjeta SD
6. Puede usar HPING a IPSpoof
7. Medidas contra el Spoofing
- Cifre todo el tráfico de la red
- Utilice varios cortafuegos
- No confíe en la autenticación basada en IP
- Utilice un número de secuencia inicial aleatorio
- Filtrado de entrada: use enrutadores y firewalls en el perímetro de la red para filtrar los paquetes entrantes que parecen provenir de una dirección IP interna
- Filtrado de salida: filtre todos los paquetes salientes con una dirección IP local no válida como dirección de origen


h4Ppy #@cK1n6 :)
> Discord: heanczko#4478
