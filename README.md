Análisis del uso de servicios de telecomunicaciones en México y Colombia

¿Los clientes usan sus servicios de la misma manera según el país, la edad y el plan contratado? Para responder esta pregunta, integré datos de clientes, planes y registros de uso para explorar los patrones de llamadas y mensajes, revisar la calidad de la información y comparar distintos segmentos.

El objetivo no fue solo describir el consumo, sino convertir los datos en evidencia útil para orientar decisiones comerciales: entender qué necesidades parecen cubrir los planes actuales, dónde hay diferencias entre grupos y qué patrones merecen una revisión más profunda.

El recorrido del análisis
Comencé explorando los tres archivos para entender qué información contenía cada uno y cómo podían relacionarse. Después revisé la calidad de los datos: busqué valores faltantes o centinela, comprobé los tipos de datos y validé las fechas. Corregí o marqué las inconsistencias pertinentes antes de avanzar, para evitar que problemas de formato distorsionaran las comparaciones.

Con las fuentes preparadas, analicé el uso de llamadas y mensajes mediante estadísticas descriptivas y visualizaciones. Comparé los patrones por país, edad y plan, y utilicé histogramas y diagramas de caja para observar la distribución del consumo y localizar valores atípicos. Traté estos valores como señales para investigar —no como prueba automática de fraude o error—, ya que pueden responder a distintas causas.

Finalmente, reuní los resultados para evaluar qué diferencias entre segmentos podrían ser relevantes para el negocio y qué preguntas convendría explorar en una siguiente etapa.

Hallazgos principales:

Uso por plan: [la distribución porcentual del tipo de plan consta de aproximadamente el 65% para el plan básico y aproximadamente el 35% para el plan premium].

Edad y tipo de producto: [la edad no es un buen criterio para diferenciar el tipo de producto que se ofrece a cada cliente, porque los clientes de diferentes edades compran lo mismo. La mayoría de los clientes (65%) elige el plan Básico independientemente de su edad].

Valores atípicos: [En users, la columna city tenía 469 valores nulos (11,73% de las filas).

En usage (o el dataframe correspondiente), duration tenía 22076 nulos (55,19%) y length tenía 17896 nulos (44,74%), posiblemente debido a un problema en el registro de datos (missing at random).

En users, age presentaba 55 valores sentinela -999 (1,3%), que fueron tratados como valores inválidos y reemplazados con la mediana].

cant_mensajes: ...(presenta outliers altos, se puede apreciar que en el plan básico se presentan más outliers)
cant_llamadas: ...(presenta outliers altos,se puede apreciar una gran similitud entre las cajas, aunque en el plan básico hay usuarios que realizan más llamadas en comparación con el promedio, lo que se traduciría como outliers altos)
cant_minutos_llamada: ...(se aprecia que la caja de premium es ligeramente más grande que la de básico, la caja de básico presenta muchos outliers muy altos, se puede apreciar que en este plan hay usuarios que realizan llamadas más prolongadas, lo que se traduciría como outliers altos)

cant_mensajes: ¿mantener o no outliers?
sí mantenerlos, aunque el límite superior es 11.5 y el máximo real es 17 mensajes, si es plausible que un usuario mande por encima del promedio.
cant_llamadas: ¿mantener o no outliers?
sí mantenerlos, aunque el límite superior es 10.5 y el máximo real es 15 mensajes, si es plausible que un usuario llame más veces que el promedio
cant_minutos_llamada: ¿mantener o no outliers?
sí mantenerlos, aunque el límite superior es 61.86 y el máximo real es 155.69 minutos, si es plausible que un usuario tenga llamadas más prolongadas que el promedio, aproximadamente 155 minutos equivaldrían a 2.5 horas.].

¿Qué decisiones podría informar?
Según los hallazgos, el análisis podría ayudar a la empresa a revisar si sus planes se ajustan a los patrones de uso de cada segmento y a identificar grupos cuyo comportamiento merece un estudio adicional. Las recomendaciones deben apoyarse en los resultados concretos; por ejemplo, si un grupo muestra un patrón de consumo consistente, podría ser útil evaluar una oferta adaptada y medir su impacto antes de implementarla.

Datos y herramientas
El proyecto integra tres fuentes:

plans.csv: características, precios y límites de los planes.
users_latam.csv: información de clientes, como edad, ciudad, fecha de registro y plan.
usage.csv: registros de uso, incluidas llamadas y mensajes.
Herramientas: Python, Jupyter Notebook, pandas, NumPy, seaborn y Matplotlib.
