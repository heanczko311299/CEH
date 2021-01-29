# Amenazas de malware

## Amenazas de malware

* El malware es un software malicioso que daña o deshabilita los sistemas informáticos y otorga un control limitado o control total de los sistemas al atacante con el propósito de robo o fraude.
* Ejemplos de malware: Trojan Horse, Backdoor, Rootkit, Ransomware, Adware, Virus, Gusanos, Spyware, Botnet, Crypter
* Técnicas comunes que los atacantes utilizan para distribuir malware: Blackhat SEO, Social Engineer Clickjacking, sitios de Spear Phishing, publicidad maliciosa, sitios web legítimos comprometidos, Drive by descargas en vulnerabilidades del navegador

## Conceptos de troyanos

* Un troyano es un programa cuyo código malicioso o dañino está contenido dentro de un programa aparentemente inofensivo o de tal manera que puede obtener el control y causar daños, como arruinar una tabla de asignación de archivos en su disco duro.
* Los troyanos se activan ante determinadas acciones predefinidas del usuario y realizan actividades anormales en el sistema.
* Cuando se instala un troyano, el atacante básicamente puede hacerle cualquier cosa a su computadora
* Cómo infectar sistemas usando un troyano
  * Cree un nuevo paquete de troyano usando un kit de construcción de caballo de Troya
  * Crear un cuentagotas, que forma parte de un paquete troyano que instala el código malicioso en el sistema de destino.
* Un contenedor vincula un ejecutable troyano con una aplicación .EXE de apariencia inocente, como juegos o aplicaciones de oficina. Cuando se ejecuta un EXE, primero instala el troyano en segundo plano.
* Los atacantes utilizan cifradores para ocultar virus, software espía y registradores de pulsaciones de teclas para que los antivirus no los detecten.
* Los atacantes pueden implementar un troyano creando un enlace malicioso / archivos adjuntos de correo electrónico
* Exploit kit: plataforma para entregar exploits y cargas útiles como troyanos, puertas traseras, bots, scripts de desbordamiento de búfer, etc.
* Evadir las técnicas antivirus:
  * Divida el archivo troyano en varias partes y comprímalas como un solo archivo
  * SIEMPRE escriba su propio troyano e introdúzcalo en una aplicación
  * Cambiar la sintaxis de los troyanos
    * Convertir archivo EXE a VB
  * Cambie el contenido del troyano usando Hex Editor y también cambie la suma de comprobación y cifre el archivo
  * Nunca use troyanos descargados de la web \ (el antivirus puede detectarlos fácilmente \)
* Los troyanos de shell de comando dan control remoto de un shell de comando
* El servidor troyano está instalado en la máquina de la víctima, lo que abre un puerto para que el atacante se conecte.
Troyanos de desfiguración: pueden destruir o cambiar todo el contenido presente en una base de datos. Mucho más peligroso cuando los atacantes apuntan a sitios web
* Troyanos botnet: infectan una gran cantidad de computadoras para crear una red de bots \ (chewbacca \)
* Troyanos de servidor proxy: convierte la computadora del usuario en servidores proxy, haciéndolos accesibles a atacantes específicos.
* Troyano VNC: el troyano VNC inicia un demonio de servidor VNC en los sistemas infectados. El atacante puede conectarse con la víctima usando cualquier visor VNC
* Troyanos HTTP / HTTPS: omiten el firewall, generan un programa secundario y el programa secundario parece ser un usuario del firewall
* Túneles ICMP
  * Los canales encubiertos son métodos en los que un atacante puede ocultar los datos en un protocolo que es indetectable
  * Se basan en técnicas llamadas tunelización, que permiten que un protocolo se transfiera a otro protocolo. muy sigiloso
* Troyanos de acceso remoto: brindan a los atacantes un control total sobre el sistema de la víctima
* Troyanos bancarios electrónicos: intercepta la información de la cuenta de una víctima antes de que se cifre
  * Roba los datos de la víctima, como la información de la tarjeta de crédito
* Troyanos de notificación: envía la ubicación de la dirección IP de la víctima al atacante
* Siempre que la computadora de la víctima se conecta a Internet, el atacante recibe la notificación

## Conceptos de virus y gusanos

