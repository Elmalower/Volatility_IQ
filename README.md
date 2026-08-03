[README.md](https://github.com/user-attachments/files/30667369/README.md)# Suite Forense - Volatility3 GUI & Vol-IQ-Analys

Este proyecto reúne dos herramientas complementarias pensadas para potenciar el análisis forense de memoria RAM utilizando los artefactos generados por Volatility3. Ambas aplicaciones ofrecen una interfaz gráfica moderna, orientada tanto a analistas forenses profesionales como a estudiantes y entusiastas de la ciberseguridad.

---

## Volatility3 GUI Forense

Volatility3 GUI Forense es una aplicación gráfica que facilita la ejecución y gestión de los plugins de Volatility3 sin necesidad de interactuar con la línea de comandos. Está diseñada para agilizar el análisis de imágenes de memoria y para hacer más accesible todo el potencial de Volatility3 mediante:

- **Selección rápida de imágenes de memoria RAM** (formatos .mem, .raw, .bin, etc).
- **Configuración sencilla** de la ruta de Volatility3 y del sistema operativo analizado.
- **Ejecución de múltiples plugins** categorizados por tipo (procesos, red, archivos, malware, credenciales, etc).
- **Aplicación de filtros avanzados** (por PID, usuario o extensión de archivo) para personalizar el análisis.
- **Extracción de archivos por offset virtual** y movimiento sencillo de los dumps extraídos.
- **Exportación de resultados** en TXT, CSV y HTML, para facilitar la documentación y el reporte de hallazgos.
- **Interfaz intuitiva y visual** con un tema oscuro/morado profesional.

Ideal tanto para laboratorios, investigaciones incidentales como para quienes desean explorar los resultados de Volatility3 sin preocuparse por la complejidad de la terminal.

![WhatsApp Image 2025-06-24 at 15 28 17_6fc9f3c2](https://github.com/user-attachments/assets/0aa256be-a670-4483-ac5e-3d4ba8583b64)

---

## Vol-IQ-Analys

Vol-IQ-Analys va un paso más allá, ofreciendo análisis avanzado, correlación y búsqueda entre múltiples archivos de salida de Volatility3. Está diseñada para escenarios donde se requiere profundizar, comparar y detectar relaciones entre distintos artefactos extraídos de la memoria.

Sus principales capacidades incluyen:

- **Carga simultánea de varios archivos forenses** generados por Volatility3 (por ejemplo, pslist, netscan, cmdline, files).
- **Correlación automática** para encontrar elementos en común (PIDs, nombres, rutas, palabras clave) entre archivos diferentes.
- **Detección avanzada de Indicadores de Compromiso (IoCs)** utilizando listas negras, reglas YARA y playbooks en YAML.
- **Cálculo de RiskScore** y visualización de correlaciones sospechosas para facilitar la priorización de hallazgos.
- **Búsquedas flexibles**: exactas, aproximadas, por nombres de persona o por PID.
- **Análisis de relaciones** entre procesos, archivos y comandos para reconstruir cadenas de ataque o persistencia.
- **Exportación fácil de todos los resultados** en TXT o HTML para informes o documentación.
- **Interfaz visual moderna y profesional**, también en tema oscuro/morado.

Pensada para contextos donde la correlación, el cruce de datos y la búsqueda detallada son clave para llegar a conclusiones forenses sólidas.

### Puntuación de riesgo

Panel que calcula y visualiza un **RiskScore** global a partir de la suma ponderada de hallazgos por categoría (archivos, DLLs, procesos, red, VirusTotal), permitiendo dimensionar de un vistazo la gravedad general del caso analizado.

![Puntuación de Riesgo](screenshots/puntuacion-riesgo.png)

### Metadata del análisis

Resumen ejecutivo del análisis con la fecha en que se ejecutó, el archivo de memoria procesado, sus hashes de integridad (MD5, SHA1, SHA256) y contadores rápidos de procesos, conexiones, módulos y detecciones. Incluye opciones de **exportación y copiado** de la metadata para reportes.

![Metadata del análisis](screenshots/metadata-analisis.png)

### Contexto completo del proceso

Vista de detalle que reconstruye el contexto completo de un proceso: su línea de comandos, proceso padre, procesos hijos y conexiones de red asociadas, con navegación directa entre procesos relacionados para facilitar el seguimiento de cadenas de ejecución.

![Contexto del proceso - conexiones de red](screenshots/contexto-proceso-red.png)
![Contexto del proceso - árbol de procesos](screenshots/contexto-proceso-arbol.png)

### Registro cronológico de procesos

Línea de tiempo de creación y finalización de procesos, con **búsqueda por texto** y **ordenamiento configurable**, además de un resumen con totales que ayuda a reconstruir la secuencia temporal de eventos en el sistema.

![Registro cronológico de procesos](screenshots/registro-cronologico.png)

### Procesos sospechosos y detecciones de VirusTotal

Listado consolidado de hallazgos de interés: procesos marcados como sospechosos por las reglas de análisis y detecciones obtenidas mediante integración con **VirusTotal**, para priorizar rápidamente los elementos que requieren revisión manual.

![Procesos sospechosos y detecciones de VirusTotal](screenshots/procesos-sospechosos-virustotal.png)

### Navegación y tabla de procesos

Interfaz principal con navegación por pestañas (Resumen, Procesos, Red, VirusTotal, IoCs, Árbol, Cronología) y una tabla de procesos con **buscador integrado**, mostrando de forma tabular los datos clave de cada proceso para su exploración.

![Navegación y tabla de procesos](screenshots/navegacion-procesos.png)

---

## Filosofía y estado del proyecto

Ambas herramientas buscan acercar el análisis forense de memoria a más personas, simplificando flujos complejos y haciendo accesibles técnicas avanzadas de correlación y búsqueda. El proyecto está en **fase de desarrollo activo**:
- Se están agregando nuevas funcionalidades y mejorando la experiencia de usuario constantemente.
- Pueden existir cambios frecuentes, ajustes y evoluciones en las capacidades de cada aplicación.

---

by maloweer | 2025

[LinkedIn - Manuel Pérez](https://www.linkedin.com/in/manuel-perez-ba7b432a0)
