# Hackear redes inalámbricas

> Objetivos: Comprender los conceptos inalámbricos, comprender los algoritmos de cifrado inalámbrico, comprender las amenazas inalámbricas, comprender la metodología de piratería inalámbrica, las herramientas de piratería inalámbricas, comprender las técnicas de piratería de bluetooth, comprender las contramedidas de piratería inalámbrica, descripción general de las pruebas de penetración inalámbrica

### Conceptos inalámbricos

* GSM: sistema universal utilizado para transporte móvil para redes inalámbricas en todo el mundo
* Ancho de banda: describe la cantidad de información que se puede transmitir a través de una conexión
* BSSID: la dirección MAC de un punto de acceso que ha configurado un conjunto de servicios básicos
* Banda ISM: un conjunto de frecuencias para las comunidades industriales, científicas y médicas internacionales
* Punto de acceso: se utiliza para conectar dispositivos inalámbricos a una red inalámbrica
* Hotspot: lugares donde la red inalámbrica está disponible para uso público
* Asociación: proceso de conectar un dispositivo inalámbrico a un punto de acceso
* Multiplexación por división de frecuencia ortogonal: método de codificación de datos digitales en múltiples frecuencias portadoras
* Espectro de propagación de secuencia directa: la señal de datos original se multiplica con un código de propagación de ruido pseudoaleatorio
* Espectro ensanchado por salto de frecuencia \ (FHSS \): método de transmisión de señales de radio cambiando rápidamente una portadora entre muchos canales de frecuencia
* Redes inalámbricas
* WiFi se refiere al estándar IEEE 802.11
* * SSID \ (identificador de conjunto de servicios \)
* Proceso de autenticación de sistema abierto: en un sistema abierto, cualquier cliente inalámbrico que desee acceder a una red WiFi envía una solicitud al AP inalámbrico para su autenticación.
* Proceso de autenticación de clave compartida: en este proceso, cada estación inalámbrica recibe una clave secreta compartida a través de un canal seguro que es distinto de los canales de comunicación 802.11.
* Servidor de autenticación centralizado \ (RADIUS \)
  * Tiza WiFi
  * WarChalking: dibuja símbolos en lugares públicos para anunciar redes Wi-Fi abiertas
  * Tipos de antenas inalámbricas
  * Antenas direccionales: se utilizan para transmitir y obtener ondas de radio desde una sola dirección
  * Antenas omnidireccionales: proporciona transmisiones horizontales de 360 ​​grados, utilizadas en estaciones base inalámbricas
  * Antena de rejilla parabólica: basada en la idea de una antena parabólica. Puede captar señales de Wi-Fi a diez millas o más
  * Antena Yagi: antena unidireccional
  * Antena dipolo: Antena bidireccional, utilizada para admitir la conexión del cliente en lugar de aplicaciones de sitio a sitio
  * Las antenas de rejilla parabólica permiten a los atacantes atacar desde más lejos \ (¡10 millas! \)

## Encriptación inalámbrica

* WEP \ (privacidad equivalente por cable \): cifrado más débil. Utiliza un vector de inicialización de 24 bits. Un WEP de 64 bits utiliza una clave de 40 bits, etc.
* Puede usar Cain & Abel para romper
* WPA \ (Wifi Protected Access \): cifrado más sólido con TKIP.
* Puede forzar las teclas sin conexión
* Puedes defenderte usando contraseñas más fuertes
* WPA2: protección de datos más sólida con AES
* WPA-2 personal utiliza una clave previamente compartida para proteger el acceso
* WPA-2 Enterprise incluye EAP o RADIUS para autenticación centralizada con kerberos, etc.

## Amenazas inalámbricas

