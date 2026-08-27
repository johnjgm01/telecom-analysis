# telecom-analysis

#*ConnectaTel -- Análisis y Segmentación de Clientes*

Este repositorio contiene el análisis de datos realizado para
ConnectaTel, con el objetivo de estudiar el comportamiento de sus
clientes, identificar problemas de calidad en los datos, segmentar a los
usuarios y obtener conclusiones útiles para la toma de decisiones
comerciales.

*Objetivo del proyecto*

El objetivo principal es analizar la información de los clientes de
ConnectaTel para:

- Identificar y tratar problemas de calidad en los datos.

- Analizar el comportamiento de uso de los clientes.

- Segmentar a los usuarios según su nivel de uso y edad.

- Detectar patrones de uso extremo (outliers).

- Generar insights y recomendaciones para mejorar la oferta de planes.

#*Datasets utilizados*

El análisis utiliza información relacionada con:

Usuarios: user_id, nombre, edad, ciudad, fecha de registro,
plan y fecha de cancelación.

Llamadas: cantidad y duración de las llamadas.

Mensajes: cantidad de mensajes enviados.

Planes: información de los planes contratados.

Estas fuentes se integran para construir el perfil de cada usuario en el
dataframe user_profile.

*Etapas del análisis*

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

#*Segmentación*

*Por nivel de uso*

Bajo uso: llamadas < 5 y mensajes < 5.

Uso medio: llamadas < 10 y mensajes < 10.

Alto uso: resto de los casos.

*Por edad*

Joven: edad < 30.

Adulto: edad < 60.

Adulto Mayor: resto de los casos.

#*Cómo ejecutar el notebook en Google Colab*

Abre Google Colab.

Selecciona Archivo → Subir notebook.

Selecciona el archivo .ipynb de este repositorio.

Verifica que los datasets estén disponibles en las rutas utilizadas
por el notebook.

Ejecuta las celdas en orden o selecciona Entorno de ejecución →
Ejecutar todas.

También puede ejecutarse desde Jupyter Notebook.

*Guía de reproducción*

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

*Tecnologías utilizadas*

Python

Pandas

NumPy

Matplotlib

Seaborn

Google Colab / Jupyter Notebook

*Principales resultados*

El análisis muestra que el grupo de Uso medio concentra la mayor
cantidad de usuarios y que Adulto es el segmento de edad más
numeroso. Los usuarios de Alto uso, aunque representan un grupo
menor, tienen potencial comercial por su mayor consumo. También se
identificaron valores extremos en llamadas, mensajes y minutos de
llamadas.

*Conclusión*

El proyecto demuestra cómo la limpieza, exploración y segmentación de
datos pueden utilizarse para comprender mejor a los clientes de
ConnectaTel y apoyar decisiones comerciales basadas en evidencia
