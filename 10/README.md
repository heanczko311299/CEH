# Negación de servicio

> Objetivos: Descripción general de los ataques DOS y DDoS, comprensión de las técnicas de las técnicas de ataque DoS / DDoS, comprensión de la red de bots, comprensión de varias herramientas de ataque DoS y DDoS, contramedidas DoS / DDoS, descripción general de las pruebas de penetración de ataques DoS

### Conceptos DoS / DDoS

* Denegación de servicio \ (DoS \) es un ataque a una computadora o red que reduce, restringe o impide la accesibilidad de los recursos del sistema a sus usuarios legítimos
* Los atacantes inundan el sistema de la víctima con solicitudes de servicio no legítimas
* El ataque DDoS involucra una multitud de sistemas comprometidos que atacan a un solo sistema objetivo \ (botnet \)

## Técnicas de ataque DoS / DDoS

* Categorías básicas de los ataques
  * Ataques volumétricos: consume el ancho de banda de la red o servicio objetivo
  * Fragmentación: abruma la capacidad del objetivo de reensamblar paquetes fragmentados
  * Ataque de agotamiento de estado de TCP: consume la tabla de estado de conexión presente, como equilibradores de carga, firewalls, servidores de aplicaciones
  * Ataque a la capa de la aplicación: consume recursos o servicios de la aplicación, lo que hace que no esté disponible para otros usuarios legítimos
  * Ataque SYN
    * El atacante envía una gran cantidad de solicitudes SYN al servidor de destino
    * La máquina de destino envía un SYN ACK en respuesta a la solicitud esperando que el ACK complete la sesión
    * El atacante nunca envía un ack
  * Ataque de inundación ICMP: tipo de DoS en el que los perpetradores envían una gran cantidad de paquetes ICMP, lo que hace que el sistema deje de responder a solicitudes legítimas de TCP / IP.
    * Para protegerse: establezca un límite de umbral que invoque una función de protección ICMP
  * Ataque de igual a igual: los atacantes indican a los clientes de los centros de intercambio de archivos p2p que se desconecten de su red p2p y se conecten al sitio web falso de las víctimas. Los atacantes pueden lanzar ataques DoS masivos y comprometer sitios web
  * Ataque de denegación de servicio permanente: también conocido como phlashing, se refiere a los ataques que causan daños irreversibles al hardware del sistema
    * A diferencia de otros ataques DoS, sabotea el hardware del sistema
  * Ataque de inundación a nivel de aplicación: los ataques de inundación a nivel de aplicación dan como resultado la pérdida de servicios
    * Con este ataque, los atacantes aprovechan las debilidades en la programación del código fuente para evitar que la aplicación procese solicitudes legítimas.
  * Denegación de servicio de reflexión distribuida \ (DRDoS \)
    * También conocido como ataque falsificado, implica el uso de múltiples máquinas intermedias y secundarias que contribuyen al ataque DDoS real contra la máquina o aplicación objetivo.

## Botnets

* Los bots son aplicaciones de software que ejecutan tareas automatizadas a través de Internet.
* Una botnet es una enorme red de sistemas comprometidos y puede ser utilizada por un atacante para lanzar un ataque DoS
* Métodos de escaneo para encontrar máquinas vulnerables: escaneo aleatorio, escaneo de listas de aciertos, escaneo topológico, escaneo de subred local, escaneo de permutación
* Herramientas de ataque DoS y DDoS
* LOIC, GoldenEye

## Contramedidas

* Técnicas
  * Perfiles de actividad
    * Incrementos en los niveles de actividad, grupos distintos, tasa promedio de paquetes, etc.
  * Detección de punto de cambio
    * Filtra el tráfico de red por direcciones IP, números de puerto específicos, almacena datos de flujo de tráfico en un gráfico que muestra la tasa de flujo de tráfico en función del tiempo
  * Análisis de señales basado en ondas
    * Analiza el tráfico de la red en términos de componentes espectrales. Divide la señal entrante en varias frecuencias para su análisis
* Estrategias de contramedidas DoS / DDoS
  * Absorber el ataque \ (requiere recursos adicionales \)
  * Servicios degradantes \ (identificar los servicios críticos y detener los no críticos \)
  * Cerrar los servicios
  * Desviar ataques: los Honeypots actúan como una tentación para un atacante. Sirve como un medio para obtener información sobre los atacantes, almacena sus actividades
  * Filtrado de entrada: protege de los ataques de inundación. Permite rastrear al originador hasta su verdadera fuente
  * Filtrado de salida: escaneo de encabezados de paquetes de direcciones IP que salen de una red. Garantiza que el tráfico no autorizado o malicioso nunca salga de la red interna
  * Mitigar ataque: equilibrio de carga, estrangulamiento
* Análisis forense posterior al ataque
  * Analizar patrones de tráfico para nuevas técnicas de filtrado, analizar enrutadores, cortafuegos y registros de IDS, pueden actualizar contramedidas de balanceo de carga y limitación
