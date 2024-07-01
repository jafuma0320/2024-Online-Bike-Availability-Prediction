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

**1. Resumen de los códigos utilizados para el análisis** 

Para la lectura de datos se ha usado la librería Dask. Dask es una librería de computación paralela y distribuida para Python. Principalmente se utiliza para manejar grandes conjuntos de datos. Permite realizar análisis y procesamiento de datos a gran escala.

Para el desarrollo de este análisis, se ha trabajado con datasets que incluyen datos históricos de uso de bicicletas y su disponibilidad en la ciudad de Barcelona. En este análisis se han limitado los datos al periodo de 2020 al 2023.

En este rango nos hemos encontrado con una gran cantidad de datos a analizar. Al principio, empezamos intentando usar Pandas, pero nos fallaba constantemente ya que nuestros ordenadores no soportaban, y fallaba la memoria constantemente. Es por ello que cambiamos a usar Dask, ya que nos facilitó hacer una lectura de datos de una forma mucho más rápida y sencilla. En nuestro caso, trabajamos leyendo los datos año por año y fuimos eliminando los datos que consideramos innecesarios como valores nulos, datos de otros años o columnas. Una vez hecha la limpieza, ya teníamos un dataframe con el que podíamos sacar la medía de la cantidad de docks disponibles por estación, año, mes, día y hora.

Con ese nuevo dataframe, y con el dataset que nos proporcionaron en la que se concretaba la cantidad de docks que había por cada estación, fuimos capaces de sacar el porcentaje de docks disponibles. Para así después hacer la agrupación por cada cinco horas, consiguiendo así el dataframe que vamos a usar en la predicción. Generar esta tabla es verdad que nos costo bastante ya que la función que hicimos no era precisamente rápida. Es por ello que guardamos el resultado en un csv para no tener que estar generándolo constantemente.

Con el dataframe con el que trabajar preparado, usando la librería train_test_split, dividimos el conjunto de datos en dos, el conjunto de entrenamiento un 80% y para el conjunto de validación el 20%. Para el test usamos los datos de que nos proporcionan del porcentaje de bicicletas disponibles para el año 2024. 

Una vez que tenemos todo dividido como queremos hemos entrenado el modelo. Hemos probado con dos distintos:
- Regresión lineal
- Random forest

La idea de ejecutar los dos era ver si conseguíamos alguna mejora en los resultados. Pero en nuestro caso no ha sido así. Con los dos modelos entrenados no hemos visto mucha diferencia entre usar uno u otro, en nuestros resultados el random forest ha sido ligeramente mejor. Tanto con el modelo de regresión lineal o con el random forest, el Mean Squared Error (MSE) es bastante parecido (regresión lineal igual a 0.01169 y en random forest igual a 0.01082). El valor es bastante bajo, por lo que indica que las predicciones del modelo están muy cerca de los valores reales. Lo mismo sucede con el coeficiente de determinación, en los dos casos el valor se acerca bastante al uno (regresión lineal igual a 0.84751 y en random forest igual a 0.85890), indicando que las predicciones se parecen bastante a los valores reales.

**2. Análisis de como el COVID-19 afecto** 

Tiendo en cuenta que los años dados incluyen el 2020 (año de la pandemia covid),  el objetivo del análisis es comparar la disponibilidad de bicicletas durante ese año y el resto de años 2021 – 2023.

*Preparación de los datos* 

•	Se tomo como base lo realizado en el ejercicio número 1 Predicción. 

•	Por cada año se realizo el filtro de la siguiente información:
  o	 status: “IN_SERVICE”
  o	num_bikes_available: todas aquellas donde menores a 90
  
•	Para el año 2023
  o	V1: eliminar la columna para los mese Setiembre y Agosto

*Principales retos/obstáculos*

•	Se inició trabajando en Collab y a pesar de estar utilizando Dask, no se podía ejecutar el código por falta de memoria. Solución, trabajar en Jupiter notebook.

•	Con el uso del Jupiter notebook tuvimos que descargar los archivos 7z para cada mes y año lo cual ocasiono problemas de espacio. Solución, crear una cuenta de Gmail provisional para poder almacenar los archivos 7z y csv.

•	El dataframe del ejercicio 1 tenia definida las siguientes columnas: station_id, num_docks_available, year, month', 'day', 'hour', sin embargo, para los gráficos que se querían obtener se quería agregar las columnas num_bikes_available, status y date. Al principio, se realizó una limpieza de los datos de estas columnas (Nan, valores numéricos o que no tenían sentido). A pesar de eso al momento de realizar compute tomaba mucho tiempo y se mostraban el mensaje “Sin disponibilidad de memoria”. Por otro lado, para num_bikes_available se identifico que habían unas cuantas estaciones con 198 bicicletas disponibles mientras que para la media del resto de estaciones solo tenia alrededor de 10. Solución, en el dask dataframe se filtro los datos por status = IN_SERVICE y para num_bikes_available se estableció el filtro de estaciones que tuvieran disponibilidad de bicicletas menor a 80. Después de estos filtros, se determino que las columnas a utilizar fueran: station_id','num_bikes_available','num_docks_available', 'year','date','month', 'day', 'hour' y se pudo realizar el compute sin problema para los años 2020, 2021, 2022.

