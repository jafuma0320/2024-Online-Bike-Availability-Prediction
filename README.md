# Universidad de Barcelona
![Logo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20Saturacion%20de%20bicicleta/Imagen%20Universidad.png)

## Departamento de Matemáticas y Informática

## Facultada de Matemáticas

## Posgrado en DataScience & Machine Learning
![Logo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20Saturacion%20de%20bicicleta/Imagen%20Post-grado.png)
>https://datascience.ub.edu/course/postgraduate-dsml

> Integrantes del proyecto:

1. Inge Ruiz de Azua Ibarra
2. Javier Fuentes Manrique
3. Beatriz Almajano
4. Evelyn Carmona Garcia

# Nombre del Proyecto: 2024-Bike-Availability-Prediction
![Logo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20Saturacion%20de%20bicicleta/Imagen%20Bicicletas.png)

# Descripción del problema  a solucionar

> Los participantes se enfrentaron al reto de desarrollar modelos predictivos para prever la disponibilidad de bicicletas aparcadas en varias estaciones de bicicletas compartidas de Barcelona.
> Las bicicletas compartidas son un medio de transporte muy popular en muchas zonas urbanas, y una predicción precisa de su disponibilidad puede ayudar a los usuarios a planificar sus desplazamientos y minimizar los tiempos de espera.

> Los participantes recibieron un conjunto de datos que incluye datos históricos de uso y disponibilidad de bicicletas.
> A partir de estos datos, los participantes tuvieron que desarrollar modelos capaces de predecir con exactitud la disponibilidad de aparcamientos en distintos momentos y lugares.
> Se animo a los participantes a utilizar en sus modelos información sobre las condiciones meteorológicas y otras características relevantes.

> El reto se evaluo en función de la exactitud de las predicciones resultantes. **Los modelos con mejores resultados serán premiados con un reconocimiento en la clasificación de Kaggle.**
> https://www.kaggle.com/competitions/2024-online-bike-availability-prediction/overview

# Tabla de contenido

# 1. Introducción

**Objetivo del proyecto**

> A. Colocar en práctica todo el conocimiento y herramientas adquiridas durante el post-grado.

> B. Prever la disponibilidad de bicicletas aparcadas en varias estaciones de bicicletas compartidas de Barcelona.

**Alcance del proyecto**

> A. Desarrollar algunos Modelos Predictivos capaces de predecir con exactitud la disponibilidad de aparcamientos en distintos momentos y lugares de Barcelona. Para contestar a la pregunta del problema. (1 Parte del proyecto)
> https://www.kaggle.com/competitions/2024-online-bike-availability-prediction/submissions

> B. Con base en los análisis de las bases de datos entregadas de la primera parte del proyecto, se deberá utilizar algunos modelos de información, tales como (COVID - 19, Bicicletas a Pedal y Motor, Saturación de Bicicletas, condiciones meteorológicas, días festivos, fines de semana, desastres naturales y otras características que a los estudiantes les parezcan relevantes.

**Tecnologías y herramientas utilizadas**

> Se utilizaron las siguientes bases de datos:
  - opendata-ajuntament.barcelona
  - Informacio_Estacions_Bicing
  - metadata_sample_submission_2024
  - sample_submission_2024

> Se utilizaron las siguientes librerías:
  - Google Collab
  - Jupyter Notebook
  - nbviewer
  - Markdown Moster
  - Dask
  - py7zr
  - wget
  - Python
  - Pandas
  - Numpy
  - Sklearn
  - Folium
  - Matplotlib
  - Seaborn
  - Plotly

# 2. Descripción del Proyecto

**Descripción general**
> Se ha realizado la predicción de la ocupación de las diferentes estaciones, utilizando los modelos predictivos Linear_Regresion y Random_Forest

> Análisis del ano 2020 Vs. los otros anos, donde se analizo el tema del COVID-19

> Análisis de las estaciones en las que es necesario reforzar el numero de bicicletas eléctricas

> Análisis de las estaciones que se encuentran sin muelles disponibles en diferentes horas.

# 3. Estructura del Proyecto

**Descripción de la estructura de carpetas y archivos**

> En este repositorio se encuentra la siguiente información :

* Carpeta predicción utilizando Dask (En este carpeta se encuentra el código para la predicción de docks disponibles)
* Carpeta Análisis de el COVID-19 afecto
* Carpeta Análisis de las Bicicletas a eléctricas
* Carpeta Análisis de Saturación de bicicleta

# 4.Conclusiones

**1. Resumen de los códigos utilizados para el análisis**  (Inge)




**2. Análisis de como el COVID-19 afecto** (Evelyn)




**3. Análisis de las Bicicletas eléctricas** 

*En el siguiente análisis queremos detectar aquellas estaciones en las que falta bicicletas eléctricas. En la limpieza de datos hacemos los siguientes filtros:*

*1) Eliminar las estaciones 529 y 530 ya que los datos no parecen correctos porque el dock disponible es 99.*

*2) Nos quedamos con aquellas estaciones cuyo estatus es IN_SERVICE (descartando el resto)*

*3) Descartamos las columnas que no son necesarias para el análisis*

*Hacemos el merge con el archivo 'Informacio_Estacions_Bicing.csv' para disponer de la latitud y la longitud*

*Con un contador, calculamos aquellas estaciones que tienen durante 5 horas seguidas 0 disponibilidad de bicicletas eléctricas*

