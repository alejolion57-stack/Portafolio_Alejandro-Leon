# Análisis de eficiencia de ventas — Walmart
### Objetivo
Optimizar presupuesto e inventario mediante análisis de eficiencia de tiendas, 
participación de departamentos y volatilidad de ventas en 2012.

### KPIs Desarrollados
- **Eficiencia:** Ventas por metro cuadrado
- **Participación:** % de ventas por departamento  
- **Riesgo:** Coeficiente de variación (volatilidad)

### Metodología
1. Limpieza y normalización de datos
2. Enriquecimiento con XLOOKUP
3. Creación de tablas dinámicas
4. Dashboard interactivo con filtros

### Insights Clave
- El tamaño de las tiendas claramente afecta el volumen de ventas semanales aunque es importante ver mas a profundidad una tienda en específico que tienes un volumen excepcional aunque no sea de las mas grandes de la cadena.
- En general las categorías de producto tienen participaciones muy similares aunque podemos destacar positivamente juguetes y juegos. Debe prestarse atención a Automotriz para incrementar su porcentaje en proximos meses.

### Implicaciones
- Es importante revisar el rendimiento de ciertas categorías en tiendas conmenor espacio para apoyar su crecimiento  aunque no exiten variaciones negativas tan significativas.
- En la participación de todos los departamentos es bastante favorable aunque: Jardín y vida al aire libre, juguetes y juegos y salud/ y bienestar representan el mayor aporte en las ventas totales del mes.
- Las categorías automotriz, Oficina escuela y manualidades y ropa pueden mejorar su perticipación tal ves con algun push promocional en tiendas.
### Dashboard Interactivo 
<img width="1168" height="805" alt="image" src="https://github.com/user-attachments/assets/9266709e-1186-4cda-98c0-17d52cb3004b" />

### Cuadro Resumen para Stakeholders
<img width="1811" height="275" alt="image" src="https://github.com/user-attachments/assets/e7e26697-2304-4829-b50b-ffa2a47604f7" />

### Diseño del Readme 
<img width="751" height="501" alt="image" src="https://github.com/user-attachments/assets/0572af91-cf7a-4be0-a8ee-808e2cb22764" />



# Monitoreo Automatizado de PM2.5 - Latinoamérica

# Objetivo
Automatizar reportes mensuales de niveles de contaminación PM2.5 
por país en Latinoamérica para el equipo de monitoreo ambiental.

# Tecnologías
- Python, Pandas, Jupyter Notebook
- Limpieza y transformación de datos
- Análisis estadístico descriptivo

# Proceso
## Paso 1: Carga y exploración de datasets y librerias para graficar
 <img width="709" height="210" alt="Screen Shot 2026-05-05 at 3 54 03 PM" src="https://github.com/user-attachments/assets/732f7433-d897-4e94-b963-b1cc0446569b" />

## Paso 2: Exploración y limpieza de datos en los dos DF "Traffic" y DF "Eco"
<img width="680" height="415" alt="Screen Shot 2026-05-05 at 3 57 03 PM" src="https://github.com/user-attachments/assets/2d5bdd56-b518-4dea-8db2-94375eab17bf" />
<img width="657" height="252" alt="Screen Shot 2026-05-05 at 3 57 34 PM" src="https://github.com/user-attachments/assets/20811bae-49a7-4d9e-a555-3c2798d0e132" />

### Descubrimiento premilimar : 
En la estructura del DF traffic, se observa que:
- Las columnas UpdateTimeUTC y UpdateTimeUTC son de tipo (object). Se deben cambiar a valores de tipo fecha (datetime)
- No se observan datos ausentes.

En la estructura del DF eco, se observa que:
- Las columnas City GDP/capita, Unemployment %, "PM2.5 (μg/m³)" y "Population (M)" estan con tipo texto (object) y ndecesitan ser remplazadas a tipo numérico, decimal (float64) para obtener un análisis realmente funcional.
- No se ven datos ausentes.




# Resultados
- Reporte automatizado que reduce tiempo de análisis de horas a minutos
- Identificación de México como el país con niveles críticos de PM2.5
- Estandarización del proceso.Reproducible y documentado.



## 📬 Contacto

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/tu-usuario)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:tu@email.com)
