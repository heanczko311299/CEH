# Olfatear

## Olfatear

> Objetivos: Descripción general de los conceptos de rastreo, comprensión de los ataques de MAC, comprensión de los ataques de DHCP, comprensión del envenenamiento de ARP, comprensión de los ataques de suplantación de MAC, comprensión del envenenamiento de DNS, herramientas de rastreo, contramedidas de rastreo, comprensión de varias técnicas para detectar el rastreo, descripción general de las pruebas de lápiz de rastreo

### Conceptos de olfateo

* Sniffing es un proceso de monitoreo y captura de todos los paquetes de datos que pasan a través de una red dada usando herramientas de sniffing \ (forma de toque de cable \)
  * Muchos puertos de conmutadores de empresas están abiertos
  * Cualquiera en la misma ubicación física puede conectarse a la red con ethernet
* Cómo funciona un rastreador
  * Sniffer enciende la NIC de un sistema al modo promiscuo que escucha todos los datos transmitidos en su segmento
* Cada computadora tiene una dirección MAC y una dirección IP
* Detección pasiva significa a través de un concentrador \ (no implica enviar paquetes \), en un concentrador el tráfico se envía a todos los puertos
  * La mayoría de las redes modernas utilizan conmutadores
* Detección activa: busca tráfico en una LAN conmutada inyectando tráfico activamente en la LAN. Implica inyectar paquetes de resolución de direcciones \ (ARP \) en la red
* Protocolos vulnerables al olfateo:
  * HTTP, Telnet y Rlogin, POP, IMAP, SMTP y NNTP
* Los rastreadores operan en la capa de enlace de datos del modelo OSI
* Hardware Protocol Analyzer: equipo que captura señales sin alterar el tráfico en un segmento de cable
  * Puede usarse para monitorear el tráfico. Permite al atacante ver bytes de datos individuales
  * Puerto de extensión: un puerto que está configurado para recibir una copia de cada paquete que pasa a través de un conmutador
  * Escuchas telefónicas: proceso de monitoreo de llamadas telefónicas e Internet por parte de terceros
  * Mediante la conexión de un dispositivo de escucha \ (hardware o software \) al circuito
  * Escuchas telefónicas activas: monitorea, registra e inyecta algo en la comunicación o el tráfico
  * Escuchas telefónicas pasivas: solo monitorea y registra el tráfico y obtiene conocimiento de los datos que contiene
  * Interceptación legal: interceptar legalmente la comunicación de datos

## Ataques MAC

* Cada conmutador tiene una memoria direccionable de contenido dinámico de tamaño fijo \ (tabla CAM \)
* La tabla CAM almacena información como la dirección MAC disponible en los puertos físicos
* Si la tabla CAM se inunda con más direcciones MAC que puede contener, entonces el conmutador se convierte en un HUB
* Los atacantes explotan esto
* Switch Port Stealing: usa mac flooding para oler los paquetes
* Cómo defenderse de los ataques MAC: use una seguridad de puerto para restringir el tráfico entrante de solo un conjunto seleccionado de direcciones MAC y limitar los ataques de inundación MAC

## Ataques DHCP

* Los servidores DHCP mantienen la información de configuración de TCP / IP \ (proporciona arrendamientos \)
* Ataque de inanición de DHCP: el atacante transmite solicitudes DHCP falsificadas e intenta arrendar todas las direcciones DHCP disponibles en el alcance de DHCP
* Como resultado, el usuario legítimo no puede obtener o renovar una dirección IP.
* DHCP deshonesto: servidor DHCP deshonesto en la red y responde a las solicitudes de DHCP con direcciones IP falsas
* Cómo defenderse contra la inanición de DHCP y el ataque de servidor no autorizado: habilite la seguridad del puerto para la inanición de DHCP y habilite la indagación de DHCP que permite que el conmutador acepte transacciones de DHCP desde un puerto de confianza

## Envenenamiento por ARP

