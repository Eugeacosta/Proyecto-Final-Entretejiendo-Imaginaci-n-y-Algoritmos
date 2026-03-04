# LogiGen AI: Framework de Prompting para la Gestión de SLAs y Visualización Logística

**Autor:** María Eugenia Acosta | Data Analytics & Insights Jr.
**Curso:** Inteligencia Artificial: Generación de Prompts (Diplomatura)

## 1. Resumen
LogiGen AI es una Prueba de Concepto (POC) basada en Inteligencia Artificial diseñada para automatizar la interpretación de métricas de logística inversa. El proyecto traduce datos técnicos de rendimiento (KPIs extraídos mediante SQL/Python) en diagnósticos ejecutivos en lenguaje natural. Además, incluye una interfaz gráfica interactiva (UI) y aprovecha tres tipos de modelos generativos (Texto-a-Texto, Texto-a-Imagen y Texto-a-Audio) para crear un sistema integral de alertas operativas sobre el cumplimiento de SLAs.

## 2. Introducción
* **Presentación del Problema:** Existe una brecha de comunicación entre los datos técnicos de logística y la toma de decisiones gerencial sobre el cumplimiento de SLAs. En operaciones de gran volumen, identificar por qué un indicador de "Retiros Delay" aumentó es un proceso lento que requiere cruzar calendarios de días hábiles, feriados y motivos de visita.
* **Relevancia y Propuesta de Solución:** Una solución de IA optimiza esta traducción de datos a lenguaje natural, permitiendo respuestas rápidas y visualmente claras. La solución se vincula directamente a la capacidad de los modelos de IA para actuar como traductores de contexto y generadores de activos visuales.

## 3. Objetivos
* Desarrollar una herramienta funcional que asista en el análisis de SLAs logísticos de retiros de equipos para operaciones de logística inversa.
* Optimizar el consumo de tokens y costos de API mediante el envío de datos pre-calculados (Fast Prompting).
* Implementar una interfaz de usuario accesible para líderes operativos sin conocimientos de programación.
* Generar activos visuales y sonoros que faciliten la comunicación de alertas críticas.

## 4. Metodología
El proyecto se desarrolló en una Jupyter Notebook (Google Colab) estructurado en las siguientes fases:
1. **Extracción y Agregación:** Simulación de extracción de datos transaccionales mediante SQL para obtener métricas agregadas (volumen, estado, provincia).
2. **Etapa Texto-a-Texto ("The Logistics Consultant Prompt"):** Implementación de un prompt con la técnica Role-Play y Delimitadores (###) para aislar los datos crudos de las instrucciones, transformando las métricas en reportes de "Causa-Raíz".
3. **Etapa Texto-a-Imagen ("The KPI Visualizer"):** Generación de material de soporte visual mediante prompts descriptivos con parámetros de estilo (estilo corporativo 3D, mapa de calor).
4. **Etapa Texto-a-Audio:** Conversión del diagnóstico gerencial en una alerta de voz automatizada.
5. **Despliegue de UI:** Integración de los modelos en una aplicación web interactiva.

## 5. Herramientas y Tecnologías
* **Python & SQL:** Para la orquestación y estructuración previa de los datos.
* **Modelo Texto-a-Texto (Google Gemini 2.5 Flash):** Seleccionado por su alta velocidad de inferencia, ideal para integraciones en tiempo real.
* **Modelo Texto-a-Audio (gTTS):** Para generar alertas operativas sonoras de forma nativa.
* **Generación de Imagen:** Para conceptualizar un mapa de calor isométrico 3D de la red logística.
* **Gradio:** Framework elegido para desplegar la interfaz gráfica de usuario (UI), permitiendo la interacción directa con el modelo sin necesidad de código adicional.

## 6. Justificación de la Viabilidad
**Viabilidad Técnica:** El proyecto es altamente factible al utilizar modelos de IA preexistentes y no requerir infraestructura compleja. El alcance está limitado a la interpretación de métricas conocidas y depuradas, asegurando que los resultados sean verificables. Al inyectar resúmenes estadísticos agregados en lugar de bases de datos crudas, la solución maximiza la eficiencia y es económicamente escalable.

## 7. Resultados
La implementación generó con éxito un entorno web funcional. Al ingresar el volumen semanal de retiros, el modelo identificó correctamente los cuellos de botella geográficos, devolviendo un reporte en formato semáforo. Simultáneamente, el sistema sintetizó el diagnóstico principal en un archivo de audio MP3 reproducible.


### Visualización del SLA (Mapa de Calor)
![Mapa de Calor de la Red Logística](<img width="2816" height="1536" alt="Gemini_Generated_Image_yo3d0lyo3d0lyo3d" src="https://github.com/user-attachments/assets/2482a55b-2191-49d0-92b8-6e8e0b2c4e0a" />
.jpg)


### Interfaz de Usuario Generada
https://jumpshare.com/share/HD3dzie0x6CAuqGknZMF

## 8. Conclusiones
* **Fast Prompting Efectivo:** El uso estricto de roles ("Senior Data Analyst") y delimitadores (`###`) eliminó las alucinaciones del modelo, garantizando diagnósticos precisos y orientados al negocio.
* **Escalabilidad:** Al dividir el análisis de datos duros (SQL) de la interpretación contextual (IA), se logró un producto robusto y muy económico de mantener.
* **Accesibilidad:** La interfaz con Gradio y la alerta de voz demostraron que la IA puede integrarse sin fricción en la rutina diaria, democratizando el acceso a los insights operativos.
