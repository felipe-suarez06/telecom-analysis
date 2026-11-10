Análisis del uso de servicios de telecomunicaciones en México y Colombia

¿Los clientes usan sus servicios de la misma manera según el país, la edad y el plan contratado? Para responder esta pregunta, integré datos de clientes, planes y registros de uso para explorar los patrones de llamadas y mensajes, revisar la calidad de la información y comparar distintos segmentos.

El objetivo no fue solo describir el consumo, sino convertir los datos en evidencia útil para orientar decisiones comerciales: entender qué necesidades parecen cubrir los planes actuales, dónde hay diferencias entre grupos y qué patrones merecen una revisión más profunda.

El recorrido del análisis
Comencé explorando los tres archivos para entender qué información contenía cada uno y cómo podían relacionarse. Después revisé la calidad de los datos: busqué valores faltantes o centinela, comprobé los tipos de datos y validé las fechas. Corregí o marqué las inconsistencias pertinentes antes de avanzar, para evitar que problemas de formato distorsionaran las comparaciones.

Con las fuentes preparadas, analicé el uso de llamadas y mensajes mediante estadísticas descriptivas y visualizaciones. Comparé los patrones por país, edad y plan, y utilicé histogramas y diagramas de caja para observar la distribución del consumo y localizar valores atípicos. Traté estos valores como señales para investigar —no como prueba automática de fraude o error—, ya que pueden responder a distintas causas.

Finalmente, reuní los resultados para evaluar qué diferencias entre segmentos podrían ser relevantes para el negocio y qué preguntas convendría explorar en una siguiente etapa.

Hallazgos principales
Completa esta sección con los resultados que obtuviste. Por ejemplo:

Uso por país: [describe la diferencia o similitud observada].
Uso por plan: [indica qué patrones encontraste entre planes].
Edad y consumo: [resume si observaste alguna tendencia].
Valores atípicos: [explica qué detectaste y cómo decidiste tratarlos].
Limitaciones: [menciona datos faltantes, sesgos o aspectos que no se pudieron evaluar].
¿Qué decisiones podría informar?
Según los hallazgos, el análisis podría ayudar a la empresa a revisar si sus planes se ajustan a los patrones de uso de cada segmento y a identificar grupos cuyo comportamiento merece un estudio adicional. Las recomendaciones deben apoyarse en los resultados concretos; por ejemplo, si un grupo muestra un patrón de consumo consistente, podría ser útil evaluar una oferta adaptada y medir su impacto antes de implementarla.

Datos y herramientas
El proyecto integra tres fuentes:

plans.csv: características, precios y límites de los planes.
users_latam.csv: información de clientes, como edad, ciudad, fecha de registro y plan.
usage.csv: registros de uso, incluidas llamadas y mensajes.
Herramientas: Python, Jupyter Notebook, pandas, NumPy, seaborn y Matplotlib.
