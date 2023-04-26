<p align='center'>
<img src ="https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png">
<p>


<h1 align='center'>
 <b>PROYECTO INDIVIDUAL Nº2</b>
</h1>

¡Bienvenidos al último proyecto individual de la etapa de labs! En esta ocasión, deberán hacer un trabajo situándose en el rol de un ***Data Analyst***.
 
# <h1 align="center">**`Telecomunicaciones`**</h1>


<p align='center'>
<img src = 'https://www.enacom.gob.ar/multimedia/noticias/N/202104/archivo_20210414032123_6165_720x447.jpg' height = 350>
<p>

<br>

<br>

### **Contexto**

Las telecomunicaciones son la transmisión de información a través de medios electrónicos como la televisión, la radio, la telefonía y el internet. El internet es una red global de computadoras interconectadas que ha transformado la forma en que nos comunicamos, trabajamos, aprendemos y nos entretenemos. La industria de las telecomunicaciones es vital en nuestra sociedad y permite la transferencia de información a escala internacional y la comunicación continua. Argentina es líder en el desarrollo de las telecomunicaciones, teniendo para el 2020 un total de [62,12 millones de conexiones](https://www.datosmundial.com/america/argentina/telecomunicacion.php). 

 <br>

### **Rol a desarrollar**

En este contexto, una empresa prestadora de servicios de telecomunicaciones le encarga a usted la realización de un **análisis** completo que permita reconocer el comportamiento de este sector a nivel nacional. Considere que la principal actividad de la empresa es brindar **acceso a internet**, pero también es importante considerar el comportamiento asociado al resto de los servicios de comunicación, con el fin de orientar a la empresa en brindar una buena calidad de sus servicios, identificar oportunidades de crecimiento y poder plantear soluciones personalizadas a sus posibles clientes.

Con el fin de monitorear la eficacia de los objetivos de la empresa, se le pide **visualizar** en un dashboard el siguiente KPI y **establecer 3 KPIs adicionales** producto de su análisis:

+ Aumentar en un 2% el acceso al servicio de internet para el próximo trimestre, cada 100 hogares, por provincia. [(Datos)](https://www.google.com/url?q=https://datosabiertos.enacom.gob.ar/visualizations/32226/penetracion-de-internet-fijo-accesos-por-cada-100-hogares/&sa=D&source=docs&ust=1671204570423891&usg=AOvVaw0YwFIM-MNjsy094L_FOFM3)

*Nota: En la sección de material de apoyo se puede encontrar más información sobre los KPIs.*

 <br>

 <br>

 <br>

<h1 align='center'>
 Propuesta de Trabajo 
</h1>

- Investigación preliminar 

- ETL

- Análisis Exploratorio de los datos (_Exploratory Data Analysis = EDA_)
  
- Dashboard

- KPIs
 
- Repositorio de GitHub

 <br>

 <br>

 ## **Investigación preliminar** 

 <h1

 <br>

### **Sobre ENACOM**

ENACOM es el acrónimo de Ente Nacional de Comunicaciones, una agencia gubernamental de Argentina responsable de regular y supervisar el mercado de las comunicaciones en el país. fue creado en Diciembre del 2015 a través del Decreto 267 en el cual se establece su rol como regulador de las comunicaciones y su objetivo principal es conducir el proceso de convergencia tecnológica y crear condiciones estables de mercado para garantizar el acceso de todos los argentinos a los servicios de internet, telefonía fija y móvil, radio, postales y televisión

Entre las principales funciones de ENACOM se encuentran la regulación y el control del uso del espectro radioeléctrico, la asignación de licencias de servicios de telecomunicaciones, la promoción de la competencia en el mercado de las comunicaciones, la protección de los derechos de los usuarios, entre otras. Su objetivo es garantizar el acceso universal, equitativo y asequible a los servicios de comunicaciones en Argentina

<br>

**Misión"**

promover y garantizar el acceso a las tecnologías de la información y la comunicación, fomentando la innovación, la competencia y la protección de los usuarios, con el objetivo de lograr una sociedad más conectada, informada y participativa

<br>

**Vision**

Posicionarse como un referente internacional en regulaciones y control de las comunicaciones, habiendo logrado altos estándares de calidad de servicios a precios competitivos, generando espacios de inclusión digital y defensa de los usuarios, e impulsando una política pública e institucional para el correcto desarrollo del mercado

<br>

**Acceso a Internet**

Entre las funciones de ENACOM en relación al acceso a Internet se encuentran la regulación y fiscalización de los servicios de conectividad, la asignación y gestión del espectro radioeléctrico y la promoción de políticas públicas que favorezcan la conectividad y la inclusión digital en todo el territorio argentino. Además, el organismo trabaja en conjunto con otros organismos gubernamentales y privados para ampliar el acceso a Internet en áreas rurales y remotas, donde la conectividad es más limitada.

<br>

**Objetivo del analisis**

 1. **Evaluar** la evolucion del acceso a Internet fijo desde el 2014 hasta el 2022 por trimestre y por provincia, así como también la suma de ingresos por año, investigando si efectivamente la Pandemia produjo un crecimiento en la utilización de Internet.
 2. **Comparar** la velocidad del acceso a internet fijo de cada provincia para realizar una mejor distribución del acceso a internet según la velocidad categorizada por rangos.
 3.  **Definir** cuál es el tipo de tecnología mas elegida, con mayor crecimiento para cubrir las necesidades de los usuarios acorde a la demanda. 
 4.  **Determinar** cuales son las localidades con servicio nulo de internet para posibilitar la llegada de la tecnología y medios de comunicación a sectores de la sociedad que aún no han tenido esa posibilidad. 
 5.  **Analizar** otros servicios como la televisión por suscripción o satelital, para ofrecer como parte de paquetes y promociones, junto al servicio de internet.

<br>

**1. Conexión a la API de Enacom**

Para conectarse a dicha api es fundamental tener claro cómo armar el request y sus requerimientos los cuales son:

- Llave de acceso : Esta es la clave del paso 1, la necesitarás para cada request, se encuentra en el siguiente link_llave.

- Numero Guid : (NUMER-GEOGR) el GUID del dataset que estás accediendo, este GUID lo puedes encontrar en la página del detalle de la vista, haciendo una búsqueda de la vista a través de la API y en muchos otros lugares.
  
<br>

**2. Recolección de datos**

La API brinda 16 dataset que contienen información relacionada a la conectividad en las diferentes provincias de Argentina, como se muestaran a continuación:

- **Penetración de Internet fijo (accesos por cada 100 hogares)** : Número de accesos al servicio de Internet fijo por cada 100 hogares por provincia.

- **Penetración por hogares nacional de Internet fijo** : Serie trimestral de la penetración del Internet fijo en la métrica por cada 100 hogares.

- **Total nacional de accesos a Internet fijo por banda ancha y banda angosta** : Número total de accesos al servicio de Internet fijo por banda ancha y banda angosta (trimestral).

- **Accesos a banda ancha y banda angosta por provincia** : Número de accesos al servicio de Internet fijo por banda ancha y banda angosta en cada provincia (trimestral).

- **Serie trimestral de accesos a Internet fijo por tecnología** : Número de accesos al servicio de Internet fijo por tipo de tecnología. Total nacional (trimestral).

- **Acceso a Internet fijo por tecnología y provincia** : Número de accesos al servicio de Internet fijo por tipo de tecnología en cada provincia (trimestral).

- **Velocidad Media de bajada de Internet fijo** : Serie histórica de la velocidad media de descarga de Internet nacional (trimestral).

- **Velocidad media de bajada de Internet fijo por provincia** : Serie histórica de la velocidad media de descarga de Internet por provincia (trimestral).

- **Distribución de los accesos totales nacionales a Internet fijo por velocidad** : Distribución de los accesos totales nacionales a Internet fijo por velocidad de bajada (último trimestre disponible).

- **Acceso a Internet Fijo por rangos de velocidad de bajada y provincia** : Número de accesos al servicio de Internet fijo por velocidad de bajada en cada provincia (trimestral).

- **Accesos a Internet fijo por velocidad bajada y provincia** : Número de accesos al servicio de Internet fijo por velocidad de bajada en cada provincia.

- **Ingresos trimestrales por la prestación del servicio de Internet fijo** : Ingresos trimestrales de los operadores por el servicio de Internet fijo.

- **Accesos a Internet fijo por velocidad de bajada y localidad** : Número de accesos al servicio de Internet fijo por velocidad de bajada en cada localidad declarada.

- **Accesos a Internet fijo por tecnología y localidad** : Número de accesos al servicio de Internet fijo por tecnología en cada localidad declarada Categoría.

- **Listado de localidades con conectividad a internet** : Listado de localidades con conectividad a internet, con detalle por tipo de conexión.

- **Conectividad al servicio de Internet** : Consulta las tecnologías disponibles en tu localidad para acceder al servicio de Internet fijo y móvil.

<br>

**3. librerias**

- **import pandas as pd**: pandas es una biblioteca de Python para el análisis y manipulación de datos. Al importarla con el alias pd, se hace más fácil referirse a sus funciones en el código. Algunas de las funciones que se pueden utilizar con pandas incluyen la carga de datos en un dataframe, la manipulación y limpieza de datos, y la agregación y análisis estadístico.

- **import numpy as np**: numpy es una biblioteca de Python para el cálculo numérico y científico. Al importarla con el alias np, se hace más fácil referirse a sus funciones en el código. Algunas de las funciones que se pueden utilizar con numpy incluyen la creación de arrays numéricos, la manipulación y el cálculo de arrays, y el álgebra lineal.

- **from sklearn.linear_model import LinearRegression**: sklearn es una biblioteca de Python para el aprendizaje automático y la minería de datos. En este caso, se importa la clase LinearRegression desde el módulo linear_model. Esta clase permite ajustar un modelo de regresión lineal a un conjunto de datos.

- **from sklearn.metrics import r2_score**: sklearn también tiene una biblioteca de métricas de evaluación para modelos de aprendizaje automático. En este caso, se importa la función r2_score, que calcula el coeficiente de determinación (R cuadrado) de un modelo de regresión.

- **from sklearn.metrics import mean_squared_error**: Esta función importa la función que calcula el error cuadrático medio de un modelo de regresión.

- **import matplotlib.pyplot as plt**: matplotlib es una biblioteca de Python para la visualización de datos. Al importarla con el alias plt, se hace más fácil referirse a sus funciones en el código. En este caso, se utiliza para crear gráficos y visualizaciones de los datos.

- **import seaborn as sns**: seaborn es otra biblioteca de Python para la visualización de datos. En este caso, se utiliza para crear gráficos más avanzados y estilizados que los que se pueden crear con matplotlib.

- **import requests**: requests es una biblioteca de Python que permite hacer solicitudes HTTP. En este caso, se utiliza para hacer solicitudes a una API o a un sitio web para descargar datos.

- **import io**: io es un módulo de Python que proporciona funciones para trabajar con flujos de entrada/salida de datos. En este caso, se utiliza para leer y escribir datos en formato de archivo

<br>


 ## **ETL** 
  <h1>


### **Eleccion de tablas**

- En primer lugar se realizo una seleccion de tablas que se consideraron iban a ser eficientes para la optencion de la información.
- A partir de este primer análisis con python pudimos determinar los tipos de datos, así como la cantidad de nulos por filas y columnas
- tambien se determino con python los errores y valores faltantes, los datos sobrantes, aquellos valores que es posible reemplazar como el - 0 por el 0.
- También podemos identificar la necesidad de normalizacion de las mayúsculas y minúsculas.
- generar y eliminar columnas 

<br>

### **Tablas**

<br>

estas fueron las tablas usadas para el proyecto:


	1  Acceso a Internet fijo por rango de velocidad por provincia
    2  Acceso a Internet fijo por tecnologia y provincia
    3  Accesos a Internet fijo por tecnología y localidad
    4  Acceso a Internet, cada 100 hogares por provincia 
    5  Calendario
    6  Ingresos trimestrales por la prestación del servicio de Internet fijo
	7  Listado de localidades con conectividad a internet
    8  Velocidad media de bajada por provincia
	
tablas extraidas de apoyo 

    9  Accesos TV por suscripcion y TV satelital
	  


<br>

**1 Acceso a Internet fijo por rango de velocidad por provincia**
- eliminamos valores nulos 
- Cambio del tipo de dato a tipo numérico de las columnas con Mbps
- Agregado de una columna personalizada con la fecha por año y trimestre 
(Query utilizada: ""1/"&Number.ToText([Trimestre]*2+([Trimestre]-2))&"/"&Number.ToText([Año]))."


<br>

**2 Acceso a Internet fijo por tecnologia y provincia**

- validamos nulos
- Cambio del tipo de dato a tipo numérico
- Errores quitados y reemplazados de la columna año y trimestre.
- Agregado de una columna personalizada con la fecha por año y trimestre

<br>

**3 Accesos a Internet fijo por tecnología y localidad**

- elimino columna 
- conviert los - 0 en 0
- elimino los .
- Cambio del tipo de dato a tipo numérico
- elimino filas que estan con valores Sin Datos

<br>

**4  Acceso a Internet, cada 100 hogares por provincia**
  
- eliminamos las "," por "."
- Cambio del tipo de dato a tipo numérico
- borramos valores nulos
- Agregado de una columna personalizada con la fecha por año y trimestre.

<br>

**5  Calendario**

- creamos una tabla con los datos de fechas para unir las tablas a usar 
- cambiamos el tipo de dato 

<br>

**6  Ingresos trimestrales por la prestación del servicio de Internet fijo**

- Cambio del tipo de dato a tipo numérico
- Agregado de una columna personalizada con la fecha por año y trimestre.


<br>

**7  Listado de localidades con conectividad a internet**

- renombramos columnas 
- Cambio del tipo de dato
- elimino columnas 
- elimino campos vacios de provincia y localidad 
- convierto en 0 = no y 1 = si para tener variables numericas 
- cambio tipos de datos
- Agregado de una Columna condicional con el título de conectividad donde se resume si cada localidad por provincia posee o no al menos algún servicio de internet.

<br>

**8  Velocidad media de bajada por provincia**

- eliminamos columnas 
- Cambio del tipo de dato a tipo numérico
- Agregado de una columna personalizada con la fecha por año y trimestre.

<br>

 **9  Accesos TV por suscripcion y TV satelital**

- cargamos los datos
- cambiamos el tipo de dato 
- eliminamos los . en los datos numericos
- agregamos columna de fecha 
	


<br>

 ## **Análisis Exploratorio de los datos (_Exploratory Data Analysis = EDA_)** 
  <h1>


### **Matriz de correlacion**
La matriz de correlación muestra la relación entre las variables en un conjunto de datos. Los valores de la matriz de correlación varían entre -1 y 1, donde un valor de 1 indica una correlación positiva perfecta, un valor de -1 indica una correlación negativa perfecta y un valor de 0 indica que no hay correlación entre las variables.


### **libreria sklearn**
- El código importa el módulo preprocessing de la librería sklearn y crea un objeto de la clase LabelEncoder().

- LabelEncoder() es una herramienta que se utiliza para codificar etiquetas de valores categóricos en valores numéricos enteros. 
Por ejemplo, si tenemos una variable "Color" con valores "Rojo", "Verde" y "Azul",
podemos usar LabelEncoder() para convertir estos valores a 0, 1 y 2, respectivamente.
 
- La función fit_transform() se utiliza comúnmente junto con LabelEncoder(), 
lo que permite ajustar el codificador a los datos y transformarlos al mismo tiempo.


<br>

 ### **1 Acceso a Internet fijo por rango de velocidad por provincia**

- HASTA 512 kbps: número de conexiones a internet con velocidad de hasta 512 kbps en la provincia.
- 512 Kbps - 1 Mbps: número de conexiones a internet con velocidad entre 512 kbps y 1 Mbps en la provincia.
- 1 Mbps - 6 Mbps: número de conexiones a internet con velocidad entre 1 Mbps y 6 Mbps en la provincia.
- 6 Mbps - 10 Mbps: número de conexiones a internet con velocidad entre 6 Mbps y 10 Mbps en la provincia.
- 10 Mbps - 20 Mbps: número de conexiones a internet con velocidad entre 10 Mbps y 20 Mbps en la provincia.
- 20 Mbps - 30 Mbps: número de conexiones a internet con velocidad entre 20 Mbps y 30 Mbps en la provincia.
- 30 Mbps: número de conexiones a internet con velocidad mayor a 30 Mbps en la provincia.
- OTROS: número de conexiones a internet con velocidad desconocida o no especificada en la provincia.
- Total: número total de conexiones a internet en la provincia# Conclusion

 En general, la matriz de correlación sugiere que las diferentes velocidades de conexión a internet no están
 fuertemente correlacionadas con el año o el trimestre, pero están correlacionadas entre sí en diferentes grados. 
 Además, hay cierta relación entre la velocidad de conexión de 20 Mbps a 30 Mbps y la categoría "OTROS".

 podemos determinar que desde que hay un cambio en las tecnologias el rango de velocidad aumento para los usuarios permitiendo tener mayores accesos para los ultimos años viendose reflejado desde el 2019 en adelante 

 <br>


 ### **2 Acceso a Internet fijo por tecnologia y provincia**

- ADSL: Es una tecnología de conexión a Internet que utiliza la línea telefónica para transmitir datos.
- Cablemodem: Es una tecnología de conexión a Internet que utiliza el cable de televisión para transmitir datos.
- Fibra óptica: Es una tecnología de conexión a Internet que utiliza cables de fibra óptica para transmitir datos. Es una tecnología más rápida que el ADSL y el cablemodem.
- Wireless: Es una tecnología de conexión a Internet que utiliza ondas de radio para transmitir datos. Es comúnmente conocido como Wi-Fi.
- Otros: Se refiere a cualquier otra tecnología de conexión a Internet que no esté clasificada en ninguna de las categorías anteriores.
- Total: Es la suma de todas las tecnologías de conexión a Internet utilizadas en la provincia durante el trimestre especificado.

 <br>


 **De la matriz de correlación presentada, podemos concluir lo siguiente**:

- Hay una correlación positiva moderada a fuerte entre las diferentes tecnologías de conexión a Internet, es decir, cuando una tecnología aumenta en uso, también lo hacen las otras tecnologías. La correlación más fuerte se observa entre Cablemodem y Total, con un valor de correlación de 0.979124.

- Las tecnologías de conexión a Internet, como ADSL, Cablemodem, Fibra óptica, Wireless y Otros, tienen una correlación positiva débil con el año y trimestre. Esto sugiere que el año y el trimestre no son los principales impulsores del uso de las tecnologías de conexión a Internet.

- El valor más alto de correlación positiva se encuentra entre ADSL y Otros, con un valor de correlación de 0.838019. Esto sugiere que estas dos tecnologías están altamente relacionadas entre sí.

podemos determinar tambien que el cambio de tecnologia que tuvo el pais marco un impacto muy grande de acceso desde el 2019 en adelante esto permitio tener mayores velocidades y que muchos hogares tuvieran acceso al servicio viendose reflejado una disminucion en tecnologias viejas y un aumento rapido en las nuevas tecnologias 

 <br>


### **3 Accesos a Internet fijo por tecnología y localidad**

- Link Indec: el código de identificación de la localidad según el Instituto Nacional de Estadística y Censos de Argentina (INDEC).
- ADSL: la cantidad de usuarios que tienen acceso a Internet mediante tecnología ADSL.
- CABLEMODEM: la cantidad de usuarios que tienen acceso a Internet mediante tecnología de cablemódem.
- DIAL UP: la cantidad de usuarios que tienen acceso a Internet mediante tecnología dial-up (línea telefónica).
- FIBRA OPTICA: la cantidad de usuarios que tienen acceso a Internet mediante tecnología de fibra óptica.
- OTROS: la cantidad de usuarios que tienen acceso a Internet mediante tecnologías distintas a las mencionadas anteriormente.
- SATELITAL: la cantidad de usuarios que tienen acceso a Internet mediante tecnología satelital.
- WIMAX: la cantidad de usuarios que tienen acceso a Internet mediante tecnología WiMAX.
- WIRELESS: la cantidad de usuarios que tienen acceso a Internet mediante tecnología inalámbrica.
- Total general: la cantidad total de usuarios de Internet en la localidad, independientemente de la tecnología que utilicen.

<br>

 **De la matriz de correlación presentada, podemos concluir lo siguiente**:

- En la matriz de correlación presentada se puede observar que existe una correlación positiva moderada a alta entre la mayoría de los tipos de conexión a internet, como se puede ver en los valores de correlación entre 0,5 y 0,9. Específicamente, las conexiones ADSL, Cablemodem y Dial Up tienen una correlación fuerte entre sí, con valores de correlación entre 0,77 y 0,9. Por otro lado, la conexión de Fibra Óptica tiene una correlación moderada con las otras conexiones, excepto con Dial Up, que tiene una correlación baja.

- Además, se puede observar que las correlaciones entre las diferentes conexiones a internet y el Total General son altas, indicando que el uso de cada una de las conexiones está fuertemente relacionado con el uso total de internet.

- En general, se puede concluir que las conexiones a internet están correlacionadas entre sí y que el uso total de internet está relacionado con el uso de cada una de las conexiones individuales.

podemos determinar que no hay un patron claro entre los datos pero se puede observar que las provincias tienen una cantidad muy similar de servicios lo cual nos permite evaluar que el servicio se esta utilizando en todo el pais 

<br>

### **4  Acceso a Internet, cada 100 hogares por provincia**

- Año: Es el año en que se realizó la medición de los datos.
- Trimestre: Hace referencia al período de tres meses en el que se realizó la medición de los datos. Un año tiene cuatro trimestres: Q1 (enero-marzo), Q2 (abril-junio), Q3 (julio-septiembre) y Q4 (octubre-diciembre).
- Provincia: Es la región geográfica en la que se realizó la medición de los datos.
- Accesos por cada 100 hogares: Es la cantidad de accesos a internet que se registraron por cada 100 hogares en la provincia en cuestión. Esta métrica se utiliza para tener una idea de la penetración de internet en los hogares de una provincia.
- Fecha_Año-Trimestre: Es una forma de presentar la información que combina la información de año y trimestre en un solo dato. Esto se utiliza comúnmente en análisis de series de tiempo para poder representar la evolución de los datos a lo largo del tiempo de manera más clara y ordenada.

podemos determinar que el acceso a internet cada 100 hogares aumentado en los ultimos años y esto puede ser debido a las mejoras de tecnologia en la red y que la cobertura ha mejorado 

tambien podemos atribuir el crecimientoo del servicio de internet a la pandemia ya que fue un factor que afecto a muchas empresas obligando la virtualidad y a la facilida de obtener un equipo electronico que se conecte a una red lo cual ha generado mayor demanda del servicio 

<br>

### **5  Calendario**

por medio de este csv vamos a conectar todas las tablas en power bi con el fin de poder generar un deshboard interactivo y relacionado entre si 

<br>

### **6  Ingresos trimestrales por la prestación del servicio de Internet fijo**

"Año": El año al que pertenece el trimestre.
"Trimestre": El trimestre al que pertenece la información.
"Ingresos (miles de pesos)": Los ingresos obtenidos por los proveedores de servicios de Internet fijo en miles de pesos.
"Periodo": El período al que pertenece la información (trimestral).

Se puede observar que el grafico muestra un crecimiento exponencial con la prestacion del servicio de internet ya que cada año los ingresos sos mayores esto debido a el uso de nuevas tecnologias para brindar el servicio y tambien fuertemente impulsado en los ultimos años desde el 2019 en adelante por la pandemia generando ingresos altos 

podemos determinar que en la matriz de correlacion hay una fuerte correlacion entre el año y los ingresos 

<br>

## **7  Listado de localidades con conectividad a internet**

- Provincia: se refiere a la provincia geográfica en la que se encuentra la localidad.
- Partido: se refiere a la subdivisión administrativa de la provincia, similar a un condado o distrito.
- Localidad: se refiere a una ciudad, pueblo u otra área geográfica habitada.
- ADSL: es una tecnología de acceso a Internet que utiliza líneas telefónicas de cobre para transmitir datos a través de una conexión de banda ancha. Esta columna indica si la localidad tiene acceso a Internet a través de esta tecnología.
- CABLEMODEM: se refiere a una tecnología de acceso a Internet que utiliza una conexión por cable de televisión para transmitir datos a través de una conexión de banda ancha. Esta columna indica si la localidad tiene acceso a Internet a través de esta tecnología.
- DIALUP: se refiere a una tecnología de acceso a Internet que utiliza una línea telefónica y un módem para establecer una conexión de acceso telefónico a Internet. Esta tecnología ya es poco utilizada debido a su baja velocidad de conexión. Esta columna indica si la localidad tiene acceso a Internet a través de esta tecnología.
- FIBRAOPTICA: es una tecnología de acceso a Internet que utiliza cables de fibra óptica para transmitir datos a alta velocidad a través de una conexión de banda ancha. Esta columna indica si la localidad tiene acceso a Internet a través de esta tecnología.
- 4G: se refiere a la cuarta generación de tecnología de comunicación móvil, que permite velocidades de conexión de banda ancha a través de una red de telefonía móvil. Esta columna indica si la localidad tiene cobertura 4G.
- 3G: se refiere a la tercera generación de tecnología de comunicación móvil, que permite velocidades de conexión más lentas que el 4G a través de una red de telefonía móvil. Esta columna indica si la localidad tiene cobertura 3G.
- TELEFONIAFIJA: se refiere a los servicios de telefonía fija tradicionales que utilizan líneas telefónicas de cobre para realizar llamadas. Esta columna indica si la localidad tiene acceso a este tipo de servicio de telefonía fija.
- WIRELESS: se refiere a los servicios de internet inalámbricos que utilizan tecnologías como Wi-Fi para conectarse a Internet. Esta columna indica si la localidad tiene acceso a servicios de internet inalámbricos.
- SATELITAL: se refiere a los servicios de internet que utilizan tecnología de satélite para conectarse a Internet. Esta columna indica si la localidad tiene acceso a servicios de internet satelital.
- Conectividad: esta columna resume el nivel general de conectividad de la localidad, basado en las tecnologías y servicios de telecomunicaciones disponibles en la misma. Puede indicar si la localidad tiene acceso a una amplia gama de opciones de conectividad, o si está limitada a solo unas pocas tecnologías de conexión.


se puede observar que todas las columnas presentan gran cantidad de datos vacios pero estos datos no s epueden borrar ya que esta tabla es clasificatoria lo que indica que los campos vacios represnetan a que en el lugar no hay ese tipo de conectividad 

se saca una columna con un resumen de si tiene o no alguna tecnologia de conexion y desde esta se trabaja la informacion por lo tanto no es necesario ni eliminar datos nulos ademas describir el df no brinda informacion importante ya que por la cantida de vacios no dara un valor representativo 

<br>

## **8  Velocidad media de bajada por provincia**

- Año: Es el año en el que se realizó la medición de la velocidad de bajada de internet en la provincia correspondiente. Por lo general, estas mediciones se llevan a cabo con cierta periodicidad, por lo que se puede tener información sobre la evolución de la velocidad de internet en el tiempo.

- Trimestre: Indica el trimestre dentro del año en el que se llevó a cabo la medición. Por lo general, se realizan mediciones trimestrales para tener una idea de la evolución de la velocidad de internet en la provincia durante todo el año.

- Provincia: Se refiere a la provincia en la que se realizó la medición de la velocidad de internet. La provincia es una división territorial de un país, y puede haber diferencias significativas en la calidad del servicio de internet entre provincias.

- Mbps (Media de bajada): Indica la velocidad media de descarga de internet en megabits por segundo (Mbps) en la provincia y trimestre correspondiente. Esta es una medida de la velocidad a la que se puede descargar información de internet en un dispositivo, como una computadora o un teléfono móvil. Una velocidad más alta de Mbps significa que la descarga de archivos, la navegación por la web y el streaming de video serán más rápidos y eficientes.


podemos observar que el promedio de velocidad ha aumentado con el tiempo esto debido al cambio de tecnologia que se hizo en el pais ademas de lo ocurrido por la pandemio que obligo a muchas empresas a pasar a la virtualidad 


En conclusión, la matriz de correlación sugiere que la velocidad media de bajada de internet ha estado aumentando con el tiempo, pero que el trimestre no tiene un efecto significativo en la velocidad media de descarga de internet


<br>

 **9  Accesos TV por suscripcion y TV satelital**

- Año: Es el año al que se refiere el período de tiempo.
- Trimestre: Es el trimestre al que se refiere el período de tiempo.
- Accesos TV por suscripción: Se refiere al número de hogares que tienen acceso a la televisión por suscripción en el área geográfica y período de tiempo específicos.
- Accesos TV satelital: Se refiere al número de hogares que tienen acceso a la televisión satelital en el área geográfica y período de tiempo específicos.
- Periodo: Se refiere al período de tiempo específico al que se refieren los datos, que en este caso está indicado por el año y el trimestre.

podemos determinar que el servicio de tv por suscriptor aumento en los ultimos años posiblemente por los cambios de tecnologia implementado en el pais, ya que este servicio mejoro en canales hd y planilla de programacion debido a los aumento de velocidades adicional vemos que el servicio de tv satelital baja posiblemente por la mejora del servicio de tv por suscripcion 


<br>

<br>


 ## **Dashboard** 
  <h1>

### **La elección de los gráficos**

<br>

**Gráfico de líneas:**
Fueron seleccionados para el análisis de la evolucion de los datos en el paso del tiempo, así como para realizar una comparación entre los distitntos items:

1 Suma de Accesos por cada 100 hogares por *año y trimestre*.

2 Accesos a Internet fijo por tecnología y provincia por *año y trimestre*.

3 Suma de ingresos por *año y trimestre*.

4 mediana de velocidad media de bajada por provincia *media de bajada*

<br>

**Gráfico Circular:** 
Fueron utiliados para realizar comparativas en el caso por TV satelital o por suscripcion.

<br>

**Gráfico de Barras apiladas:**
 Utilizado para delimitar el top 10 de provincias con menor velocidad media de bajada.

<br>

**Gráfico de Barras columnas:** 
Ingresos (miles de pesos)  de Ingresos trimestrales por la prestación del servicio de Internet fijo

<br>

**Mapa de Argentina:**
 Importé un mapa externo para poder realizar este gráfico. En el podemos ir visualizando geográficamente los datos analizados en la tabla de acceso a internet cada 100 hogares.

- *Tabla:* Aquí figuran todas las localidades segun sus provincias, que NO poseen conectividad ni acceso a internet a través de ningun tipo de tecnología.

- *Treemap:* Muestra la distribución por provincia a partir de la proporción en tamaño de la cantidad de accesos por localidad que poseen conectividad a internet.

- *Tooltip:* Al seleccionar cada Provincia del gráfico Treemap se aparece una ventana con la tabla completa de las localidades de cada una de esas provincias que tienen o no conectividad a internet.

- *Filtros*
La mayoría de los gráficos estan filtrados por año, trimestre y provincia.

<br>

**Segmentacion de datos:**
año, trimestre, provincia

<br>

**tarjetas:**
- Acceso a Internet fijo por tecnologia y provincia [total]
- Acceso a Internet fijo por tecnologia y provincia [Accesos por cada 100 hogares]
- power query

<br>

**tarjetas:**
Velocidad media de bajada por provincia [Velocidad media de bajada por provincia]

<br>

**grafico de areas:**
- suma ADSL
- suma cablemodel
- suma fibra optica
- suma otros 
- suma wireless
- suma acceso internet por suscriptor 
- suma acceso internet por satelite

<br>

**grafico tabla:**
- localidad
- provincia
- conectividad 


<br>

## *La paleta de colores, el diseño y la tipografía*
El diseño está construido sobre la base de tres colores que son el azul, el verde azulado y el blanco. Esta paleta fue extraída del logo de ENACOM y luego utilizada en claros y oscuros para generar distintas combinaciones. El blanco y el gris de los cuadros y el fondo quedan prolijos, buscan generar esa tranquilidad y contraste para que los colores resalten los graficos y la información reelevante. 
La tipografía es standard (Calibri) en casi todos los casos, normalizando la información para generar armonía, que la letra sea legible y entendible. 
Los bordes de los graficos y las formas coinciden en los costados, hay una coherencia entre las distitnas páginas. 
La lectura esta pensada de izquierda a derecha y de arriba a abajo, colocando los filtros al principio a la izquierda para indicar que aquellos modifican el resto de los gráficos, así como los KPIs están ubicados en la parte superior del dashboard, con información mas importante, general e introductoria, dándole la importancia que necesita.

<br>

<br>


 ## **kpis** 

  <h1>


## **se seleccionaron estos KPIs**

<br>

- Aumento o disminución de la variación porcentual trimestral del servicio de internet, cada 100 hogares por provincia. 
- Acceso a Internet cada 100 habitantes por provincia
- Suma total del Accesos a Internet por provincia
- Promedio o velocidad media de bajada por provincia


<br>

## **Conclusiones**


<br>


- El acceso a Internet fijo, ha aumentado progresivamente desde el año 2014 y se ha acrecentado especialmente en los últimos años. Podemos razonar a partir de los datos, que la pandemia fue un factor fundamental para esta aceleración en la digitalización universal. No solo fue necesario para comunicarnos con nuestros seres queridos y compartir momentos de ocio, sino también para realizar todas las actividades de estudio y trabajo. 

- Asimismo, si bien se ha magnificado la actividad a través de las redes y a tecnología, la brecha entre los que aún no tienen acceso se ha hecho mas grande, siendo urgente así como oportuno, la posibilidad de generar accesos a las localidades que aún no tienen esta posibilidad que son un montón y se expresan en el presente proyecto.
- También podemos observar que en la ubicación geográfica estas oportunidades se dan de manera centralizada entre las provincias de Buenos Aires y Córdoba como las que mas accesos a Internet tienen cada 100 hogares, siendo Tierra del Fuego una excepción pero que por ahí el dato está transgiversado por la cantidad de población en relación a la ocupación del territorio.
Es una oportunidad para la empresa, facilitar el acceso a internet en estas regiones, así como también mejorar la velocidad de bajada (es decir la calidad de internet) para que el servicio sea mejor en todo el país. Nuevamente las provincias con menor velocidad media de bajada son las mas alejadas geográficamente de Buenos Aires.

- Se observa que el cable modem y la fibra óptica aumentan casi a la par, aunque en los últimos trimestres se ve una disminución en el uso de cable modem y reemplazo por fibra óptica que los hogares eligen cada vez mas como tecnología para su conectividad. Es importante para el negocio estar al tanto de esta nueva demanda para poder satisfacer a los usuarios.

- La suma de ingresos en lo que refiere a Internet viene en aumento. Finalmente y habiendo realizado una comparación con algunos datos de otras tablas, pude concluir que puede ser una buena idea sumar a estos servicios paquetes o promociones que incluyan suscripciones de TV para seguir impulsando el crecimiento de ambos servicios.



<br>

## Github
 <h1>