# Inyección SQL

> Objetivos: comprender los conceptos de inyección SQL, comprender varios tipos de ataques de inyección SQL, comprender la metodología de inyección SQL, herramientas de inyección SQL, comprender diferentes técnicas de evasión de IDS, contramedidas de inyección SQL, herramientas de detección de inyección SQL

### Conceptos de inyección SQL

* La inyección de SQL es una técnica que se utiliza para aprovechar las vulnerabilidades de entrada no validadas para pasar comandos SQL a través de una aplicación web para su ejecución por la base de datos backend.
* Normalmente para recuperar información
* Este es un defecto en las aplicaciones web.
* El atacante puede desfigurar una página web con este ataque
* Pueden agregar información a su sitio web, extraer datos e insertar nuevos datos

## Tipos de inyección SQL

* Inyección SQL basada en errores: el atacante coloca una entrada incorrecta intencionalmente en la aplicación para ver los mensajes de error a nivel de la base de datos. Utiliza esto para crear inyecciones SQL cuidadosamente diseñadas
* Inyección SQL ciega: el atacante no tiene mensajes de error del sistema con el que trabajar. En cambio, el ataque simplemente envía una consulta SQL maliciosa a la base de datos.
* Siempre que vea SELECT, probablemente sea un comando SQL
* Comando Union SQL, uniendo una consulta falsificada a la consulta original
* Inyección SQL basada en el tiempo: evalúa el retraso de tiempo en respuesta a consultas de verdadero o falso

## Metodología de inyección SQL

* Recopilación de información y detección de vulnerabilidades SQL
* Los atacantes analizan las solicitudes web GET y POST para identificar todos los campos de entrada
* Luego, lanza el ataque
* Inyecciones SQL avanzadas
* Prueba de pluma de caja negra de inyección SQL
* Envíe comillas simples y datos de entrada para ver dónde no se desinfecta la entrada del usuario
* Envíe largas cadenas de datos basura para detectar saturaciones de búfer
* Se utilizó corchete derecho como datos de entrada

## Técnicas de evasión

* Evadir IDS
* Cadenas de entrada oscuras
* Codificación hexadecimal
* Manipulación de espacios en blanco
* Comentario en línea
* Codificación de caracteres

## Contramedidas

* Use firewalls en el servidor SQL
* No haga suposiciones sobre el tamaño, tipo o contenido de los datos que recibe la aplicación
* Evite construir SQL dinámico con valores de entrada concatenados
