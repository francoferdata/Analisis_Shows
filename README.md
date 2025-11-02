# Análisis Exploratorio de Shows de TV Populares (EDA)

Este proyecto realiza un Análisis Exploratorio de Datos (EDA) sobre un dataset de 10,000 shows de TV populares extraídos de TMDb.

El objetivo principal es **entender las características de los programas de TV exitosos**, respondiendo a preguntas como:

¿De dónde vienen los shows más populares y cuándo se produjeron?

¿Qué define el "éxito"? ¿Es lo mismo ser "popular" que estar "bien calificado"?

¿Qué relación existe entre la popularidad, la calificación de la audiencia y el número de votos?

---

## Stack Tecnológico
* **Python y Pandas:** Para la manipulación y limpieza de datos.
* **Matplotlib y Seaborn:** Para la visualización de datos.
* **AST (Abstract Syntax Trees):** Para el procesamiento de columnas complejas (listas como strings).

---

## Flujo del Análisis
El notebook de Jupyter (`shows.ipynb`) sigue una estructura lógica:

**Limpieza y Procesamiento de Datos:** Manejo de duplicados (basado en `id`), conversión de fechas (`first_air_date`), y procesamiento de columnas complejas (como `origin_country` usando `ast`).

**Análisis Geográfico y Temporal:** Exploración del origen de los shows (país, idioma) y su evolución en el tiempo.

**Análisis de Métricas de Éxito:** Investigación de las variables `popularity`, `vote_average` y `vote_count` para definir y entender el éxito.

**Análisis Estadístico:** Revisión de estadísticas descriptivas y una matriz de correlación para cuantificar las relaciones entre las métricas.

---

## Hallazgos Clave

**Dominio de EE.UU. y Crecimiento Exponencial:** Estados Unidos domina abrumadoramente la producción de shows populares. Además, la producción de contenido ha experimentado un crecimiento exponencial desde 2010, coincidiendo con el auge de las plataformas de streaming.
<img width="505" height="249" alt="Captura de pantalla 2025-11-01 175126" src="https://github.com/user-attachments/assets/8b2d99de-27e5-4fb9-a6a2-f3f1a1172e80" />



**Popularidad vs. Calidad casi no están Correlacionadas:** El éxito no es unidimensional. El análisis de correlación (Pearson: **0.15**) demuestra que **ser "popular" no es lo mismo que ser "bien calificado"**. La relación es muy débil.

<img width="500" height="383" alt="Captura de pantalla 2025-11-01 175247" src="https://github.com/user-attachments/assets/4bf8248a-4d5a-44a5-ad8c-50a32833af82" />




**Popularidad y Votos tienen una Correlación Moderada:** La popularidad y el número de votos (`vote_count`) tienen una **correlación positiva moderada (0.49)**. Esto indica que, si bien no miden lo mismo, los shows más populares tienden a acumular más votos.

<img width="501" height="365" alt="Captura de pantalla 2025-11-01 175521" src="https://github.com/user-attachments/assets/30ba9533-1148-43c9-b9f4-a08e23bb77b8" />


