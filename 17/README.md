# Hackear plataformas móviles

> Objetivos: comprender los vectores de ataque de la plataforma móvil, comprender varias amenazas y ataques de Android, comprender varias amenazas y ataques de iOS, comprender varias amenazas y ataques del sistema operativo Windows Phone, comprender varias amenazas de blackberry como ataques, comprender la administración de dispositivos móviles \ (MDM \), dispositivos móviles Directrices de seguridad y herramientas de seguridad, descripción general de las pruebas de lápiz móvil

## Vectores de ataque de plataforma móvil

* Los 10 principales riesgos de OWASP Mobile
  * Almacenamiento de datos inseguro
  * Suposición de que el malware no ingresará al sistema. El jailbreak evita el cifrado
  * Fuga de datos involuntaria
  * Cuando un usuario coloca datos confidenciales en una ubicación accesible para otras aplicaciones
  * Criptografía rota
  * Algoritmos de cifrado débiles. Los usuarios deben utilizar algoritmos ARS o 3DES
  * Decisión de seguridad a través de entradas no confiables
  * Las aplicaciones utilizan mecanismos de protección que dependen de los valores de entrada \ (cookies, variables ambientales, campos de formulario ocultos \), pero un atacante puede alterar estos valores de entrada para evitar el mecanismo de protección
* Falta de protecciones binarias: la falta de protecciones binarias en una aplicación móvil la expone a ella y al propietario a una amplia variedad de riesgos técnicos y comerciales si no es segura. Debe utilizar contramedidas como
  * Técnicas de codificación segura
  * Controles de detección de jailbreak
  * Controles de suma de comprobación
  * Controles de fijación de certificados
* Anatomía de un ataque móvil
  * El dispositivo - & gt; la red & gt; el centro de datos
  * Hacer clic en Jacking: engañar a los usuarios para que hagan clic en algo diferente de lo que creen que están haciendo. Los atacantes obtienen información confidencial o toman el control del dispositivo
  * Framing: una página web integrada en otra página web que utiliza elementos iFrame en HTML
  * Drive By Downloading: descarga no intencionada de software de Internet. Android se ve afectado por este ataque
  * Man in the Middle: el atacante implanta un código malicioso en el dispositivo móvil de la víctima
  * Desbordamientos de búfer: escritura de datos en suites de búfer,
  * Almacenamiento en caché de datos: almacenamiento en caché en dispositivos móviles utilizados para interactuar con aplicaciones web, los atacantes intentan explotar los cachés de datos
  * Ataques basados ​​en teléfono / SMS
  * Ataques de banda base: aprovechamiento de vulnerabilidades en el procesador de banda base GSM / 3GPP del teléfono, que envía / recibe señales a las torres
  * SMiShing: tipo de phishing en el que el atacante utiliza un mensaje de texto SMS para vincularlo a un sitio malicioso
  * Ataques de RF \ (radiofrecuencia \): explote las vulnerabilidades encontradas en diferentes canales de comunicación periféricos que normalmente se utilizan en las comunicaciones de dispositivo a dispositivo cercanas
  * Ataques basados ​​en aplicaciones
  * Almacenamiento de datos confidenciales: algunas aplicaciones emplean una seguridad débil en la arquitectura de su base de datos, lo que las convierte en objetivos para que el atacante piratee y robe información confidencial del usuario almacenada en ellas
  * Sin cifrado / cifrado débil: las aplicaciones que transmiten datos sin cifrar o cifrados débilmente son susceptibles a ataques como el secuestro de sesiones
  * Validación de SSL inadecuada: lagunas de seguridad en las aplicaciones El proceso de validación de SSL puede permitir a los atacantes eludir la seguridad de los datos
  * Manipulación de configuración: las aplicaciones pueden usar archivos y bibliotecas externos, modificando esas entidades o afectando la capacidad de las aplicaciones de usar esos resultados en un ataque de manipulación de configuración
  * Inyección dinámica de tiempo de ejecución: los atacantes manipulan y abusan del tiempo de ejecución de una aplicación para eludir bloqueos de seguridad, verificaciones lógicas, privilegios de acceso a partes de una aplicación y robar datos.
  * Permisos no deseados: las aplicaciones mal configuradas pueden, en ocasiones, abrir puertas a los atacantes al proporcionar permisos no deseados
  * Privilegios escalados: los atacantes se involucran en ataques de escalada de privilegios, que aprovechan fallas de diseño, errores de programación, errores o descuidos de configuración para obtener acceso a los recursos.
  * Ataques basados ​​en SO
  * iOS Jailbreak: eliminación de los mecanismos de seguridad establecidos por Apple para evitar códigos maliciosos
  * Enraizamiento de Android: permite a los usuarios obtener control privilegiado \ (acceso de root \) dentro del subsistema de Android.
  * Contraseñas y datos accesibles
  * Software cargado por el operador: el software o las aplicaciones preinstaladas en los dispositivos pueden contener vulnerabilidades que un atacante puede aprovechar para realizar actividades maliciosas, como eliminar, modificar o robar datos en el dispositivo, escuchar llamadas
  * Explotaciones de día cero: inicie un ataque aprovechando una vulnerabilidad previamente desconocida en un sistema operativo o aplicación móvil.
  * El punto de ataque basado en la red
  * WiFi \ (cifrado débil o sin cifrado \)
  * Puntos de acceso no autorizados: los atacantes instalan un punto de acceso inalámbrico ilícito por medios físicos, lo que les permite acceder a una red protegida al secuestrar las conexiones de los usuarios de la red.
  * Man in the Middle \ (MITM \): los atacantes vigilan las conexiones de red existentes entre dos sistemas
  * SSLStrip: tipo de ataque MITM que aprovecha las vulnerabilidades en la implementación de SSL / TLS
  * Secuestro de sesión: el atacante roba los ID de sesión válidos
  * Envenenamiento por DNS: los atacantes explotan los servidores DNS y redirigen a los usuarios del sitio web a otro sitio web que elija el atacante.
  * Certificados SSL falsos: los certificados SSL falsos representan otro tipo de ataques MITM. El atacante emite un certificado SSL falso para interceptar el tráfico en una conexión HTTPS supuestamente segura
  * El centro de datos
  * Dos puntos de entrada principales: servidor web y una base de datos
  * Ataques basados ​​en servidor web
  * Vulnerabilidades de la plataforma: explotación de vulnerabilidades en el sistema operativo, el software del servidor o los módulos de la aplicación que se ejecutan en el servidor web
  * Mala configuración del servidor
  * XSS
  * CSRF
  * Validación de entrada débil
  * Ataques de fuerza bruta
  * Ataques a bases de datos
  * Inyección SQL
  * Volcado de datos
  * Ejecución de comandos del sistema operativo
  * Escalada de privilegios
  * Sandboxing: ayuda a proteger sistemas y usuarios al limitar los recursos a los que la aplicación puede acceder en la plataforma móvil; sin embargo, las aplicaciones maliciosas pueden aprovechar las vulnerabilidades

