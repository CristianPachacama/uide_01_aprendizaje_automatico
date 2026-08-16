# Reto

## Diseño e implementación de un sistema analítico responsable

 
## Objetivo y alcance del reto

El estudiante deberá desarrollar un pipeline analítico en código que combine segmentación no supervisada (clustering), reducción dimensional (PCA y t-SNE), validación cruzada, control del overfitting, entrenamiento de modelos (XGBoost) e interpretabilidad estadística. El objetivo es crear una herramienta técnica que apoye las decisiones institucionales de retención estudiantil sin comprometer la generalización, la transparencia ni la protección de los datos.

 

## Modalidad del entregable

Notebook (.ipynb). Esta modalidad interactiva permite integrar la ejecución de código en Python, las visualizaciones de los datos y la justificación narrativa (mediante celdas de Markdown). 

 

## Prueba práctica

Elabore un Notebook estructurado como una propuesta técnica y analítica para María Fernanda y el comité directivo de la Universidad Andina Digital. Utilice los datos Open University Learning Analytics Dataset (OULAD) ([dataset](https://www.kaggle.com/datasets/anlgrbz/student-demographics-online-education-dataoulad/data)).

El desarrollo debe contener las siguientes cinco fases integrando código y celdas de texto explicativas:

1. **Análisis Exploratorio y Clustering:** Defina qué variables utilizará para segmentar a los estudiantes. Aplique el preprocesamiento necesario (estandarización de escalas, manejo de valores faltantes y outliers) y ejecute un algoritmo de clustering (como K-means, jerárquico o DBSCAN). Evalúe matemáticamente la calidad de los agrupamientos (ej. Coeficiente de Silhouette).
2. **Reducción Dimensional (PCA y t-SNE):** Implemente PCA para condensar las variables de intensidad de uso y analice la varianza explicada por los primeros componentes. Luego, aplique t-SNE para visualizar los agrupamientos de estudiantes en dos dimensiones.
3. **Estrategia de Validación y Prevención de Fugas de Información:** Configure las particiones de datos (entrenamiento y prueba), respetando la temporalidad de las cohortes si los datos lo permiten. Establezca un flujo con validación cruzada (cross-validation) para la selección de hiperparámetros.
4. **Modelado Predictivo y Optimización (XGBoost):** Entrene un modelo predictivo base (ej. Árbol de Decisión) y compárelo frente a un modelo XGBoost. Configure hiperparámetros clave, aplique técnicas de regularización, subsampling y parada temprana (early stopping).
5. **Interpretabilidad Estadística y Recomendación Ejecutiva:** Aplique técnicas de interpretabilidad sobre el modelo XGBoost (como importancia de variables o valores SHAP) para extraer explicaciones tanto globales (qué afecta a toda la universidad) como locales (qué afecta a un estudiante específico).
6. **Maestro:** Para construir el conjunto de datos definitivo que alimentará todas las fases del reto, el proceso de integración debe estructurarse utilizando siempre la llave compuesta de Estudiante, Módulo y Semestre (id_student, code_module, code_presentation) para mantener la granularidad correcta. Primero, se debe cruzar el registro de interacciones (studentVle.csv) con el catálogo de recursos (vle.csv) para pivotar los datos y obtener la suma de clics separados por tipo de actividad (ej. foros, cuestionarios, recursos). Segundo, se debe enlazar el historial de notas (studentAssessment.csv) con la tabla maestra de evaluaciones (assessments.csv), permitiendo calcular el promedio de calificaciones y los días de retraso en las entregas. Tercero, estas dos tablas previamente agregadas deben unirse a la base demográfica (studentInfo.csv), la cual aporta el contexto categórico (edad, nivel socioeconómico, intentos previos) y la variable objetivo (final_result). Finalmente, el flujo concluye binarizando la variable objetivo para perfilar el abandono ("Withdrawn" = 1) y gestionando los valores nulos generados tras los cruces (ej. imputando ceros a estudiantes sin clics registrados), consolidando así un único DataFrame robusto y listo para el preprocesamiento analítico.

