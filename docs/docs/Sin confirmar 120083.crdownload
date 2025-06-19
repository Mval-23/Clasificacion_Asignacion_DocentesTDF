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

Los datos fueron provistos por el equipo informático de la Junta de Clasificación y Disciplina de Educación Secundaria de Río Grande, Tierra del Fuego, AeIAS, con previa autorización de la Secretaria de Gestión Educativa, Prof. Silvina Solohaga. Se trabajó sobre un dataset procesado con atributos extraídos del sistema de inscripción docente.

## Dataset

**Nombre del archivo**: `dataset_jcyd_ok.xlsx`  
**Cantidad de registros**: 52.936  
**Columnas**: 16  
**Fuente**: Junta de Clasificación y Disciplina de Educación Secundari, ciudad de Río Grande.  
**Adquisición**: Mediante autorización de la Secretaria de Gestión Educativa.

|Nombre de columna |Entradas|	         Tipo de datos                       |	      Descripción                                                            |
|------------------|--------|------------------------------------------------|----------------|--------------------------------------------------------------|
|idespacio         | 52,936 | tipo entero (int64).                           |	Clave de identidad del Espacio curricular                                    |
|Idtitulo          | 52,936 | tipo objeto (string).                          |	Clave de identidad del Título                                                |
|idtitulo_real     |  52,936| tipo entero (int64).                           |	Clave de identidad del Título según los datos del título y la casa de estudio|
|Idcasaestudio     | 52,936 | tipo objeto (string)                           | Clave de identidad de la casa emisora del título                              |
|Carácter          | 52,936 | tipo objeto (string).                          | Nombre que se clasifican los títulos en el espacio curricular                 |
|idNivel_espacio   | 52,935 | tipo flotante (float64) - una entrada es nula. | Clave de identidad del Nivel del Espacio curricular o cargo                   |
|desc_espacio      | 52,935 | tipo objeto (string) - una entrada es nula.    | Descripción del Cargo o Espacio curricular                                    |
|tipo_espacio      | 52,935 | tipo objeto (string) - una entrada es nula.    | Tipo de cargo o espacio curricular                                            |
|ciudad_espacio	   | 52,935 | tipo flotante (float64) - una entrada es nula. | La ciudad que se encuentra habilitado el cargo o espacio curricular           |
|resolucion_espacio| 52,935 | tipo objeto (string) - una entrada es nula.    | Resolución del plan de estudio del título relacionado al espacio curricular   |
|titulo	           | 52,811 | tipo objeto (string)- 125 entradas son nulas.  |	Nombre del título                                                            |
|resolucion        | 50,811 | tipo objeto (string)-2,125 entradas son nulas. |	Resolución del plan de estudio del título                                    |
|nombre	           | 52,695 | tipo objeto (string)- 241 entradas son nulas.	 |  nombre de la casa de estudio que emitió el título                            |
|facultad          | 14,125 | tipo objeto (string)-38,811 entradas son nulas.|	facultad de la casa de estudio que emitió el título                          |
|provincia	       | 50,367 | tipo objeto (string)- 2,569 entradas son nulas.|	provincia de la casa de estudio que emitió el título                         |
|ciudad	           | 42,042 | tipo objeto (string)-10,894 entradas son nulas.|	ciudad de la casa de estudio que emitió el título                            |




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
  
**Entrenamiento/Test:** División 80/20 con estratificación.

**Preprocesamiento:** One-Hot Encoding para variables categóricas.



## Métricas de Evaluación 

| Modelo              | Precisión | Recall | F1-Score | Accuracy |
| ------------------- | --------- | ------ | -------- | -------- |
| Regresión Logística | 0.88      | 0.85   | 0.75     | 0.84     |
| Árbol de Decisión   | 0.86      | 0.87   | 0.74     | 0.84     |
| Random Forest       | 0.88      | 0.88   | 0.75     | 0.85     |



## Interpretación de Resultados 

- El modelo Random Forest ofreció el mejor desempeño general, siendo capaz de predecir adecuadamente las tres categorías.

- Se evidenció una alta correlación entre título, institución y el carácter docente asignado.
  
- Es el más confiable para ayudar a la Junta a automatizar la clasificación docente.

- La versión especializada de regresión logística por espacio con pocos datos permitió detectar qué espacios curriculares presentan escasez de aspirantes con títulos adecuados. Esto se evidenció al analizar los espacios que contaban con menos de 100 registros: muchos de ellos no tienen suficientes docentes que, según el modelo, puedan ser clasificados como "Docente" o "Habilitante". 


## Conclusión Final
Como conclusión, todos estos notebooks reflejan el proceso completo de Machine Learning: desde el análisis exploratorio y limpieza, hasta la implementación de distintos modelos y la evaluación de sus desempeños.
sin embargo, el modelo Random Forest es el mejor para este problema porque tiene el mejor rendimiento general en las tres clases, y la mayor precisión total. Es el más confiable para ayudar a la Junta a automatizar la clasificación docente. El sistema podría aplicarse para asistir a la Junta de Clasificación, reducir errores humanos, y acelerar los procesos. 
Asimismmo, ante una brecha entre la oferta académica de formación docente y la demanda real del sistema educativo para esos espacios, la aplicación de dichos modelos puede generar alertas y recomendaciones para políticas educativas.



