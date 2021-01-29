# Secuestro de sesión

> Objetivos: Comprender los conceptos de secuestro de sesiones, Comprender el secuestro de sesiones a nivel de aplicación, Comprender el secuestro de sesiones a nivel de red, Herramientas de secuestro de sesiones, Contramedidas de secuestro de sesiones, Descripción general de las pruebas de penetración de secuestro de sesiones

## Conceptos de secuestro de sesiones

* ¿Qué es el secuestro de sesiones?
  * Dado que la mayor parte de la autenticación se produce al comienzo de una sesión TCP, esto permite al atacante acceder a la máquina. Puede tomar la galleta y jugarla como si fuera suya.
  * Sin embargo, la cookie caducará después de algún tiempo. Es mucho más fácil robar cookies que forzar una contraseña / token
* ¿Por qué el secuestro de sesiones tiene éxito?
  * Sin bloqueo de cuenta por ID de sesión no válidos
  * Algoritmo de generación de ID de sesión débil
  * Manejo inseguro de ID de sesión
  * Tiempo de caducidad de sesión indefinido
  * La mayoría de las computadoras que usan TCP / IP son vulnerables
  * La mayoría de las contramedidas no funcionan a menos que use cifrado
* Proceso de secuestro de sesión
  * Ataque de referencia: el atacante intenta atraer a un usuario para que haga clic en un enlace a un sitio malicioso.
  * Obtener solicitud \ [extraer la página web \]
  * Durante el proceso de secuestro de sesión \ (syn-ack \), el atacante debe programarlo para saltar a la sesión
  * Fuerza bruta: el atacante intenta diferentes ID hasta que lo logra
  * Sniff & gt; Monitor & gt; Session Desynchronization & gt; Session ID prediction & gt; Command Injection
* Tipos de secuestro de sesiones
  * Ataque activo: el atacante encuentra una sesión activa y se hace cargo
  * Ataque pasivo: el ataque secuestra una sesión, pero se sienta y observa y registra todo el tráfico que se envía
  * Secuestro de sesión en el modelo OSI: escalada de nivel de red, secuestro de nivel de aplicación
  * Modelo OSI a nivel de red: el secuestro a nivel de red se puede definir como la interceptación del paquete durante la transmisión entre el cliente y el servidor
  * Secuestro de nivel de aplicación: el secuestro de nivel de aplicación consiste en obtener el control sobre la sesión de usuario de HTTP mediante la obtención de los ID de sesión
* Spoofing vs Hijacking
  * Ataque de suplantación de identidad: pretende ser otro usuario
    * Attack pretende ser otro usuario
  * Secuestro: proceso de hacerse cargo de una sesión activa existente

## Secuestro de sesión a nivel de aplicación

* Un token de sesión puede verse comprometido de varias formas
* Sesión olfateando
  * Olfatear para capturar un token o ID de sesión válido
* Token de sesión predecible
  * Predecir una ID de sesión generada por un algoritmo débil
  * Adivina un valor de sesión único o deduce el ID de sesión
* Ataque de hombre en el medio
  * Intrusión de una conexión existente e interceptación
  * Los atacantes utilizan diferentes técnicas y dividen la conexión TCP
* Ataque de hombre en el navegador
  * Utiliza un caballo de Troya para interceptar llamadas entre el navegador y sus mecanismos de seguridad.
  * Puede ser una extensión maliciosa
* Ataque de secuencia de comandos entre sitios
  * XSS permite a los atacantes inyectar scripts maliciosos del lado del cliente en páginas web
* Código Javascript malicioso
  * El caballo de Troya puede cambiar la configuración del proxy en el navegador del usuario
* Ataque de falsificación de solicitud entre sitios \ (CSRF \)
  * Un ataque CSRF aprovecha la sesión activa de la víctima con un sitio confiable para realizar actividades maliciosas
* Ataque de repetición de sesión
  * En la respuesta de sesión, el atacante escucha la conversación entre el usuario y el servidor y captura el token de autenticación del usuario.
  * Una vez que se captura el token de autenticación, el atacante reproduce la solicitud al servidor con el token de autenticación
* Fijación de sesiones
  * La fijación de sesión es un ataque que permite a un atacante secuestrar una sesión de usuario válida
  * El ataque intenta atraer a un usuario para que se autentique con una ID de sesión conocida y luego secuestra la sesión validada por el usuario
  * El atacante debe proporcionar una ID de sesión de aplicación web legítima e intentar atraer al navegador de la víctima para que la use
* Falsificación de solicitud CSRF Cross site:
  * El usuario visita el sitio bancario. El atacante hace que el usuario visite su sitio de alguna manera. Su sitio infecta y agrega a su sesión e inserta más comandos en su sesión y hace cosas que ella no autorizó.
