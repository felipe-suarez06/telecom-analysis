# telecom-analysis
Análisis de una empresa de telecomunicaciones con operaciones en México y Colombia. Para entender cómo los clientes usan realmente los servicios móviles (llamadas y mensajes).

El objetivo de la empresa es identificar patrones de uso, detectar comportamientos atípicos y comprender qué segmentos de clientes muestran necesidades diferenciadas, con el fin de optimizar la oferta comercial y mejorar la experiencia del usuario.

Para ello, se trabajará con tres fuentes de datos:
-plans.csv: los planes actuales (precio, minutos incluidos, GB incluidos, costo por extra).
-users_latam.csv: información de clientes: edad, ciudad, fecha de registro, plan contratado.
-usage.csv: el detalle de uso real: llamadas (duración) y mensajes (longitud).

Misión: explorar, limpiar y analizar estas bases de datos para construir una visión clara, confiable y accionable sobre el comportamiento de uso de los clientes y cómo varía entre diferentes grupos de usuarios.

Preguntas del negocio:
¿Qué segmentos de clientes muestran mayor o menor uso de llamadas y mensajes?
¿Qué usuarios presentan valores atípicos que puedan indicar comportamientos inusuales, fraude o errores de registro?
¿Cómo varía el uso según la edad y el tipo de plan contratado?
¿Qué patrones pueden ayudar a diseñar mejores planes, optimizar la oferta y mejorar la satisfacción del cliente?

Objetivos de aprendizaje del proyecto
Al finalizar este proyecto, podrás:

-Integrar y limpiar bases de datos provenientes de tres fuentes distintas.
-Aplicar técnicas de validación, estandarización de tipos de datos y detección de valores inconsistentes.
-Construir un perfil estadístico del uso (llamadas y mensajes) por cliente y por segmentos demográficos.
-Detectar outliers y comportamientos atípicos mediante métodos estadísticos y visuales.
-Crear segmentaciones de clientes basadas en edad, país y comportamiento de uso.
-Visualizar diferencias entre segmentos y extraer insights comerciales relevantes.
-Documentar todo el proceso en un Jupyter Notebook, junto con un README reproducible para subirlo a GitHub.

🛠️ Herramientas de la lección
Jupyter Notebook
Python: pandas, numpy, seaborn, matplotlib

 Flujo general del proyecto:
Paso----Acción----Resultado para el negocio
1. Cargar y explorar----Cargar y explorar plans, users_latam, usage.----Visión clara de la estructura y tipos de columna de cada dataset.
2. Identificación de problemas de calidad----Contar nulos, detectar sentinels, revisar fechas fuera de rango.----Lista priorizada de problemas que pueden sesgar decisiones.
3. Limpieza básica----Reemplazar sentinels, convertir fechas, imputar o marcar NA según reglas.----Datos consistentes y listos para análisis estadístico.
4. Summary statistics----Revisar las medidas clave en variables categóricas y numéricas.----Medidas clave (media, mediana, percentiles) que muestran el comportamiento típico y extremo
5. Visualización & outliers----Creación de histogramas y boxplots.----Visualización de sesgos, patrones de usuarios o datos atípicos.
6. Segmentación----Crear segmentaciones basadas en reglas claras; visualizar proporciones con countplots.----Segmentos accionables que permiten diseñar ofertas, campañas y migraciones de plan.
7. Insight ejecutivo----Redactar conclusiones y recomendaciones comerciales basadas en los pasos anteriores.----Responder a las preguntas del negocio y proponer acciones concretas.
8. Publicación----Subir tu notebook + README a GitHub.----Entrega reproducible para revisión y ejecución por stakeholders.

Ejecutar el noteboo en Google Colab.
