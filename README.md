# Categorización de los ciclones de los últimos 3 años en base a la velocidad de sus vientos
![](RackMultipart20231130-1-zmtep8_html_957da2369959fe46.png)

**FACULTAD**** DE INGENIERIA CIVIL**\
**INGENIERO**** TOPOGRAFO ****GEOMATICO**\
**Autores** :\
Hernán Córdova Araiza\ 100%
Rene Antonio Alfaro Ríos\ 100%
Edgar Oswaldo Sebastián López\ 100%
Alejandra Atanacio Mancilla\ 100%
**Grado y**** Grupo**: 3ºB\
**Asesor** :Sebastián Gonzales Zepeda\
**Resumen**

En este proyecto vamos a analizar los ciclones, sus categorías y principalmente las velocidades de los vientos en estos últimos tres años. Para ello rescatamos información en páginas confiables que nos brindan las fechas en que estos ciclones tocaron tierra en cierta ubicación, contamos con tablas de datos en Excel sobre los antecedentes de estos ciclones, principalmente sus velocidades. Este código nos facilita la información que necesitamos, ya que como son 100 datos, nos tardaríamos mucho en calcular cada categoría una por una

**Introducción**

La velocidad de los ciclones en México es un fenómeno meteorológico de gran relevancia, dada la ubicación geográfica del país, que lo expone regularmente a la influencia de huracanes y tormentas tropicales. La comprensión de la velocidad de estos ciclones es esencial para evaluar su impacto potencial en términos de vientos, lluvias y marejadas, así como para implementar estrategias de gestión de riesgos y preparación ante desastres.

**Desarrollo**

Empezamos obteniendo los datos de internet a cerca de las velocidades en Km/h y agruparlos en una tabla de datos de Excel ordenados, para realizar un código que nos determine la categoría que es cada uno con la librería de pandas y nos arroje una nueva columna con el nombre de "Categoría", dándonos como resultado la categoría de cada ciclón, ya que el rango que tenemos es de "235", lo que nos dice que entre la velocidad más baja y más alta, tenemos una diferencia de 235 Km/h, esto nos dice que hay velocidades muy pequeñas y también muy altas entre estos 100 datos.
**Manejo de datos**

El manejo de datos que tenemos lo tenemos organizado en Excel, donde se llevara a cabo este proyecto, por eso haremos un código que tenga acceso a esta tabla de datos y nos pueda dar la información que deseamos.

| DANIELLE | 110 |
| --- | --- |
| EARL | 110 |
| BLANCA | 110 |
| CARLOS | 115 |
| DT 17 | 120 |
| PATRICIA | 120 |
| BORIS | 120 |
| OOLIE | 120 |
| TRUDY | 120 |
| AGATHA | 120 |
| KAY | 130 |
| LESTER | 130 |
| ORLENE | 130 |
| ROSLYN | 130 |
| CUATRO | 130 |
| USA | 140 |
| DOLORES | 140 |
| NORA | 140 |
| OLAF | 150 |
| PAMELA | 150 |
| RICK | 150 |
| GRACE | 155 |
| HERNAN | 160 |
| CRISTOBAL | 165 |
| HANNA | 165 |
| NANA | 165 |
| GAMMA | 165 |
| DELTA | 175 |
| ZETA | 185 |
| LORENA | 195 |
| NARDA | 195 |
| DIECICIETE-E | 205 |
| PRICILLA | 240 |
| FERNAND | 260 |

|

| **Nombre del ciclon** | **Velocidad**** Viento** |
| --- | --- |
| BUD | 25 |
| --- | --- |
| DIECINUEVE | 45 |
| --- | --- |
| ROSA | 45 |
| --- | --- |
| SERGIO | 45 |
| --- | --- |
| VICENTE | 45 |
| --- | --- |
| WILLA | 45 |
| --- | --- |
| BEATRIZ | 55 |
| --- | --- |
| CALVIN | 55 |
| --- | --- |
| LIDIA | 55 |
| --- | --- |
| MAX | 55 |
| --- | --- |
| FRANKLIN | 55 |
| --- | --- |
| KATIA | 55 |
| --- | --- |
| UNO E | 55 |
| --- | --- |
| JAVIER | 55 |
| --- | --- |
| NEWTON | 55 |
| --- | --- |
| COLIN | 55 |
| --- | --- |
| DANIELLE | 55 |
| --- | --- |
| EARL | 55 |
| --- | --- |
| BLANCA | 55 |
| --- | --- |
| CARLOS | 55 |
| --- | --- |
| DT 16 | 55 |
| --- | --- |
| PATRICIA | 55 |
| --- | --- |
| BORIS | 55 |
| --- | --- |
| OOLIE | 55 |
| --- | --- |
| TRUDY | 65 |
| --- | --- |
| AGATHA | 65 |
| --- | --- |
| KAY | 65 |
| --- | --- |
| LESTER | 65 |
| --- | --- |
| ORLENE | 65 |
| --- | --- |
| ROSLYN | 65 |
| --- | --- |
| CUATRO | 65 |
| --- | --- |
| USA | 65 |
| --- | --- |
| DOLORES | 65 |
| --- | --- |

