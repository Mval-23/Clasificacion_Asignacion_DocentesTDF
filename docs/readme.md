![Alt text](image.png)
## TECNICATURA SUPERIOR EN CIENCIA DE DATOS E INTELIGENCIA ARTIFICIAL
## APRENDIZAJE AUTOMATICO

# INFORME FINAL
# Proyecto de Aprendizaje Automático:  Clasificación y Asignación de Docentes con Aprendizaje Automático

Este proyecto aplica técnicas de aprendizaje automático para automatizar la clasificación de docentes aspirantes en el nivel secundario, con el objetivo de mejorar la eficiencia, transparencia y equidad en los procesos de asignación docente.

## Autora
**Demari Monica Valeria**  
Profesor: Lic. Martin Mirabete

## Objetivo del Proyecto

Desarrollar un modelo de Aprendizaje Automático capaz de predecir la **clasificación docente** en tres categorías:

- **Docente**
- **Habilitante**
- **Supletorio**

Basándose en los siguientes atributos:
- Título del aspirante
- Nombre de la casa de estudio y provincia
- Espacio curricular 

## Origen de los Datos

Los datos fueron provistos por la Junta de Clasificación y Disciplina de Educación Secundaria de Río Grande, Tierra del Fuego, AeIAS, con previa autorización de la Secretaria de Gestión Educativa, Prof. Silvina Solohaga. Se trabajó sobre un dataset procesado con atributos extraídos del sistema de inscripción docente.

## Dataset

**Nombre del archivo**: `dataset_jcyd_ok.xlsx`  
**Cantidad de registros**: 52.936  
**Columnas**: 16  
**Fuente**: Junta de Clasificación, ciudad de Río Grande.  
**Adquisición**: Mediante autorización oficial (ver informe en PDF).


## Contenido del Repositorio
| Carpeta                       | Archivo                                                   | Descripción                                                 |
|-------------------------------|-----------------------------------------------------------|-------------------------------------------------------------|
|    Data                       | `Readme`                                                  | Estructura de la carpeta "data"                             |
|    Data/Raw                   | `dataset_jcyd_ok.xlsx`                                    | Dataset original                                            |
|    Data/processed             | `dataset_docentes_etl.csv`                                | Dataset procesado                                           |  
|    docs                       | `README.md`                                               | Enlace del video                                            |
|    docs/docs                  | `README.md`                                               | Informe final                                               |
|    docs/docs                  | `A-FORO -Dominios de interés para el parcial.pdf`         | Documento PDF informado en Foro del campus                  |
|    docs/docs                  | `B-Entrega 1- Descripción y Formulación del Objetivo.pdf` | Documento PDF presentado en el campus                       |
|    docs/docs                  | `C-Entrega 2- Descripción del Dataset y Origen.pdf`       | Documento PDF ipresentado en el campus                      |
|    docs/docs                  | `README_Entrega_2.md `                                    | Descripción del Dataset y Origen                            |
|    noteooks                   | `Readme`                                                  | Estructura de la carpeta "notebook"                         |
|    noteooks                   | `1-Descripción del dataset.ipynb`                         | Acceso y descripción completa del dataset                   |
|    noteooks                   | `2-Limpieza y Tratamiento de Datos .ipynb`                | Proceso ETL                                                 |
|    noteooks                   | `3-Modelo_Regresion_Logistica.ipynb`                      | Notebook con modelo de Regresion Logística y visualizaciones|
|    noteooks                   | `4-Arbol_Decision.ipynb`                                  | Notebook con modelo de árbol de decisión                    |
|    noteooks                   | `5-Modelo_Random_Forest.ipynb`                            | Notebook con modelo Random forest                           |
|    noteooks                   | `6-Regresion_Logistica_Por_Espacio_Poco_Dato .ipynb`      | Notebook de regresión aplicada a espacios con pocos datos   |


## Análisis Exploratorio (EDA)

Se identificaron 3 clases en la variable objetivo:

- Docente (D): 13.297 registros

- Habilitante (H): 20.355 registros

- Supletorio (S): 19.284 registros

Se analizaron:

Los espacios curriculares: 468 únicos, siendo el más frecuente “Preceptor/a”.

Los títulos únicos: 2.375, el más común fue “Profesor/a de Educación Física”.

Las casas de estudio: múltiples provincias, con una importante cantidad de valores faltantes (notablemente en columnas como facultad, provincia, ciudad).

Se realizaron visualizaciones de:

Distribución de la variable objetivo.

Frecuencias de los espacios curriculares y títulos.

Mapas de calor para detección de valores nulos.


## Modelos de Aprendizaje Automático desarrollados

Se implementaron y compararon tres modelos principales:
- Regresión Logística Multiclase
- Árbol de Decisión
- Random Forest
- 
**Entrenamiento/Test:** División 80/20 con estratificación.
**Preprocesamiento:** One-Hot Encoding para variables categóricas.



## Métricas de Evaluación 

| Modelo              | Precisión | Recall | F1-Score | Accuracy |
| ------------------- | --------- | ------ | -------- | -------- |
| Regresión Logística | 0.79      | 0.78   | 0.78     | 0.78     |
| Árbol de Decisión   | 0.74      | 0.73   | 0.73     | 0.73     |
| Random Forest       | 0.83      | 0.82   | 0.82     | 0.82     |



## Interpretación de Resultados y Conclusiones

- El modelo Random Forest ofreció el mejor desempeño general, siendo capaz de predecir adecuadamente las tres categorías.

- Se evidenció una alta correlación entre título, institución y el carácter docente asignado.

- La versión especializada de regresión logística por espacio con pocos datos permitió mantener una buena tasa de predicción incluso en condiciones de escasez de datos, sin embargo esto nos indica la falta de aspirantes para cubrir dichos espacios y/o cargos.


## Conclusión Final
El modelo desarrollado cumple el objetivo general de automatizar y optimizar la clasificación docente. El sistema podría aplicarse para asistir a la Junta de Clasificación, reducir errores humanos, y acelerar los procesos. 



