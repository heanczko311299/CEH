# Robo de sesión

> Objetivos: Comprender los conceptos de secuestro de sesiones, Comprender el secuestro de sesiones a nivel de aplicación, Comprender el secuestro de sesiones a nivel de red, Herramientas de secuestro de sesiones, Contramedidas de secuestro de sesiones, Descripción general de las pruebas de penetración de secuestro de sesiones

## Conceptos de Robo de sesiones

- ¿Qué es el secuestro de sesiones?
  * Acceder a la informacion o manipular una sesion de un usuario en alguna aplicacion o red
- ¿Por qué el secuestro de sesiones tiene éxito?
  * Sin bloqueo de cuenta por ID de sesión no válidos
  * Algoritmo de generación de ID de sesión débil
  * Manejo inseguro de ID de sesión
  * Tiempo de caducidad de sesión indefinido
  * La mayoría de las computadoras que usan TCP / IP son vulnerables
  * La mayoría de las contramedidas no funcionan a menos que use cifrado
- Proceso de secuestro de sesión
  * Ataque de referencia: el atacante intenta atraer a un usuario para que haga clic en un enlace a un sitio malicioso.
  * Obtener solicitud
  * Durante el proceso de secuestro de sesión, el atacante debe programarlo para saltar a la sesión
  * Fuerza bruta: el atacante intenta diferentes ID hasta que lo logra
  * Sniff & gt; Monitor & gt; Session Desynchronization & gt; Session ID prediction & gt; Command Injection
- Tipos de secuestro de sesiones
  * Ataque activo: el atacante encuentra una sesión activa y se hace cargo
  * Ataque pasivo: el ataque secuestra una sesión, pero se sienta y observa y registra todo el tráfico que se envía
  * Modelo OSI a nivel de red:
  * Secuestro de nivel de aplicación:
- Spoofing vs Hijacking

## Robo de sesión a nivel de aplicación

- Un token de sesión puede verse comprometido de varias formas
- Sesión olfateando
- Token de sesión predecible
- Ataque de hombre en el medio
- Ataque de hombre en el navegador
- Ataque de secuencia de comandos entre sitios
- Código Javascript malicioso
- Ataque de falsificación de solicitud entre sitios
- Ataque de repetición de sesión
- Fijación de sesiones
- Falsificación de solicitud CSRF Cross site:

h4Ppy #@cK1n6 :)
> Discord: heanczko#4478