*Nos quedamos con el top 50 (por falta de memoria en el ordenador, no tiene capacidad para trabajar con más*
*Y las representamos en el mapa para ver si se concentran en una misma zona*

*Por otro lado, representamos el total de bicicletas eléctricas en cada año, para analizar cuál ha sido el comportamiento*


**4. Análisis de Saturación de bicicleta**

*Según el Station_id, Latitud, Longitud & Código Postal*

*Días entre semana (Lunes a Viernes), No Festivos, Fines de semana, Días Festivos*

> 1. Grafico con los Station_id & Codigo_Postal

![Mapa](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20Saturacion%20de%20bicicleta/1.%20Mapa_identificando_todos_Station_id.png)

> 2. Análisis del año 2023

![Codigo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20Saturacion%20de%20bicicleta/2.%20Filtrado_2023.png)

![Codigo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20Saturacion%20de%20bicicleta/2.1.%20Filtrado_dias_EntreSemana_%26_NO_Festivos__and_dias_FindeSemana_%26_Festivos.png)

> 3. Análisis de los días entre Semana (Lunes a viernes) y NO Festivos, sin muelles disponibles, entre 08h00 & 10h00.

![Mapa]()

> En el mapa podemos localizar las 45 estaciones que se encuentran llenas a primera hora de la mañana en días laborables 08h00 & 10h00, seguramente coincidiendo con puntos de gran afluencia de empresas.

> 4. Análisis de los Fines de Semana o Festivos, sin muelles disponibles, entre las 08h00 & 10h00 A.M.

![Mapa](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/4.%20Analisis%20de%20los%20Fines%20de%20Semana%20o%20Festivos%2C%20sin%20muelles%20disponibles%2C%20entre%20las%2008h00%20%26%2010h00%20A.M.png)
> En el mapa podemos localizar las 17 estaciones que en fin de semana o Festivos, tienen las estaciones llenas de bicicletas, sin muelles disponibles, en algun momento entre las 8h00 and 10h00.

> 5. Análisis de los días Festivos & Fines de Semana, sin muelles disponibles, entre las 12h00 & 18h00 P.M.

![Mapa](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/5.%20Analisis%20de%20los%20dias%20Festivos%20%26%20Fines%20de%20Semana%2C%20sin%20muelles%20disponibles%2C%20entre%20las%2012h00%20%26%2018h00%20P.M..png)
> En el mapa podemos localizar las 70 estaciones que entre los días festivos y fines de semanas entre las 12h00 & 18h00 P.M. Se encuentran llenas. Estas estaciones estan pegadas al paseo marítimo y al borde de la playa, coincidiendo con las horas donde todavía hay claridad (es de día) para aprovechar de la playa.

> 6. Análisis de los días Festivos & Fines de Semana, sin muelles disponibles, entre las 19h00 & 23h00 P.M

![Mapa](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/6.%20Analisis%20de%20los%20dias%20Festivos%20%26%20Fines%20de%20Semana%2C%20sin%20muelles%20disponibles%2C%20entre%20las%2019h00%20%26%2023h00%20P.M.png)
> En el mapa podemos localizar las 46 estaciones, entre las 19h00 y las 23h00, donde estas estaciones del centro parece estar llenas.

> 7. Análisis sobre el llenado/vaciado de bicicletas, en ciertas estaciones. Los Festivos o Fin de Semana, entre 12h00 & 23h00

![Mapa](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/7.%20Analisis%20sobre%20el%20llenado_vaciado%20de%20bicicletas%2C%20en%20ciertas%20estaciones.%20Los%20Festivos%20o%20Fin%20de%20Semana%2C%20entre%2012h00%20%26%2023h00.png)
> En el mapa podemos localizar las 101 estaciones que se encuentran llenas en Festivos y Fines de semana entre las 12h00 y las 23h00,
> Mostrando lugares desde donde más gente toma bicicletas para desplazarse en el Fin de Semana.
> La recomendación seria que en estas estaciones habría que llenar/surtir con las bicicletas obtenidas anteriormente de las estaciones llenas por el Área del Centro o el Área de la Playa.

> 8. Análisis mapa con información del porcentaje de muelles disponibles de los Festivos o Fin de Semana, entre 12h00 & 23h00

![Mapa](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/8.%20Analisis%20mapa%20con%20informaci%C3%B3n%20del%20porcentaje%20de%20muelles%20disponibles%20de%20los%20Festivos%20o%20Fin%20de%20Semana%2C%20entre%2012h00%20%26%2023h00.png)

> 9. Análisis y generación del mapa con el tamaño de los círculos en función del Inverso del Percentage_docks_available

![Mapa](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/9.%20Analisis%20y%20generacion%20del%20mapa%20con%20el%20tamano%20de%20los%20circulos%20en%20funcion%20del%20Inverso%20del%20Percentage_docks_available.png)
> Este último mapa muestra las estaciones según el nivel de saturación durante el día entre 12h00 & 23h00 de días festivos y fines de semanas.
> Las estaciones con más saturación tienen círculos más grandes, es decir, aquellas que tienen más bicicletas según capacidad y por tanto menos muelles disponibles.
> Claramente se ven las estaciones del Área del Centro y el Área de la Playa, son las más saturadas, en comparación con el resto de estaciones.

> Mariona y Pere, el mapa interactivo se encuentra en el Collab (Bike_kaggel_4_pre-processing_data.ipynb), si hacen click en alguna estación del mapa podrán obtener/observar/analizar la información sobre esa estación como el Station_id o la proporción de bicicletas disponibles.


