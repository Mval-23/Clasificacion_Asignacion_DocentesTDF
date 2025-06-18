# Proyecto de Aprendizaje Automático: Clasificación de Docentes

Este proyecto aplica técnicas de aprendizaje automático para automatizar la clasificación de docentes aspirantes en el nivel secundario, con el objetivo de mejorar la eficiencia, transparencia y equidad en los procesos de asignación docente.



## Descripción General

El sistema predice la clasificación de un aspirante en una de las siguientes categorías:

- **Docente**
- **Habilitante**
- **Supletorio**

Basándose en los siguientes atributos:
- Título del aspirante
- Nombre de la casa de estudio y provincia
- Espacio curricular 

##  Origen de los Datos

Los datos fueron provistos por la Junta de Clasificación y Disciplina de Educación Secundaria de Río Grande, Tierra del Fuego, AeIAS, con previa autorización de la Secretaria de Gestión Educativa, Prof. Silvina Solohaga. Se trabajó sobre un dataset procesado con atributos extraídos del sistema de inscripción docente.


## Análisis Exploratorio (EDA)

Se realizaron:
- Gráficos de distribución de clases
- Conteo de los títulos más frecuentes
- Exploración de relaciones entre títulos y espacios curriculares

**Conclusiones:**
- Alta concentración en ciertos títulos (Ej: Profesor en Lengua, Matemática)
- Supletorios presentan mayor variedad de títulos y asignaciones



## Modelos Desarrollados

Se probaron los siguientes modelos:
- Regresión Logística Multinomial
- Árbol de Decisión
- Random Forest
- 
**Entrenamiento/Test:** División 80/20 con estratificación.
**Preprocesamiento:** One-Hot Encoding para variables categóricas.



## Métricas de Evaluación (Random Forest)

| Clase        | Precisión | Recall | F1-score |
|--------------|-----------|--------|----------|
| Docente      | 0.86      | 0.90   | 0.88     |
| Habilitante  | 0.86      | 0.85   | 0.85     |
| Supletorio   | 0.77      | 0.74   | 0.75     |

- **Accuracy general:** 84%
- Se observó mayor dificultad en predecir "Supletorios", confundidos con "Habilitantes".



## Conclusiones Finales

- El modelo logra automatizar la clasificación con alto nivel de precisión.
- Random Forest fue el más efectivo para este problema.
- Se recomienda incorporar más variables (puntaje, antigüedad) para afinar la clasificación.
- El sistema puede usarse como herramienta de apoyo para la Junta de Clasificación.

---

## Contenido del Repositorio " Clasificacion_Asignacion_DocentesTDF"

| Carpeta del Cookecuter              | Archivo                             | Descripción                                                 |
|-------------------------------------|-------------------------------------|-------------------------------------------------------------|
|    Data                             | `Readme`                            | Estructura de la carpeta "data"                             |
|    Data/Raw                         | `dataset_jcyd_ok.xlsx`              | Dataset original                                            |
|    Data/processed                   | `dataset_docentes_etl.csv`          | Dataset procesado                                           |
|    docs                             | `README.md`                         | Este archivo                                                                     |
|    docs                             | `dataset_docentes_etl.csv`          | Dataset procesado                                           |
|    docs                             | `dataset_docentes_etl.csv`          | Dataset procesado                                           |
|    docs                             | `dataset_docentes_etl.csv`          | Dataset procesado                                           |
|    docs                             | `dataset_docentes_etl.csv`          | Dataset procesado                                           |
|    docs                             | `dataset_docentes_etl.csv`          | Dataset procesado                                           |
|                                     | `modelo_final.ipynb`                | Notebook con modelo principal y visualizaciones             |
|                                    Data/Rawl_Decision.ipynb`              | Notebook con modelo de árbol de decisión                    |
|                                     | `Regresion_Logistica_Por_Espacio...`| Notebook de regresión aplicada a espacios con pocos datos   |
|                                     | `video_explica_modelo.mp4`          | Video de presentación del proyecto                          |
|                                     | `README.md`                         | Este archivo                                                |

---

## 🚀 Recomendaciones Futuras

- Implementar optimización de hiperparámetros.
- Agregar interpretabilidad del modelo (ej: SHAP).
- Construir dashboard interactivo para uso institucional.

---

> Realizado por: **Demari Monica Valeria**

> Tecnicatura Superior en Ciencia de Datos e Inteligencia Artificial

> Profesor: **Lic. Martin Mirabete**

