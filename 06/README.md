# Piratería del sistema

## Piratería del sistema

### Información disponible antes de la etapa de pirateo del sistema

1. Huella: rango de IP, espacio de nombres, empleados
2. Módulo de exploración: evaluación de objetivos, sistemas identificados, servicios identificados
3. Enumeración: sondeo intrusivo, listas de usuarios, fallas de seguridad

### Objetivos de piratería del sistema:

1. Obtener acceso: descifrado de contraseñas, ingeniería social
2. Escalar privilegios \ (obtener otras contraseñas \): aprovechar las vulnerabilidades conocidas del sistema
3. Ejecución de aplicaciones \ (puertas traseras \): troyanos, spywares, puertas traseras, registradores de teclas
4. Ocultar archivos: rootkits, esteganografía
5. Cubriendo pistas - Eliminación de registros

## Cracking de contraseñas

* Las técnicas de descifrado de contraseñas se utilizan para recuperar contraseñas de sistemas informáticos
* Los atacantes utilizan técnicas de descifrado de contraseñas para obtener acceso no autorizado
* La mayoría de los cracks tienen éxito debido a contraseñas adivinables
* Tipos de ataques a contraseñas
  * Ataques no electrónicos: el atacante no necesita conocimientos técnicos para descifrar la contraseña \ (mirar el teclado / pantalla, convencer a la gente, botes de basura, etc.)
  * Ataques activos en línea: el atacante realiza el craqueo comunicándose directamente con la máquina de la víctima \ (diccionario, fuerza bruta, basado en reglas - alguna información conocida \)
  * Ataques pasivos en línea: realiza craqueo sin comunicarse con el grupo
  * Ataque sin conexión: el atacante copia el archivo de contraseña e intenta descifrarlo
* Las contraseñas predeterminadas las establece el fabricante
* Los troyanos pueden recopilar nombres de usuario y contraseñas y enviarlos al atacante, ejecutarse en segundo plano
* Puede usar una unidad USB para un enfoque físico
* Ataque de inyección de hash: el atacante inyecta el hash comprometido en la sesión local y luego lo usa para validar el recurso de red. Encuentra y extrae un hash de cuenta de administrador de dominio registrado
* Ataque pasivo en línea: rastreo de cables
  * Herramientas Packet Sniffer en LAN
  * Los datos de captura pueden incluir información confidencial como contraseñas
  * Las credenciales rastreadas se utilizan para obtener acceso no autorizado
* Ataque de mesa arcoiris
  * Tabla precalculada que contiene listas de palabras como archivos de diccionario, listas de fuerza bruta y sus valores hash
  * Compara los hashes
  * Fácil de recuperar contraseñas comparando hashes de contraseña capturados con tablas precalculadas
* Ataque sin conexión: ataque de red distribuida \ (DNA \)
  * Se utiliza una técnica de ADN para recuperar contraseñas de archivos hash o protegidos con contraseña utilizando el poder de procesamiento no utilizado de las máquinas en la red para descifrar las contraseñas.
* Autenticación de Microsoft
  * Windows almacena las contraseñas en la base de datos del Administrador de cuentas de seguridad \ (SAM \) o en la base de datos de Active Directory en los dominios. Están hash.
  * Autenticación NTLM
    * Tipos de protocolo de autenticación NTLM
    * Protocolo de autenticación LM
    * Estos protocolos almacenan la contraseña del usuario en la base de datos SAM utilizando diferentes métodos de hash
  * Autenticación Kerberos
    * Microsoft ha actualizado su protocolo de autenticación predeterminado
  * Salazón de contraseñas
    * Se agregan cadenas aleatorias de caracteres a la contraseña antes de calcular sus hases
      * Ventaja: la salazón hace que sea más difícil revertir los hashes
* Utilice crackers de contraseñas como L0phtCrack, Cain & Abel, RainbowCrack
* Habilite SYSKEY con una contraseña segura para cifrar y proteger la base de datos SAM

## Privilegios en aumento

* Un atacante puede obtener acceso a la red utilizando una cuenta de usuario que no sea administrador, el siguiente paso es obtener privilegios de administrador
* Escalada de privilegios mediante el secuestro de DLL
  * Si los atacantes colocan una DLL maliciosa en el directorio de la aplicación, se ejecutará en lugar de la DLL real
* Restablecimiento de contraseñas mediante el símbolo del sistema
  * Un administrador puede restablecer contraseñas mientras que un administrador
* Contramedidas: restrinja los privilegios de inicio de sesión interactivo, use la política de privilegios mínimos, implemente múltiples factores, ejecute servicios como cuentas sin privilegios, parchee los sistemas regularmente, use la técnica de encriptación, reduzca la cantidad de código, realice la depuración

## Ejecución de aplicaciones

* Los atacantes ejecutan programas maliciosos de forma remota en la máquina de la víctima para recopilar información
  * Puertas traseras
  * Galletas
  * Registradores de teclas
  * Software espía
