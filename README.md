# Análisis Exploratorio de Datos (EDA) - Campañas de Marketing Bancario

## Descripción del Proyecto
Este proyecto realiza un análisis exploratorio de datos sobre campañas de marketing de una institución bancaria. El objetivo es identificar patrones de comportamiento de los clientes y factores determinantes para la suscripción de productos/servicios.

## Estructura del Repositorio
* `/datos/raw/`: Datasets originales sin modificar (.csv y .xlsx).
* `/datos/processed/`: Dataset final unificado y limpio (`dataset_banco_limpio.csv`).
* `/notebooks/`: Cuadernos de Jupyter (`01_Limpieza_y_Transformacion.ipynb`) con el código de importación, limpieza, análisis y visualización.

## Fases del Análisis y Metodología
1. **Unificación de datos:** Lectura y concatenación de datos demográficos de clientes (2012-2014) y cruce (Left Join) con los registros de campañas de marketing.
2. **Limpieza y transformación:** Gestión de valores nulos (imputación por la mediana para variables numéricas y 'unknown' para categóricas). Estandarización de formatos y corrección de tipos de datos.
3. **Análisis descriptivo:** Cálculo de estadísticos, detección de colinealidad en variables macroeconómicas y agrupación por segmentos.
4. **Visualización:** Generación de gráficos (Heatmap, Barplot e Histograma) con Matplotlib y Seaborn.

## Principales Hallazgos (Insights)
* **Ingresos vs Decisión:** No existe una diferencia significativa en el nivel de ingresos medio entre los clientes que contratan el producto y los que no, descartando el poder adquisitivo como factor principal de conversión.
* **Comportamiento Digital:** Existe un patrón de consumo web en forma de "U" respecto a la edad. Los perfiles con mayor número de visitas mensuales son los clientes de más de 60 años y los menores de 30 años.
* **Colinealidad Macroeconómica:** Los indicadores de tasa de empleo, IPC y euríbor presentan correlaciones positivas superiores a 0.75, fluctuando de forma conjunta según el ciclo económico.
