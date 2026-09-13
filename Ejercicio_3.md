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
 
Como se definió en la parte anterior, una base de datos es una colección compartida de datos relacionados que se utiliza para 
apoyar las actividades de una organización en particular. Esta tiene las siguientes características:
 
## Integración
 
En el enfoque de bases de datos, idealmente cada elemento de datos se almacena en un solo lugar de la base de datos. La integración 
de todos los datos de una organización dentro de un sistema de base de datos tiene varias ventajas: primero, permite compartir los 
datos entre los empleados y demás personas que tienen acceso al sistema; segundo, da a los usuarios la capacidad de generar más 
información a partir de una cantidad determinada de datos de la que sería posible sin dicha integración.
 
## Persistencia
 
Silberschatz, Korth y Sudarshan explican que los lenguajes de las bases de datos se diferencian de los lenguajes de programación tradicionales 
en que trabajan directamente con datos que son persistentes, es decir, datos que siguen existiendo una vez que el programa que los creó ha concluido. 
Las relaciones de las bases de datos y sus tuplas son ejemplos de datos persistentes; en cambio, los únicos datos persistentes con los que 
trabajan directamente los lenguajes de programación tradicionales son los archivos.
 
## Redundancia controlada
 
La redundancia de datos es una situación que ocurre en una base de datos cuando un campo necesita actualizarse en más de una tabla. 
En el enfoque de bases de datos, idealmente cada elemento de datos se almacena en un solo lugar. En algunos casos la redundancia de 
datos aún existe para mejorar el rendimiento del sistema, pero dicha redundancia es controlada mediante la programación de las aplicaciones 
y se mantiene al mínimo, introduciendo la menor redundancia posible al diseñar la base de datos.
 
## Integridad
 
La integridad de los datos se refiere al mantenimiento y aseguramiento de que los datos en una base de datos sean correctos y consistentes.
 
## Independencia de datos
 
Otra ventaja de un sistema gestor de bases de datos es que permite la independencia de los datos. Es decir, las descripciones de los datos del 
sistema, o los datos que describen a los datos (metadatos), están separados de los programas de aplicación. Esto es posible porque los cambios 
en la estructura de los datos son manejados por el sistema gestor de la base de datos y no están incrustados en el programa mismo.
 
## Seguridad
 
No todos los usuarios de un sistema de base de datos tendrán los mismos privilegios de acceso. Por ejemplo, un usuario podría tener acceso de 
solo lectura (es decir, la capacidad de leer un archivo pero no modificarlo), mientras que otro podría tener privilegios de lectura y escritura 
(la capacidad de leer y modificar un archivo). Por esta razón, un sistema gestor de bases de datos debe proporcionar un subsistema de seguridad
para crear y controlar distintos tipos de cuentas de usuario y restringir el acceso no autorizado.
 
## Concurrencia
 
La concurrencia es la capacidad de la base de datos de permitir que múltiples usuarios accedan al mismo registro sin afectar negativamente el 
procesamiento de las transacciones. Esto se logra mediante las llamadas estrategias de control de concurrencia: funciones de la base de datos que
permiten que varios usuarios accedan al mismo elemento de datos al mismo tiempo.
 
## Recuperación
 
El respaldo (backup) y la recuperación son métodos que permiten proteger los datos contra su pérdida. El sistema de base de datos proporciona un 
proceso independiente al del respaldo de red, dedicado a respaldar y recuperar los datos. Si un disco duro falla y la base de datos almacenada en 
él deja de estar accesible, la única forma de recuperarla es a partir de un respaldo. Si un sistema informático falla en medio de un proceso 
complejo de actualización, el subsistema de recuperación es responsable de asegurar que la base de datos sea restaurada a su estado original.

## 3. Archivos frente a bases de datos
 
## Redundancia
 
En los sistemas basados en archivos, es común que la misma información se almacene por duplicado en distintos archivos (por ejemplo, 
un departamento de Ventas y uno de Contratos guardando datos similares de un mismo cliente o propiedad). El enfoque de bases de datos 
integra estos archivos para reducir esa duplicación, aunque no la elimina por completo: a veces se mantiene cierta redundancia de forma
controlada, ya sea para representar relaciones entre datos o para mejorar el rendimiento.
 
## Inconsistencia
 
Cuando un dato se repite en varios archivos sin control, actualizarlo implica hacerlo en cada copia por separado, lo que aumenta el 
riesgo de que las copias queden desincronizadas (inconsistentes). Al reducir o controlar la redundancia mediante una base de datos, 
un dato solo necesita actualizarse una vez, y el nuevo valor está disponible de inmediato para todos los usuarios.
 