NORA | 65 |
| --- | --- |
| OLAF | 65 |
| PAMELA | 65 |
| RICK | 65 |
| GRACE | 70 |
| HERNAN | 75 |
| CRISTOBAL | 75 |
| HANNA | 75 |
| NANA | 75 |
| GAMMA | 75 |
| DELTA | 75 |
| ZETA | 75 |
| LORENA | 75 |
| NARDA | 75 |
| DIECICIETE-E | 75 |
| PRICILLA | 85 |
| FERNAND | 85 |
| BUD | 85 |
| DIECINUEVE | 85 |
| ROSA | 90 |
| SERGIO | 95 |
| VICENTE | 95 |
| WILLA | 95 |
| BEATRIZ | 95 |
| CALVIN | 95 |
| LIDIA | 95 |
| MAX | 100 |
| FRANKLIN | 100 |
| KATIA | 100 |
| UNO E | 100 |
| JAVIER | 100 |
| NEWTON | 100 |
| COLIN | 100 |
**Código**

from google.colab import files

import pandas as pd

defcategorizar\_ciclon(velocidad\_viento):

    if velocidad\_viento \< 74:

        return"Categoría 1: Tormenta tropical"

    elif velocidad\_viento \< 96:

        return"Categoría 2: Huracán"

    elif velocidad\_viento \< 111:

        return"Categoría 3: Huracán mayor"

    elif velocidad\_viento \< 130:

        return"Categoría 4: Huracán muy fuerte"

    else:

        return"Categoría 5: Huracán extremadamente fuerte"

archivo\_cargado = files.upload()

nombre\_archivo = list(archivo\_cargado.keys())[0]

datos\_ciclones = pd.read\_excel(nombre\_archivo)

datos\_ciclones['Categoria'] = datos\_ciclones['VelocidadViento'].apply(categorizar\_ciclon)

archivo\_salida = 'datos\_ciclones\_con\_categoria.xlsx'

datos\_ciclones.to\_excel(archivo\_salida, index=False)

print(f'Se ha agregado la columna de categoría y se ha guardado en {archivo\_salida}')

Este código que elaboramos para el proyecto lee los datos proporcionados en el archivo Excel sobre las velocidades de viento que generan los ciclones, calcula la categoría para cada velocidad de cada ciclón y agrega una nueva columna llamada "categoría" al archivo Excel, actualizando la información de ese archivo y guardando la información en uno nuevo.
**Resultados**

1. Como resultado el código funciono como esperábamos, insertando nuestro archivo Excel y generando la nueva columna en otro archivo guardado

![](RackMultipart20231130-1-qm7150_html_6e66d338114b1955.png)

1. Una vez ejecutado nos mandó el nuevo archivo Excel a los archivos de Google Colab, donde lo descargamos para ver los resultados.

![](RackMultipart20231130-1-qm7150_html_94d11f1c13c82331.png)
1. Y como ultimo hacemos la comparación de las tablas de datos para comprobar el código ejecutado

![](RackMultipart20231130-1-dyw0wy_html_3d58833e4ff5e94d.png) ![](RackMultipart20231130-1-dyw0wy_html_30bfc8fb11517007.png)

![](RackMultipart20231130-1-dyw0wy_html_16b5fa44de3ad3ca.png) ![](RackMultipart20231130-1-dyw0wy_html_eee3c74cbeaf9f2.png)
![](RackMultipart20231130-1-lbet6i_html_6675cdf7b510a702.png) ![](RackMultipart20231130-1-lbet6i_html_c5756c0d18768001.png)

**Conclusiones**

Este código es una herramienta útil para categorizar ciclones tropicales en función de su velocidad del viento, siguiendo la Escala de Huracanes de Saffir-Simpson. Este tipo de análisis es crucial para comprender la intensidad de los ciclones y evaluar su potencial impacto.

La utilización de Python en entornos como Google Colab permite la manipulación eficiente de datos y facilita la automatización de tareas, como la categorización de ciclones. La combinación de bibliotecas como pandas y openpyxl permite cargar, procesar y guardar datos de manera sencilla.
#POSTER CIENTIFICO
![](https://github.com/reneee27/Proyecto/blob/main/Ciclones/ciclones.png)
