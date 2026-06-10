# 💻Experimento A/B — Landing Page

Análisis estadístico de un experimento A/B sobre dos versiones de una página de inicio, orientado a respaldar una decisión de negocio basada en datos.

---

## 📋 Descripción del proyecto

Este proyecto evalúa el rendimiento de dos versiones de una landing page (A y B) a partir de datos de 40,000 usuarios expuestos durante enero de 2026. El análisis compara la tasa de conversión, el gasto promedio y el comportamiento según fuente de tráfico y tipo de usuario, aplicando pruebas estadísticas para validar cada conclusión.

---

## 📁 Estructura del repositorio

```
├── Proyecto_Landing_Experiment_A_B.ipynb   # Notebook principal con el análisis completo
├── landing_experiment.csv                  # Dataset del experimento (no incluido)
└── README.md
```

---

## 📊 Dataset

El archivo `landing_experiment.csv` contiene las siguientes columnas:

| Columna | Descripción |
|---|---|
| `user_id` | Identificador único del usuario |
| `date` | Fecha de exposición a la landing page |
| `landing` | Versión de la página mostrada (A o B) |
| `region` | Región geográfica del usuario |
| `dispositivo` | Tipo de dispositivo utilizado |
| `traffic_source` | Canal de adquisición (Organic, Email, Ads, Referral) |
| `user_type` | Tipo de usuario (Nuevo o Recurrente) |
| `converted` | Indica si el usuario realizó una conversión (0/1) |
| `gasto` | Monto gastado (0 si no convirtió) |

- **Total de registros:** 40,000
- **Período:** 1 al 28 de enero de 2026
- **Balance del experimento:** Página A (19,982 usuarios) / Página B (20,018 usuarios)

---

## 🔬 Metodología

El análisis sigue una secuencia progresiva de seis pasos:

1. **Carga y validación de datos** — revisión de tipos, nulos, duplicados y calidad general.
2. **Gasto promedio (A vs B)** — prueba de Levene + prueba t de Student (Welch).
3. **Tasa de conversión (A vs B)** — prueba z de proporciones.
4. **Fuente de tráfico y conversión** — prueba Chi-cuadrada de independencia.
5. **Tipo de usuario y conversión** — prueba Chi-cuadrada de independencia.
6. **Visualización de resultados** — gráficos de volumen y proporciones por segmento.

Nivel de significancia utilizado: **α = 0.05**

---

## 📈 Resultados principales

### Página A vs Página B

| Métrica | Página A | Página B | Diferencia |
|---|---|---|---|
| Tasa de conversión | 12.57% | 15.96% | +3.39 pp ✅ |
| Gasto promedio por cliente | $61.09 | $68.75 | +$7.66 ✅ |

Ambas diferencias son **estadísticamente significativas** (p < 0.0001).

### Fuente de tráfico

| Canal | Tasa de conversión |
|---|---|
| Email | ~15.0% |
| Ads | ~14.7% |
| Organic | Menor tasa, mayor volumen absoluto |
| Referral | Tasa más baja |

Existe asociación significativa entre fuente de tráfico y conversión (χ² = 8.66, p = 0.034).

### Tipo de usuario

Las tasas de conversión de Nuevos (14.36%) y Recurrentes (14.09%) son prácticamente idénticas. **No se encontró asociación significativa** (p = 0.474).

---

## 💡 Recomendaciones

1. **Implementar la Página B.** Supera a la A en conversión y en gasto promedio por cliente.
2. **Priorizar Email y Ads** en la estrategia de adquisición por su mayor tasa de conversión relativa.
3. **Mantener Organic** como fuente de volumen de conversiones absolutas.
4. **No es necesario personalizar la experiencia** por tipo de usuario; la landing funciona de manera uniforme para nuevos y recurrentes.

---

## 🛠️ Tecnologías utilizadas

- Python 3
- pandas
- numpy
- matplotlib
- seaborn
- scipy (ttest_ind, levene, chi2_contingency)
- statsmodels (proportions_ztest)

---

## ▶️ Cómo ejecutar el proyecto

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/landing-ab-experiment.git
   cd landing-ab-experiment
   ```

2. Instala las dependencias:
   ```bash
   pip install pandas numpy matplotlib seaborn scipy statsmodels
   ```

3. Coloca el archivo `landing_experiment.csv` en la ruta `/datasets/landing_experiment.csv` o ajusta la ruta en el notebook.

4. Abre y ejecuta el notebook:
   ```bash
   jupyter notebook Proyecto_Landing_Experiment_A_B.ipynb
   ```