## Dependencia programa-datos
 
En los sistemas basados en archivos, la descripción de los datos y la lógica para acceder a ellos están incrustadas dentro de cada 
programa de aplicación, lo que hace que los programas dependan directamente de la estructura de los datos. Cualquier cambio en esa 
estructura (por ejemplo, ampliar el tamaño de un campo) puede obligar a modificar todos los programas afectados. Un sistema gestor 
de bases de datos, en cambio, separa la descripción de los datos de las aplicaciones, logrando independencia de datos y facilitando 
el mantenimiento.
 
## Por qué el enfoque de archivos dio origen a los sistemas gestores
 
Estos tres problemas (redundancia, inconsistencia y dependencia programa-datos) generaban sistemas costosos de mantener, propensos a errores y difíciles de escalar conforme una organización crecía y sus departamentos necesitaban compartir información entre sí. Los sistemas gestores de bases de datos (DBMS) surgieron como respuesta a estas limitaciones: al centralizar los datos en un solo repositorio integrado y controlado por un software especializado, se resolvían de raíz la duplicación descontrolada, la falta de consistencia y la rigidez que generaba la dependencia entre programas y datos, además de aportar beneficios adicionales como seguridad, control de concurrencia y respaldo/recuperación centralizados.
 
## Desventajas
 
Aunque las bases de datos tienen muchísimas ventajas sobre los archivos físicos, sigue siendo importante tener en cuenta que no son un sistema definitivo y que, dependiendo de las necesidades, capacidades y usuarios, pueden no ser el mejor método.
 
Un ejemplo de esto es su complejidad: una base de datos puede llegar a ser una pieza de software muy compleja, en la que cambios en el diseño pueden causar serias consecuencias para una organización. Si además se desea que un profesional la administre, hay que considerar su salario, y si a esto se le suman servicios adicionales, como el almacenamiento en la nube, los costos van creciendo aún más.
 
Por último, las bases de datos pueden llegar a depender de otros servicios (como el mencionado anteriormente de guardar archivos en la nube) y los usuarios no siempre pueden confiar en que todos los componentes del sistema funcionen en su totalidad todo el tiempo, ya que una falla puede provocar la pérdida de información u otros recursos de gran valor.

# 4. Usuarios de una base de datos
 
## Diseñadores de las bases de datos
 
Son los responsables de identificar los datos que se almacenarán en la base de datos y de elegir las estructuras apropiadas para representarlos y almacenarlos. Esta tarea se realiza principalmente antes de implementar y llenar la base de datos. Es responsabilidad de los diseñadores comunicarse con todos los posibles usuarios para conocer sus requisitos y crear un diseño que satisfaga sus necesidades. En muchos casos forman parte de la plantilla del DBA, y pueden asumir otras responsabilidades una vez completado el diseño. Interactúan con los grupos de usuarios potenciales, desarrollan vistas de la base de datos según sus requisitos, y luego integran esas vistas en un diseño final capaz de soportar las necesidades de todos los grupos de usuarios.
 
## Programadores de aplicaciones (y analistas de sistemas)
 
Implementan las especificaciones definidas (normalmente por los analistas de sistemas) como programas; después verifican, depuran, documentan y mantienen esas transacciones ya preestablecidas ("enlatadas"). Estos analistas y programadores, comúnmente conocidos como desarrolladores de software o ingenieros de software, deben familiarizarse con todas las posibilidades que ofrece el DBMS para poder desempeñar sus tareas.
 
## Usuarios finales
 
Son las personas cuyo trabajo requiere acceso a la base de datos para realizar consultas, actualizaciones e informes; la base de datos existe principalmente para ser utilizada por ellos. Se dividen en varias categorías:
 
- **Casuales:** acceden ocasionalmente y necesitan información distinta cada vez; usan un lenguaje de consulta sofisticado. Suelen ser administradores de nivel medio o alto.
- **Principiantes o paramétricos:** representan una parte considerable de los usuarios finales; consultan y actualizan constantemente la base de datos mediante transacciones estándar ya programadas y probadas (por ejemplo, cajeros bancarios o agentes de viajes).
- **Sofisticados:** incluyen ingenieros, científicos y analistas que están completamente familiarizados con el DBMS para implementar sus propias aplicaciones y satisfacer requisitos complejos.
- **Independientes:** mantienen bases de datos personales usando paquetes de software con interfaces fáciles de usar (por ejemplo, alguien que usa un programa de impuestos para guardar su información financiera personal).
## Administradores de las bases de datos (DBA)
 
