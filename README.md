# Universidad de Barcelona
![Logo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20Saturacion%20de%20bicicleta/Imagen%20Universidad.png)

## Departamento de Matematicas y Informatica

## Facultada de Matematicas

## Posgrado en DataScience & Machine Learning
![Logo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20Saturacion%20de%20bicicleta/Imagen%20Post-grado.png)
>https://datascience.ub.edu/course/postgraduate-dsml

> Integrantes del proyecto:

1. Inge Ruiz de Azua Ibarra,
2. Javier Fuentes Manrique,
3. Beatriz Almajano,
4. Evelyn Carmona Garcia,

# Nombre del Proyecto: 2024-Bike-Availability-Prediction
![Logo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20Saturacion%20de%20bicicleta/Imagen%20Bicicletas.png)

# Descripcion del problema  a solucionar

> Los participantes se enfrentaron al reto de desarrollar modelos predictivos para prever la disponibilidad de bicicletas aparcadas en varias estaciones de bicicletas compartidas de Barcelona.
> Las bicicletas compartidas son un medio de transporte muy popular en muchas zonas urbanas, y una predicción precisa de su disponibilidad puede ayudar a los usuarios a planificar sus desplazamientos y minimizar los tiempos de espera.

> Los participantes recibieron un conjunto de datos que incluye datos históricos de uso y disponibilidad de bicicletas.
> A partir de estos datos, los participantes tuvieron que desarrollar modelos capaces de predecir con exactitud la disponibilidad de aparcamientos en distintos momentos y lugares.
> Se animo a los participantes a utilizar en sus modelos información sobre las condiciones meteorológicas y otras características relevantes.

> El reto se evaluo en función de la exactitud de las predicciones resultantes. **Los modelos con mejores resultados serán premiados con un reconocimiento en la clasificación de Kaggle.**
> https://www.kaggle.com/competitions/2024-online-bike-availability-prediction/overview

# Tabla de contenido

# 1. Introduccion

**Objetivo del proyecto**

> A. Colocar en práctica todo el conocimiento y herramientas adquiridas durante el post-grado.

> B. Prever la disponibilidad de bicicletas aparcadas en varias estaciones de bicicletas compartidas de Barcelona.

**Alcance del proyecto**

> A. Desarrollar algunos Modelos Predictivos capaces de predecir con exactitud la disponibilidad de aparcamientos en distintos momentos y lugares de Barcelona. Para contestar a la pregunta del problema. (1 Parte del proyecto)
> https://www.kaggle.com/competitions/2024-online-bike-availability-prediction/submissions

> B. Con base en en los analisis de las bases de datos entregadas de la primera parte del proyecto, se debera utilizar algunos modelos de informacion, tales como (COVID - 19, Bicicletas a Pedal y Motor, Saturacion de Bicicletas, condiciones meteorologicas, dias festivos, fines de semana, desastres naturales y otras caracteristicas que a los estudiantes les parezcan relevantes.

**Tecnologias y herramientas utilizadas**

> Se utilizaron las siguientes bases de datos:
  - opendata-ajuntament.barcelona
  - Informacio_Estacions_Bicing
  - metadata_sample_submission_2024
  - sample_submission_2024

> Se utilizaron las siguientes librerias:
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

# 2. Descripcion del Proyecto

**Descripción general**
> Se ha realizado la prediccion de la ocupacion de las diferentes estaciones, utilizando los modelos predictivos Linear_Regresion y Random_Forest

> Analisis del ano 2020 Vs. los otros anos, donde se analizo el tema del COVID-19

> Analisis de las estaciones en las que es necesario reforzar el numero de bicicletas electricas

> Analisis de las estaciones que se encuentran sin muelles disponibles en diferentes horas.

# 3. Estructura del Proyecto

**Descripción de la estructura de carpetas y archivos**

> En este repositorio encontraran el cuatro (4) Collab de Google Drive, en los cuales se encuentran la siguiente informacion :

* Carpeta predicion utilizando Dask (En este carpeta se encuentra el codigo para la prediccion de docks_disponibles)
* Carpeta Analisis de el COVID-19 afecto
* Carpeta Analisis de las Bicicletas a electricas
* Carpeta Analisis de Saturacion de bicicleta

# 4.Conclusiones

**1. Resumen de los codigos utilizados para el analisis**  (Inge)




**2. Analisis de como el COVID-19 afecto** (Evelyn)




**3. Analisis de las Bicicletas electricas** 

*En el siguiente análisis queremos detectar aquellas estaciones en las que falta bicicletas eléctricas. En la limpieza de datos hacemos los siguientes filtros:*

*1) Eliminar las estaciones 529 y 530 ya que los datos no parecen correctos porque el dock disponible es 99.*

*2) Nos quedamos con aquellas estaciones cuyo estatus es IN_SERVICE (descartando el resto)*

*3) Descartamos las columnas que no son necesarias para el análisis*

*Hacemos el merge con el archivo 'Informacio_Estacions_Bicing.csv' para disponer de la latitud y la longitud*

*Con un contador, calculamos aquellas estaciones que tienen durante 5 horas seguidas 0 disponibilidad de bicicletas eléctricas*

