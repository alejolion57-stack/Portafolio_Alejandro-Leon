# 📡 Análisis de Clientes — ConnectaTel

> Proyecto de análisis de datos desarrollado como parte del bootcamp de Analista de Datos de **TripleTen**.

---

## 🎯 Objetivo del Proyecto

Evaluar el comportamiento de los clientes de **ConnectaTel**, una empresa de telecomunicaciones en Latinoamérica, con datos registrados hasta el año 2024.

El análisis busca:
- Construir un **perfil estadístico** de los clientes.
- Detectar **comportamientos atípicos** (outliers y sentinels).
- Crear **segmentos de clientes** por edad y nivel de uso.
- Identificar **patrones de consumo** para diseñar estrategias de retención y mejoras en los planes.

---

## 🗂️ Datasets Utilizados

| Archivo | Descripción |
|---|---|
| `plans.csv` | Información de los planes disponibles: precio, minutos incluidos, GB incluidos y costo por extras. |
| `users_latam.csv` | Información de los clientes: edad, ciudad, fecha de registro, plan contratado y estado de churn. |
| `usage.csv` | Detalle del uso real de los servicios: llamadas, mensajes y duración. |

Los archivos se encuentran en la ruta `/datasets/` dentro del entorno de ejecución.

---

## 🔬 Etapas del Análisis

**Paso 1 — Carga y exploración**
Carga de los tres datasets, revisión de estructura, columnas y tipos de datos.

**Paso 2 — Identificación de problemas de calidad**
Detección de valores nulos, sentinels (valores inválidos como `-999` en `age` y `"?"` en `city`) y fechas imposibles (`reg_date` con año 2026).

**Paso 3 — Limpieza básica**
Corrección de sentinels por la mediana, reemplazo de ciudades inválidas por `NaN`, marcado de fechas fuera de rango como `NaT`, y verificación de valores MAR (Missing At Random) en `duration` y `length`.

**Paso 4 — Estadísticas de uso por usuario**
Agregación del dataset `usage` por `user_id` para calcular total de mensajes, llamadas y minutos. Integración con el dataset de usuarios en `user_profile`.

**Paso 5 — Visualización y outliers**
Histogramas de `age`, `cant_mensajes`, `cant_llamadas` y `cant_minutos_llamada` con diferenciación por plan (Básico vs. Premium). Análisis del método IQR para decisión sobre outliers.

**Paso 6 — Segmentación de clientes**
Creación de dos columnas de segmentación usando `np.where`:
- `grupo_edad`: Joven / Adulto / Adulto Mayor
- `grupo_uso`: Bajo uso / Uso medio / Alto uso

**Paso 7 — Insight ejecutivo**
Síntesis de hallazgos en formato ejecutivo con problemas detectados, caracterización de segmentos y recomendaciones accionables para el negocio.

---

## ▶️ Cómo Ejecutar el Notebook

### Google Colab 

1. Abre el siguiente enlace:  
   👉 [Abrir en Google Colab](https://colab.research.google.com/github/alejolion57-stack/Portafolio_Alejandro-Leon/blob/main/telecom-analysis.ipynb)


### Repositorio en Github

 👉 [Abrir en Github](https://github.com/alejolion57-stack/Portafolio_Alejandro-Leon/blob/main/telecom-analysis.ipynb)


## 🔁 Guía de Reproducción

1. Asegúrate de contar con los tres archivos CSV en la ruta correcta (`/datasets/` o `/content/` según el entorno).
2. Ejecuta las celdas **en orden secuencial** — cada paso depende del anterior.
3. Las librerías requeridas son: `pandas`, `numpy`, `matplotlib` y `seaborn`. Todas están disponibles por defecto en Google Colab.
4. El notebook no requiere claves de API ni conexiones externas.
5. Los resultados incluyen gráficos interactivos y tablas de resumen al final de cada sección.

---

## 🛠️ Tecnologías Usadas

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Jupyter Notebook`

---

## 👤 Autor

**Alejandro León**  
[GitHub](https://github.com/alejolion57-stack) · Bootcamp Analista de Datos — TripleTen
