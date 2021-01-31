# Reto 1 CEH Interno

> Antes de iniciar, recuerda hacer prueba de red, debes tener alcance a la Metasplotable y a internet.

## Objetivo
### Principal
¿Quien es el papá de Bobby?
### Militarizado
Controlar una forma de acceder a la informacion de Bobby

## Reconocimento
### Dork
- Bobby es mi amigo 'el descuidado'
- Bobby es usuario de Instagram, Twitter y Mutillidae 
- Mutillidae es una web con vulnerabilidades
- Reconocimiento de red y script de vulnerabilidades RustScan 
- Ingresa a Mutillidae en Metasploitable del Laboratorio http://metasploitable/mutillidae
- Reconoce los directorios con DirSearch

## Militarizacion:
### Estrategia
- Ciclo del error (Tabu): deja notas en todas partes, encontre la nota 
- Exceso de seguridad (Totem): depende de la seguridad de Mutillidae (login - cookies)

### Armamento
- SQL Injection para ingresar a alguna sesion
- Vulnerar las cookies con Mozilla buscando informacion Bobby

## Entrega:
- login.php
- index posterior al inicio de sesion

## Explotacion:
- Roba SQL Injection en login.php
- Adivina las cookies y roba la sesion de Bobby para obtener el nombre de su papá.
	
## Instalación:
- Crea un usuario, donde puedas mantener el acceso.
> Utiliza usuarios que no sean sospechosos ejem. soporte@mutillidae.org
- Borra los logs.
	
## Comando & Control:
- Confirma el acesso a la cuenta de bobby por medio de las cookies con tu nuevo usuario.
		
## Acciones en el objetivo:
- El conocer el apodo del Admin de mutillidae 'Monkey!', son acciones en el objetivo.

## Referencias

### Conocimientos 
##### Ethical Hacking Session Hijacking

### Pruebas de seguridad aplicativa OWASP10.2017 
##### A1- Injection 
##### A3- Broken Autentication & Session management

### Pruebas de Intrusión CyberKillChain