•	Para el año 2023 aparecería el  siguiente error “Hay una columna extra V1 no definida en la metadata”. Al momento de realizar la consulta al dask dataframe ddf_2023.dtype, la columna V1 no aparecía. Solución, se buscó en los csv de cada mes del 2023 y se encontró que sólo en los meses de setiembre y agosto aparecía esta columna y mediante código se eliminaron.

*Interpretación de los gráficos*

El contenido de estos gráficos los puedes ver en la carpeta llamada : Análisis de el COVID-19 afecto.

A.	Media de bicicletas disponibles por día Antes, Durante, y Después del confinamiento el 2020'

![Logo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20el%20COVID-19%20afecto/01%20Media%20de%20disponibilidad%20de%20bicis%20por%20dia.jpg)

B.	Media de bicicletas disponibles por mes Antes, Durante, y Después del confinamiento – 2020

![Logo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20el%20COVID-19%20afecto/02%20Media%20de%20disponibilidad%20de%20bicis%20por%20mes.jpg)

*Antes del Confinamiento (Enero - Medio de Marzo):*
Observamos una tendencia general al alza en la disponibilidad de bicicletas desde principios de año hasta el comienzo del confinamiento en marzo. Esto podría indicar un aumento en la demanda de bicicletas públicas, posiblemente a que las personas les agrada movilizarse en bicicleta.

*Durante el Confinamiento (Medio de Marzo - Finales de Junio):*
Marcado en rojo, se ve un cambio notable en la disponibilidad de bicicletas. Al inicio del confinamiento, hay un aumento súbito en la disponibilidad de bicicletas, alcanzando un pico a principios de abril. Esto sugiere que menos personas estaban utilizando las bicicletas debido a las restricciones de movilidad.
Posteriormente, hay una ligera disminución en la disponibilidad durante el resto del confinamiento, lo que podría indicar un uso gradual de bicicletas a medida que las restricciones se fueron relajando.

*Después del Confinamiento (Finales de Junio - Diciembre):*
La disponibilidad de bicicletas muestra una tendencia a la baja, alcanzando su punto más bajo en septiembre. Esto podría reflejar un aumento en el uso de bicicletas a medida que las personas comenzaron a retomar sus actividades normales.
A partir de octubre, la disponibilidad de bicicletas empieza a aumentar nuevamente, lo que podría indicar una menor demanda o una mayor oferta de bicicletas.

El confinamiento tuvo un impacto significativo en la disponibilidad de bicicletas,
La recuperación gradual en la disponibilidad post-confinamiento sugiere que los patrones de uso de bicicletas no volvieron inmediatamente a los niveles pre-confinamiento.
La disponibilidad de bicicletas también parece estar influenciada por otros factores por ejemplo estacionales.

C.	Disponibilidad media de bicicletas por mes y hora en 2020

![Logo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20el%20COVID-19%20afecto/03%20Disponibilidad%20Media%20de%20bicis%20por%20mes%20y%20horas.jpg)

*Tendencias Generales por Mes:*
Enero a Junio: La disponibilidad de bicicletas es relativamente alta, especialmente durante los meses de abril y mayo, donde se observa una media superior a 12 bicicletas disponibles en casi todas las horas del día.
Julio a Septiembre: Hay una disminución notable en la disponibilidad media de bicicletas, alcanzando los valores más bajos en agosto y septiembre, con medias en torno a 7-8 bicicletas disponibles.
Octubre a Diciembre: La disponibilidad media de bicicletas aumenta nuevamente, con valores similares a los observados en los primeros meses del año.

*Tendencias por Hora del Día:*
Mañanas y Noches (0:00 - 6:00, 18:00 - 23:00): Durante estas horas, la disponibilidad de bicicletas es generalmente alta en comparación con el resto del día. Esto sugiere un menor uso de bicicletas en las primeras y últimas horas del día.
Horas Pico (7:00 - 10:00, 16:00 - 18:00): Se observa una ligera disminución en la disponibilidad de bicicletas durante estas horas, indicando un mayor uso posiblemente relacionado con los desplazamientos.
Hay una tendencia a que las bicicletas sean más disponibles durante las primeras horas de la mañana y las últimas horas de la noche, mientras que el uso parece aumentar durante las horas laborales y de la tarde

*Impacto del Confinamiento:*
Marzo a Junio: Durante el periodo del confinamiento (especialmente abril y mayo), se nota una alta disponibilidad de bicicletas, lo que puede indicar un menor uso debido a las restricciones de movilidad.

*Estacionalidad:*
Verano (Julio y Agosto): La disponibilidad de bicicletas disminuye considerablemente, lo que podría estar relacionado con un mayor uso debido a las vacaciones de verano.
Invierno (Diciembre): Aunque no se observa una disminución tan marcada como en verano, la disponibilidad de bicicletas es menor que en los meses de primavera y otoño.

