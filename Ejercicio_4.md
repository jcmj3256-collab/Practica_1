# Ejercicio 4. Estado del Arte: Literatura Científica Arbitrada

---

## Ficha Técnica 1 — Bases de Datos Autónomas y Optimización Adaptativa

1. **Cita en formato APA (7.ª edición):**  
   Pavlo, A., Angulo, G., Arulraj, J., Lin, H., Lin, J., Menon, P., Mowke, P., Perron, M., Quah, I., Santurkar, S., Tomasic, A., Toor, S., Van Aken, D., Wang, Z., Wu, Y., Xian, R., & Zhang, T. (2017). Self-driving database management systems: Forecasting, modeling, and planning. *Proceedings of the VLDB Endowment*, 10(12), 1905–1916. https://doi.org/10.14778/3137765.3137794

2. **Problema que aborda el artículo:**  
   La excesiva complejidad en la configuración operativa, aprovisionamiento de recursos físicos, ajuste de parámetros (*knob tuning*) y selección de esquemas de indexación en sistemas gestores de bases de datos relacionales, factores que superan la capacidad de optimización manual de los administradores (DBA).

3. **Método o propuesta de los autores:**  
   Diseño de una arquitectura integrada de motor relacional autónomo (*self-driving DBMS*) que incorpora modelos de aprendizaje automático directamente en su núcleo. El sistema estructura una canalización de pronóstico de cargas futuras, modelado de costos de ejecución en memoria y planificación automatizada de acciones sin requerir interrupción de servicio ni supervisión humana.

4. **Resultado principal:**  
   Se evidenció que un motor relacional puede predecir con precisión fluctuaciones en patrones transaccionales complejos y generar configuraciones de índices y memoria dinámicas en tiempo de ejecución, logrando reducciones sustanciales de latencia y un consumo de recursos significativamente superior al ajuste manual tradicional.

5. **Relación con la Unidad Temática I:**  
   Se vincula explícitamente con los temas **Sistema Gestor de Bases de Datos: Módulos componentes** (optimizador de consultas, gestor de almacenamiento y catálogo del sistema) y con las **Responsabilidades y perfil del Administrador de la Base de Datos (DBA)**.

6. **Aporte para el proyecto del curso:**  
   Ilustra de forma contundente cómo las decisiones de diseño conceptual repercuten en el desempeño del motor, subrayando que un modelo relacional bien normalizado y con índices adecuados previene la degradación física y la ineficiencia transaccional.

---

## Ficha Técnica 2 — Concurrencia Transaccional y Bancos de Prueba

1. **Cita en formato APA (7.ª edición):**  
   Difallah, D. E., Pavlo, A., & Curino, C. (2019). OLTP-Bench: An extensible testbed for benchmarking relational databases. *Proceedings of the VLDB Endowment*, 7(4), 277–288. https://doi.org/10.14778/2732269.2732272

2. **Problema que aborda el artículo:**  
   La carencia de marcos de experimentación estandarizados, extensibles y reproducibles para evaluar rigurosamente el comportamiento transaccional, las políticas de aislamiento ACID y el control de concurrencia en motores relacionales bajo cargas de trabajo dinámicas y extremas.

3. **Método o propuesta de los autores:**  
   Creación del entorno de evaluación multi-hilo *OLTP-Bench*, plataforma capaz de emular y orquestar de manera simultánea 15 cargas transaccionales representativas de la industria, modulando tasas de peticiones, contención de bloqueos (*locks*) y variaciones de esquemas sobre motores SQL en tiempo de ejecución.

4. **Resultado principal:**  
   Descubrieron comportamientos anómalos de degradación de rendimiento y contención severa de bloqueos en diversos motores de base de datos consolidados ante variaciones súbitas de concurrencia, estableciendo una metodología empírica fundamental para calibrar el aislamiento transaccional y la persistencia.

5. **Relación con la Unidad Temática I:**  
   Guarda correspondencia directa con las **Características de una base de datos** (particularmente **Concurrencia**, **Integridad** y **Recuperación ante fallos**), así como con la arquitectura **Cliente-Servidor** y el procesamiento de transacciones.

6. **Aporte para el proyecto del curso:**  
   Brinda una perspectiva práctica sobre la vital necesidad de definir llaves primarias, llaves foráneas y reglas de integridad referencial estrictas, garantizando que el sistema soporte múltiples transacciones simultáneas sin corromper la consistencia de los datos.