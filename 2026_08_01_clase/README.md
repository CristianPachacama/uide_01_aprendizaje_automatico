# Objetivo y alcance del reto

El estudiante deberá diseñar y ejecutar una propuesta de análisis preliminar respaldada por código en Python para evaluar si los datos institucionales pueden sustentar un modelo de alerta temprana. Aplicará curaduría de datos, exploración visual avanzada, identificación de variables aleatorias y análisis matricial de esperanza, varianza y covarianza en NumPy y Pandas para justificar decisiones de modelado responsable.

 

# Modalidad del entregable

Formato técnico-práctico (Notebook / Script en Python). Esta modalidad permite documentar decisiones mediante código reproducible en NumPy y Pandas, redactar la formulación matemática explícita, describir riesgos de interpretación y presentar una propuesta metodológica verificable. El formato favorece la trazabilidad del razonamiento analítico, la ingeniería de datos previa y la comunicación profesional con actores técnicos y directivos.

 

# Prueba práctica

A partir de un Dataset.ipynbDescargar Dataset.ipynb, elabore un informe técnico en Jupyter Notebook para María Fernanda y la Universidad Andina del Pacífico resolviendo los siguientes puntos prácticos:

1. **Definición de Unidad de Análisis e Ingesta:** Defina la unidad de análisis (estudiante-semestre o estudiante-asignatura) y ejecute en Pandas el código de agregación necesario para estructurar la tabla final.
2. **Curaduría y Control de Data Leakage:** Trate programáticamente duplicados, nulos y tipos de datos. Implemente un filtro explícito por ventana temporal (<= Semana 8) que detecte y elimine automáticamente variables futuras (data leakage).
3. **Clasificación y Encoding:** Clasifique 8 variables del dataset (discretas, continuas, ordinales, binarias) y aplique la estrategia adecuada de codificación (encoding) en Python.
4. **Visualización Exploratoria:** Genere 5 gráficos en Matplotlib/Seaborn (distribuciones estratificadas y matriz de correlación) que permitan identificar patrones y posibles sesgos en los datos.
5. **Análisis Estadístico Matricial:** Utilizando NumPy, calcule la esperanza, varianza y matriz de covarianza de los indicadores. Evalúe si la variabilidad entre sedes evidencia heterocedasticidad.
6. **Recomendación Ejecutiva:** Redacte una conclusión técnica y ética breve justificando si la universidad debe proceder con el modelado predictivo o completar primero la fase de diagnóstico de datos.