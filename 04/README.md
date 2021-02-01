# Enumeración

## Concepto

* En la fase de enumeración, el atacante crea conexiones activas al sistema y realiza consultas dirigidas para obtener más información. Utiliza esta información para identificar puntos de ataque al sistema y realizar ataques a contraseñas

* Técnicas de enumeración
- Extrae nombres de usuario usando ID de correo electrónico
- Extrae nombres de usuario usando SNMP
- Extraer grupos de usuarios de Windows
- Extrae información usando las contraseñas predeterminadas
- Direcciones activas de fuerza bruta
- Extrae información usando DNS Zone Transfer

* Puertos populares para enumerar
- TCP / UDP 53 - Transferencia de zona DNS
- TCP / UDP 135 - Microsoft EPC Endpoint Manager
- UDP 137 - Servicio de nombres NetBIOS \ (NBNS \)
- TCP 139 - SMB sobre NetBIOS
- TCP / UDP 445 - SMB sobre TCP \ (host directo \)
- UDP 161 - Protocolo simple de administración de red \ (SNMP \)
- TCP / UDP 389 - Protocolo ligero de acceso a directorios \ (LDAP \)
- TCP / UDP 3268 - Servicio de catálogo global
- TCP 25 - Protocolo simple de transferencia de correo \ (SMTP \)
- TCP / UDP 162 - Trampa SNMP

## Enumeración NetBIOS

* El nombre NetBIOS es una cadena ASCII única de 16 que se utiliza para identificar los dispositivos de red
* La utilidad Nbtstat muestra las estadísticas del protocolo NetBIOS sobre TCP / IP, las tablas de nombres NetBIOS / caché
* La utilidad Net View se utiliza para obtener una lista de todos los recursos compartidos de hosts remotos o grupos de trabajo.

## Enumeración SNMP

* La enumeración SNMP es un proceso de enumeración de cuentas de usuario y dispositivos en un sistema de destino mediante SNMP
* SNMP contiene un administrador y un agente. Los agentes están integrados en cada red, el administrador está instalado en una computadora separada
* SNMP tiene dos contraseñas
- El atacante usa cadenas de comunidad predeterminadas para extraer información
- Lo usa para extraer información sobre recursos de red como hosts, enrutadores, dispositivos, recursos compartidos
* Base de información de gestión \ (MIB \)
- MIB es una base de datos virtual que contiene una descripción formal de todos los objetos de red administrados mediante SNMP

## Enumeración LDAP

- LDAP es un protocolo de Internet para acceder a servicios de directorio distribuidos
- El atacante consulta el servicio LDAP para recopilar información como nombres de usuarios válidos, direcciones, detalles departamentales, etc.

## Enumeración NTP

- Network Time Protocol \ (NTP \) está diseñado para sincronizar relojes de computadoras en red
- Utiliza el puerto UDP 123
- Puede usarlo para encontrar información importante en una red
- Puede usar Nmap, Wireshark

## Enumeración SMTP y DNS

* SMTP tiene 3 comandos integrados
- VRFY: valida a los usuarios
- EXPN: indica las direcciones de entrega reales de alias y listas de correo
- RCPT TO: define los destinatarios del mensaje
* Los servidores SMTP responden de manera diferente a estos comandos
* Los atacantes pueden interactuar directamente con SMTP a través del indicador de telnet y recopilar una lista de usuarios válidos en el servidor SMTP

## Contramedidas de enumeración

* Contramedidas SNMP
- Eliminar el agente SNMP y apagar el servicio SNMP \ (bloque 161 \)
- Cambiar el nombre de la cadena de comunidad predeterminada
- Actualice a SNMP3, que cifra contraseñas / mensajes
- Implementar una opción de seguridad adicional llamada "restricciones adicionales para conexiones anónimas"
- Asegúrese de que el acceso a las tuberías de sesión nula, los recursos compartidos de sesión nula y el filtrado IPsec estén restringidos
* Contramedidas DNS
- Deshabilitar las transferencias de zona DNS a los hosts que no son de confianza
- Asegúrese de que los hosts privados y sus direcciones IP no se publiquen en los archivos de zona DNS del servidor DNS público
- Utilice servicios de registro de DNS premium para ocultar información confidencial
- Utilice contactos de administrador de red estándar para registros de dns con el fin de evitar ataques de ingeniería social
* Contramedidas SMTP
- Ignore los mensajes de correo electrónico a destinatarios desconocidos
- Deshabilitar las funciones de relé abierto
- No incluya información confidencial del servidor de correo ni del host local en las respuestas por correo

* Contramedidas LDAP
- Restrinja el acceso al directorio activo mediante el uso de software como citrix
- Habilitar bloqueo de cuenta
- Utilice la tecnología SSL para el tráfico LDAP

* Prueba de pluma de enumeración
- Se utiliza para identificar cuentas de usuario válidas o recursos compartidos mal protegidos
- La información puede ser usuarios y grupos, recursos de red
- Se utiliza en combinación con los datos recopilados en la fase de reconocimiento.
- Pasos en la prueba de pluma de enumeración
1. Encuentra el rango de la red
2. Calcular la máscara de subred
3. Experimentar el descubrimiento de host
4. Realizar escaneo de puertos
5. Realizar enumeración NetBIOS
6. Realizar enumeración SNMP
7. Realizar enumeración LDAP
8. Realizar enumeración NTP
9. Realizar enumeración SMTP
10. Realizar enumeración de DNS
11. Documentar todos los hallazgos


h4Ppy #@cK1n6 :)
> Discord: heanczko#4478