* Software como RemoteExec puede instalar software de forma remota, ejecutar programas / scripts
* Hay registradores de pulsaciones de teclas de hardware y software (USB vs App)
* Software espía
  * Registra la interacción del usuario
  * Oculta su proceso
  * Componente oculto del programa gratuito
  * Recopilar información sobre la víctima u organización
* También existe software espía GPS
* Contramedidas para Keyloggers
  * Bloqueador de elementos emergentes
  * anti-spyware / virus
  * Software de firewall
  * Software anti-keylogging
  * Reconocer correos electrónicos de phishing y eliminar
  * Elija nuevas contraseñas para diferentes cuentas en línea
  * Evite abrir correos electrónicos no deseados
* Hay Anti-keyloggers por ahí
* Los rootkits son programas que ocultan su presencia y las actividades maliciosas de un atacante, otorgándoles acceso completo al servidor o host en ese momento o en el futuro.
  * Rootkit típico tiene programas de puerta trasera, programas DDos, rastreadores de paquetes, utilidades de borrado de registros, bots de IRC, etc.
* 6 tipos de rootkits
  * Rootkit de nivel de hipervisor: actúa como hipervisor y modifica la secuencia de arranque de la computadora para cargar el sistema operativo host como una máquina virtual.
  * Rootkit de nivel de cargador de arranque: reemplaza el cargador de arranque original con uno controlado por el atacante
  * Hardware / Firmware Rootkit: se oculta en dispositivos de hardware o firmware de plataforma que no se inspecciona para verificar la integridad del código
  * Rootkit de nivel de aplicación: reemplaza los archivos binarios de la aplicación normal con un troyano falso o modifica el comportamiento de las aplicaciones existentes
  * Rootkit de nivel de kernel: agrega código malicioso o reemplaza el kernel del sistema operativo original y los códigos de controlador de dispositivo
  * Rootkits de nivel de biblioteca: reemplaza las llamadas del sistema originales con falsas para ocultar información sobre el atacante
* Detección de rootkits
  * Detección basada en integridad: compara una instantánea del sistema de archivos, los registros de arranque o la memoria
  * Tecnología basada en firmas: compara las características de todos los procesos del sistema y archivos ejecutables con una base de datos de huellas dactilares de rootkit conocidas
  * Detección basada en heurística / comportamiento: cualquier desviación en la actividad normal del sistema
  * Perfilado de la ruta de ejecución en tiempo de ejecución: compara las rutas de ejecución en tiempo de ejecución de todos los procesos del sistema antes y después de la infección de rootkit
  * Detección basada en vistas cruzadas: enumera elementos clave en el sistema informático, como archivos del sistema, procesos y claves de registro, y los compara con un algoritmo para generar un conjunto de datos similar que no depende de API comunes.
* Flujo de datos NTFS
  * El flujo de datos alternativo NTFS \ (ADS \) es un flujo oculto de Windows que contiene metadatos para el archivo, como atributos, recuento de palabras, nombre del autor, tiempo de acceso y modificación de los archivos
  * Con la transmisión NTFS, un atacante puede ocultar archivos dentro del sistema casi por completo.
  * Puede ocultar un archivo al lado de otro archivo \ (troyano en un readme.txt \)
  * Contramedidas: utilice un verificador de integridad de archivos de terceros
* Esteganografía
  * La esteganografía es una técnica para ocultar un mensaje secreto dentro de un mensaje ordinario y extraerlo en el destino.
  * Utilizar una imagen gráfica como portada es el método más popular para ocultar los datos en archivos.
  * Los atacantes pueden utilizar la esteganografía para ocultar mensajes como la lista de servidores comprometidos, el código fuente de las herramientas de piratería, los planes para futuros ataques, etc.
  * Esteganografía técnica: tinta invisible / micropuntos, métodos físicos para esconderse
  * Esteganografía lingüística: tipo que oculta el mensaje en otro archivo
    * Semagramas: uso de símbolos para ocultar información.
  Inserción de bits menos significativos: el bit más a la derecha de un píxel se llama LSB
  * Enmascaramiento y filtrado: la técnica de creación oculta datos similares a las marcas de agua en papel real. Puede detectarse con un simple análisis estadístico. Principalmente en imágenes en escala de grises.
  * Algoritmos y Transformación
    * Ocultar datos en funciones matemáticas utilizadas en algoritmos de compresión
    * Los datos se incrustan cambiando los coeficientes de una transformación de una imagen
  * Esteganografía de audio: información en frecuencia oculta
* Esteganálisis
  * Arte de descubrir y reproducir mensajes encubiertos mediante esteganografía. Ataca los esfuerzos de esteganografía 

## Cubriendo pistas

* Técnicas utilizadas para cubrir pistas
   * Desactivar auditoría: desactiva las funciones de auditoría del sistema de destino
   * Borrado de registros: el atacante borra / elimina las entradas del registro del sistema para sus actividades
   * Manipulación de registros: manipula registros de manera que no se vean atrapados en acciones legales
* Si el sistema es explotado con metasploit, el atacante usa el shell meterpreter para borrar los registros

## Pruebas de penetración

* Craqueo de contraseña
* Escalada de privilegios
* Ejecutar aplicaciones
* Ocultar archivos
* Cubriendo pistas
