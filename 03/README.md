# Escaneo de Redes 📽

## Concepto

* El escaneo de red se refiere a un conjunto de procedimientos para identificar hosts, puertos y servicios en una red, es uno de los componentes de la recopilación de informacion del atacante para crear un perfil del objetivo

* Tipos de escaneo
1. Escaneo de puertos
2. Escaneo de servicios
3. Escaneo de vulnerabilidades

* Banderas de comunicación TCP
- URG: los datos contenidos en el paquete deben procesarse urgentemente
- PSH: envía todos los datos almacenados en búfer inmediatamente
- FIN: finaliza transmisiones
- ACK: reconoce los recibos de un paquete
- RST: restablece una conexión
- SYN: inicia una sincronizacion entre hosts

## 3- Way Handshake

-

    
## Banner Grabbing

1. Un atacante utiliza técnicas de captura de banners para identificar hosts de red que ejecutan versiones de aplicaciones y sistemas operativos con vulnerabilidades conocidas
2. La captura de pancartas o la toma de huellas digitales del sistema operativo es el método para determinar el sistema operativo que se ejecuta en un sistema de destino remoto. Hay dos tipos
 > Captura activa y pasiva
3. La identificación de los sistemas operativos permite que un ataque descubra las vulnerabilidades que se ejecutan en un sistema de destino remoto
4. Un atacante usa la captura de pancartas para identificar el sistema operativo utilizado en el host de destino y así determinar las vulnerabilidades del sistema
5. Herramientas como Netcat leen y escriben datos a través de conexiones de red
6. Contramedidas
- Mostrar banners falsos
- Apague los servicios innecesarios
- Utilice ServerMask
7. Ocultar extensiones de archivo de páginas web

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
