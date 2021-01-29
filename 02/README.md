# Footprinting y Reconocimiento

## Conceptos

* Footprinting es el proceso de recopilar tanta información como sea posible sobre una red objetivo
* Amenazas de huellas: ingeniería social, ataques a redes y sistemas, fuga de información, pérdida de privacidad, espionaje corporativo, pérdida comercial

## Metodología

1. Huella a través de motores de búsqueda
   1. Google, Netcraft \ (URL restringidas, Determinar SO \), motor de búsqueda SHODAN, GMAPS, Google Finance, etc.
2. Huella mediante técnicas avanzadas de piratería de Google
   1. Utilizando una técnica para localizar cadenas de texto específicas dentro de los resultados de búsqueda mediante un operador avanzado en el motor de búsqueda \ (encontrar objetivos vulnerables \), los operadores de Google para localizar cadenas de texto específicas, GHDB
3. Huella a través de sitios de redes sociales
   1. Identificaciones falsas de compañeros de trabajo, búsqueda de información personal, seguimiento de sus grupos, etc., Facebook, Twitter, LinkedIn, etc.
4. Huella del sitio web
   1. Ver información del sistema de sitios web, información personal, examinar comentarios de fuente HTML, Web Spiders, archive.org, sitios de duplicación, etc.
5. Huella de correo electrónico
   1. Puede obtener la dirección IP del destinatario, la ubicación geográfica, el correo electrónico recibido y leído, la duración de la lectura, la detección de proxy, los enlaces, la información del sistema operativo y del navegador, reenviar el correo electrónico
6. Inteligencia competitiva
   1. La recopilación de inteligencia competitiva es el proceso de identificar, recopilar, analizar y verificar, y utilizar la información sobre sus competidores de fuentes como Internet. Monitoreo del tráfico web, etc.
   2. No interfiere y es de naturaleza sutil
   3. Este método es legal
7. Perfil de WHOIS
   1. Las bases de datos de WHOIS son mantenidas por registros regionales de Internet y contienen PI de los propietarios de dominios
8. Huella DNS
   1. El atacante puede recopilar información de DNS para determinar hosts clave en la red
9. Huella de red
   1. La información del alcance de la red ayuda a los atacantes a crear un mapa de la red objetivo.
   2. Busque el rango de direcciones IP mediante la búsqueda en la base de datos whois de ARIN
   3. Los programas Traceroute funcionan con el concepto de protocolo ICMP y utilizan el campo TTL en el encabezado de los paquetes ICMP para descubrir la ruta a un host de destino.
10. Huella a través de la ingeniería social
    1. Arte en la explotación del comportamiento humano para extraer información confidencial
    2. Los ingenieros sociales dependen del hecho de que las personas desconocen

## Herramientas

* Maltego
* Recon-NG \ (Marco de reconocimiento web \)

## Contramedidas

1. Restrinja el acceso de los empleados a los sitios de redes sociales.
2. Configurar servidores web para evitar la fuga de información
3. Eduque a los empleados para que utilicen seudónimos
4. Limita la cantidad de información que publicas.
5. Utilice técnicas de huella para descubrir y eliminar información confidencial
6. Utilice servicios de registro anónimos
7. Hacer cumplir las políticas de seguridad



