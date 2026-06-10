# 🌫️ Monitoreo Automatizado de PM2.5 — Latinoamérica

Análisis de contaminación atmosférica y congestión urbana en ciudades latinoamericanas, integrando datos de tráfico e indicadores económicos para apoyar decisiones de inversión en movilidad e infraestructura.

---

## 📋 Descripción del proyecto

Este proyecto automatiza el monitoreo mensual de niveles de contaminación PM2.5 por país en Latinoamérica, y los cruza con datos de tráfico y PIB per cápita para identificar patrones entre movilidad urbana y productividad económica. El análisis se centra en el año 2024 y permite reducir el tiempo de generación de reportes de horas a minutos.

**Objetivos:**
- Obtener una vista consolidada del tráfico promedio por ciudad y año para analizar patrones generales.
- Automatizar reportes mensuales de niveles de PM2.5 por país para el equipo de monitoreo ambiental.

---

## 📁 Estructura del repositorio

```
├── Análisis_contaminación_atmosférica.ipynb   # Notebook principal con el análisis completo
├── datasets/
│   ├── traffic.csv                            # Datos de tráfico urbano por ciudad
│   └── eco.csv                                # Indicadores económicos y ambientales por ciudad
└── README.md
```

---

## 📊 Datasets

### Dataset de Tráfico (`traffic`)
Registros de congestión urbana con múltiples entradas por ciudad. Variables clave:

| Columna | Descripción |
|---|---|
| `city` | Ciudad |
| `year` | Año del registro |
| `jams_delay` | Minutos de retraso por congestión |
| `UpdateTimeUTC` | Fecha/hora de actualización (convertida a datetime) |

### Dataset Económico y Ambiental (`eco`)
Indicadores anuales por ciudad. Variables clave:

| Columna | Descripción |
|---|---|
| `city` | Ciudad |
| `year` | Año |
| `city_gdp_capita` | PIB per cápita (convertido a float64) |
| `unemployment_pct` | Tasa de desempleo (convertida a float64) |
| `pm25` | Niveles de PM2.5 en μg/m³ (convertido a float64) |
| `population_m` | Población en millones (convertida a float64) |

---

## 🛠️ Metodología

El análisis sigue cinco pasos principales:

1. **Carga y exploración** de los datasets `traffic` y `eco`.
2. **Limpieza y transformación de datos:**
   - Conversión de columnas de fecha a `datetime`.
   - Eliminación del símbolo `%` en `unemployment_pct` y conversión a `float64`.
   - Cambio de coma a punto decimal en `pm25`.
   - Estandarización de nombres de columnas.
   - Validación de valores nulos.
3. **Filtrado** al año 2024 para trabajar con el período más reciente y relevante.
4. **Agregación:** cálculo de promedios anuales por ciudad para simplificar el análisis.
5. **Integración:** merge entre `traffic` y `eco` usando `city` y `year` como claves, conservando solo los registros presentes en ambos datasets.

---

## 📈 Visualizaciones

Se generaron tres tipos de gráficos para respaldar los hallazgos:

- **Boxplot** — distribución de minutos de congestión (`jams_delay`) por ciudad.
- **Histograma** — distribución del PIB per cápita entre ciudades en 2024.
- **Gráfico de barras** — comparación de `jams_delay` y `city_gdp_capita` por ciudad.

---

## 🔍 Hallazgos principales

1. **Relación inversa entre congestión y PIB:** a mayor congestión (retrasos, índices de tráfico), menor PIB per cápita en términos generales.
2. **Ciudades latinoamericanas críticas:** Bogotá, Lima y Ciudad de México concentran los niveles más altos de congestión con menor productividad relativa.
3. **Ciudades desarrolladas como referente:** Londres, Berlín y Tokio muestran mejor balance entre movilidad y productividad, con PIB per cápita elevado incluso con tráfico moderado.
4. **Ciudad de México — caso especial:** congestión extremadamente alta pero con un PIB per cápita no tan bajo, posiblemente por su escala económica y centralización.
5. **Buenos Aires:** congestión media-alta con un PIB relativamente alto dentro de la región, lo que sugiere mayor resiliencia económica o mejor infraestructura relativa.
6. **México:** identificado como el país con niveles más críticos de PM2.5 en la región.

---

## 💡 Recomendaciones

### Ciudades prioritarias para inversión

| Prioridad | Ciudad | Situación |
|---|---|---|
| 🔴 Alta | Bogotá y Lima | Alta congestión + baja productividad. Impacto negativo directo del tráfico sobre el desempeño económico. |
| 🟡 Media | Ciudad de México | Escala crítica: mejoras pequeñas generan beneficios masivos. |
| 🟢 Optimización | Buenos Aires | Mantener eficiencia del sistema actual y evitar deterioro. |

### Propuestas de inversión
- **Transporte público masivo:** metro, BRT y corredores troncales.
- **Infraestructura vial inteligente:** semáforos adaptativos y gestión en tiempo real.
- **Gestión de demanda:** políticas de teletrabajo y descentralización urbana.

### Análisis adicionales recomendados
- Modelos de regresión para cuantificar el impacto del tráfico sobre el PIB.
- Series de tiempo para identificar tendencias de largo plazo.
- Incorporación de variables estructurales: informalidad laboral, uso de transporte público e inversión en infraestructura.
- Validar que el PIB esté ajustado por paridad de poder adquisitivo (PPA) para evitar comparaciones sesgadas.

---

## ✅ Resultados técnicos

- Reporte automatizado que reduce el tiempo de análisis de horas a minutos.
- Identificación de México como el país con niveles más críticos de PM2.5.
- Proceso estandarizado, reproducible y documentado.

---

## 🛠️ Tecnologías utilizadas

- Python 3
- pandas
- matplotlib
- seaborn
- Jupyter Notebook

---

## ▶️ Cómo ejecutar el proyecto

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/monitoreo-pm25-latam.git
   cd monitoreo-pm25-latam
   ```

2. Instala las dependencias:
   ```bash
   pip install pandas matplotlib seaborn jupyter
   ```

3. Coloca los archivos de datos en la carpeta `datasets/`.

4. Abre y ejecuta el notebook:
   ```bash
   jupyter notebook Análisis_contaminación_atmosférica.ipynb
   ```

---

## 📬 Contacto

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/tu-usuario)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:tu@email.com)
