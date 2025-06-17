![Alt text](image.png)
## TECNICATURA SUPERIOR EN CIENCIA DE DATOS E INTELIGENCIA ARTIFICIAL
## APRENDIZAJE AUTOMATICO
### Profesor Lic. Martin Mirabete
### Alumna: Demari Monica Valeria
# Optimizacion de la Clasificacion y Asignacion de Docentes en Tierra del Fuego utilizando Aprendizaje Automatico

<a target="_blank" href="https://cookiecutter-data-science.drivendata.org/">
    <img src="https://img.shields.io/badge/CCDS-Project%20template-328F97?logo=cookiecutter" />
</a>

El proyecto consiste en optimizar la asignacion y clasificacion de aspirantes inscriptos para ejercer la docencia en el nivel secundario en la educacion secundaria mediante el analisis de datos.
### Desarrollo
 #### 	Descripcion del Proyecto
En este proyecto propongo la implementación de un modelo de aprendizaje automático para optimizar la asignación y clasificación de docentes en el nivel secundario. Ante la creciente disponibilidad de datos y la heterogeneidad en la formación académica de los aspirantes, buscaré automatizar y mejorar la eficacia y equidad de este proceso.
#### •	Objetivo General:
El objetivo central de este proyecto es desarrollar un modelo de aprendizaje automático capaz de automatizar y optimizar el proceso de clasificación de los aspirantes inscriptos para ejercer la docencia en el nivel secundario. La clasificación se realizará en las categorías de "Docente", "Habilitante" y "Suplente", tomando como base los títulos académicos y otros atributos relevantes presentes en el conjunto de datos proporcionado por la Junta de Clasificación de Educación Secundaria, y que a su vez proporcione recomendaciones predictivas sobre el espacio curricular más adecuado para cada docente, en base a su formación académica.
#### • Objetivos Específicos:
•	Predecir la clasificación docente ("Docente", "Habilitante" o "Suplente") según su título, institución emisora y provincia.
•	Determinar qué espacios curriculares son los más apropiados para cada docente.
•	Identificar relaciones y patrones ocultos entre la formación académica y la asignación curricular.
•	Sugerir recomendaciones alternativas de asignación curricular.

#### •	Contexto del problema y su relevancia
Actualmente, el proceso de clasificación de aspirantes para la Junta de Clasificación y Disciplina de Educación Secundaria, crucial para la asignación de espacios curriculares y cargos, se realiza de forma manual. Esto lo hace propenso a errores humanos y consume una considerable cantidad de tiempo y recursos.
A pesar del desarrollo en curso de un sistema de merituación por parte de los referentes informáticos, como estudiante considero una oportunidad significativa para aplicar técnicas de aprendizaje automático a los datos históricos de inscripción. La implementación de un modelo de aprendizaje automático es altamente relevante, ya que una mejor asignación puede determinar:
•	Mayor precisión, es decir que reduce la probabilidad de errores en la clasificación, garantizando una asignación docente más justa y eficiente.
•	Mayor eficiencia: La automatización del proceso acelerará la clasificación de aspirantes, liberando a los miembros de la Junta para otras tareas críticas.
•	Análisis predictivo: El modelo puede generar insights valiosos sobre la demanda de docentes en distintas áreas, facilitando la toma de decisiones estratégicas para la planificación e implementación de nuevas modalidades educativas.

#### •	Tipo de Problema y Modelos de ML
El problema principal es de clasificación: la variable objetivo es caracter, con clases "D" (Docente), "H" (Habilitante), "S" (Supletorio). También puede expandirse a un problema de recomendación (opcional en versiones futuras del proyecto). Para ello, como opción podría usar Modelos de regresion logistica, o Random Forest, como así también SVM (Support Vector Machine).

## Project Organization

```
├── LICENSE            <- Open-source license if one is chosen
├── Makefile           <- Makefile with convenience commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
│
├── docs               <- A default mkdocs project; see www.mkdocs.org for details
│
├── models             <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`.
│
├── pyproject.toml     <- Project configuration file with package metadata for 
│                         Clasificacion_Asignacion_DocentesTDF and configuration for tools like black
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
├── setup.cfg          <- Configuration file for flake8
│
└── Clasificacion_Asignacion_DocentesTDF   <- Source code for use in this project.
    │
    ├── __init__.py             <- Makes Clasificacion_Asignacion_DocentesTDF a Python module
    │
    ├── config.py               <- Store useful variables and configuration
    │
    ├── dataset.py              <- Scripts to download or generate data
    │
    ├── features.py             <- Code to create features for modeling
    │
    ├── modeling                
    │   ├── __init__.py 
    │   ├── predict.py          <- Code to run model inference with trained models          
    │   └── train.py            <- Code to train models
    │
    └── plots.py                <- Code to create visualizations
```

--------

