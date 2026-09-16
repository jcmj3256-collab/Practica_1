# Ejercicio 1. Control de versiones con Git y GitHub

## Parte A. Investigación

### 1. ¿Qué es un sistema de control de versiones y qué problema resuelve en un trabajo en equipo?
Un Sistema de Control de Versiones (VCS, por sus siglas en inglés) es una herramienta de infraestructura orientada a registrar, clasificar y auditar cronológicamente el conjunto de transformaciones aplicadas al código fuente, scripts de bases de datos y documentación de un proyecto.

En un esquema de trabajo en equipo, resuelve problemas críticos:
* **Eliminación de sobreescritura destructiva:** Evita que el guardado simultáneo de un desarrollador sobreescriba y destruya de manera silenciosa las modificaciones realizadas por otro miembro sobre el mismo recurso.
* **Trazabilidad histórica y autoría granular:** Registra de manera inmutable quién realizó cada alteración, en qué momento exacto y bajo qué justificación técnica documentada en el mensaje de confirmación.
* **Entornos aislados de experimentación:** Permite la bifurcación de líneas de desarrollo paralelas (ramas) para crear nuevas características o validar esquemas sin comprometer la estabilidad de la rama troncal productiva.
* **Reversión determinista de fallos:** Facilita regresar el árbol de trabajo a un estado histórico funcional y libre de errores si una nueva integración introduce incompatibilidades o defectos.

### 2. Diferencia entre Git y GitHub
Git y GitHub no son sinónimos ni herramientas equivalentes:
* **Git** es un software distribuido de control de versiones que opera localmente en la máquina del usuario. Gestiona el historial mediante un Grafo Acíclico Dirigido (DAG) de instantáneas (*snapshots*), permitiendo crear confirmaciones, ramas e inspeccionar diferencias sin necesidad de conexión a red ni servidores externos.
* **GitHub** es una plataforma de servicios web orientada a la gobernanza y hospedaje remoto de repositorios Git. Proporciona control de acceso, auditorías de seguridad, integración y despliegue continuo (CI/CD mediante *GitHub Actions*), seguimiento de incidencias (*issues*) y revisión colaborativa de código a través de *Pull Requests*.

### 3. Glosario Técnico de Términos

* **Repositorio (*Repository*):** Estructura de base de datos administrada por Git (ubicada en la carpeta oculta `.git`) que alberga el grafo inmutable de confirmaciones, referencias de ramas y el historial completo del proyecto.  
  *Ejemplo:* El repositorio del proyecto que contiene los archivos de la materia (`README.md`, scripts y documentación).
* **Confirmación (*Commit*):** Objeto criptográfico inmutable identificado por una suma SHA-1 que captura una instantánea exacta del árbol de archivos en el área de preparación (*stage*), junto con sus metadatos de autoría y descripción técnica.  
  *Ejemplo:* `commit a46406b - "Agrega README inicial de la practica"`.
* **Rama (*Branch*):** Puntero móvil que referencia la última confirmación realizada dentro de una línea de desarrollo divergente e independiente.  
  *Ejemplo:* Una rama llamada `feature/ejercicio-1` creada para elaborar la investigación sin tocar la rama `main`.
* **Fusión (*Merge*):** Algoritmo de unión mediante el cual Git integra los historiales y cambios de dos ramas divergentes en una sola confirmación de consolidación.  
  *Ejemplo:* Integrar los cambios de `feature/ejercicio-1` dentro de `main` al validar los requisitos.
* **Conflicto de fusión (*Merge Conflict*):** Evento en el que Git suspende una fusión automática porque dos desarrolladores modificaron concurrentemente las mismas líneas de un archivo con datos incompatibles, requiriendo intervención manual.  
  *Ejemplo:* Dos integrantes asignando puertos o contraseñas distintas en la misma línea del archivo `compose.yaml`.
* **Pull Request (PR):** Mecanismo de colaboración provisto por plataformas remotas donde un colaborador solicita la integración formal de una rama secundaria a una rama protegida, facilitando la discusión técnica y la aprobación colegiada.  
  *Ejemplo:* Abrir un PR para incorporar el desarrollo del Ejercicio 1 hacia la rama principal del equipo.
* **Archivo `.gitignore`:** Archivo plano donde se configuran expresiones regulares para omitir deliberadamente archivos temporales, logs o credenciales del rastreo de Git.  
  *Ejemplo:* Incluir entradas como `.env`, `*.log` y directorios de configuración local `.vscode/`.
* **Archivo `README.md`:** Portada técnica y catálogo de navegación del proyecto en formato Markdown, que resume autores, objetivo, requisitos de ejecución e índice de archivos.  
  *Ejemplo:* El `README.md` raíz que presenta los nombres, el grupo 3CV2 y los enlaces a los 5 ejercicios.

### 4. Flujo de trabajo basado en ramas y revisión entre pares (*Peer Review*)
En flujos modernos como *GitHub Flow*, la rama principal se preserva en un estado rigurosamente probado y listo para producción. Todo cambio, investigación o configuración de base de datos se desarrolla en una rama aislada (*feature branch*).

La revisión obligatoria entre pares previa a la fusión es fundamental porque:
1. **Detección temprana de anomalías:** Permite que un segundo par de ojos examine inconsistencias conceptuales, credenciales filtradas o malas prácticas de modelado antes de su integración final.
2. **Mitigación del factor de dependencia (*Bus Factor*):** Garantiza que todos los miembros del equipo conozcan la arquitectura del sistema, evitando que la continuidad del proyecto recaiga en una sola persona.
3. **Estandarización:** Conserva la consistencia de estilos, formatos de entrega y estructura de carpetas en todo el repositorio.

---

## Parte B. Práctica

1. **Cuenta y repositorio:** Repositorio colaborativo alojado en GitHub y configurado con acceso mutuo para el equipo.
2. **README.md:** Archivo principal con datos de identificación de los integrantes (Grupo 3CV2, ISC) y el índice completo de navegación.
3. **Archivo .gitignore:** Implementado para evitar la inclusión de archivos temporales del sistema, configuraciones locales y credenciales.
4. **Historial de confirmaciones:** Mínimo de confirmaciones descriptivas distribuidas en el flujo de trabajo colaborativo.
5. **Flujo de ramas y Pull Request:** Implementación de rama de característica, apertura de Pull Request descriptivo y fusión (*merge*) a la rama base.

### Evidencias de ejecución

* **Captura del historial de ramas y confirmaciones (`git log --oneline --graph --all`):**  
  `evidencias/git/git-log-graph.png`

* **Captura del Pull Request fusionado (Merged):**  
  `evidencias/git/pr-fusionado.png`