* El Protocolo de resolución de direcciones \ (ARP \) es un protocolo sin estado que se utiliza para resolver direcciones IP en direcciones de máquina \ (MAC \)
* Todos los dispositivos de red difunden consultas ARP en la red para encontrar la dirección MAC de la máquina
* Cuando una máquina necesita comunicarse con otra, busca en la tabla ARP. Si no está allí, ARP \ _REQUEST se transmite a través de la red.
* Los paquetes ARP se pueden falsificar
* La suplantación de ARP implica la construcción de una gran cantidad de solicitudes ARP falsificadas
* El interruptor se establece en "modo de reenvío" después de que la tabla ARP se inunda con respuestas ARP falsificadas
* Los atacantes inundan la caché ARP de una computadora objetivo con entradas falsificadas, lo que también se conoce como envenenamiento
* La suplantación de identidad ARP es un método para atacar una LAN Ethernet
* Usando mensajes ARP falsos, un atacante puede desviar todas las comunicaciones entre dos máquinas para que todo el tráfico se intercambie a través de su PC
* Herramientas ARP: Cain & Abel, WinArpAttacker
* Cómo defenderse: implementar inspección ARP dinámica, indagación DHCP, detección de suplantación de identidad XArp

## Spoofing

* El atacante puede rastrear la red en busca de direcciones MAC y luego falsificarlas para recibir todo el tráfico destinado al usuario. Permite al atacante acceder a la red.
* Suplantación de identidad de IRDP: el protocolo de descubrimiento de enrutadores ICMP permite al host descubrir la dirección IP de los enrutadores activos.
* El atacante envía un mensaje de anuncio de enrutador IRDP falsificado al host en la subred, lo que hace que cambie su enrutador predeterminado
* Cómo defenderse: indagación DHCP, inspección ARP dinámica, protección de fuente IP

## Envenenamiento por DNS

* El envenenamiento de DNS es una técnica que engaña a un servidor DNS haciéndole creer que ha recibido autenticación cuando en realidad no lo ha hecho.
* Resultados en sustitución de una dirección IP falsa
* El atacante puede crear entradas DNS falsas
* Suplantación de DNS de intranet: debe estar conectado a la LAN y ser capaz de rastrear. Funciona bien contra conmutadores con ARP que envenenan el enrutador.
* El atacante de suplantación de DNS de la intranet infecta la máquina con un troyano y cambia la IP del DNS a la del atacante
* Envenenamiento por DNS del servidor proxy: el atacante envía un troyano a la máquina que cambia la configuración del servidor proxy del host en Internet Explorer a la del atacante y la redirecciona a un sitio web falso.
* Envenenamiento de caché de DNS: se refiere a alterar o agregar registros de DNS falsificados en la caché de resolución de DNS para que una consulta de DNS se redirija a un sitio malicioso
* Cómo defenderse: resuelva todas las consultas de DNS al servidor DNS local, bloquee las solicitudes de DNS para que no vayan a servidores externos, configure el firewall para restringir la búsqueda de DNS externa, implemente IDS e implemente correctamente, implemente DNSSEC

## Herramientas de olfateo

* Wireshark

## Contramedidas

* Restringir el acceso físico
* Usar cifrado
* Agregar dirección MAC permanente a la puerta de enlace a la caché ARP
* Utilice direcciones IP estáticas
* Desactivar las transmisiones de identificación de red
* Utilice IPV6
* Utilice HTTPS en lugar de HTTP
* Utilice un interruptor que Hub
* Utilice SFTP en lugar de FTP

## Técnicas de detección de olfateo

* Ejecuta IDS y nota si la dirección mac de ciertas máquinas ha cambiado
* Verifique qué máquinas están funcionando en modo promiscuo
* El modo promiscuo permite que un dispositivo de red intercepte y lea cada paquete de red
* Solo una máquina en modo promiscuo almacena en caché la información ARP
* Una máquina en modo promiscuo responde al mensaje de ping ya que tiene información correcta sobre el host que envía una solicitud de ping

## Prueba de la pluma de olfateo

* La prueba de rastreo de lápiz se utiliza para verificar si la transmisión de datos desde una organización es segura contra ataques de rastreo e interceptación.