* Virus: un programa de autorreplicación que produce su propia copia atacándose a otro programa, sector de arranque de la computadora o documento
  * Transmitido a través de descargas, unidades flash infectadas, archivos adjuntos de correo electrónico
* Etapas de la vida del virus
  * Diseño: creando el virus
  * Replicación: replicar el virus en el sistema de destino
  * Lanzamiento: ejecutar / ejecutar el virus \ (archivo .exe \)
  * Detección: el sistema de destino identifica virus
  * Incorporación: actualización de software antivirus
  * Eliminación: los usuarios instalan una actualización antivirus para eliminar el virus.
* Indicaciones de un ataque de virus: actividades anormales \ (lentas, alertas antivirus, falta de carpetas, etc. \)
* Hay muchos antivirus falsos que en realidad son virus
* El ransomware restringe los archivos de la computadora hasta que se paga una suma
* Virus del sector de arranque: mueve MBR a otra ubicación en el disco duro
* Virus de archivos: infecta archivos que se ejecutan o interpretan en el sistema, como \ (archivos COM, EXE, SYL, OVL, OBJ, MNU y BAT
* Virus multipartito: infecta el sector de arranque del sistema y los archivos ejecutables al mismo tiempo \ (híbrido, los 2 principales combinados \) \)
* Macro virus: infecta archivos creados por Microsoft Word o Excel. La mayoría de estos están escritos en lenguaje de macros Visual Basic para Aplicaciones \ (VBA \)
* Infectar plantillas, convertir documentos infectados en archivos de plantilla
* Virus de clúster: modifican el contenido de la tabla de directorios para que apunte a los usuarios a los procesos del sistema al código de virus en lugar del programa real.
  * Solo hay una copia del virus en el disco que infecta todos los programas del sistema informático.
  * Se iniciará primero cuando se inicie cualquier programa en el sistema informático
* Virus Stealth / Tunneling: este virus evade el software antivirus al interceptar sus solicitudes al sistema operativo
  * El virus puede devolver una versión no infectada del archivo al software antivirus, por lo que parece que el archivo está "limpio".
* Virus de cifrado: utiliza un cifrado simple para cifrar el código. El virus se cifra con una clave diferente para cada archivo infectado. AV Scanner no puede detectar directamente estos tipos de virus utilizando métodos de detección de firmas
* Código polimórfico: código que muta manteniendo intacto el algoritmo original. El código polimórfico bien escrito no tiene partes que permanezcan iguales en cada infección
* Virus metamórficos: se reescriben por completo cada uno para infectar nuevos ejecutables
  * Se puede reprogramar a sí mismo traduciendo su propio código en una representación temporal y luego de nuevo al código normal.
* Sobrescritura de archivos o virus de cavidad: sobrescribe una parte del archivo host que es constante \ (generalmente nulos \), sin aumentar la longitud del archivo y conservando su funcionalidad
* Virus infecciosos dispersos: infecta solo ocasionalmente, o solo archivos cuya longitud se encuentra dentro de un rango estrecho. Al infectarse con menos frecuencia, intentan minimizar la probabilidad de ser descubiertos.
* Virus acompañantes / de camuflaje: crea un archivo complementario para cada archivo ejecutable que infecta el virus. Por lo tanto, un virus acompañante puede guardarse como notepad.com y cada vez que el usuario ejecuta notepad.exe \ (buen programa \), la computadora cargará el virus notepad.com e infectará
* Shell Virus: El código de virus forma un shell alrededor del código del programa host de destino, convirtiéndose en el programa original y el código host como su subrutina. Casi todos los programas de arranque son virus de shell
* Virus de extensión de archivos: cambia las extensiones de los archivos. Ex. .TXT es un archivo seguro. El archivo de virus es BAD.TXT.VBS pero solo se mostrará como bad.txt. Cuando se abre, se ejecuta un script.
* Add-on Virus: agrega su código al código de host sin realizar ningún cambio en este último o reubicar el código de host para insertar su propio código al principio
* Virus intrusivos: sobrescriba el código de host parcial o completamente con el código viral
* Virus de acción transitoria / directa: transfiere todos los controles del código de host a donde reside en la memoria. El virus se ejecuta cuando se ejecuta el código del host y se termina por sí mismo o sale de la memoria tan pronto como finaliza la ejecución del código del host
* Terminar and Stay Resident Virus: permanece permanentemente en la memoria durante toda la sesión de trabajo incluso después de que el programa del anfitrión se ejecuta y finaliza. Eliminado solo reiniciando el sistema.
* Gusanos informáticos: programas maliciosos que se replican, ejecutan y se propagan a través de conexiones de red de forma independiente sin interacción humana. La mayoría se crean solo para replicarse y propagarse, pero algunos tienen cargas útiles
  * Los atacantes usan cargas útiles para instalar puertas traseras, lo que los convierte en zombies para una botnet
  * Un gusano es un tipo especial de malware que puede replicarse y usar memoria, pero no puede adjuntarse a otros programas.
  * Un gusano aprovecha las funciones de transporte de archivos o información en una computadora y se propaga a través de la red infectada

