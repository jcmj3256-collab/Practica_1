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

# 6. Sistema gestor de bases de datos
 
## Módulos componentes
 
Los sistemas de bases de datos se dividen en módulos que atienden cada una de las responsabilidades del sistema general. A grandes rasgos, los componentes funcionales se dividen en el **gestor de almacenamiento** y el **procesador de consultas**:
 
- **Gestor de almacenamiento:** es fundamental porque las bases de datos suelen requerir grandes cantidades de espacio (desde cientos de gigabytes hasta terabytes en las bases de datos corporativas más grandes). Como la memoria principal no puede almacenar toda esa información, los datos se guardan en disco y se intercambian con la memoria principal cuando se necesitan. Dado que este intercambio es lento comparado con la velocidad del procesador, el sistema debe estructurar los datos para minimizar dicho intercambio.
- **Procesador de consultas:** ayuda a simplificar y facilitar el acceso a los datos mediante vistas de alto nivel, de modo que los usuarios no tengan que lidiar con los detalles físicos de la implementación. Es responsable de traducir las actualizaciones y consultas escritas en lenguajes no procedimentales (a nivel lógico) en una secuencia eficiente de operaciones a nivel físico.
- **Gestor de transacciones:** garantiza que la base de datos permanezca en un estado consistente (correcto) a pesar de fallos del sistema, y que la ejecución concurrente de transacciones se realice sin conflictos.
*(Pendiente: agregar aquí lo relacionado con el catálogo/diccionario de datos si tu libro lo menciona como módulo aparte.)*
 
## Lenguajes de bases de datos
 
- **DDL (lenguaje de definición de datos):** se utiliza para definir el esquema conceptual (y, en algunos DBMS, también el interno) de la base de datos. El DBMS cuenta con un compilador DDL que procesa estas sentencias, identifica las estructuras del esquema y guarda su descripción en el catálogo del sistema.
- **DML (lenguaje de manipulación de datos):** permite a los usuarios recuperar, insertar, borrar y modificar datos una vez que la base de datos ya existe y contiene información. Existen dos tipos:
  - **DML de alto nivel (no procedimental o declarativo):** permite especificar operaciones complejas de forma concisa, indicando qué datos se quieren recuperar en lugar de cómo hacerlo. Puede usarse de forma interactiva o incrustado en un lenguaje de programación. También se le llama *set-at-a-time*, porque puede recuperar varios registros con una sola sentencia (SQL es el ejemplo típico).
  - **DML de bajo nivel (procedimental):** debe incrustarse en un lenguaje de programación de propósito general y recupera los registros uno por uno (*record-at-a-time*), por lo que se necesitan estructuras como bucles para procesar varios registros.
- **VDL (lenguaje de definición de vistas):** se utiliza para especificar las vistas de usuario y su mapeo hacia el esquema conceptual. En los DBMS relacionales, SQL cumple esta función.
- **SDL (lenguaje de definición de almacenamiento):** se utiliza para especificar el esquema interno (físico) de la base de datos. En los DBMS relacionales actuales ya no suele existir como lenguaje independiente; en su lugar, el personal del DBA controla la indexación y el almacenamiento mediante parámetros y especificaciones propias del sistema.
- **Lenguaje integrado (caso de SQL):** en los DBMS actuales, estos lenguajes normalmente no están separados, sino que se combinan en un solo lenguaje comprensivo. SQL, por ejemplo, combina DDL, VDL y DML, además de sentencias para restricciones y evolución del esquema.
- **Control de transacciones:** SQL incluye comandos para especificar el inicio y el final de una transacción (por ejemplo, COMMIT para confirmar los cambios y ROLLBACK para deshacerlos), lo cual está a cargo del gestor de transacciones mencionado en la sección de módulos.
- **DCL (lenguaje de control de datos):** SQL cuenta con estructuras de lenguaje para especificar la concesión y revocación de privilegios a los usuarios. Estos privilegios normalmente corresponden al derecho de utilizar ciertos comandos SQL (como SELECT, INSERT, DELETE o UPDATE) para acceder a determinadas relaciones. A cada relación se le asigna un propietario, quien —junto con el personal del DBA— puede otorgar a usuarios seleccionados el privilegio de usar esas sentencias, así como el privilegio de crear esquemas, tablas o vistas. Estos comandos se conocen como **GRANT** y **REVOKE**.
## Clasificación de los DBMS
 
