# 🛍️ NovaRetail+: Atribución de Ingresos y Optimización del Inversión Publicitaria

> **Enfoque de Negocio:** Análisis estadístico avanzado de correlaciones para identificar los verdaderos *drivers* del ingreso anual, evaluar la eficiencia del gasto publicitario y prevenir decisiones fallidas basadas en falsas causalidades.

---

## 💼 Problema de Negocio

En el sector de *E-commerce* y *Retail*, **NovaRetail+** busca optimizar su estrategia de retención y asignación de presupuesto comercial. El equipo directivo enfrenta dos interrogantes operativas clave:
1. **Atribución de Ingresos:** ¿Qué comportamientos o atributos del cliente realmente impulsan el rendimiento económico anual de la empresa (ingreso anual) frente a métricas superficiales o de vanidad?
2. **Ineficiencia en Marketing Directo:** Se destina presupuesto a pautas publicitarias personalizadas bajo el supuesto de que "a mayor gasto publicitario, más visitas y compras". Sin embargo, existe incertidumbre sobre si la pauta genera tráfico real o si se está invirtiendo de manera heterogénea en clientes que igual consumirían la plataforma de forma orgánica.

**Pregunta Estratégica:** ¿Cómo podemos priorizar los canales de impacto económico real e identificar ineficiencias en la inversión publicitaria mediante rigor cuantitativo?

---

## 🎯 Objetivos de la Investigación

* **Identificación de Drivers Económicos Clave:** Evaluar mediante métricas paramétricas y no paramétricas las variables con mayor asociación al ingreso anual.
* **Evaluación de Eficiencia Publicitaria:** Analizar la relación entre la inversión en publicidad dirigida y las métricas de tráfico (*Visitas/Mes*).
* **Detección de Falsas Causalidades:** Desmitificar supuestos de negocio y aislar variables sin consistencia estadística (ej. impacto directo de suscripciones *Premium* o atributos aislados).
* **Fundamentación de Experimentos Comerciales:** Traducir las correlaciones en iniciativas de optimización de presupuesto de marketing y pruebas A/B.

---

## 📊 Arquitectura de Datos

El análisis se basó en el procesamiento de un dataset unificado de cierre operativo:

* `novaretail_comportamiento_clientes_2024.csv`: Registros integrados del periodo **2024** que abarcan atributos demográficos, interacciones en la plataforma, suscripciones, gasto publicitario asignado, volumen transaccional e ingresos anuales por cliente.

---

## 🛠️ Metodología y Flujo de Trabajo

| Paso | Fase Técnica | Implementación & Propósito de Negocio |
| :--- | :--- | :--- |
| **1** | **Ingesta y Diagnóstico** | Carga del dataset y exploración de estructuras, tipos de datos y métricas base. |
| **2** | **Gobernanza y Supuestos** | Depuración de errores, validación de variables clave y documentación de supuestos de negocio. |
| **3** | **Exploración Visual** | Uso de *Heatmaps* (patrones globales) y *Scatterplots* para la inspección de distribuciones bilaterales. |
| **4** | **Cálculo de Correlaciones** | Aplicación matemática de **Pearson** (relaciones lineales) y **Spearman** (monotónas), complementadas con *Punto Biserial* y *V de Cramér*. |
| **5** | **Interpretación de Negocio** | Traducción de la evidencia numérico-visual en implicaciones estratégicas de retención y facturación. |
| **6** | **Limitaciones y Roadmap** | Delimitación metodológica de los hallazgos y diseño de próximos pasos experimentales. |

---

## 💻 Stack Tecnológico

* **Entorno de Desarrollo:** Jupyter Notebook
* **Lenguaje:** Python
* **Procesamiento de Datos:** `pandas`, `numpy`
* **Análisis Estadístico:** `scipy.stats`
* **Visualización de Datos:** `seaborn`, `matplotlib`

---

## 📈 Hallazgos Clave & Evidencia Cuantitativa

### 🔹 Hallazgo 1: Las Compras Mensuales son el Driver Exclusivo del Ingreso Anual
* **Evidencia Visual & Numérica:** Alineación casi perfecta en *Scatterplot*. Correlación de Pearson $r = 0.96$ / Spearman $\rho = 0.96$.
* **Interpretación:** Existe una asociación directa y lineal casi absoluta entre la frecuencia de compra mensual y la facturación anual. 
* **Implicación de Negocio:** El ingreso anual depende críticamente del volumen transaccional mensual. Variables como la suscripción a programas *Premium* no mostraron un impacto directo de magnitud similar, confirmando que la conversión mensual debe ser el foco operativo principal.

### 🔹 Hallazgo 2: Ineficiencia y Distribución Heterogénea del Gasto Publicitario
* **Evidencia Visual & Numérica:** Nube de puntos ascendente dispersa. Correlación de Pearson $r = 0.57$ / Spearman $\rho = 0.55$.
* **Interpretación:** Existe una relación moderada entre la inversión publicitaria por cliente y sus visitas mensuales, pero **no demuestra causalidad**.
* **Implicación de Negocio:** Se detectaron ineficiencias claras: existen clientes con alto gasto publicitario asignado que registran pocas visitas, y clientes altamente activos de forma orgánica con mínima asignación de pauta. Reasignar o redistribuir de forma homogénea el presupuesto de marketing puede maximizar el tráfico y, potencialmente, la conversión a compras.

---

## ⚠️ Limitaciones del Estudio

1. **Correlación $\neq$ Causalidad:** Que el gasto publicitario y las visitas varíen juntos no garantiza que la publicidad genere el tráfico. Existen **variables omitidas** no controladas en este corte (ej. temporadas de descuento como *Black Friday*, *CyberMonday*, o campañas de competidores).
2. **Efecto Temporal:** Muestra estática del periodo 2024 que requiere actualización continua dada la volatilidad del mercado de *retail*.

---

## 🚀 Próximos Pasos Recomendados

* **Pruebas y Experimentos Controlados (A/B Testing):** Diseñar un grupo de control (usuarios sin publicidad directa) y un grupo de prueba para evaluar la tasa de incremento real en visitas y compras (*incrementality*).
* **Auditoría de Eficiencia de Pauta:** Revisar la regla de asignación del presupuesto de marketing directo para evitar sobre-invertir en clientes que ya tienen comportamiento recurrente orgánico.
* **Segmentación Multivariable:** Explorar patrones combinando variables demográficas (edad, región, dispositivo) mediante técnicas de *clustering*, ya que de forma aislada no presentaron correlaciones lineales significativas.

---

## 💻 Cómo ejecutar el Notebook
Para visualizar y ejecutar el análisis, se recomienda el uso de **Google Colab** por su facilidad para manejar entornos de Python:

1.  Accede a [https://colab.research.google.com/drive/1HZSxcBO-SCn_WPiViip83faUhyrABily#scrollTo=ezgZAoMNEeRg]
2.  Ejecuta las celdas secuencialmente presionando `Shift + Enter`.

## 🛠️ Guía de Reproducción
Para replicar este análisis en un entorno local:
1.  **Clonar el repositorio** o descargar los archivos fuente.
2.  **Ejecución:** Abre tu editor preferido (Jupyter Notebook, VS Code o PyCharm) y corre el script completo para generar los gráficos y el reporte final.
