# Análisis de uso de servicios de telecomunicaciones

Análisis del comportamiento de clientes de una empresa de telecomunicaciones con operaciones en México y Colombia, enfocado en el uso de llamadas y mensajes.

El proyecto busca identificar patrones de consumo, detectar comportamientos atípicos y comprender las necesidades de distintos segmentos de clientes. Los resultados pueden ayudar a optimizar la oferta comercial y mejorar la experiencia del usuario.

## Objetivos del negocio

- Identificar qué segmentos usan más o menos las llamadas y los mensajes.
- Detectar valores atípicos que puedan corresponder a comportamientos inusuales, fraude o errores de registro.
- Analizar cómo varía el uso según la edad, el país y el plan contratado.
- Encontrar patrones que ayuden a diseñar mejores planes y mejorar la satisfacción del cliente.

## Fuentes de datos

El análisis utiliza tres archivos:

- `plans.csv`: información de los planes disponibles, incluidos precios, minutos y datos incluidos, y costos por consumo adicional.
- `users_latam.csv`: datos de los clientes, como edad, ciudad, fecha de registro y plan contratado.
- `usage.csv`: detalle del uso real de los servicios, incluidas la duración de las llamadas y la longitud de los mensajes.

## Flujo de trabajo

1. **Carga y exploración:** revisar la estructura, las columnas y los tipos de datos de cada archivo.
2. **Evaluación de calidad:** contar valores nulos, identificar valores centinela y revisar fechas fuera de rango.
3. **Limpieza:** reemplazar valores centinela, convertir fechas y tratar o marcar los valores faltantes según corresponda.
4. **Estadística descriptiva:** analizar variables numéricas y categóricas, incluyendo medias, medianas y percentiles.
5. **Visualización y detección de valores atípicos:** crear histogramas y diagramas de caja para explorar distribuciones y posibles anomalías.
6. **Segmentación:** agrupar clientes con criterios definidos, como edad, país, plan y comportamiento de uso.
7. **Conclusiones ejecutivas:** resumir hallazgos y proponer recomendaciones comerciales.
8. **Publicación:** documentar el proceso en un Jupyter Notebook y compartir el proyecto en GitHub.

## Herramientas

- Python
- Jupyter Notebook
- pandas
- NumPy
- seaborn
- Matplotlib

## Objetivos de aprendizaje

Al finalizar el proyecto, podrás:

- Integrar y limpiar datos provenientes de distintas fuentes.
- Validar datos, estandarizar tipos y detectar inconsistencias.
- Describir el uso de llamadas y mensajes por cliente y segmento demográfico.
- Detectar valores atípicos con métodos estadísticos y visuales.
- Crear segmentos de clientes según edad, país y comportamiento.
- Visualizar diferencias entre grupos y extraer conclusiones comerciales.
- Documentar un análisis reproducible en un notebook y un README.

## Estructura sugerida del repositorio

```text
telecom-analysis/
├── data/
│   ├── plans.csv
│   ├── users_latam.csv
│   └── usage.csv
├── notebooks/
│   └── telecom_analysis.ipynb
└── README.md
