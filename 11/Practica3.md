# Practica 3 

> Antes de iniciar, recuerda probar la conexion, configura tu localhost en este caso configuramos la IP como 'mr.robot.cft'

## Objetivo
### - Key 1
### - Key 2
### - Key 3

## 1. Reconocimiento (Recoonnaissance)
### - Reconocimiento del sistema
- Reconocimiento de red
- Reconoce app web http://mr.robot.ctf:?????
- Busca vulnerabilidaes en algun directorio
- Necesitas recolectar la pista oficial y la siguiente:
> Pista: Practica 1 + CMS
- Buscar algo que explotar en el CMS
> Varios metodos de entregar el exploit, erro404 y carga de plugins
- Obtienes el key 1 en alguna parte de este reconocimiento

## 2. Militarizacion (Weaponization)
### - Estrategia
- Ciclo del error (Tabu): tiene problemas de configuración, deja informacion expuesta
- Exceso de seguridad (Totem):  Confia en un sistema de gestion de contenidos (WP)
	
### - Armamento 
- Robar la sesion del usuario de WP con un ataque de fuerza bruta, prueba con WPScan o Hydra
- Robar la sesion del servidor con un [ReverseShell](https://github.com/heanczko311299/githack/blob/main/Trucos/ReverseShell.md), 

## 3. Entrega (Delivery)
- wp-login
- error404 - pluggins
- Prepara la recepcion del [ReverseShell](https://github.com/heanczko311299/githack/blob/main/Trucos/ReverseShell.md)
		
## 4. Explotación (Exploitation)
- Activa el pluggin o produce un error para obtener la shell en tu maquina atacante
- Obten un shell interactivo utilizando python
	$ python -c 'import pty; pty.spawn("/bin/bash")'
- Busca el key 2
- Desifra el hash con [John](https://github.com/openwall/john), para obtener el Key 2
	
## 5. Instalación (Installation)
- Crea una cuenta en WP con máximos privilegios, que te permita tener acceso diferente al usuario hackeado
- Busca instalarte en el root para obtener el key 3
- Busca archivos con SUID configurado que permitan que ejecutes en root
> Quiza aqui encuentres una pista
- Escala privilegios para instalarte en root y obtener el key 3
- Crea una cuenta para acceder a la informacion del root sin realizar la explotacion
	
## 6. Mando y Control (Command & Control)
- Ingresa a la cuenta creada y a la robada, comprueba que tienes acceso ambas cuentas
- Ingresa en la cuenta con las credenciales de SSH, y prueba el acceso a root.
		
## 7. Acciones en el objetivo (Actions on Objectives)
- Modifica el mensaje de error con en mensaje personal de tu equipo.
> Se creativo
- En lista 3 tecnicas con las podrias hacer daño

## Referencias

### Conocimientos de Ethical Hacking
* **[Robo de Sesiones (Session Hijacking)](https://github.com/heanczko311299/CEH/blob/main/11/README.md)**

### Pruebas de seguridad aplicativa 
* **OWASP10.2017 / A1 - Injection Command** 
* **OWASP10.2017 / A6- Security Misconfiguration**

### Pruebas de Penetración
* **[CyberKillChain](https://github.com/heanczko311299/githack/tree/main/Metodologias/CyberKillChain/README.md)**

h4Ppy #@cK1n6 :)
