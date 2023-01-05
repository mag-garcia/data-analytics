
<p align=center><img src=https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png><p>

#  <h2 align="center">**PROYECTO INDIVIDUAL Nº3**</h2>

# <h1 align="center">**`Telecomunicaciones`**</h1>


## **Descripción del problema (Contexto y rol a desarrollar)**


### **Contexto**
La industria de las telecomunicaciones ha jugado un papel vital en nuestra sociedad, facilitando la información a escala internacional y permitiendo la comunicación continua incluso en medio de una pandemia mundial. La transferencia de datos y comunicación se realiza en su mayoría a través de internet, líneas telefónicas fijas, telefonía móvil, casi en cualquier lugar del mundo. 

En comparación con la media mundial, Argentina está a la vanguardia del desarrollo de las telecomunicaciones, teniendo para el 2020 un total de [62,12 millones conexiones](https://www.datosmundial.com/america/argentina/telecomunicacion.php). 

### **Rol a desarrollar**

En este contexto, una empresa prestadora de servicios de telecomunicaciones nos encarga la realización de un **análisis** completo que permita reconocer el comportamiento de este sector a nivel nacional. 

Para eso, tomando los datos de la API de ENACOM, visualizaremos y analizaremos los siguientes KPIs:

+ Aumento o disminución de la variación porcentual **trimestral** del servicio de internet, cada 100 hogares por provincia. [(dataset)](https://www.google.com/url?q=https://datosabiertos.enacom.gob.ar/visualizations/32226/penetracion-de-internet-fijo-accesos-por-cada-100-hogares/&sa=D&source=docs&ust=1671204570423891&usg=AOvVaw0YwFIM-MNjsy094L_FOFM3)

+ Aumento o disminución de la variación porcentual **semestral** de la velocidad del servicio de internet fijo por provincia. [(dataset)](https://datosabiertos.enacom.gob.ar/dataviews/245546/velocidad-media-de-bajada-de-internet-fijo-por-provincia/)

+ Aumento o disminución de la variación porcentual **semestral** del uso de fibra optica para conexiones por provincia.
[(dataset)](https://datosabiertos.enacom.gob.ar/dataviews/240898/acceso-a-internet-fijo-por-tecnologia-y-provincia/)

+ Aumento o disminución de la variación porcentual **trimestral** de los ingresos de empresas de telecomunicacion. [(dataset)](https://datosabiertos.enacom.gob.ar/visualizations/29879/ingresos-trimestrales-por-la-prestacion-del-servicio-de-internet-fijo/)


### **Fuente de datos**:
- [Dataset principal](https://datosabiertos.enacom.gob.ar/dashboards/20000/acceso-a-internet/) Se sugiere el uso de la API
- [Datasets complementarios](https://datosabiertos.enacom.gob.ar/home)
- Otros datasets de busqueda propia.

<br>

# Análisis Exploratorio de los datos y transformaciones

## Tablas:


### **acceso_100_hogares** : Hogares con disponibilidad a internet cada 100 hogares, separado por provincia, año y trimestre, desde 2014 hasta 2020.

*Transformación :* Las columnas AÑO y TRIMESTRE fueron transformadas a datos numericos, y se creó una nueva columna "fecha" fusionando los datos de trimestre con los de año.

### **acceso_tecnologia** : Diferenciación de los tipos de conexiones de internet segun provincia, año y trimestre.

*Transformación :* Se quitaron errores, se creo una nueva columna "fecha" fusionando los datos de trimestre con los de año.

### **velocidad_media**: Media de la velocidad de bajada de internet, segun provincia, año y trimestre.

*Transformación :* Se quitaron errores, se creó una nueva columna "fecha" fusionando los datos de trimestre con los de año.

### **ingresos** : Ingresos trimestrales de los operadores por el servicio de Internet fijo

*Transformación :* Se creó una nueva columna "fecha" fusionando los datos de trimestre con los de año.


## Tablas adicionales:

**calendario** con las fechas que abarca el analisis, para relacionar las fechas trimestrales de cada tabla que lo requiriera.

**provincia** con todas las provincias que aparecen en las tablas, como tabla intermedia para normalizar los nombres.