Uso durante el Confinamiento: El confinamiento llevó a una alta disponibilidad de bicicletas debido a las restricciones de movilidad.
Variaciones Estacionales: Los meses de verano muestran una baja disponibilidad de bicicletas, indicando un uso más intensivo durante estos meses.
Patrones Horarios: Las bicicletas son menos disponibles durante las horas pico de la mañana y la tarde, lo que sugiere su uso principal para desplazamientos diarios.

D.	Disponibilidad de bicicletas por meses para los años 2020 y 2021

![Logo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20el%20COVID-19%20afecto/04%20Disponibilidad%20Media%20de%20bicis%20por%20mes%202020%20y%202021.jpg)

*Comparación General entre 2020 y 2021:*
En la mayoría de los meses, la disponibilidad de bicicletas en 2021 es inferior a la de 2020. Esto sugiere que hubo un mayor uso de bicicletas en 2021, lo cual podría estar relacionado con la relajación de las restricciones y el aumento de la movilidad.

*Impacto del Confinamiento:*
Marzo a Junio 2020: La disponibilidad de bicicletas en estos meses es notablemente alta en 2020, especialmente en abril y mayo. Esto coincide con el periodo de confinamiento, donde el uso de bicicletas se redujo debido a las restricciones.

Marzo a Junio 2021: En 2021, la disponibilidad durante estos meses es menor, lo que indica un mayor uso de bicicletas en comparación con el mismo periodo en 2020. Esto sugiere que las personas empezaron a retomar sus actividades normales y utilizar más las bicicletas.

E.	Disponibilidad media de bicicletas por meses para los años 2020 – 2023

![Logo](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/main/Analisis%20de%20el%20COVID-19%20afecto/05%20Disponibilidad%20Media%20de%20bicis%20por%20mes%202020%20al%202023.jpg)

*Tendencia general:*
A lo largo de los años, la disponibilidad de bicicletas sigue un patrón estacional. Hay un aumento en la disponibilidad durante los meses más cálidos y una disminución durante los meses más fríos.

*Pico de disponibilidad:*
El período entre marzo y junio muestra una mayor disponibilidad de bicicletas, con un pico en abril. Durante los meses más fríos, la disponibilidad disminuye.


**3. Análisis de las Bicicletas eléctricas** 

En el siguiente análisis queremos detectar aquellas estaciones en las que hay escasez de bicicletas eléctricas. Descartamos el año 2020, porque ya hemos visto que al ser año Covid los datos son diferentes. 

Antes de empezar a trabajar, hacemos un análisis de los datos para entender mejor que valor aporta cada una de las columnas.
El principal problema que nos hemos encontrado es la capacidad de memoria para procesar la gran cantidad de datos. Por ello, hemos tenido que analizar cada año por separaddo.

En la limpieza de datos hacemos los siguientes filtros:

1) Eliminar las estaciones 529 y 530 ya que los datos no parecen correctos porque el dock disponible es 99.

2) Nos quedamos con aquellas estaciones cuyo estatus es IN_SERVICE (descartando el resto).

3) Descartamos las columnas que no son necesarias para el análisis.

Hacemos el merge con el archivo 'Informacio_Estacions_Bicing.csv' para disponer de la latitud y la longitud

Con un contador, calculamos aquellas estaciones que tienen durante 5 horas seguidas 0 disponibilidad de bicicletas eléctricas

Nos quedamos con el top 50 (por falta de memoria en el ordenador, no tiene capacidad para trabajar con más)
Y las representamos en el mapa para ver si se concentran en una misma zona

*AÑO 2021*

![Mapa](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/6f3f2702b1b65c71812e78b054ee7947b03058e0/Analisis%20de%20las%20Bicicletas%20a%20electricas/Escasez%20bicis%20el%C3%A9ctricas%202021.png)

*AÑO 2022*

![Mapa](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/6f3f2702b1b65c71812e78b054ee7947b03058e0/Analisis%20de%20las%20Bicicletas%20a%20electricas/Escasez%20bicis%20el%C3%A9ctricas%202022.png)


*AÑO 2023*

![Mapa](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/6f3f2702b1b65c71812e78b054ee7947b03058e0/Analisis%20de%20las%20Bicicletas%20a%20electricas/Escasez%20bicis%20el%C3%A9ctricas%202023.png)


*Una vez tenemos el top 50 de cada año, hacemos un nuevo contador que suma el número de veces que aparece cada estación. Para dar más peso al año 2023 lo ponderamos multiplicando por 3. Representamos el resultado en un mapa:

![Mapa](https://github.com/jafuma0320/2024-Online-Bike-Availability-Prediction/blob/abe71277547d4e2bd50c57f870441eca6c3add5b/Analisis%20de%20las%20Bicicletas%20a%20electricas/Captura%20de%20pantalla%202024-07-01%20220515.png))

*Podemos comprobar que la gran mayoría están situadas por la zona de la costa (como se podía sospechar, ya que al ser Barcelona una ciudad con desnivel, se utilizan para subir las eléctricas y quedan las estaciones de menor desnivel desprovistas de estas). Sin embargo también hay algunas estaciones por la zona de Nou Barris, Les Corts i l'Eixample que también tienen insuficiencia.



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


