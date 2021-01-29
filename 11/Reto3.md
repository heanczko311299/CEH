### Reto 3

## Objetivo

	Quiero la db de usuarios en Mutillidae!!!
	Quiero acceso con pivoting al servidor!!!

## Referencias

## CEH v10

- Session Hijacking

## OWASP10.2017

- A2* Cross-Site Scripting (XSS)
- A5* Cross-Site Request Forgery (CSRF)
- A6* Security Misconfiguration
- A9* Insufficient Transport Layer Protection

** Antes de iniciar, recuerda hacer prueba de red y verificar los accesos a Mutillidae e Internet.

### CyberKillChain

## Reconocimento: 
- Reutiliza recursos

## Militarizacion:
- Ciclo del error: 
  - Son recurrentes los errores de usuarios ¿Que podriamos explotar?
				 
- Exceso de seguridad (Totem): 
  - Mucha confianza en los administradores de la red ¿Que podriamos explotar?

## Entrega:
- Entregar XSS en JSON en pen-test-tool-lookup.php
- Entregar sniffing a la red.
- Entregar fuerza bruta en login.php
- Entrega CSRF en register.php
- Entrega injection (Command) en dns-lookup.php
		
## Explotacion:
- Obten la base de datos de usuarios de la aplicacion y guardala.
- Obten un shell interactivo.
	
## Instalación:
- Escala privilegios hasta el root.
- Instala backdoor en FTP.
	
## Comando & Control:
- Salir de la sesion.
- Comprobar acceso al backdoor.
- Realizar pivoting.
		
## Acciones en el objetivo:
- Prueba las vulnerabilidades de red en la metasploitable, los exploits los encuentras en este repositorio.