Los DBMS se clasifican según varios criterios:
 
- **Modelo de datos:** relacional (el más usado actualmente), orientado a objetos, objeto-relacional, jerárquico o de red. Los modelos jerárquico y de red son más antiguos, pero todavía se usan en sistemas heredados (por ejemplo, IMS de IBM).
- **Número de usuarios:** sistemas de un solo usuario (usados sobre todo en PCs) frente a sistemas multiusuario, que permiten acceso simultáneo de varias personas (la mayoría de los DBMS actuales).
- **Número de sitios:** un DBMS **centralizado** almacena los datos en un solo computador; un DBMS **distribuido (DDBMS)** reparte los datos y el software entre varios sitios conectados por red. Cuando varios DBMS autónomos se acoplan entre sí, se le llama DBMS **federado**.
- **Costo:** va desde soluciones de código abierto y gratuitas (como MySQL o PostgreSQL) hasta sistemas empresariales que pueden costar millones de dólares al año en licencias, mantenimiento y soporte.
- **Propósito:** de propósito general (para múltiples aplicaciones) o de propósito especial (diseñados para una aplicación específica, como los sistemas de reservas de aerolíneas, muchas veces asociados a procesamiento de transacciones en línea u OLTP).

# 7. Sistema de base de datos: arquitectura, independencia de datos y arquitecturas centralizada y cliente-servidor
 
## Arquitectura de tres niveles (esquemas)
 
**Fuente:** Elmasri, R., & Navathe, S. B. *Fundamentos de sistemas de bases de datos*. Capítulo 2.
 
La arquitectura de tres esquemas (también conocida como arquitectura ANSI-SPARC) organiza la base de datos en tres niveles:
 
- **Nivel interno:** cuenta con un esquema interno, que describe la estructura de almacenamiento físico de la base de datos. Utiliza un modelo de datos físico y detalla todo lo relacionado con el almacenamiento de los datos y las rutas de acceso a ellos.
- **Nivel conceptual:** cuenta con un esquema conceptual, que describe la estructura de toda la base de datos para una comunidad de usuarios. Oculta los detalles de las estructuras de almacenamiento físico y se concentra en describir las entidades, los tipos de datos, las relaciones, las operaciones de los usuarios y las restricciones. Suele describirse mediante un modelo de datos representativo, a menudo basado en un diseño previo con un modelo de datos de alto nivel.
- **Nivel de vista o externo:** incluye varios esquemas externos o vistas de usuario. Cada esquema externo describe la parte de la base de datos que interesa a un grupo particular de usuarios, ocultándoles el resto de la base de datos. Al igual que el esquema conceptual, normalmente se implementa mediante un modelo de datos representativo.
## Independencia de datos
 
**Fuente:** Elmasri, R., & Navathe, S. B. *Fundamentos de sistemas de bases de datos*. Capítulo 2.
 
La arquitectura de tres esquemas permite explicar el concepto de independencia de datos: la capacidad de cambiar el esquema en un nivel del sistema sin tener que modificar el esquema del nivel inmediatamente superior. Existen dos tipos:
 
- **Independencia lógica de datos:** es la capacidad de cambiar el esquema conceptual (por ejemplo, para expandir la base de datos agregando un tipo de registro, o para reducirla eliminando uno) sin tener que modificar los esquemas externos ni los programas de aplicación que dependen de ellos. Es más difícil de lograr, porque implica que los cambios estructurales o de restricciones no afecten a las aplicaciones existentes.
- **Independencia física de datos:** es la capacidad de cambiar el esquema interno (por ejemplo, reorganizando archivos físicos o agregando estructuras de acceso para mejorar el rendimiento) sin necesidad de modificar el esquema conceptual ni los esquemas externos. Este tipo de independencia sí se logra en la mayoría de las bases de datos actuales, ya que se le ocultan al usuario los detalles de cómo y dónde se almacenan físicamente los datos.
Cuando el esquema de un nivel cambia, solo se actualiza el mapeo entre ese nivel y el siguiente, gracias a la información de mapeo que el DBMS mantiene en su catálogo; así, las aplicaciones que hacen referencia al nivel superior no necesitan modificarse. Sin embargo, mantener estos mapeos entre niveles genera cierta sobrecarga de procesamiento, razón por la cual pocos DBMS implementan la arquitectura de tres esquemas de forma completa.
 