Ataques de control de acceso: tiene como objetivo penetrar en una red evadiendo las medidas de control de acceso WLAN, como los filtros AP MAC y los controles de acceso al puerto Wi-Fi.
* Ataques de integridad: envío de marcos de datos o gestión de control falsificados a través de una red inalámbrica
* Ataques de confidencialidad: intento de interceptar información confidencial enviada a través de asociaciones inalámbricas
* Ataques de disponibilidad: DoS
* Ataques de autenticación: robar la identidad de los clientes Wi-Fi, su PI, inicios de sesión, etc. para el acceso no autorizado a los recursos de la red
* Ataque de punto de acceso deshonesto: secuestrar conexiones y actuar como un intermediario olfateando
* Asociación errónea de clientes: el atacante configura un punto de acceso no autorizado fuera del perímetro corporativo y atrae a los empleados de la organización para que se conecten con él.
* Ataque de punto de acceso mal configurado: accidentes para configuraciones que puede explotar
* Ataque de conexión AD Hoc: los clientes Wifi se comunican directamente en forma ad-hoc y no requieren AP para retransmitir paquetes. El ataque puede atacar el sistema operativo directamente ya que el cifrado es débil
* Ataque de punto de acceso de Honeyspot: el atacante se aprovecha de múltiples WLAN en el área y usa el mismo SID
* AP MAC Spoofing: el pirata informático falsifica la dirección MAC del equipo cliente WLAN para enmascarar a un cliente autorizado
* Ataque de señal de interferencia: amplificador de alta ganancia

## Metodología de piratería inalámbrica

1. WiFi Discovery: descubre la red WiFi
2. Mapeo GPS: los atacantes crean un mapa de la red Wi-Fi descubierta y crean una base de datos
3. Análisis de tráfico inalámbrico: identificación de vulnerabilidades, reconocimiento de WiFi, herramientas para captura y análisis de paquetes
4. Lanzar ataques inalámbricos
   1. Ataque de fragmentación: puede obtener 1500 bytes de datos PRGA que pueden usarse para ataques de inyección
   2. Mac Spoofing: los atacantes cambian la dirección MAC a la de un usuario autenticado para evitar el filtrado MAC configurado en un punto de acceso.
   3. Denegación de servicio: ataques de desautenticación y disociación
   4. Man in the middle attack MITM: el atacante falsifica su MAC, envía una solicitud deAuth y luego se pone en el medio
   5. Ataque de envenenamiento por ARP inalámbrico:
   6. Punto de acceso no autorizado: el atacante de APs inalámbricos se instala en una red sin autorización y no están bajo la administración del administrador de la red. No están configurados con ninguna seguridad.
   7. Evil Twin: replica el nombre de otro AP inalámbrico a través de SSID común
5. Descifrar el cifrado de Wi-Fi
   1. Crack WEP usando Aircrack
   2. Crack WPA-PSK usando aircrack
   3. Agrietamiento WEP usando Cain & Abel
6. Comprometer la red Wi-Fi
   * ¿Qué es el análisis de espectro?
   * Los analizadores de espectro de RF examinan las transmisiones de radio Wi-Fi y miden la potencia \ (amplitud \)
   * Emplear análisis estadístico para trazar el uso espectral
   * Puede usarse para ataques DoS

## Hackeo de Bluetooth

* Explotación de vulnerabilidades de implementación de Bluetooth Stack
Bluesmacking: ataque DoS que desborda los dispositivos habilitados para Bluetooth con paquetes aleatorios que provocan que el dispositivo se bloquee
* Bluejacking: envío de mensajes no solicitados por bluetooth a dispositivos habilitados para bluetooth, como teléfonos móviles, computadoras portátiles, etc.
* Bluesnarfing: robo de información de un dispositivo inalámbrico a través de una conexión bluetooth
  * Blue Sniff: código de prueba de concepto para una utilidad de protección bluetooth
  * Bluebugging: acceder de forma remota a los dispositivos habilitados para bluetooth y usar sus funciones
  * BluePrinting: recopilación de información sobre dispositivos habilitados para bluetooth, como fabricante, modelo de dispositivo, firmware
  * Ataque de suplantación de MAC: interceptación de datos destinados a otros dispositivos habilitados para bluetooth
  * MITM: Modificación de datos entre la comunicación de dispositivos habilitados para bluetooth en una piconet
  * Modos de Bluetooth:
  * Detectable, Detectable limitado \ (cronometrado \), No detectable
  * Modos de emparejamiento
  * Modelos no emparejables: rechaza todas las solicitudes de emparejamiento
  * Modo de emparejamiento: se emparejará a pedido

## Contramedidas

* Cómo defenderse de la piratería de bluetooth
  * Use patrones no regulares como claves PIN
  * Mantenga el dispositivo en modo no detectable
  * Mantenga un control de todos los dispositivos emparejados
  * Siempre habilite las encriptaciones

## Herramientas de seguridad inalámbrica

* Sistemas inalámbricos de prevención de intrusiones
