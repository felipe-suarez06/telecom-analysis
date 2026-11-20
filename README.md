**Título:**  Análisis de una empresa de telecomunicaciones (**ConnectaTel**)

 Una empresa de telecomunicaciones con operaciones en México y Colombia enfrentaba una incógnita: ¿estaban los planes actuales realmente alineados con el uso real de sus usuarios? La falta de visibilidad en los patrones de consumo impedía una segmentación efectiva.

- **Problema:** Tenía tres fuentes de datos heterogéneas (`plans`, `users`, `usage`) que requerían una integración y limpieza rigurosa antes de extraer cualquier insight fiable.
- **Qué hice:**
1. **Ingeniería de Datos:** No solo cargué los archivos; realicé una validación de calidad profunda. Detecté inconsistencias en las fechas y valores atípicos que, de no haberse tratado, habrían sesgado las medias de consumo.
2. **Análisis Exploratorio (EDA):** Más allá de calcular promedios, busqué correlaciones entre el comportamiento (llamadas/mensajes) y variables demográficas (edad/país).
3. **Segmentación Estratégica:** Clasifiqué a los usuarios no solo por su plan contratado, sino por su *comportamiento real*, lo cual reveló discrepancias clave entre la oferta y el uso.
- **Resultado:**
    - **Uso de los planes:** aproximadamente el 65% de los clientes eligió el plan Básico y el 35% el Premium.
    - **Edad y elección del plan:** la edad no parece ser un criterio útil para diferenciar la oferta; clientes de distintas edades eligen ambos planes, aunque el Básico es el más popular.
    
    **Calidad de los datos**
    
    - En `users`, la ciudad tenía 469 valores faltantes (11.73%).
    - En `usage`, `duration` tenía 22,076 valores faltantes (55.19%) y `length`, 17,896 (44.74%). Esto podría deberse a problemas de registro.
    - En `users`, la edad incluía 55 valores inválidos de `999` (1.3%), que se reemplazaron por la mediana.
    
    **Valores atípicos**
    
    Se observaron valores altos en mensajes, llamadas y minutos de llamada. En general, el plan Básico mostró más valores extremos; en minutos de llamada, también aparecieron llamadas especialmente largas en ese plan.
    
    **Decisión:** conservar estos valores, ya que son plausibles y pueden reflejar diferencias reales en el uso:
    
    - **Mensajes:** hasta 17, aunque el límite superior de referencia era 11.5.
    - **Llamadas:** hasta 15, frente a un límite superior de 10.5.
    - **Minutos de llamada:** hasta 155.69 minutos (unas 2.5 horas), frente a un límite superior de 61.86.
- **¿Qué demuestra esto?**

Este proyecto muestra mi capacidad para transformar datos crudos en recomendaciones de negocio, garantizando siempre la calidad y reproducibilidad del análisis.

- **🛠️ Skills:**
    - **Jupyter Notebook**
    - **Python**: `pandas`, `numpy`, `seaborn`, `matplotlib`