En cualquier organización donde muchas personas comparten los mismos recursos, se necesita un administrador que los supervise. En un entorno de bases de datos, el recurso principal es la base de datos misma, y el secundario es el DBMS y el software relacionado. El DBA es responsable del acceso autorizado a la base de datos, de coordinar y monitorear su uso, y de adquirir los recursos de software y hardware necesarios. También es responsable de resolver problemas como brechas de seguridad o tiempos de respuesta deficientes. En empresas grandes, el DBA cuenta con un equipo de apoyo para realizar estas funciones.

# 5. Ciclo de vida de una base de datos
 
## 1. Database planning (Planeación de la base de datos)
 
Planificar cómo se pueden realizar las etapas del ciclo de vida de la forma más eficiente y efectiva posible.
 
**Entregable:** un plan de la base de datos, que incluye la declaración de misión y los objetivos de misión del proyecto.
 
## 2. System definition (Definición del sistema)
 
Especificar el alcance y los límites del sistema de base de datos, incluyendo sus principales vistas de usuario, sus usuarios y las áreas de aplicación.
 
**Entregable:** un documento de definición del sistema, con el alcance y las vistas de usuario identificadas.
 
## 3. Requirements collection and analysis (Recolección y análisis de requisitos)
 
Recolección y análisis de los requisitos para el nuevo sistema de base de datos.
 
**Entregable:** una especificación de requisitos del sistema.
 
## 4. Database design (Diseño de la base de datos)
 
Diseño conceptual, lógico y físico de la base de datos.
 
**Entregable:** los modelos o esquemas conceptual, lógico y físico de la base de datos.
 
## 5. DBMS selection (Selección del DBMS, opcional)
 
Selección de un DBMS adecuado para el sistema de base de datos.
 
**Entregable:** un reporte o recomendación con el DBMS elegido y la justificación de la elección.
 
## 6. Application design (Diseño de la aplicación)
 
Diseño de la interfaz de usuario y de los programas de aplicación que usan y procesan la base de datos.
 
**Entregable:** el diseño de la interfaz de usuario y las especificaciones de los programas de aplicación.
 
## 7. Prototyping (Prototipado, opcional)
 
Construcción de un modelo funcional del sistema de base de datos, que permite a los diseñadores o usuarios visualizar y evaluar cómo se verá y funcionará el sistema final.
 
**Entregable:** un prototipo funcional del sistema.
 
## 8. Implementation (Implementación)
 
Creación de las definiciones físicas de la base de datos y de los programas de aplicación.
 
**Entregable:** la base de datos físicamente implementada, junto con los programas de aplicación desarrollados.
 
## 9. Data conversion and loading (Conversión y carga de datos)
 
Carga de los datos del sistema anterior hacia el nuevo sistema y, cuando es posible, conversión de las aplicaciones existentes para que funcionen sobre la nueva base de datos.
 
**Entregable:** la base de datos ya poblada con los datos migrados, y las aplicaciones anteriores adaptadas al nuevo sistema.
 
## 10. Testing (Pruebas)
 
El sistema de base de datos se prueba en busca de errores y se valida contra los requisitos especificados por los usuarios.
 
**Entregable:** un sistema probado y validado, junto con el reporte de errores encontrados y corregidos.
 
## 11. Operational maintenance (Mantenimiento operativo)
 
El sistema de base de datos ya está completamente implementado. Se monitorea y mantiene de forma continua, y cuando es necesario, los nuevos requisitos se incorporan al sistema repitiendo las etapas anteriores del ciclo de vida.
 
**Entregable:** el sistema en operación continua, con actualizaciones y ajustes documentados conforme surgen nuevas necesidades.

 ---
 
**Referencias**
 
Watt, A., & Eng, N. (2014). *Database Design – 2nd Edition*. BCcampus. https://opentextbc.ca/dbdesign01/
 
Ackoff, R. L. (1999). *Ackoff's Best*. New York: John Wiley & Sons, pp. 170–172.
 
Bourgeois, D. T. (2019). *Information Systems for Business and Beyond*. Saylor Academy. 
https://resources.saylor.org/wwwresources/archived/site/textbooks/Information%20Systems%20for%20Business%20and%20Beyond.pdf
 
Connolly, T. (2005, 4th Edition Pearson Educated). 

Elmasri, R., & Navathe, S. B. Fundamentos de Sistemas de Bases de Datos. Pearson. 5ta Edicion (2007)  
*Database Systems: A Practical Approach to Design, Implementation, and Management*.  

Silberschatz, A., Korth, H. F., & Sudarshan, S. *Fundamentos de bases de datos*. McGraw-Hill. Quinta Edición (2006)    