## Ingeniería inversa de malware

* Sheep Dipping se refiere al análisis de archivos sospechosos, mensajes entrantes, en busca de malware
  * Una computadora de inmersión de ovejas se instala con monitores de puerto, monitores de archivos, monitores de red y software antivirus y se conecta a una red solo bajo condiciones estrictamente controladas
* Sistemas de sensores antivirus: colección de software informático que detecta y analiza las amenazas de código malicioso
* Procedimiento de análisis de malware:
  * Realizar análisis estáticos cuando el malware está inactivo
  * Recopilar información de los valores de cadena que se encuentran en binario con herramientas
  * Configure la conexión de red y verifique que no haya errores
  * Ejecute el virus y controle las acciones del proceso y la información del sistema con la ayuda del monitor / explorador de procesos
  * Registre la información del tráfico de la red usando herramientas de monitoreo \ (vista TCP, netResident \)
  * Determine los archivos agregados, los procesos que se generan y los cambios en el registro con herramientas
  * Recopilar solicitudes de servicio e información de tablas DNS, intentos de conexiones entrantes y salientes utilizando herramientas
  
## Malware Detection

* Trojans open unused ports in victims machine to connect back to Trojan handlers
* Look for connection established to unknown or suspicious IP addresses
  * You can use a port monitoring tool 
* Scanning for Suspicious Processes
  * Trojans camouflage themselves as genuine Windows services 
  * Some trojans use Portable Executable to inject into various processes 
  * Processes are visible but may look like a legitimate processes and helps bypass desktop firewalls
  * Trojans can also use rootkit methods to hide their processes 
  * Use process monitoring tools to detect hidden trojans and backdoors
* Trojans are installed along with device drivers downloaded from untrusted sources
  * Scan suspicious drivers and verify they are genuine and downloaded from publishers original site
* Trojans normally modify system’s files and folders. Use these tools to detect changes
  * SIGVERIF: checks integrity of critical files digitally signed by microsoft
  * FCIV - Computes MD5 or SHA-1 cryptographic hashes for files
  * TRIPWIRE: system integrity verifier that scan and reports critical system file for changes
* Scanning for suspicious network activities
  * Trojans connect back to handlers and send confidential info to attackers 
  * Use network scanners
* Virus Detection Methods
  * Anti-virus executes the malicious code to simulate. Effective for dealing with encrypted and polymorphic viruses 
  * Heuristic Analysis: Can be static or dynamic. In static, anti-virus analyzes the file format and code structure to determine is code is viral. In dynamic, the AV performs a code emulation 

## Counter-Measures

* Trojan Countermeasures
  * Avoid opening email attachments from unknown senders
  * Block unnecessary ports 
  * Avoid accepting programs transferred by instant messaging
  * Hard weak default configs and unused functionality including protocols/services
  * Monitor internal network traffic for odd ports 
  * Avoid downloading and executing apps from untrusted sources 
  * Install security updates
  * Scan CD’s and DVD’s w/ antivirus software
  * Restrict permissions within desktop environment 
  * Manage local workstation file integrity 
  * Run Host-Based Antivirus
* Backdoor Countermeasures
  * Anti-viruses
  * Educate users not to download from untrusted sites

## Anti-Malware Software

Norton, Mcafee, Nessus etc.
