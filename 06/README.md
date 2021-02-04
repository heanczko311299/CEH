# Hackeo de sistema

## Conceptos

### Información disponible antes de la etapa de pirateo del sistema

1. Footprinting
2. Reconocimiento
3. Enumeración

### Objetivos de piratería del sistema:

1. Obtener acceso: descifrado de contraseñas, ingeniería social
2. Escalar privilegios: aprovechar las vulnerabilidades conocidas del sistema
3. Ejecución de aplicaciones: troyanos, spywares, puertas traseras, registradores de teclas
4. Ocultar archivos: rootkits, esteganografía
5. Cubriendo pistas: eliminación de registros

### Cracking de contraseñas

* Las técnicas de descifrado de contraseñas se utilizan para recuperar contraseñas de sistemas informáticos
* Los atacantes utilizan técnicas de descifrado de contraseñas para obtener acceso no autorizado
* La mayoría de los cracks tienen éxito debido a contraseñas adivinables
* Tipos de ataques a contraseñas
* Las contraseñas predeterminadas las establece el fabricante
* Los troyanos pueden recopilar nombres de usuario y contraseñas y enviarlos al atacante, ejecutarse en segundo plano
* Puede usar una unidad USB para un enfoque físico
* Ataque de inyección de hash: el atacante inyecta el hash comprometido en la sesión local y luego lo usa para validar el recurso de red. Encuentra y extrae un hash de cuenta de administrador de dominio registrado
* Ataque pasivo en línea: rastreo de cables
* Ataque de mesa arcoiris
* Ataque sin conexión: ataque de red distribuida
* Autenticación de Microsoft
* Utilice crackers de contraseñas como L0phtCrack, Cain & Abel, RainbowCrack
* Habilite SYSKEY con una contraseña segura para cifrar y proteger la base de datos SAM

### Escalacion de privilegios

* Un atacante puede obtener acceso a la red utilizando una cuenta de usuario que no sea administrador, el siguiente paso es obtener privilegios de administrador
* Escalada de privilegios mediante el secuestro de DLL
* Restablecimiento de contraseñas mediante el símbolo del sistema
* Contramedidas: restrinja los privilegios de inicio de sesión interactivo, use la política de privilegios mínimos, implemente múltiples factores, ejecute servicios como cuentas sin privilegios, parchee los sistemas regularmente, use la técnica de encriptación, reduzca la cantidad de código, realice la depuración

### Ejecución de aplicaciones

* Los atacantes ejecutan programas maliciosos de forma remota en la máquina de la víctima para recopilar información
* Software como RemoteExec puede instalar software de forma remota, ejecutar programas
* Software espía
* Software espía GPS
* Anti-keyloggers
* Los rootkits son programas que ocultan su presencia y las actividades maliciosas de un atacante, otorgándoles acceso completo al servidor o host en ese momento o en el futuro.
* Detección de rootkits
* Flujo de datos NTFS
* Esteganografía
* Esteganálisis

### Cubriendo pistas

* Desactivar auditoría: desactiva las funciones de auditoría del sistema de destino
* Borrado de registros: el atacante borra / elimina las entradas del registro del sistema para sus actividades
* Manipulación de registros: manipula registros de manera que no se vean atrapados en acciones legales
* Si el sistema es explotado con metasploit, el atacante usa el shell meterpreter para borrar los registros

h4Ppy #@cK1n6 :)
> Discord: heanczko#4478
