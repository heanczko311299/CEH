# Hackear aplicaciones web

> Objetivos: comprender los conceptos de las aplicaciones web, comprender las amenazas de las aplicaciones web, comprender la metodología de piratería de las aplicaciones web, las herramientas de piratería de las aplicaciones web, comprender las contramedidas de las aplicaciones web, las herramientas de seguridad de las aplicaciones web, la descripción general de las pruebas de lápiz de las aplicaciones web

### Conceptos de aplicaciones web

* Las aplicaciones web proporcionan una interfaz entre los usuarios finales y los servidores web a través de un conjunto de páginas.
* La tecnología web, como la Web 2.0, admite funciones comerciales críticas como CRM, SCM

## Amenazas de aplicaciones web

* Envenenamiento por cookies: al cambiar la información de una cookie, los atacantes pueden evitar el proceso de autenticación
* Directory Traversal: da acceso a directorios sin restricciones
* Entrada no validada: atemperar solicitudes http, campo de formulario, campos ocultos, cadenas de consulta, etc. Ejemplos de estos ataques incluyen inyección SQL, XSS, desbordamientos de búfer
* Cross Site Scripting: eludir los mecanismos de identificación del cliente para obtener privilegios, inyectar scripts maliciosos en páginas web
* Defectos de inyección: inyectar código malicioso, comandos, scripts en las puertas de entrada de aplicaciones defectuosas
* Inyección SQL: tipo de ataque en el que los atacantes inyectan comandos SQL a través de datos de entrada y luego manipulan los datos
* Inyección LDAP para obtener acceso directo a las bases de datos detrás del árbol LDAP
* Manipulación de parámetros / formularios: manipula los parámetros intercambiados entre el cliente y el servidor para modificar los datos de la aplicación, como la acreditación y los permisos del usuario.
* DoS: destinado a finalizar operaciones
* Control de acceso roto: método en el que el atacante identifica una falla relacionada con el control de acceso y omite la autenticación, luego compromete la red
* Falsificación de solicitudes entre sitios: ataque en el que un usuario autenticado realiza determinadas tareas en la aplicación web que elige un atacante.
Fugas de información: puede ocasionar grandes pérdidas a la empresa.
* Manejo inadecuado de errores: importante para definir cómo debe comportarse un sistema o red cuando se produce un error. De lo contrario, el error puede brindar la posibilidad de que un atacante ingrese al sistema. Un error inadecuado puede provocar un ataque DoS
* Manipulación de registros: los atacantes pueden inyectar, eliminar o manipular los registros de aplicaciones para ocultar sus identidades
* Desbordamiento del búfer: ocurre cuando la aplicación no protege su propiedad de búfer y permite escribir más allá de su tamaño máximo
* Gestión de sesión rota: cuando las credenciales, como las contraseñas, no están protegidas correctamente
* Errores de configuración de seguridad
* Gestión de cuenta rota: actualización de cuenta, recuperación / restablecimiento de contraseña olvidada / perdida
* Almacenamiento inseguro: los usuarios deben mantener la seguridad adecuada de sus ubicaciones de almacenamiento
* Exploits de plataforma: cada plataforma \ (BEA WEBLOGIC, COLD FUSION \) tiene sus propias vulnerabilidades
* Referencias de objetos directos inseguros: cuando los desarrolladores exponen objetos como archivos, registros, el resultado es una referencia de objetos directos inseguros
* Almacenamiento criptográfico inseguro: los datos confidenciales deben cifrarse correctamente mediante cifrado. Sin embargo, algunas técnicas criptográficas tienen debilidades inherentes
* Secuestro de autenticación: una vez que un atacante compromete un sistema, puede ocurrir la suplantación de identidad del usuario
* Ataques de acceso a la red: pueden permitir niveles de acceso que los métodos de aplicación HTTP estándar no podrían otorgar.
* Detección de cookies
* Ataque de servicios web: los servicios web se basan en protocolos XML como SOAP \ (protocolo simple de acceso a objetos) para la comunicación entre servicios web
* Protección insuficiente de la capa de transporte
* Manipulación oculta
* Ataques de protocolo DMZ
* Redirecciones y reenvíos no validados
* No restringir el acceso a la URL
* Aplicación de ofuscación
* Exploits de gestión de seguridad
* Ataque de fijación de sesión: el atacante engaña al usuario para que acceda a un servidor web genuino utilizando un valor de ID de sesión explícito. El atacante asume la identidad de la víctima y explota las credenciales en el servidor
* Ejecución de archivos maliciosos

