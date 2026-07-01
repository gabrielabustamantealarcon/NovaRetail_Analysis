# NovaRetail_Analysis
Explorando drivers de comportamiento en NovaRetail+ Análisis avanzado de correlaciones para identificar factores clave del ingreso anual
🎯 Objetivo del Proyecto

El propósito central es entender qué factores del comportamiento del cliente están más fuertemente asociados con el ingreso anual generado. A través de este análisis, se busca:
* **Identificar patrones de comportamiento:** Evaluar las interacciones y dinámicas de los usuarios dentro de la plataforma.
* **Descubrir relaciones significativas:** Determinar mediante técnicas estadísticas qué variables impactan o coinciden en mayor medida con el rendimiento económico de la empresa.
* **Detección de correlaciones engañosas:** Aislar factores que simulan una causalidad aparente pero carecen de consistencia estadística o lógica de negocio.
* **Optimización y Recomendación:** Convertir hallazgos analíticos en recomendaciones responsables de negocio para guiar las iniciativas de retención y crecimiento.

📊 Datasets Utilizados

El análisis se basa en el procesamiento de la siguiente fuente de datos integrada:
* `novaretail_comportamiento_clientes_2024.csv`: Registro unificado que concentra los atributos demográficos, métricas de interacción en la plataforma y el volumen de transacciones e ingresos anuales correspondientes a cada cliente evaluado durante el periodo de cierre de 2024.

🛠️ Herramientas Utilizadas

El entorno de desarrollo y las librerías seleccionadas para garantizar el rigor metodológico del análisis son:
* **Jupyter Notebook** como entorno de desarrollo.
* **Python** y sus librerías especializadas: `pandas`, `numpy`, `seaborn`, `matplotlib`.

🚀 Etapas del Análisis

El proyecto sigue un flujo de trabajo estructurado para garantizar la integridad de los resultados y una interpretación de resultados altamente profesional:

| Paso | Acción | Resultado esperado |
| :---: | :--- | :--- |
| **1** | Cargar y explorar el dataset | Entender estructura, columnas, tipos de datos y métricas clave iniciales. |
| **2** | Preparar datos y documentar supuestos | Datos sin errores y listos para el reporte. Definición de variables relevantes y reglas del análisis. |
| **3** | Visualizar relaciones iniciales | Uso de Heatmaps para patrones globales y Scatterplots para relaciones específicas. |
| **4** | Calcular correlaciones adecuadas | Aplicación matemática de Pearson/Spearman, Punto biserial y V de Cramér según corresponda. |
| **5** | Interpretar resultados | Transformación de la evidencia en una interpretación responsable e implicación de negocio. |
| **6** | Limitaciones y próximos pasos | Delimitación de qué no se puede concluir a partir del análisis actual + propuesta de qué hacer después. |
