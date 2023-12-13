# Telecomunicaciones en Argentina
![Imagen](https://github.com/AleGS2108/PI-Data_Analytics/blob/main/resources/caratula.jpg)

Lab N°2: Data Analytics

La conectividad a Internet se ha convertido en un pilar fundamental de la sociedad moderna, transformando la forma en que vivimos, trabajamos, aprendemos y nos comunicamos. En un mundo cada vez más interconectado, las telecomunicaciones desempeñan un papel esencial en la habilitación de esta revolución digital. La mejora constante del alcance y la calidad de la conectividad a Internet es crucial para satisfacer las crecientes demandas de una sociedad cada vez más dependiente de la tecnología.

Este proyecto se centra en explorar y comprender la importancia de las telecomunicaciones en la mejora de la conectividad a Internet, utilizando datos proporcionados por la ENACOM (Ente Nacional de Comunicaciones de Argentina).

# Contenido del repositorio
En este repositorio se encuentran almacenadas cuatro carpetas y tres archivos:
* En la carpeta **Dataset extra - Población** se encuentra un archivo complementario relacionado a estimaciones de población para distintos periodos y provincias de Argentina, obtenidos de [INDEC - Argentina](https://www.indec.gob.ar/indec/web/Nivel4-Tema-2-24-85).
* En la carpeta **Datasets limpios** se encuentra la data limpia después de realizado el proceso de ETL.
* En la carpeta **Datasets en bruto** se encuentra la data en bruto obtenida de la página de ENACOM.
* En la carpeta **Datasets KPI** se encuentra la data transformada después de realizado el proceso de EDA, la cual se ha utilizado para la realización del dashboard.
* En la carpeta **resources** se encuentran los recursos (imágenes).
* En el archivo **ETL** se encuentra la documentación y el paso a paso del ETL.
* En el archivo **EDA** se encuentra la documentación y el paso a paso del EDA.
* En el archivo **Dashboard** se encuentra la presentación de Power Bi correspondiente al proyecto, la cual muestra el estado actual de los KPI´s.

# ETL
El proceso ETL (Extract, Transform, Load) es fundamental en la gestión de datos que constó de tres etapas clave:
* Extracción (Extract): En esta fase, los datos se recopilaron desde la página de ENACOM. Si bien en un principio pensó en utilizarse la API para descar toda la información, ésta se vió con errores por lo que se decidió trabajar descargando los archivos en formato xlsx.
* Transformación (Transform): Después de la extracción, los datos se sometieron a una serie de transformaciones y limpiezas, incluyendo la normalización de datos, la conversión de formatos, la agregación y la limpieza de datos erróneos.
* Carga (Load): En la etapa final, los datos transformados se cargaron a datasets limpios, organizados y almacenados de manera que sean accesibles para su posterior análisis, consultas y generación de informes.

# EDA
Se basó en el análisis de mejora y expansión de la cobertura de red en Argentina, con una ventana temporal de 4 años.

Si bien se hizo un análisis de la mayoría de los datasets, no todos fueron involucrados en la elaboración del dashborad. Este se debe a que se concluyó que no era información relevante en persecución del objetivo general o que bien había mucho más que analizar pero resulto imposible por la falta de información.

# KPI's
Ya habiendo establecido el objetivo general, el primer KPI planteado se basó en el análisis del crecimiento porcentual de conexiones en cada provincia. Para el mismo se tuvo en cuenta el porcentaje de conexiones por año (dividiento el total de conexiones por la población). Haciendo énfasis en los datos brindados para los años 2022 y 2018 se calculo el porcentaje de crecimiento de acceso a Internet para cada provincia.

Así se estableció como indicador que para el año 2023, se espera un incremento del 1.5% para todas las provincias ya que la media del crecimiento es de 5.25% en 4 años (es decir 1.3% anual)

![Imagen](https://github.com/AleGS2108/PI-Data_Analytics/blob/main/resources/porcentaje_conexiones_menores_1%2C5.jpg)

![Imagen](https://github.com/AleGS2108/PI-Data_Analytics/blob/main/resources/crecimeinto_porcentual_4_años.jpg)

Siguiendo con el análisis se decidió analizar la velocidad media de bajada de las conexiones. Es la FCC (Federal Communications Commission) quien ha determinado que la velocidad de bajada a partir de la cual se considera la Banda Ancha y, por lo tanto, una conexión a internet de alta calidad es a partir de 25Mbps, por lo que se fijó la vmb en 30Mbps para salvaguardar cualquier falla de cobertura, ya que el dataframe provee un dato promedio de velocidad de bajada.

Se analizó la vmb de cada provincia para cada año para verificar si se cumplía con el límite de vmb mínimo para ser considerado de banda ancha.

Se observó que todos los años iba incrementando, pero aún así no había alcanzado a abarcarse todas las provincias. Es por ello que se planteo como indicador que para el año 2023, el incrementó de provincias con acceso a una red de calidad de Internet debía aumentar en un mínimo de 2 provincias. (La media de crecimiento durante los 4 años fue de aproximadamente 20%, por lo que se espera un crecimiento del 7.5% para el próximo año).

![Imagen](https://github.com/AleGS2108/PI-Data_Analytics/blob/main/resources/distribución_vmb_anual.jpg)

![Imagen](https://github.com/AleGS2108/PI-Data_Analytics/blob/main/resources/crecimiento_porcentual_provincias_mayor_30mbps.jpg)

Por último, decidió analizarse la cantidad de reclamos recibidos por delegación, ésto para saber donde deben presentarse medidas de mejoras del personal. Sin embargo la ventana temporal cambió ya que se cuentan con datos a partir del mes 1 del año 2023 hasta el mes 9 del mismo año. Y habiendo analizado la cantidad de reclamos recibidas por delegación, se estableció como objetivo disminuir en un 20% en el lapso del último trimestre del año.

![Imagen](https://github.com/AleGS2108/PI-Data_Analytics/blob/main/resources/cantidad_reclamos_delegación.jpg)

#  Herramientas utilizadas
* Python
* Pandas
* Matplotlib
* Seaborn
* Power BI

## Contacto

Para cualquier pregunta o comentario, no dudes en ponerte en contacto: [correo](mailto:mags.noa21@gmail.com) 
o por [linkedin](https://www.linkedin.com/in/m-alejandro-garcia-soto-a35680212/).

¡Muchas gracias por la atención!