## Metodología de piratería

* Los piratas informáticos son los primeros en implantar la infraestructura web
* Descubrimiento del servidor, ubicación
* Descubrimiento de servicios: puertos de escaneo
* Agarre de banner: técnica de huellas para obtener información sensible sobre el objetivo. Pueden analizar la respuesta del servidor a determinadas solicitudes \ (identificación del servidor \)
* Detectar firewalls y proxies de aplicaciones web en el sitio de destino
* Utilice el método de seguimiento para proxy y la respuesta de cookies para un firewall
* Descubrimiento de contenido oculto: Web spidering encuentra automáticamente contenido oculto
* Lanzar un ataque al servidor web para explotar las vulnerabilidades identificadas, lanzar DoS
* Mecanismo de autenticación de ataque
* Enumeración de nombre de usuario
* Mensajes de error detallados. Nombres de usuario predecibles
* Explotación de cookies
* Envenenamiento \ (manipulación \), repetición de olfateo
* Ataque de sesión
* Predicción de sesión, fuerza bruta, envenenamiento
* Ataque de contraseña:
* Adivinar, fuerza bruta
* Ataque de autorización: encuentra cuentas legítimas y luego aumenta lentamente los privilegios
* Mecanismo de gestión de sesiones de ataque: implica el intercambio de información confidencial entre el servidor y los clientes. Si la administración de sesiones es insegura, el atacante puede aprovechar una sesión de administración de sesiones defectuosa
* Evitando los controles de autenticación
* Realizar ataques de inyección: aprovechar el mecanismo de validación de entrada vulnerable implementar
Conectividad de datos de ataque: conexión de base de datos de ataque que forma un enlace entre un servidor de base de datos y su software cliente
* Inyección de cadena de conexión: el atacante inyecta parámetros en una cadena de conexión. Ataques CSPP \ (Ataques de parámetros de cadena de conexión \).
* Connection Pool DoS: el atacante examina la configuración de la agrupación de conexiones y construye una gran consulta SQL, y ejecuta varias consultas simultáneamente para consumir todas las conexiones

## Contramedidas

* Esquemas de codificación: empleando esquemas de codificación de datos para manejar de forma segura caracteres inusuales y datos binarios en la forma que usted desee
* Ej. edición unicode
* Cómo defenderse de los ataques de inyección SQL
* Limitar la longitud de la entrada del usuario
* Realizar validación de entrada
* Cómo defenderse de xss
* Validar todos los encabezados, cookies, cadenas, campos de formulario. Usar firewall
* Cómo configurar contra DoS
* Configure el firewall para denegar el acceso al tráfico ICMP
* Realizar una validación de entrada completa
* Cómo defenderse del ataque a los servicios web
* Protección de múltiples capas

## Herramientas

* N-Stalker es un conjunto eficaz de herramientas de evaluación de seguridad web

## Prueba de penetración

1. Recopilación de información
2. Prueba de gestión de la configuración
3. Prueba de autenticación
4. Prueba de gestión de sesiones
5. Pruebas de autorización
6. Prueba de validación de datos
7. Pruebas DoS
8. Prueba de servicios web
9. Pruebas AJAX
10. Utilice las herramientas de Kali Linux
11. Metasploit
