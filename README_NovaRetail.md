# 🛒 Análisis de Comportamiento de Clientes — NovaRetail+

---

## 🎯 Objetivo del Proyecto

NovaRetail+ es una plataforma de comercio electrónico en Latinoamérica con millones de usuarios. Para el cierre de 2024, el equipo de **Crecimiento y Retención** planteó la siguiente pregunta de negocio:

**¿Qué factores del comportamiento del cliente están más fuertemente asociados con el ingreso anual generado?**

El análisis es de tipo **correlacional (exploratorio)** — identifica patrones y asociaciones entre variables, pero no establece relaciones de causalidad.

---

## 🗂️ Dataset Utilizado

| Archivo | Descripción |
|---|---|
| `novaretail_comportamiento_clientes_2024.csv` | Dataset con 15,000 registros y 12 columnas que describen el perfil y comportamiento de cada cliente durante 2024. |

### Variables del dataset

| Variable | Tipo | Descripción |
|---|---|---|
| `id_cliente` | Categórica | Identificador único del cliente |
| `edad` | Numérica | Edad del cliente |
| `nivel_ingreso` | Numérica | Ingreso anual estimado del cliente |
| `visitas_mes` | Numérica | Número de visitas al sitio/app por mes |
| `compras_mes` | Numérica | Número de compras realizadas por mes |
| `gasto_publicidad_dirigida` | Numérica | Inversión publicitaria asignada al usuario |
| `satisfaccion` | Numérica | Calificación de satisfacción (escala 1–5) |
| `miembro_premium` | Binaria | 1 si tiene suscripción premium, 0 si no |
| `abandono` | Binaria | 1 si abandonó la plataforma, 0 si no |
| `tipo_dispositivo` | Categórica | Móvil, escritorio o tablet |
| `region` | Categórica | Norte, sur, este u oeste |
| `ingreso_anual` | Numérica | **Variable objetivo** — ingreso generado para la empresa |

---

## 🔬 Etapas del Análisis

**Sección 1 — Carga y exploración inicial**
Carga del dataset, revisión de estructura, tipos de datos y valores faltantes. El dataset no presentó nulos.

**Sección 2 — Preparación de datos y supuestos**
Corrección del tipo de dato de `edad` (de `float64` a `int64`). Clasificación de variables en numéricas, binarias y categóricas. Documentación de supuestos metodológicos: uso de Pearson para variables numéricas, Spearman para relaciones monótonas, correlación punto-biserial para variable numérica vs. binaria, y V de Cramér para variables categóricas.

**Sección 3 — Visualización de relaciones**
Heatmap de correlación general para identificar pares relevantes. Scatterplots focalizados en los tres pares con mayor asociación: `compras_mes` vs. `ingreso_anual`, `visitas_mes` vs. `ingreso_anual`, y `gasto_publicidad_dirigida` vs. `visitas_mes`. Se usó `miembro_premium` como variable de segmentación visual (hue).

**Sección 4 — Coeficientes de correlación**
Cálculo de coeficientes según tipo de variable: Pearson para pares numéricos, punto-biserial para relaciones con variables binarias (`miembro_premium`, `abandono`), y V de Cramér para `region` vs. `tipo_dispositivo`.

**Sección 5 — Interpretación de resultados para el negocio**
Cinco hallazgos documentados con evidencia visual, evidencia numérica, interpretación no causal e implicación de negocio concreta.

**Sección 6 — Limitaciones y próximos pasos**
Documentación de restricciones del análisis (colinealidad, variables discretas, membresía subrepresentada) y tres pasos accionables para profundizar el análisis.

---

## 📊 Principales Hallazgos

- **`compras_mes` es el factor más fuertemente asociado con `ingreso_anual`** (Pearson r ≈ 0.97), una relación casi perfecta que sugiere que ambas variables capturan el mismo constructo de valor del cliente.
- **`visitas_mes` tiene una correlación moderada con `ingreso_anual`** (r ≈ 0.34) — las visitas son necesarias pero no suficientes para generar ingreso.
- **`gasto_publicidad_dirigida` se asocia moderadamente con `visitas_mes`** (r ≈ 0.58) — la publicidad atrae tráfico, pero no garantiza conversión.
- **La membresía premium y el abandono no muestran asociación lineal con el ingreso anual** (punto-biserial ≈ 0), lo que sugiere que el modelo premium requiere revisión estratégica.
- **Región y tipo de dispositivo son variables independientes** (V de Cramér ≈ 0.01) — no se requiere diferenciación de UX por zona geográfica.

---

## ▶️ Cómo Ejecutar el Notebook

### Opción A — Google Colab (recomendado)

1. Abre el notebook directamente:  
   👉 [Abrir en Google Colab](https://colab.research.google.com/github/alejolion57-stack/Portafolio_Alejandro-Leon/blob/main/Proyecto_NovaRetail.ipynb)

2. Sube el archivo CSV al entorno de Colab:
   ```python
   from google.colab import files
   files.upload()  # Sube novaretail_comportamiento_clientes_2024.csv
   ```

3. Ajusta la ruta de carga en la primera celda:
   ```python
   df = pd.read_csv('novaretail_comportamiento_clientes_2024.csv')
   ```

4. Ejecuta todas las celdas con **Runtime → Run all**.

### Opción B — Entorno local (Jupyter)

1. Clona el repositorio:
   ```bash
   git clone https://github.com/alejolion57-stack/Portafolio_Alejandro-Leon.git
   cd Portafolio_Alejandro-Leon
   ```

2. Instala las dependencias:
   ```bash
   pip install pandas numpy matplotlib seaborn scipy jupyter
   ```

3. Abre el notebook:
   ```bash
   jupyter notebook Proyecto_NovaRetail.ipynb
   ```

---

## 🔁 Guía de Reproducción

1. Asegúrate de tener el archivo `novaretail_comportamiento_clientes_2024.csv` disponible en la ruta correcta.
2. Ejecuta las celdas **en orden secuencial** — cada sección depende de la anterior.
3. Las librerías requeridas son: `pandas`, `numpy`, `matplotlib`, `seaborn` y `scipy`. Todas están preinstaladas en Google Colab.
4. El notebook no requiere conexiones externas ni claves de API.
5. Los resultados incluyen un heatmap, tres scatterplots con línea de tendencia y tablas de coeficientes al final de cada sección analítica.

---

## 🛠️ Tecnologías Usadas

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `SciPy` · `Jupyter Notebook`

---

## 👤 Autor

**Alejandro León**  
[GitHub](https://github.com/alejolion57-stack) · Bootcamp Analista de Datos — TripleTen
