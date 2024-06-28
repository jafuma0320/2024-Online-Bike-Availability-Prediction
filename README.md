# Universidad de Barcelona
![Logo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Imagen%20Universidad.png)

## Departamento de Matematicas y Informatica

## Facultada de Matematicas

## Posgrado en DataScience & Machine Learning
![Logo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Imagen%20Post-grado.png)
>https://datascience.ub.edu/course/postgraduate-dsml

> Integrantes del proyecto:

1. Inge Ruiz de Azuaibarra,
2. Javier Fuentes Manrique,
3. Beatriz Almajano,
4. Evelyn Carmona Garcia,

# Nombre del Proyecto: 2024-Bike-Availability-Prediction
![Logo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Imagen%20Bicicletas.png)

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

> A. Colocar en practica todo el conocimiento y herrmientas adquieras durante el post-grado.

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

# 2. Descripcion del Proyecto

**Descripción general**: Una visión general de lo que hace tu proyecto.

**Funcionalidades principales**: Lista de las funcionalidades más importantes.

# 3. Estructura del Proyecto

**Descripción de la estructura de carpetas y archivos**

> En este repositorio encontraran el cuatro (4) Collab de Google Drive, en los cuales se encuentran la siguiente informacion :

* Jupyter Notebook (Inge - Codigo de Dash y los modelos predictivos)
* Jupyter Notebook (Evelyn - Codigo de Dash y el analisis del COVID)
* Jupyter Notebook (Beatriz - Codigo de Dash y el analisis de las bicicletas de Pedal y Motor)
* Bike_kaggel_1_Availability_Prediction.ipynb
* Bike_kaggel_2_pre-processing_data.ipynb
* Bike_kaggle_3_pre-processing_data.ipynb
* Bike_kaggel_4_pre-processing_data.ipynb

# 4. Pruebas

**Resultados de las pruebas**

> Anexar las bitacoras o diarios de Inge

> Anexar las bitacoras o diarios de Evelyn

> Anexar las bitacoras o diarios de Beatriz

> En el siguiente Collab se intento correr el codigo con Dash pero fue imposible, por problema de memoria del computador.
> Este Collab se conservo solo para informacion general, no hay que tenerlo en cuenta para para el desarrollo del problema.

* Bici_kaggle_Dask_5_dates.ipynb

# 5.Conclusiones

**1. Resumen de los codigos utilizados para el analisis**  (Inge)




**2. Analisis de como el COVID-19 afecto** (Evelyn)




**3. Analisis de las Bicicletas a Motor y a Pedal** (Beatriz)



**4. Analisis de Saturacion de bicicleta**
*Segun el Station_id, Latitud, Longitud & Codigo Postal*
*Dias entre semana (Lunes a Viernes), No Festivos, Fines de semana, Dias Festivos*

> 1. Grafico con los Station_id & Codigo_Postal

![Mapa](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/1.%20Mapa_identificando_todos_Station_id.png)

> 2. Analisis del ano 2023

![Codigo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/2.%20Filtrado_2023.png)

![Codigo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/3.%20Filtrado_dias_EntreSemana_%26_NO_Festivos__and_dias_FindeSemana_%26_Festivos.png)

> 3. Analisis de los dias entre Semana (Lunes a viernes) y NO Festivos, sin muelles disponibles, entre 08h00 & 10h00.

![Mapa](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/4.%20Analisis%20de%20los%20dias%20entre%20Semana%20(Lunes%20a%20viernes)%20y%20NO%20Festivos%2C%20entre%2008h00%20%26%2010h00.png)

> 4. Analisis de los Fines de Semana o Festivos, sin muelles disponibles, entre las 08h00 & 10h00 A.M.

![Mapa]()

> 5. Analisis de los dias Festivos & Fines de Semana, sin muelles disponibles, entre las 12h00 & 18h00 P.M.

![Mapa]()

> 6. Analisis de los dias Festivos & Fines de Semana, sin muelles disponibles, entre las 19h00 & 23h00 P.M

![Mapa]()

> 7. Analisis sobre el llenado/vaciado de bicicletas, en ciertas estaciones. Los Festivos o Fin de Semana, entre 12h00 & 23h00

![Mapa]()

> 8. Analisis mapa con información del porcentaje de muelles disponibles de los Festivos o Fin de Semana, entre 12h00 & 23h00

![Mapa]()

> 9. Analisis y generacion del mapa con el tamano de los circulos en funcion del Inverso del Percentage_docks_available

![Mapa]()



