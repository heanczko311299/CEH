# Practica 1

> Antes de iniciar, recuerda hacer prueba de red, debes tener alcance a la Metasplotable y a internet.

## Objetivo
### - Principal
¿Quien es el papá de Bobby?
### - Militarizado
Controlar una forma de acceder a la informacion de Bobby

## 1. Reconocimiento (Recoonnaissance)
### - Dork
- Bobby es mi amigo 'el descuidado'
- Bobby es usuario de Instagram, Twitter y Mutillidae 
- Mutillidae es una web con vulnerabilidades
### - Reconocimiento del sistema
- Reconocimiento de red y script de vulnerabilidades RustScan 
- Ingresa a Mutillidae en Metasploitable del Laboratorio http://metasploitable/mutillidae
- Reconoce los directorios con DirSearch

## 2. Militarizacion (Weaponization)
### - Estrategia
- Ciclo del error (Tabu): deja notas en todas partes, encontre la nota 
- Exceso de seguridad (Totem): depende de la seguridad de Mutillidae (login - cookies)

### - Armamento 
- Robar con SQL Injection alguna sesion
- Adivinar las cookies con Mozilla buscando informacion Bobby, mantener herramientas de cifrado si se requieren

## 3. Entrega (Delivery)
- login.php
- index posterior al inicio de sesion

## 4. Explotación (Exploitation)
- Robar SQL Injection en login.php
- Adivinar las cookies y roba la sesion de Bobby para obtener el nombre de su papá
> Pista: Pirata uruguayo de Hamburgo
	
## 5. Instalación (Installation)
- Crear un usuario, donde puedas mantener el acceso.
> Utilizar usuarios que no sean sospechosos ejem. soporte@mutillidae.org
	
## 6. Mando y Control (Command & Control)
- Confirmar el acesso a la cuenta de bobby por medio de las cookies con tu nuevo usuario
- Borra los logs
		
## 7. Acciones en el objetivo (Actions on Objectives)
- Buscar obtener datos de otros usuarios
- Conservar reconocimientos de red y aplicacion para futuros ataques

## Referencias

### Conocimientos de Ethical Hacking
* **[Robo de Sesiones (Session Hijacking)](https://github.com/heanczko311299/CEH/blob/main/11/README.md)**

### Pruebas de seguridad aplicativa 
* **OWASP10.2017 / A1 - Injection** 
* **OWASP10.2017 / A3- Broken Autentication & Session management**

### Pruebas de Penetración
* **[CyberKillChain](https://github.com/heanczko311299/githack/tree/main/Metodologias/CyberKillChain/README.md)**

h4Ppy #@cK1n6 :)