## Arquitectura centralizada
 
Las arquitecturas de los DBMS han seguido tendencias similares a las de los sistemas de cómputo en general. En un inicio, se usaban mainframes que procesaban todas las funciones del sistema —incluyendo las aplicaciones de usuario, las interfaces y toda la funcionalidad del DBMS— mientras los usuarios accedían mediante terminales sin capacidad de procesamiento propio, que solo mostraban información. Cuando bajó el precio del hardware y los usuarios empezaron a usar PCs y estaciones de trabajo, al principio estas computadoras se usaban de forma similar a los terminales: el DBMS seguía siendo centralizado, con toda la funcionalidad, ejecución de aplicaciones e interacción del usuario ocurriendo en una sola máquina. Con el tiempo, los sistemas comenzaron a aprovechar la capacidad de procesamiento disponible del lado del usuario, lo que dio origen a las arquitecturas cliente/servidor.
 
## Arquitectura cliente-servidor
 
La arquitectura cliente/servidor surgió para entornos donde múltiples PCs, estaciones de trabajo, servidores de archivos, impresoras y servidores de bases de datos están conectados a través de una red. La idea central es definir servidores especializados con funciones específicas (por ejemplo, un servidor de archivos, uno de impresión, o uno de bases de datos), a los que acceden múltiples máquinas cliente. Un **cliente** es típicamente la máquina de un usuario, que ofrece interfaz y procesamiento local; un **servidor** es un sistema con el hardware y software necesarios para prestar servicios a los clientes (acceso a archivos, impresión, bases de datos, etc.). Sobre esta estructura básica se desarrollaron dos tipos principales de arquitecturas DBMS: de **dos capas** (el cliente se conecta directamente al servidor de base de datos) y de **tres capas**, descrita a continuación.
 
Muchas aplicaciones web utilizan justamente esta arquitectura de **tres capas**, que agrega una capa intermedia entre el cliente y el servidor de base de datos. Esta capa intermedia se conoce como **servidor de aplicaciones** o **servidor web**, y actúa como intermediaria almacenando las reglas de negocio (procedimientos o restricciones) usadas para acceder a los datos del servidor de bases de datos; también puede mejorar la seguridad verificando las credenciales del cliente antes de enviar una solicitud al servidor de bases de datos.
 
En esta arquitectura:
- Los **clientes** contienen las interfaces gráficas (GUI) y algunas reglas de negocio específicas de la aplicación.
- El **servidor intermedio** acepta las solicitudes del cliente, las procesa, envía comandos a la base de datos, y luego actúa como conducto para pasar los datos (parcialmente procesados) de vuelta al cliente, donde se terminan de procesar para mostrarse al usuario.
Así, la interfaz de usuario, las reglas de negocio y el acceso a los datos forman las tres capas. También existe una variante equivalente con otra nomenclatura: **capa de presentación** (muestra información y permite la entrada de datos), **capa lógica de negocio** (aplica las reglas y restricciones intermedias) y **capa de servicios de base de datos** (administración de los datos).
 
Si la capa inferior se divide a su vez en un servidor web y un servidor de base de datos, se obtiene una **arquitectura de cuatro capas**. Es común dividir aún más las capas entre el usuario y los datos almacenados, dando lugar a **arquitecturas de n-capas** (donde n suele ser 4 o 5), generalmente subdividiendo la capa lógica de negocio. Esto permite que cada capa se ejecute en el procesador o sistema operativo más adecuado, y que se manipule de forma independiente. En sistemas ERP y CRM también suele usarse una capa adicional llamada **middleware**, que conecta los módulos front-end con varias bases de datos back-end.
 
Además, los avances en cifrado y compresión de datos ayudan a que la transferencia de información entre servidores y clientes sea más segura y eficiente, aunque la seguridad de las redes sigue siendo una preocupación importante.

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
