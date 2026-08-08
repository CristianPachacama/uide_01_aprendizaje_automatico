# Reto

## Modelado Predictivo para Riesgo Crediticio

 

### Objetivo y alcance del reto

El estudiante deberá desarrollar un pipeline analítico y predictivo funcional para evaluar el riesgo de los clientes de la institución. Aplicará técnicas de limpieza de datos, exploración visual de variables y construirá modelos de aprendizaje supervisado (regresión y clasificación) para justificar decisiones financieras responsables.

 

### Modalidad del entregable

Notebook (ipynb). Esta modalidad interactiva permite integrar el código en Python, las visualizaciones y la justificación narrativa de las decisiones de modelado en un solo documento. El notebook favorece la reproducibilidad del razonamiento analítico, la implementación técnica de los algoritmos y la comunicación profesional con actores técnicos y directivos.

 

## Prueba práctica

Elabore un Notebook estructurado como un diagnóstico preliminar y motor predictivo para María Fernanda y el comité directivo de Crédito Andino Digital. Para este ejercicio, utilice un conjunto de datos público de riesgo crediticio (dataset).

El desarrollo debe contener las siguientes fases:

1. **Preparación de Datos**: Inicie con la definición de la unidad de análisis recomendada, justificando si cada fila debe representar un cliente único o una solicitud de crédito. Ejecute las tareas de limpieza requeridas: tratamiento de duplicados, imputación de valores faltantes, codificación de variables categóricas y prevención de fugas de información.
2. **Exploración Visual y Diagnóstico**: Identifique y clasifique todas las variables (discretas, continuas, ordinales o categóricas). Proponga al menos cinco visualizaciones exploratorias adecuadas, indicando qué patrón, asimetría, desbalanceo de clases o riesgo de negocio permite observar cada una de ellas antes de pasar al modelado.
3. **Modelado Supervisado**: Entrene y evalúe dos algoritmos predictivos:
    * **Modelo de Regresión**: Para predecir una variable continua (ej. estimar ingresos, monto esperado de atraso o el límite de crédito recomendado).
    * **Modelo de Clasificación**: Para la toma de decisiones binarias (ej. predecir si un cliente incurrirá en mora o no).
4. **Evaluación de Modelos y Recomendación Ejecutiva**: Calcule las medidas de desempeño generales para ambos modelos entrenados. Basándose en estos resultados, redacte una conclusión estratégica para el comité directivo. Justifique si la institución debería utilizar un umbral de clasificación estricto para minimizar riesgos, o un umbral más flexible para priorizar la inclusión financiera y el acompañamiento preventivo. El notebook debe evidenciar de forma clara y auditable que el aprendizaje automático requiere transformar datos en evidencia confiable antes de automatizar decisiones operativas.
