# Análisis de Encuesta de Calidad de Aerolínea Comercial con Apache Spark

Este repositorio contiene una serie de notebooks de Databricks desarrollados para analizar un archivo `.csv` que contiene datos del resultado de una encuesta de calidad en una aerolínea comercial. Los notebooks utilizan distintas capacidades de Apache Spark para procesar y analizar estos datos, desde operaciones básicas con RDDs hasta análisis avanzados con DataFrames, Machine Learning y datos en streaming.

## Notebooks en el Repositorio

### 1. Encuesta_Aerolinea_RDD

Este notebook utiliza Resilient Distributed Datasets (RDDs) para analizar el archivo csv de la encuesta. Se enfoca en responder preguntas específicas como el número de personas que consideran el sistema de reservas online satisfactorio (con una puntuación igual o superior a 3 y el número de observaciones para el vuelo de mayor distancia. Además, incluye filtrados por tipo de cliente ("Loyal Customer") y ordena los resultados por la distancia de vuelo de manera descendente.

### 2. Encuesta_Aerolinea_DataFrame

Basándose en los resultados y métricas del primer notebook, este segundo análisis utiliza Spark DataFrames para lograr resultados similares con una interfaz más estructurada y potente. Selecciona observaciones por género, edad y clase, y ordena por edad de manera ascendente. También filtra por tipo de viaje, clase y distancias de vuelo mayores a 1.000 kilómetros, además de considerar las valoraciones del servicio a bordo. Se emplean consultas SQL a través de `spark.sql` para responder a preguntas específicas.

### 3. Encuesta_Aerolinea_MLlib

Este notebook introduce el uso de MLlib para crear un modelo de Regresión Logística que clasifique la satisfacción del cliente. El proceso incluye la extracción y limpieza de datos, conversión de columnas categóricas, ensamblaje de características, entrenamiento del modelo, y evaluación de precisión. Se introduce la posibilidad de visualizar la curva ROC con la librería handyspark.

### 4. ML para Datos en Streaming

Finalmente, este notebook demuestra un flujo de trabajo completo de ciencia de datos para datos en streaming, implementando y evaluando un modelo de Machine Learning (Regresión Logística) para clasificar datos en tiempo real. Se detalla la preparación del modelo, la división de datos para simular streaming, la configuración de la fuente de streaming, implementación de consultas en tiempo real, y la evaluación de la precisión del modelo en este contexto.

## Objetivo General

El objetivo de estos notebooks es demostrar la flexibilidad y potencia de Apache Spark para el análisis de datos complejos, desde la manipulación básica de datos hasta técnicas avanzadas de análisis en streaming y machine learning. Los notebooks están diseñados para proporcionar una comprensión clara de cómo se pueden aplicar estas herramientas en un escenario de análisis de datos real, específicamente para evaluar la calidad del servicio de una aerolínea comercial a través de encuestas de satisfacción.

## Uso

Para utilizar estos notebooks, clone este repositorio en su entorno Databricks y siga las instrucciones específicas en cada notebook para la instalación de dependencias y configuración de entorno necesarias.
