# Monitoreo Automatizado de PM2.5 - Latinoamérica

## Objetivos
1. Obtener una vista consolidada del tráfico promedio por ciudad y año, para analizar patrones generales sin depender de datos diarios.
2. Automatizar reportes mensuales de niveles de contaminación PM2.5 por país en Latinoamérica para el equipo de monitoreo ambiental.

## Tecnologías
- Python, Pandas, Jupyter Notebook
- Limpieza y transformación de datos
- Análisis estadístico descriptivo

## Proceso
### Paso 1: Carga y exploración de datasets y librerias para graficar
 <img width="709" height="210" alt="Screen Shot 2026-05-05 at 3 54 03 PM" src="https://github.com/user-attachments/assets/732f7433-d897-4e94-b963-b1cc0446569b" />

### Descubrimiento premilimar : 
En la estructura del DF traffic, se observa que:
- Las columnas UpdateTimeUTC y UpdateTimeUTC son de tipo (object). Se deben cambiar a valores de tipo fecha (datetime)
- No se observan datos ausentes.

En la estructura del DF eco, se observa que:
- Las columnas City GDP/capita, Unemployment %, "PM2.5 (μg/m³)" y "Population (M)" estan con tipo texto (object) y ndecesitan ser remplazadas a tipo numérico, decimal (float64) para obtener un análisis realmente funcional.
- No se ven datos ausentes.
  
### Paso 2: Exploración y limpieza de datos en los dos DF "Traffic" y DF "Eco"
<img width="680" height="415" alt="Screen Shot 2026-05-05 at 3 57 03 PM" src="https://github.com/user-attachments/assets/2d5bdd56-b518-4dea-8db2-94375eab17bf" />
<img width="657" height="252" alt="Screen Shot 2026-05-05 at 3 57 34 PM" src="https://github.com/user-attachments/assets/20811bae-49a7-4d9e-a555-3c2798d0e132" />
 
  ### Otras acciones en el proceso de limpieza:
  Una vez descubiertos los factores a corregir, hice las correcciones para estandarizar 
  los formatos y hacelos más fáciles de comprender
   - Renombrando columnas a términos más claros
   - Corregir formatos numéricos para garantizar un análisis veraz
     
### Paso 3: Filtré la información del año 2004 para trabajar el período más reciente y relevante.
<img width="530" height="139" alt="Screen Shot 2026-05-06 at 10 23 26 AM" src="https://github.com/user-attachments/assets/c5dae44d-2428-463e-bd85-24b9a0522c92" />

### Paso 4: Resumir los datos para su análisis
Como el dataset de tráfico contenía múltiples registros por ciudad. Era imortante, calcular los promedios anuales por ciudad para simplificar el análisis y obtener una visión más clara de las tendencias generales.

### 4.1 Cálculo  promedios de tráfico por ciudad
<img width="930" height="214" alt="Screen Shot 2026-05-06 at 10 35 06 AM" src="https://github.com/user-attachments/assets/d718b755-206c-450e-a27c-5cd670cfb11f" />

### Paso 5: Unir tráfico (tabla principal) con indicadores económicos
Combino la información de tráfico y economía en un solo DataFrame para analizar cómo las condiciones económicas se relacionan con la movilidad urbana: 
 1. Selecciono las columnas relevantes de cada dataset 
 2. Hago una .copy() para evitar modificar el dataset original.
 3. Uno ambos DataFrames y defino como claves de unión a city y year.
 4. Mantengo solo las ciudades y años presentes en ambos datasets.
 5. Guardo el resultado en una nueva variable llamada merged .
<img width="806" height="327" alt="Screen Shot 2026-05-06 at 10 41 43 AM" src="https://github.com/user-attachments/assets/516561bb-4ab9-4ee5-8855-a33e4fa553ae" />
<img width="539" height="418" alt="Screen Shot 2026-05-06 at 10 44 40 AM" src="https://github.com/user-attachments/assets/cda945e7-48ce-417c-82af-4c8dfbf40fda" />

# Graficación de resultados para el análisis
<img width="551" height="148" alt="Screen Shot 2026-05-06 at 10 52 05 AM" src="https://github.com/user-attachments/assets/111a9b30-c188-498a-b37c-9d9a52a39044" />
<img width="720" height="532" alt="Screen Shot 2026-05-06 at 10 53 31 AM" src="https://github.com/user-attachments/assets/79558e22-91fd-465c-aef0-1bea7c7fd831" />


<img width="782" height="194" alt="Screen Shot 2026-05-06 at 10 49 24 AM" src="https://github.com/user-attachments/assets/cf813d77-f6d1-4744-b98d-1a8b605efd64" />
<img width="602" height="392" alt="Screen Shot 2026-05-06 at 10 50 19 AM" src="https://github.com/user-attachments/assets/e06b81ec-fbe7-45b3-b2d2-241f5087bc7a" />



**Recomendaciones**  

Ciudades prioritarias para inversión:
- Las ciudades que deben priorizarse son Bogotá (en primerísimo lugar) seguido por  Lima, dos ciudades que presentan la combinación más crítica de alta congestión y baja productividad económica, lo que indica un fuerte impacto negativo del tráfico sobre el desempeño económico. 

- En segundo nivel, Mexico City también requiere atención estratégica debido a su escala, donde pequeñas mejoras pueden generar beneficios masivos.

- Por su parte, Buenos Aires debe enfocarse en optimización más que en transformación estructural.

Validación de fuentes:
Es fundamental validar la calidad y comparabilidad de las fuentes utilizadas, especialmente en indicadores de tráfico y PIB per cápita. Se recomienda asegurar que los datos de congestión provengan de metodologías consistentes y que el PIB esté ajustado por paridad de poder adquisitivo, para evitar comparaciones sesgadas entre ciudades como Bogotá, Lima y Buenos Aires.

Análisis adicionales requeridos:
Para fortalecer los hallazgos, es necesario realizar análisis más robustos como modelos de regresión que cuantifiquen el impacto del tráfico sobre el PIB, así como incorporar series de tiempo que permitan identificar tendencias. También se recomienda incluir variables estructurales como informalidad laboral, uso del transporte público y niveles de inversión en infraestructura, especialmente en ciudades como Bogotá y Lima donde estos factores son determinantes.

Propuestas de inversión:
Las inversiones deben enfocarse en transporte público masivo (metro, BRT), infraestructura vial inteligente (semáforos adaptativos, gestión en tiempo real) y políticas de gestión de demanda como teletrabajo y descentralización urbana. En ciudades como Bogotá y Lima, estas acciones pueden traducirse directamente en mejoras de productividad, mientras que en Buenos Aires el enfoque debe ser mantener la eficiencia del sistema actual y evitar su deterioro.


### Resultados técnicos
- Reporte automatizado que reduce tiempo de análisis de horas a minutos
- Identificación de México como el país con niveles críticos de PM2.5
- Estandarización del proceso.Reproducible y documentado.

# Contacto
