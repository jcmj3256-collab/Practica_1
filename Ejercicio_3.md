# Ejercicio 3. Investigación: Que es una base de datos?

## 1. Dato, información y base de datos
 
## Dato
 
**Watt y Eng (2014):** El dato es información factual, como una medición o una estadística, sobre objetos 
y conceptos. Usamos los datos para discusiones o como parte de un cálculo. Un dato puede ser una persona, 
un lugar, un evento, una acción o cualquiera de un número de cosas. Un solo hecho es un elemento de dato.
 
**Ackoff (1999):** Los datos son símbolos que representan las propiedades de objetos y eventos.
 
**Comparación:** Ambas definiciones nos dicen que estas pueden ser representaciones de diferentes cosas, 
creo que la única diferencia entre ambas es que además de estar más desarrollada, la definición de Watt y 
Eng no solo habla de ser un reflejo del mundo o concepto, sino que además estas pueden ser usadas para medir 
diferentes cosas, como veremos en las siguientes definiciones de información.

## Información
 
**Ackoff (1999):** La información consiste en datos ya procesados, dirigido dicho procesamiento a incrementar 
su utilidad. Por ejemplo, los censores recolectan datos. Al igual que los datos, la información también representa 
las propiedades de objetos y eventos, pero lo hace de forma más compacta y útil que los datos. La diferencia entre 
dato e información es funcional, no estructural.
 
**Bourgeois (2019):** Los datos son los fragmentos en bruto de información, sin contexto. Al agregarles contexto por 
ejemplo, aclarar que ciertos números representan la cantidad de estudiantes inscritos en determinadas clases los datos 
se convierten en información.
 
**Comparación:** Ambas nos dicen que la información parte de los datos y de cómo al ser "estudiados" o analizados estos 
nos empiezan a dar una imagen o representación sobre este cúmulo de datos con el que se inició. Bourgeois no ahonda tanto 
en la definición, como sí lo hace Ackoff pero sus definiciones son prácticamente iguales.

## Base de datos
 
**Watt y Eng (2014):** Una base de datos es una colección compartida de datos relacionados que se utiliza para apoyar 
las actividades de una organización en particular. Una base de datos puede verse como un repositorio de datos que se 
define una sola vez y luego es accedido por varios usuarios.
 
**Connolly:** Una colección compartida de datos relacionados lógicamente, junto con una descripción de dichos datos, 
diseñada para satisfacer las necesidades de información de una organización. La base de datos es un repositorio único, 
posiblemente grande, que puede ser usado simultáneamente por muchos departamentos y usuarios. En lugar de archivos 
desconectados con datos redundantes, todos los elementos de datos están integrados con una mínima duplicación.
 
**Comparación:** Al igual que en las definiciones anteriores ambas nos dicen prácticamente lo mismo solo profundizando 
más o menos en el tema, en este caso, la definición de Connolly además de dar la definición, también nos habla sobre 
duplicidad y redundancia de datos, que es algo que todavía no se ha explicado pero que se verá más adelante en el documento.

## 2. Características de una base de datos
 
Como se definió en la parte anterior, una base de datos es una colección compartida de datos relacionados que se utiliza para apoyar las actividades de una organización en particular. Esta tiene las siguientes características:
 
## Integración
 
En el enfoque de bases de datos, idealmente cada elemento de datos se almacena en un solo lugar de la base de datos. La integración de todos los datos de una organización dentro de un sistema de base de datos tiene varias ventajas: primero, permite compartir los datos entre los empleados y demás personas que tienen acceso al sistema; segundo, da a los usuarios la capacidad de generar más información a partir de una cantidad determinada de datos de la que sería posible sin dicha integración.
 
## Persistencia
 
Silberschatz, Korth y Sudarshan explican que los lenguajes de las bases de datos se diferencian de los lenguajes de programación tradicionales en que trabajan directamente con datos que son persistentes, es decir, datos que siguen existiendo una vez que el programa que los creó ha concluido. Las relaciones de las bases de datos y sus tuplas son ejemplos de datos persistentes; en cambio, los únicos datos persistentes con los que trabajan directamente los lenguajes de programación tradicionales son los archivos.
 
## Redundancia controlada
 
La redundancia de datos es una situación que ocurre en una base de datos cuando un campo necesita actualizarse en más de una tabla. En el enfoque de bases de datos, idealmente cada elemento de datos se almacena en un solo lugar. En algunos casos la redundancia de datos aún existe para mejorar el rendimiento del sistema, pero dicha redundancia es controlada mediante la programación de las aplicaciones y se mantiene al mínimo, introduciendo la menor redundancia posible al diseñar la base de datos.
 
## Integridad
 
La integridad de los datos se refiere al mantenimiento y aseguramiento de que los datos en una base de datos sean correctos y consistentes.
 
## Independencia de datos
 
Otra ventaja de un sistema gestor de bases de datos es que permite la independencia de los datos. Es decir, las descripciones de los datos del sistema, o los datos que describen a los datos (metadatos), están separados de los programas de aplicación. Esto es posible porque los cambios en la estructura de los datos son manejados por el sistema gestor de la base de datos y no están incrustados en el programa mismo.
 
## Seguridad
 
No todos los usuarios de un sistema de base de datos tendrán los mismos privilegios de acceso. Por ejemplo, un usuario podría tener acceso de solo lectura (es decir, la capacidad de leer un archivo pero no modificarlo), mientras que otro podría tener privilegios de lectura y escritura (la capacidad de leer y modificar un archivo). Por esta razón, un sistema gestor de bases de datos debe proporcionar un subsistema de seguridad para crear y controlar distintos tipos de cuentas de usuario y restringir el acceso no autorizado.
 
## Concurrencia
 
La concurrencia es la capacidad de la base de datos de permitir que múltiples usuarios accedan al mismo registro sin afectar negativamente el procesamiento de las transacciones. Esto se logra mediante las llamadas estrategias de control de concurrencia: funciones de la base de datos que permiten que varios usuarios accedan al mismo elemento de datos al mismo tiempo.
 
## Recuperación
 
El respaldo (backup) y la recuperación son métodos que permiten proteger los datos contra su pérdida. El sistema de base de datos proporciona un proceso independiente al del respaldo de red, dedicado a respaldar y recuperar los datos. Si un disco duro falla y la base de datos almacenada en él deja de estar accesible, la única forma de recuperarla es a partir de un respaldo. Si un sistema informático falla en medio de un proceso complejo de actualización, el subsistema de recuperación es responsable de asegurar que la base de datos sea restaurada a su estado original.

 ---
 
**Referencias**
 
Watt, A., & Eng, N. (2014). *Database Design – 2nd Edition*. BCcampus. https://opentextbc.ca/dbdesign01/
 
Ackoff, R. L. (1999). *Ackoff's Best*. New York: John Wiley & Sons, pp. 170–172.
 
Bourgeois, D. T. (2019). *Information Systems for Business and Beyond*. Saylor Academy. 
https://resources.saylor.org/wwwresources/archived/site/textbooks/Information%20Systems%20for%20Business%20and%20Beyond.pdf
 
Connolly, T. (2005, 4th Edition Pearson Educated). 
*Database Systems: A Practical Approach to Design, Implementation, and Management*.

Silberschatz, A., Korth, H. F., & Sudarshan, S. *Fundamentos de bases de datos*. McGraw-Hill. Quinta Edición (2006)    
