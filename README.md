#
Mo![co2](https://github.com/user-attachments/assets/db3c1836-9f66-488e-92cd-1f1344bd7c1c)
vilidad-Urbana
Proyecto de Data Analysis con Python, Pandas, Seaborn y Matplotlib.

Este repositorio contiene un análisis completo que explora la relación entre movilidad urbana y productividad económica en ciudades latinoamericanas, utilizando datos reales provenientes de TomTom Traffic Index y OECD Cities. El objetivo principal es identificar patrones que permitan evaluar en qué ciudades conviene invertir en infraestructura de transporte para mejorar la eficiencia urbana y el desarrollo económico.

Contenido del proyecto.

1. Carga y exploración inicial de datos
Se importan los datasets originales y se realiza una inspección preliminar para entender su estructura, tipos de datos y posibles inconsistencias.
Incluye:

  Revisión con .head() y .info()
  Identificación de columnas problemáticas
  Detección de valores nulos o formatos incorrectos

2. Limpieza y preparación de datos
Ambos datasets requieren transformaciones para poder ser analizados correctamente.
Se realizan tareas como:

  Estandarización de nombres de columnas a snake_case
  Conversión de fechas a datetime
  Limpieza de valores numéricos con separadores europeos (coma y punto)
  Conversión de porcentajes y valores monetarios a float
  Creación de nuevas columnas derivadas (ej. población total)

3. Filtrado temporal y extracción de año
Para asegurar un análisis consistente, se extrae el año de los registros de tráfico y se filtra únicamente la información correspondiente a 2024, generando datasets limpios y comparables.

4. Agregación y resumen de movilidad urbana
El dataset de tráfico contiene múltiples registros por ciudad.
Se calculan promedios anuales por ciudad para métricas clave como:

  jams_delay
  traffic_index_live
  jams_length_kms
  mins_delay
  Tiempos de viaje promedio

Esto permite obtener una visión consolidada del comportamiento del tráfico en cada ciudad.

5. Unión de movilidad y economía
Se combinan ambos datasets mediante un inner join usando city y year como llaves.
El resultado es un dataset final que integra:

  Indicadores de congestión
  PIB per cápita
  Desempleo
  Contaminación (PM2.5)
  Población total

6. Visualización y análisis exploratorio
Se generan gráficos para identificar patrones y relaciones entre movilidad y economía:

Boxplot de congestión (jams_delay)

Histograma de PIB per cápita

Comparaciones visuales entre indicadores

Estas visualizaciones permiten detectar valores extremos, tendencias y posibles correlaciones entre tráfico y desarrollo económico.

🎯 Resultados clave
Ciudad con mayor congestión promedio en 2024: Ciudad de México, superando incluso a Tokio, Nueva York y Londres.
Se observan diferencias significativas entre ciudades, lo que sugiere que la congestión no depende únicamente del PIB per cápita.
Algunas ciudades con alto PIB muestran congestión moderada, mientras que otras con PIB medio presentan niveles críticos de tráfico.

🚀 Tecnologías utilizadas
  Python 3
  Pandas
  NumPy
  Seaborn
  Matplotlib
  Jupyter Notebook
