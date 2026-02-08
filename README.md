# Estadística para Data Science

Este proyecto aborda un análisis estadístico completo aplicado a un *dataset* de salud relacionado con el riesgo de cáncer de pulmón, combinando **análisis descriptivo**, **inferencia estadística**, **modelado predictivo** y **series temporales**.  
El objetivo principal es comprender los datos, evaluar relaciones estadísticas entre variables y aplicar distintos modelos según el tipo de problema.

---

## Estructura del Proyecto

### PARTE 1: Análisis Descriptivo (Dataset Propio)

**1.1 Carga y Vista General**  
Se realiza la carga del *dataset* y una inspección inicial para entender su estructura, tipos de variables y posibles valores faltantes.

**1.2 Clasificación de Variables**  
Las variables se clasifican según su naturaleza:
- Binarias
- Discretas
- Ordinales

Esta clasificación permite aplicar correctamente técnicas estadísticas y visualizaciones adecuadas.

**1.3 Estadísticos Descriptivos**  
Se analizan medidas de tendencia central y dispersión (media, mediana, desviación estándar, cuartiles), prestando especial atención a distribuciones sesgadas y presencia de valores extremos.

**1.4 Detección de Outliers**  
Se emplean diagramas de caja (*boxplots*) y métricas robustas para identificar valores extremos.

**1.5 Visualización de Distribuciones**  
Se visualizan las distribuciones de las variables para corroborar valores observados anterioremente de normalidad, asimetría y curtosis.

---

### PARTE 2: Inferencia y Modelado (Dataset Propio)

**2.1 Análisis de Correlación**  
Se estudian relaciones entre variables y, en particular, se aplican **tests estadísticos de independencia** para determinar si existe una relación estadísticamente significativa entre variables categóricas y la variable objetivo binaria.

**2.2 Relaciones Bivariantes**  
Se analizan relaciones entre pares de variables mediante *scatterplots* y visualizaciones condicionadas por la variable objetivo, extrayendo patrones relevantes.

**2.3 Regresión Lineal (Scikit-Learn)**  
Se plantea un modelo de regresión lineal entre dos variables continuas:
- Se distingue explícitamente entre **inferencia** (interpretación de coeficientes, significancia estadística) y **predicción** (evaluación del error predictivo).
- Se verifican las suposiciones del modelo y se discute su impacto sobre la inferencia y la predicción.

**2.4 Regresión Logística**  
Se aborda un problema de **clasificación**, comparando conceptualmente regresión lineal vs regresión logística:
- Se entrena un modelo logístico con dos variables (una explicativa y la variable objetivo binaria) para contrastar metodologías.
- Se evalúa el rendimiento mediante *Precision*, *Recall* y *F1-score*.
- Se entrena un segundo modelo usando todas las avriables, sanaliza el posible sobreajuste comparando métricas en *train* y *test* y la importacia de cada variable.

**2.5 Regresión Lineal vs Regresión Logística**  
Se comparan ambos enfoques destacando:
- Diferencias entre problemas de regresión y clasificación.
- Diferencias en métricas, objetivos y supuestos de los modelos.

---

### PARTE 3: Regresión Lineal “From Scratch” (Dataset Propio)

Se implementa manualmente un modelo de regresión lineal mediante un procedimiento iterativo (descenso de gradiente):
- Cálculo explícito de coeficientes.
- Comparación de resultados con el modelo de `scikit-learn` basado en **OLS**.
- Discusión sobre convergencia, interpretabilidad y equivalencia de resultados.

---

### PARTE 4: Series Temporales (Datos Simulados)

Se trabaja con una serie temporal simulada:
- Aplicación de **medias móviles** con distintos periodos para suavizar la señal y analizar la tendencia.
- **Descomposición de la serie temporal** en tendencia, estacionalidad y residuo.
- Interpretación de cada componente y justificación de la utilidad de estas técnicas para el análisis temporal.

