# 🍔 Perfil de consumidor — Food Delivery 🍕

`Python` · `Pandas` · `Google Colab` · `Power BI`

**Notebook:** [Perfil_de_consumidor_food_delivery.ipynb](https://github.com/alejolion57-stack/Portafolio_Alejandro-Leon/blob/main/Perfil_de_consumidor_food_delivery.ipynb)

---

## 📋 Descripción del proyecto

Este proyecto construye el **perfil de cliente** de un e-commerce de comida a domicilio a partir de un dataset de Kaggle con información demográfica y de satisfacción. El trabajo cubre la exploración inicial, la limpieza del dataset en Python y el diseño de un **dashboard en Power BI** con tres tableros que dan una radiografía del consumidor, su demografía y su grado de satisfacción con la marca.

## 🎯 Objetivo

Identificar quiénes son los clientes (edad, género, ocupación, escolaridad, ingresos) y qué tan satisfechos están, para apoyar decisiones de segmentación y comunicación.

## 📂 Dataset

- **Fuente:** Kaggle *(agrega aquí el enlace exacto al dataset)*
- **Original:** 388 filas × 14 columnas
- **Después de la limpieza:** 285 filas × 11 columnas

| Columna | Descripción |
|---|---|
| `Age` | Edad del cliente |
| `Gender` | Género (Male / Female) |
| `Marital Status` | Estado civil (Single, Married, Prefer not to say) |
| `Occupation` | Ocupación (Student, Employee, Self Employed, Housewife) |
| `Monthly Income` | Rango de ingreso mensual (rupias) |
| `Educational Qualifications` | Nivel educativo (School, Graduate, Post Graduate, Ph.D, Uneducated) |
| `Family size` | Tamaño del hogar |
| `Customer Type` | Tipo de cliente (New, Regular, Frequent) |
| `Pin code` | Código postal |
| `Output` | Resultado del pedido (Yes / No) |
| `Feedback` | Valoración del cliente (Positive / Negative) |

## 📊 KPIs definidos

- Edad promedio de clientes
- Ocupación
- Escolaridad
- Distribución por género
- Ingreso promedio vs. educación
- Tipo de cliente vs. ingreso mensual
- Tipo de cliente vs. *feedback*
- Grado de satisfacción por edad, género y nivel de ingresos

## 🔎 Etapas del análisis

1. **Exploración inicial:** revisión de estructura, tipos de datos, nulos y duplicados (`head`, `info`, `isnull`, `duplicated`).
2. **Limpieza del dataset:**
   - Eliminación de **103 filas duplicadas** (≈ 26,5 %), por ejemplo los índices 205, 332 y 348. Se pasó de 388 a 285 registros.
   - Validación del **código postal**: conversión a texto y verificación del formato de 6 dígitos (`\d{6}`).
   - Eliminación de columnas innecesarias: `Unnamed: 13` (error) y `latitude` / `longitude`.
   - Estandarización de `Occupation`: `Self Employeed` → `Self Employed` y `House wife` → `Housewife`.
   - Validación de variables categóricas con `value_counts()`.
3. **Exportación** del dataset limpio a `perfil food delivery limpio.csv` (`utf-8-sig`) para el dashboard.
4. **Dashboard en Power BI** con tres tableros: General, Demografía *(ajusta el nombre)* y Satisfacción.

<!-- Sube tus capturas a una carpeta /images y descomenta estas líneas
![Dashboard General](images/dashboard_general.png)
![Dashboard Demografía](images/dashboard_demografia.png)
![Dashboard Satisfacción](images/dashboard_satisfaccion.png)
-->

## 📈 Panorama del dataset limpio (285 clientes)

| Variable | Distribución |
|---|---|
| Género | Hombres 164 (57,5 %) · Mujeres 121 (42,5 %) |
| Ocupación | Estudiantes 144 · Empleados 94 · Independientes 38 · Amas de casa 9 |
| Educación | Graduate 126 · Post Graduate 125 · Ph.D 21 · School 11 · Uneducated 2 |
| Tipo de cliente | Regular 162 · Frecuente 105 · Nuevo 18 |
| Feedback | Positivo 231 (81 %) · Negativo 54 (19 %) |

## 💡 Resultado clave

Un dataset limpio y consistente, listo para análisis, y un dashboard de tres tableros que permite explorar el perfil demográfico del cliente y cruzarlo con su satisfacción.

## 🚀 Cómo reproducirlo

1. Descarga el dataset de Kaggle y guárdalo como `perfil food delivery.csv`.
2. Abre el notebook en [Google Colab](https://colab.research.google.com/) o Jupyter y sube el CSV.
3. Ejecuta las celdas en orden; al final se genera `perfil food delivery limpio.csv`.
4. Carga el CSV limpio en **Power BI Desktop** para construir o explorar el dashboard.

## 🧰 Herramientas

`Python 3` · `pandas` · `Google Colab` · `Power BI`

---

## Contacto

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Alejandro%20León-0077B5?style=for-the-badge&logo=linkedin&logoColor=1E293B)](https://www.linkedin.com/in/alejandrole%C3%B3nospina/)
[![Email](https://img.shields.io/badge/Email-alejolion57%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:alejolion57%40gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Portafolio-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/alejolion57-stack)