*Nos quedamos con el top 50 (por falta de memmoria en el ordenador, no tiene capacidad para trabajar con más*
*Y las representamos en el mapa para ver si se concentran en una misma zona*

*Por otro lado, representamos el total de bicicletas eléctricas en cada año, para analizar cuál ha sido el comportamiento*


**4. Analisis de Saturacion de bicicleta**

*Segun el Station_id, Latitud, Longitud & Codigo Postal*

*Dias entre semana (Lunes a Viernes), No Festivos, Fines de semana, Dias Festivos*

> 1. Grafico con los Station_id & Codigo_Postal

![Mapa](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20Saturacion%20de%20bicicleta/1.%20Mapa_identificando_todos_Station_id.png)

> 2. Analisis del ano 2023

![Codigo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20Saturacion%20de%20bicicleta/2.%20Filtrado_2023.png)

![Codigo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20Saturacion%20de%20bicicleta/2.1.%20Filtrado_dias_EntreSemana_%26_NO_Festivos__and_dias_FindeSemana_%26_Festivos.png)

> 3. Analisis de los dias entre Semana (Lunes a viernes) y NO Festivos, sin muelles disponibles, entre 08h00 & 10h00.

![Mapa](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20Saturacion%20de%20bicicleta/3.%20Analisis%20de%20los%20dias%20entre%20Semana(Lunes%20a%20viernes)%20y%20NO%20Festivos%2C%20sin%20muelles%20disponibles%2C%20entre%2008h00%20%26%2010h00.png)

> En el mapa podemos localizar las 45 estaciones que se encuentran llenas a primera hora de la mañana en dias laborables 08h00 & 10h00, seguramente coincidiendo con puntos de gran afluencia de empresas.

> 4. Analisis de los Fines de Semana o Festivos, sin muelles disponibles, entre las 08h00 & 10h00 A.M.

![Mapa](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20Saturacion%20de%20bicicleta/4.%20Analisis%20de%20los%20Fines%20de%20Semana%20o%20Festivos%2C%20sin%20muelles%20disponibles%2C%20entre%20las%2008h00%20%26%2010h00%20A.M.png)

> En el mapa podemos localizar las 17 estaciones que en fin de semana o Festivos, tienen las estaciones llenas de bicicletas, sin muelles disponibles, en algun momento entre las 8h00 and 10h00.

> 5. Analisis de los dias Festivos & Fines de Semana, sin muelles disponibles, entre las 12h00 & 18h00 P.M.

![Mapa](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20Saturacion%20de%20bicicleta/5.%20Analisis%20de%20los%20dias%20Festivos%20%26%20Fines%20de%20Semana%2C%20sin%20muelles%20disponibles%2C%20entre%20las%2012h00%20%26%2018h00%20P.M..png)

> En el mapa podemos localizar las 70 estaciones que entre los días festivos y fines de semanas entre las 12h00 & 18h00 P.M. Se encuentran llenas. Estas estaciones estan pegadas al paseo marítimo y al borde de la playa, coincidiendo con las horas donde todavia hay claridad (es de dia) para aprovechar de la playa.

> 6. Analisis de los dias Festivos & Fines de Semana, sin muelles disponibles, entre las 19h00 & 23h00 P.M

![Mapa](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20Saturacion%20de%20bicicleta/6.%20Analisis%20de%20los%20dias%20Festivos%20%26%20Fines%20de%20Semana%2C%20sin%20muelles%20disponibles%2C%20entre%20las%2019h00%20%26%2023h00%20P.M.png)

> En el mapa podemos localizar las 46 estaciones, entre las 19h00 y las 23h00, donde estas estaciones del centro parece estar llenas.

> 7. Analisis sobre el llenado/vaciado de bicicletas, en ciertas estaciones. Los Festivos o Fin de Semana, entre 12h00 & 23h00

![Mapa]()
> En el mapa podemos localizar las 101 estaciones que se encuentran llenas en Festivos y Fines de semana entre las 12h00 y las 23h00,
> Mostrando lugares desde donde más gente toma bicicletas para desplazarse en el Fin de Semana.
> La recomendacion seria que en estas estaciones habria que llenar/surtir con las bicicletas obtenidas anteriormente de las estaciones llenas por el Area del Centro o el Area de la Playa.

> 8. Analisis mapa con información del porcentaje de muelles disponibles de los Festivos o Fin de Semana, entre 12h00 & 23h00

![Mapa]()

> 9. Analisis y generacion del mapa con el tamano de los circulos en funcion del Inverso del Percentage_docks_available

![Mapa]()
> Este último mapa muestra las estaciones según el nivel de saturación durante el día entre 12h00 & 23h00 de días festivos y fines de semanas.
> Las estaciones con más saturación tienen círculos más grandes, es decir, aquellas que tienen más bicicletas según capacidad y por tanto menos muelles disponibles.
> Claramente se ven las estaciones del Area del Centro y el Area de la Playa, son las más saturadas, en comparacion con el resto de estaciones.

> Mariona y Pere, el mapa interactivo se encuentra en el Collab (Bike_kaggel_4_pre-processing_data.ipynb), si hacen click en alguna estación del mapa podran obtener/observar/analizar la información sobre esa estación como el Station_id o la proporción de bicicletas disponibles.


