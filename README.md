# telecom-analysis

## ConnectaTel -- Análisis y Segmentación de Clientes

Este repositorio contiene el análisis de datos realizado para
ConnectaTel, con el objetivo de estudiar el comportamiento de sus
clientes, identificar problemas de calidad en los datos, segmentar a los
usuarios y obtener conclusiones útiles para la toma de decisiones
comerciales.

### Objetivo del proyecto 

El objetivo principal es analizar la información de los clientes de
ConnectaTel para:

- Identificar y tratar problemas de calidad en los datos.

- Analizar el comportamiento de uso de los clientes.

- Segmentar a los usuarios según su nivel de uso y edad.

- Detectar patrones de uso extremo (outliers).

- Generar insights y recomendaciones para mejorar la oferta de planes.

### Datasets utilizados

El proyecto utiliza tres datasets principales:

- `plans.csv`: contiene la información de los planes ofrecidos por ConnectaTel.
- `users_latam.csv`: contiene la información de los usuarios, como edad, ciudad, fecha de registro, plan y fecha de cancelación.
- `usage.csv`: contiene los registros de uso de los clientes, incluyendo llamadas y mensajes.

Los archivos se cargan en Python utilizando Pandas:

python
`plans = pd.read_csv('/datasets/plans.csv')`
`users = pd.read_csv('/datasets/users_latam.csv')`
`usage = pd.read_csv('/datasets/usage.csv')`

Estas fuentes se integran para construir el perfil de cada usuario en el
dataframe user_profile.

### Etapas del análisis

Exploración inicial: revisión de estructuras, tipos de datos,
estadísticas y valores faltantes.

Limpieza y preparación: tratamiento de valores ausentes, datos
inválidos y fechas fuera del período de análisis.

Análisis exploratorio: estudio de llamadas, mensajes y minutos
de llamadas.

Detección de outliers: identificación de patrones de uso
extremo.

Segmentación de clientes: creación de grupo_uso y
grupo_edad.

Visualización: gráficos de distribución de usuarios por nivel de
uso y edad.

Insight ejecutivo: conclusiones y recomendaciones comerciales.

### Segmentación

#### *Por nivel de uso*

Bajo uso: llamadas < 5 y mensajes < 5.

Uso medio: llamadas < 10 y mensajes < 10.

Alto uso: resto de los casos.

#### *Por edad*

Joven: edad < 30.

Adulto: edad < 60.

Adulto Mayor: resto de los casos.

### Como ejecutar el notebook en Google Colab

Abre Google Colab.

Selecciona Archivo → Subir notebook.

Selecciona el archivo .ipynb de este repositorio.

Verifica que los datasets estén disponibles en las rutas utilizadas
por el notebook.

Ejecuta las celdas en orden o selecciona Entorno de ejecución →
Ejecutar todas.

También puede ejecutarse desde Jupyter Notebook.

### Guía de reproducción

Clona o descarga este repositorio.

Abre el notebook principal.

Carga los datasets.

Ejecuta las celdas de exploración y limpieza.

Ejecuta el análisis exploratorio y la detección de outliers.

Crea las variables grupo_uso y grupo_edad.

Genera las visualizaciones.

Revisa el insight ejecutivo y las recomendaciones finales.

Las celdas deben ejecutarse en orden para que los dataframes y variables
necesarios estén disponibles.

#### Tecnologías utilizadas

Python

Pandas

NumPy

Matplotlib

Seaborn

Google Colab / Jupyter Notebook

#### Principales resultados

El análisis permitió identificar varios hallazgos relevantes sobre la calidad de los datos y el comportamiento de los clientes de ConnectaTel

- Se identificaron y trataron diferentes problemas de calidad en los datos, principalmente valores faltantes, valores inválidos y registros con fechas fuera del período de análisis. Por ejemplo, se encontraron valores faltantes en las columnas `city` y `churn_date`, además de registros con edades inválidas y fechas de registro fuera del período establecido

- La segmentación por nivel de uso mostró que el grupo de **Uso medio** concentra la mayor cantidad de clientes. El segmento de **Bajo uso** representa una proporción menor, mientras que **Alto uso** es el grupo más reducido

- En la segmentación por edad, el grupo **Adulto** es el más representativo de la base de clientes, seguido por **Adulto Mayor** y **Joven**

- Se identificaron valores extremos en variables relacionadas con el consumo, especialmente en la cantidad de llamadas, mensajes y minutos de llamadas, Estos valores fueron analizados como posibles patrones de consumo elevado y no simplemente como errores.

- Los resultados permiten identificar oportunidades para diferenciar la oferta comercial de acuerdo con las características y necesidades de cada segmento

  El análisis muestra que la base de clientes de ConnectaTel está compuesta principalmente por **usuarios adultos con un nivel de uso medio**. Este segmento representa la mayor oportunidad para desarrollar estrategias comerciales dirigidas a incrementar la fidelización y el consumo.

Por otro lado, los clientes clasificados como **Alto uso**, aunque son menos numerosos, representan un segmento de especial interés debido a su mayor nivel de consumo. Para ellos pueden diseñarse planes con mayores cantidades de minutos, llamadas y mensajes, así como beneficios exclusivos.

Los clientes de **Bajo uso** también representan una oportunidad para ofrecer alternativas más económicas y ajustadas a su consumo real. De esta manera, ConnectaTel puede evitar que estos usuarios paguen por servicios que no utilizan y mejorar su experiencia.

#### Conclusion

En conclusión, la segmentación realizada permite a ConnectaTel pasar de una oferta generalizada a una estrategia más **personalizada y basada en el comportamiento de sus clientes**. La creación de planes diferenciados por nivel de uso y edad podría contribuir a mejorar la satisfacción, aumentar el consumo y fortalecer la fidelización de los usuarios.
