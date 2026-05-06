# Monitoreo Automatizado de PM2.5 - Latinoamérica

## Objetivo
Automatizar reportes mensuales de niveles de contaminación PM2.5 
por país en Latinoamérica para el equipo de monitoreo ambiental.

## Tecnologías
- Python, Pandas, Jupyter Notebook
- Limpieza y transformación de datos
- Análisis estadístico descriptivo

## Proceso
### Paso 1: Carga y exploración de datasets y librerias para graficar
 <img width="709" height="210" alt="Screen Shot 2026-05-05 at 3 54 03 PM" src="https://github.com/user-attachments/assets/732f7433-d897-4e94-b963-b1cc0446569b" />

### Paso 2: Exploración y limpieza de datos en los dos DF "Traffic" y DF "Eco"
<img width="680" height="415" alt="Screen Shot 2026-05-05 at 3 57 03 PM" src="https://github.com/user-attachments/assets/2d5bdd56-b518-4dea-8db2-94375eab17bf" />
<img width="657" height="252" alt="Screen Shot 2026-05-05 at 3 57 34 PM" src="https://github.com/user-attachments/assets/20811bae-49a7-4d9e-a555-3c2798d0e132" />

### Descubrimiento premilimar : 
En la estructura del DF traffic, se observa que:
- Las columnas UpdateTimeUTC y UpdateTimeUTC son de tipo (object). Se deben cambiar a valores de tipo fecha (datetime)
- No se observan datos ausentes.

En la estructura del DF eco, se observa que:
- Las columnas City GDP/capita, Unemployment %, "PM2.5 (μg/m³)" y "Population (M)" estan con tipo texto (object) y ndecesitan ser remplazadas a tipo numérico, decimal (float64) para obtener un análisis realmente funcional.
- No se ven datos ausentes.




### Resultados
- Reporte automatizado que reduce tiempo de análisis de horas a minutos
- Identificación de México como el país con niveles críticos de PM2.5
- Estandarización del proceso.Reproducible y documentado.

