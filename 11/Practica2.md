# Practica 2 

> Antes de iniciar, recuerda hacer prueba de red, debes tener alcance a la Metasplotable y a internet

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
- En la entrega dns-lookups.php, acepta ejecucición de codigo remoto con &&

## 2. Militarizacion (Weaponization)
### - Estrategia
- Ciclo del error (Tabu): el sistemas utiliza versiones obsoletas y vulnerables
- Exceso de seguridad (Totem):  Se confia en que el usuario realizara la busqueda correcta de DNS en dns-lookup.php
	
### - Armamento 
- Robar la sesion con un exploit, de acuerdo a la respuesta que acepte el servidor
> netcat, tiene una version obsoleta, algunos [trucos](https://github.com/heanczko311299/githack/blob/main/Trucos/ReverseShell.md) pueden ayudarte.

## 3. Entrega (Delivery)
- login.php
- dns-lookup.php
- Prepara la recepcion del [ReverseShell](https://github.com/heanczko311299/githack/blob/main/Trucos/ReverseShell.md)
		
## 4. Explotación (Exploitation)
- Envia en entrega dns-lookup.php
- Obten un shell interactivo utilizando [Python](https://github.com/heanczko311299/githack/blob/main/Trucos/Python.md)
- Busca algun dato sobre Jakub en la carpeta
- Consigue el apellido haciendo Dorking, tendras el objetivo
	
## 5. Instalación (Installation)
- No se puede ejecutar nada desde www-data.
- Busca un archivo que te permita robar alguna sesion del servidor.
> Quiza las siglas del equipo donde jugo su final de Champions ayude.
- Obtener la clave cifrada y prueba en [CyberChef](https://gchq.github.io/CyberChef/)
> Base64 / Hex / Base64
- Ingresa al usuario encontrado con:
- Y la contraseña para tener acceso, nos instalaremos aqui, no generamos backdoor
	
## 6. Mando y Control (Command & Control)
- Salir de la sesion.
- Ingresa en la cuenta con las credenciales de SSH, y prueba el acceso a root.
		
## 7. Acciones en el objetivo (Actions on Objectives)
- Si el login.php es vulnerable a SQL Injection, el login de user-info lo será? Qué obtenemos?
- En lista las versiones vulnerables que validaste en la entrega, y prepara los exploits.

## Referencias

### Conocimientos de Ethical Hacking
* **[Robo de Sesiones (Session Hijacking)](https://github.com/heanczko311299/CEH/blob/main/11/README.md)**

### Pruebas de seguridad aplicativa 
* **OWASP10.2017 / A1 - Injection Command** 
* **OWASP10.2017 / A6- Security Misconfiguration**

### Pruebas de Penetración
* **[CyberKillChain](https://github.com/heanczko311299/githack/tree/main/Metodologias/CyberKillChain/README.md)**

h4Ppy #@cK1n6 :)
