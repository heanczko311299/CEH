# Amenazas de malware

## Amenazas de malware

- El malware es un software malicioso que daña o deshabilita los sistemas informáticos y otorga un control limitado o control total de los sistemas al atacante con el propósito de robo o fraude.
- Ejemplos de malware: Trojan Horse, Backdoor, Rootkit, Ransomware, Adware, Virus, Gusanos, Spyware, Botnet, Crypter
- Técnicas comunes que los atacantes utilizan para distribuir malware: Blackhat SEO, Social Engineer Clickjacking, sitios de Spear Phishing, publicidad maliciosa, sitios web legítimos comprometidos, Drive by descargas en vulnerabilidades del navegador

## Toyanos
- Un troyano es un programa cuyo código malicioso o dañino está contenido dentro de un programa aparentemente inofensivo o de tal manera que puede obtener el control y causar daños, como arruinar una tabla de asignación de archivos en su disco duro.
- Los troyanos se activan ante determinadas acciones predefinidas del usuario y realizan actividades anormales en el sistema.
- Cuando se instala un troyano, el atacante básicamente puede hacerle cualquier cosa a su computadora
- Cómo infectar sistemas usando un troyano
- Los troyanos de shell de comando dan control remoto de un shell de comando
- El servidor troyano está instalado en la máquina de la víctima, lo que abre un puerto para que el atacante se conecte.
Troyanos de desfiguración: pueden destruir o cambiar todo el contenido presente en una base de datos. Mucho más peligroso cuando los atacantes apuntan a sitios web
- Troyanos botnet: infectan una gran cantidad de computadoras para crear una red de bots
- Troyanos de servidor proxy: convierte la computadora del usuario en servidores proxy, haciéndolos accesibles a atacantes específicos.
- Troyano VNC: el troyano VNC inicia un demonio de servidor VNC en los sistemas infectados. El atacante puede conectarse con la víctima usando cualquier visor VNC
- Troyanos HTTP / HTTPS: omiten el firewall, generan un programa secundario y el programa secundario parece ser un usuario del firewall
- Túneles ICMP
- Troyanos de acceso remoto: brindan a los atacantes un control total sobre el sistema de la víctima
- Troyanos bancarios electrónicos: intercepta la información de la cuenta de una víctima antes de que se cifre

## Conceptos de virus y gusanos

- Virus: un programa de autorreplicación que produce su propia copia atacándose a otro programa, sector de arranque de la computadora o documento
  * Transmitido a través de descargas, unidades flash infectadas, archivos adjuntos de correo electrónico
- Etapas de la vida del virus
  * Diseño: creando el virus
  * Replicación: replicar el virus en el sistema de destino
  * Lanzamiento: ejecutar 
  * Detección: el sistema de destino identifica virus
  * Incorporación: actualización de software antivirus
  * Eliminación: los usuarios instalan una actualización antivirus para eliminar el virus.
- El ransomware restringe los archivos de la computadora hasta que se paga una suma
- Virus del sector de arranque: mueve MBR a otra ubicación en el disco duro
- Virus de archivos: infecta archivos que se ejecutan o interpretan en el sistema,
- Virus multipartito: infecta el sector de arranque del sistema y los archivos ejecutables al mismo tiempo
- Macro virus: infecta archivos creados por Microsoft Word o Excel. La mayoría de estos están escritos en lenguaje de macros Visual Basic para Aplicaciones
- Infectar plantillas, convertir documentos infectados en archivos de plantilla
- Virus de clúster: modifican el contenido de la tabla de directorios para que apunte a los usuarios a los procesos del sistema al código de virus en lugar del programa real.
  * Solo hay una copia del virus en el disco que infecta todos los programas del sistema informático.
  * Se iniciará primero cuando se inicie cualquier programa en el sistema informático
- Virus Stealth/Tunneling: este virus evade el software antivirus al interceptar sus solicitudes al sistema operativo
  * El virus puede devolver una versión no infectada del archivo al software antivirus, por lo que parece que el archivo está "limpio".
- Virus de cifrado: utiliza un cifrado simple para cifrar el código. El virus se cifra con una clave diferente para cada archivo infectado. AV Scanner no puede detectar directamente estos tipos de virus utilizando métodos de detección de firmas
- Código polimórfico: código que muta manteniendo intacto el algoritmo original. El código polimórfico bien escrito no tiene partes que permanezcan iguales en cada infección
- Virus metamórficos: se reescriben por completo cada uno para infectar nuevos ejecutables
  * Se puede reprogramar a sí mismo traduciendo su propio código en una representación temporal y luego de nuevo al código normal.
- Sobrescritura de archivos o virus de cavidad: sobrescribe una parte del archivo host que es constante, sin aumentar la longitud del archivo y conservando su funcionalidad
- Virus infecciosos dispersos: infecta solo ocasionalmente, o solo archivos cuya longitud se encuentra dentro de un rango estrecho. Al infectarse con menos frecuencia, intentan minimizar la probabilidad de ser descubiertos.
- Virus acompañantes/camuflaje: crea un archivo complementario para cada archivo ejecutable que infecta el virus. Por lo tanto, un virus acompañante puede guardarse como notepad.com y cada vez que el usuario ejecuta notepad.exe, la computadora cargará el virus notepad.com e infectará
- Shell Virus: El código de virus forma un shell alrededor del código del programa host de destino, convirtiéndose en el programa original y el código host como su subrutina. Casi todos los programas de arranque son virus de shell
- Virus de extensión de archivos: cambia las extensiones de los archivos. Ex. .TXT es un archivo seguro. El archivo de virus es BAD.TXT.VBS pero solo se mostrará como bad.txt. Cuando se abre, se ejecuta un script.
- Add-on Virus: agrega su código al código de host sin realizar ningún cambio en este último o reubicar el código de host para insertar su propio código al principio
- Virus intrusivos: sobrescriba el código de host parcial o completamente con el código viral
- Virus de acción transitoria/directa: transfiere todos los controles del código de host a donde reside en la memoria. El virus se ejecuta cuando se ejecuta el código del host y se termina por sí mismo o sale de la memoria tan pronto como finaliza la ejecución del código del host
- Terminar and Stay Resident Virus: permanece permanentemente en la memoria durante toda la sesión de trabajo incluso después de que el programa del anfitrión se ejecuta y finaliza. Eliminado solo reiniciando el sistema.
- Gusanos informáticos: programas maliciosos que se replican, ejecutan y se propagan a través de conexiones de red de forma independiente sin interacción humana. La mayoría se crean solo para replicarse y propagarse, pero algunos tienen cargas útiles
  * Los atacantes usan cargas útiles para instalar puertas traseras, lo que los convierte en zombies para una botnet
  * Un gusano es un tipo especial de malware que puede replicarse y usar memoria, pero no puede adjuntarse a otros programas.
  * Un gusano aprovecha las funciones de transporte de archivos o información en una computadora y se propaga a través de la red infectada

h4Ppy #@cK1n6 :)
> Discord: heanczko#4478

