[README.md](https://github.com/user-attachments/files/28814504/README.md)

---

**Soy Alejandro León** 
-

Un director creativo con pasíon por el análisis de datos. Un analista de datos con experiencia en estrategia y creatividad. 

---

**🛠️ Así va mi stack técnico**
-
<div align="leftd">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Google Sheets](https://img.shields.io/badge/Google%20Sheets-34A853?style=flat&logo=google-sheets&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=mysql&logoColor=white)

---

## 📁 Proyectos del bootcamp con Tripleten
Soy apenas un aprendiz en el mundo de la sitematización para análisis de datos y estos son mis primeros pinos:

### 📊 Análisis de eficiencia de ventas — Walmart
`Google Sheets` &nbsp;·&nbsp; `Tablas dinámicas` &nbsp;·&nbsp; `KPIs`

**Objetivo del proyecto:** Optimización de presupuesto e inventario mediante análisis de eficiencia de tiendas, participación de departamentos y volatilidad de ventas en 2012.

**KPIs desarrollados:**
- Eficiencia: ventas por metro cuadrado
- Participación: % de ventas por departamento
- Riesgo: coeficiente de variación (volatilidad)

**Resultado clave:** Identificación de tiendas 25% más eficientes y recomendaciones de redistribución de inventario.

---

### 📊 Análisis de eficiencia de ventas — Walmart
🛒 Optimización de embudo de conversión — E-commerce
`SQL` &nbsp;·&nbsp; `CTEs` &nbsp;·&nbsp; `Funnel Analysis`

**Objetivo del proyecto:** Análisar el customer journey completo desde primera visita hasta compra para identificar puntos de fuga en el embudo de conversión.

**Etapas del análisis:**
1. Descubrimiento (`first_visit`)
2. Interés (`select_item` / `select_promotion`)
3. Conversión (compra)

**Resultado clave:** Identificación de los principales puntos de abandono para optimizar la experiencia de compra.

---

### 🌍 Monitoreo automatizado de PM2.5 — Latinoamérica
`Python` &nbsp;·&nbsp; `Pandas` &nbsp;·&nbsp; `Jupyter Notebook`

**Objetivo del proyecto:** Automatización de reportes mensuales de niveles de contaminación PM2.5 por país en Latinoamérica para equipos de monitoreo ambiental.

**Etapas del análisis:**
1. Carga y exploración de datasets
2. Limpieza de valores faltantes y duplicados
3. Cálculo de métricas (máx, mín, promedio) por país
4. Documentación paso a paso en Notebook

**Resultado clave:** Reducción del tiempo de análisis de horas a minutos · proceso reproducible y documentado.

---
### 📡 Análisis de clientes — ConnectaTel
`Python` &nbsp;·&nbsp; `Pandas` &nbsp;·&nbsp; `Jupyter Notebook`; `NumPy`; `Matplotlib`; `Seaborn`; `Jupyter Notebook`


**Objetivo del proyecto:** Evaluar el comportamiento de los clientes de ConnectaTel, una empresa de telecomunicaciones en Latinoamérica, con datos registrados hasta el año 2024.

**Etapas del análisis:**
1. Carga y exploración Carga de los tres datasets, revisión de estructura, columnas y tipos de datos.

2. Identificación de problemas de calidad Detección de valores nulos, sentinels (valores inválidos como -999 en age y "?" en city) y fechas imposibles (reg_date con año 2026).

3. Limpieza básica Corrección de sentinels por la mediana, reemplazo de ciudades inválidas por NaN, marcado de fechas fuera de rango como NaT, y verificación de valores MAR (Missing At Random) en duration y length.

4. Estadísticas de uso por usuario Agregación del dataset usage por user_id para calcular total de mensajes, llamadas y minutos. Integración con el dataset de usuarios en user_profile.

5. Visualización y outliers Histogramas de age, cant_mensajes, cant_llamadas y cant_minutos_llamada con diferenciación por plan (Básico vs. Premium). Análisis del método IQR para decisión sobre outliers.

6. Segmentación de clientes Creación de dos columnas de segmentación 

**Resultados:** 
Análisis segmentado (edad - uso) y recomendaciones con posibles acciones de comunicación y promoción para  las gerencias de Mercadeo y Comercial.

---
### 🛒 Análisis de Comportamiento de Clientes — NovaRetail+
`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `SciPy` · `Jupyter Notebook`

**Objetivo del Proyecto:** NovaRetail+ es una plataforma de comercio electrónico en Latinoamérica con millones de usuarios. Para el cierre de 2024, el equipo de **Crecimiento y Retención** planteó la siguiente pregunta de negocio:***¿Qué factores del comportamiento del cliente están más fuertemente asociados con el ingreso anual generado?***

El análisis es de tipo **correlacional (exploratorio)** — identifica patrones y asociaciones entre variables, sin establecer relaciones de causalidad.

---

**Etapas del análisis:**
1. **Carga y exploración inicial:** Carga del dataset, revisión de estructura, tipos de datos y valores faltantes. El dataset no presentó nulos.

2. **Preparación de datos y supuestos:** Corrección del tipo de dato de `edad` (de `float64` a `int64`). Clasificación de variables en numéricas, binarias y categóricas. Documentación de supuestos metodológicos: uso de Pearson para variables numéricas, Spearman para relaciones monótonas, correlación punto-biserial para variable numérica vs. binaria, y V de Cramér para variables categóricas.

3. **Visualización de relaciones:** Heatmap de correlación general para identificar pares relevantes. Scatterplots focalizados en los tres pares con mayor asociación: `compras_mes` vs. `ingreso_anual`, `visitas_mes` vs. `ingreso_anual`, y `gasto_publicidad_dirigida` vs. `visitas_mes`. Se usó `miembro_premium` como variable de segmentación visual (hue).

4. **Coeficientes de correlación:** Cálculo de coeficientes según tipo de variable: Pearson para pares numéricos, punto-biserial para relaciones con variables binarias (`miembro_premium`, `abandono`), y V de Cramér para `region` vs. `tipo_dispositivo`.

5. **Interpretación de resultados para el negocio:** Cinco hallazgos documentados con evidencia visual, evidencia numérica, interpretación no causal e implicación de negocio concreta.

6. **Limitaciones y próximos pasos:** Documentación de restricciones del análisis (colinealidad, variables discretas, membresía subrepresentada) y tres pasos accionables para profundizar el análisis.

---

**Principales Hallazgos:**
- **`compras_mes` es el factor más fuertemente asociado con `ingreso_anual`** (Pearson r ≈ 0.97), una relación casi perfecta que sugiere que ambas variables capturan el mismo constructo de valor del cliente.
- **`visitas_mes` tiene una correlación moderada con `ingreso_anual`** (r ≈ 0.34) — las visitas son necesarias pero no suficientes para generar ingreso.
- **`gasto_publicidad_dirigida` se asocia moderadamente con `visitas_mes`** (r ≈ 0.58) — la publicidad atrae tráfico, pero no garantiza conversión.
- **La membresía premium y el abandono no muestran asociación lineal con el ingreso anual** (punto-biserial ≈ 0), lo que sugiere que el modelo premium requiere revisión estratégica.
- **Región y tipo de dispositivo son variables independientes** (V de Cramér ≈ 0.01) — no se requiere diferenciación de UX por zona geográfica.

---
# 💻 Experimento A/B — Landing Page
`Python 3`·`pandas` · `numpy` · `matplotlib` · `seaborn` ·`scipy (ttest_ind, levene, chi2_contingency)` ·`statsmodels (proportions_ztest)`


**📋 Descripción del proyecto:** Este proyecto evalúa el rendimiento de dos versiones de una landing page (A y B) a partir de datos de 40,000 usuarios expuestos durante enero de 2026. El análisis compara la tasa de conversión, el gasto promedio y el comportamiento según fuente de tráfico y tipo de usuario, aplicando pruebas estadísticas para validar cada conclusión.

---

**Etapas del análisis:** 
1. **Carga y validación de datos** — revisión de tipos, nulos, duplicados y calidad general.
2. **Gasto promedio (A vs B)** — prueba de Levene + prueba t de Student (Welch).
3. **Tasa de conversión (A vs B)** — prueba z de proporciones.
4. **Fuente de tráfico y conversión** — prueba Chi-cuadrada de independencia.
5. **Tipo de usuario y conversión** — prueba Chi-cuadrada de independencia.
6. **Visualización de resultados** — gráficos de volumen y proporciones por segmento.

Nivel de significancia utilizado: **α = 0.05**

---

## 📈 Resultados principales

**Página A vs Página B**

| Métrica | Página A | Página B | Diferencia |
|---|---|---|---|
| Tasa de conversión | 12.57% | 15.96% | +3.39 pp ✅ |
| Gasto promedio por cliente | $61.09 | $68.75 | +$7.66 ✅ |

Ambas diferencias son **estadísticamente significativas** (p < 0.0001).

**Fuente de tráfico**

| Canal | Tasa de conversión |
|---|---|
| Email | ~15.0% |
| Ads | ~14.7% |
| Organic | Menor tasa, mayor volumen absoluto |
| Referral | Tasa más baja |

**Existe asociación significativa** entre fuente de tráfico y conversión (χ² = 8.66, p = 0.034).

**Tipo de usuario:** Las tasas de conversión de Nuevos (14.36%) y Recurrentes (14.09%) son prácticamente idénticas. **No se encontró asociación significativa** (p = 0.474).

---

**💡 Recomendaciones:**
1. **Implementar la Página B.** Supera a la A en conversión y en gasto promedio por cliente.
2. **Priorizar Email y Ads** en la estrategia de adquisición por su mayor tasa de conversión relativa.
3. **Mantener Organic** como fuente de volumen de conversiones absolutas.
4. **No es necesario personalizar la experiencia** por tipo de usuario; la landing funciona de manera uniforme para nuevos y recurrentes.


---

**Contacto**
-
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Alejandro%20León-0077B5?style=for-the-badge&logo=linkedin&logoColor=1E293B)](https://www.linkedin.com/in/alejandrole%C3%B3nospina/)
[![Email](https://img.shields.io/badge/Email-alejolion57%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:alejolion57@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Portafolio-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/alejolion57-stack)
