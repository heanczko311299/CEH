# Reto 1 CEH Interno

> Antes de iniciar, recuerda hacer prueba de red, debes tener alcance a la Metasplotable y a internet.

## Objetivo
¿Quien es el papá de Bobby?

## Referencias
### CEH: Conocimientos de Ethical Hacking

	Session Hijacking

### OWASP10.2017

	A1- Injection
	A3- Broken Autentication & Session management

### Pentest-CyberKillChain

## Reconocimento: 

- Bobby es usuario de Twitter, Reddit, Github y Mutillidae. 
- Mutillidae es una web con vulnerabilidades, veamos los directorios con dirsearch.
- Ingresa a Mutillidae en Metasploitable del Laboratorio http://metasploitable/mutillidae
- 

## Militarizacion:
- Ciclo del error (Tabu): deja notas en todas partes.
- Exceso de seguridad (Totem): Depende de la seguridad de Mutillidae (login - cookies vulnerables)

## Entrega:
- Roba una sesion con un SQL Injection en login.php
- Adivina las cookies de la sesion de Bobby, en el index.
	* @google pirata hamburgo, rodrigo

## Explotacion:
- Actualiza el front y accede a la sesion de Bobby para obtener el nombre de su papá.
	
## Instalación:
- Crea un usuario, donde puedas mantener el acceso.
	** Utiliza usuarios que no sean sospechosos ejem. soporte@mutillidae.org
- Borra los logs.
	
## Comando & Control:
- Confirma el acesso a la cuenta de bobby por medio de las cookies con tu nuevo usuario.
		
## Acciones en el objetivo:
- El conocer el apodo del Admin de mutillidae 'Monkey!', son acciones en el objetivo.