## Hackear el sistema operativo Android

* La API de administración de dispositivos proporciona funciones de administración de dispositivos a nivel del sistema
  * El enraizamiento permite a los usuarios de Android obtener un control privilegiado \ (acceso de root \)
  * Implica explotar vulnerabilidades de seguridad en el firmware del dispositivo
  * Protección de dispositivos Android:
  * Habilitar bloqueos de pantalla
  * No rootee su dispositivo
  * Descargar aplicaciones solo desde Android Market
  * Mantenga el dispositivo actualizado con el software de Google
  * No descargue directamente archivos APK
  * Actualiza el sistema operativo con regularidad
  * Utilice la aplicación protectora gratuita
  * Política de dispositivos de Google Apps: permite al administrador del dominio establecer políticas de seguridad para su dispositivo Android

## Hackear iOS

* Capas del SO
  * Cocoa Touch: marco clave que ayuda a crear la aplicación iOS. Define apariencia, servicios básicos como el tacto
  * Medios: contiene tecnología de gráficos, audio y video con experiencia en aplicaciones
  * Core Services: contiene servicios fundamentales del sistema para aplicaciones
  * Sistema operativo principal: función de bajo nivel en la que se basan la mayoría de las otras tecnologías
  * Tethered \ (el kernel será parcheado al reiniciar \) y sin ataduras

## Hackear Windows Phone

## Hackear Blackberry

* Firma de código malicioso: las aplicaciones de Blackberry deben estar firmadas por RIM. El atacante puede obtener claves de firma de código para una aplicación maliciosa y publicarla en la tienda
  * Explotaciones de archivos JAD: un archivo jad permite al usuario revisar los detalles de la aplicación y decidir si descargarla. Sin embargo, los atacantes crearon archivos .jad falsificados para engañar al usuario
  * Ataques de datos PIM: PIM \ (administrador de información personal \) incluye direcciones, libros, calendarios, tareas
  * Las aplicaciones maliciosas pueden eliminar o modificar estos datos.
  * Vulnerabilidades de las conexiones TCP / IP: si el firewall del dispositivo está apagado, las aplicaciones firmadas pueden abrir conexiones TCP sin que se le solicite al usuario.
  * Las aplicaciones maliciosas crean una conexión inversa con el atacante, lo que le permite usar el dispositivo infectado como un proxy TCP y obtener acceso a los recursos internos de la organización.

## Gestión de dispositivos móviles \ (MDM \)

* MDM proporciona plataformas para la distribución inalámbrica o por cable de aplicaciones, datos y ajustes de configuración para todo tipo de dispositivos móviles, teléfonos inteligentes, tabletas, etc.
  * Ayuda a implementar políticas en toda la empresa para reducir los costos de soporte
  * Puede administrar dispositivos BYOD y de propiedad de la empresa

## Pautas y herramientas de seguridad móvil

* Reglas generales
* No cargue demasiadas aplicaciones y evite la carga automática de fotos a las redes sociales
* Realizar una evaluación de seguridad de la Arquitectura de la Aplicación.
* Mantener el control y la gestión de la configuración
  * Instalar aplicaciones de tiendas de aplicaciones de confianza
  * Limpie o elimine de forma segura los datos que se deshacen del dispositivo
  * Asegúrese de que el bluetooth esté desactivado de forma predeterminada
  * No comparta la ubicación dentro de las aplicaciones habilitadas para GPS
  * Nunca conecte dos redes separadas como Wi-Fi y Bluetooth simultáneamente
