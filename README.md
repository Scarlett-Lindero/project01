# Saturación obstétrica en México en 2024: ¿Por qué más de la mitad de los partos son cesáreas?


## 1. Descripción del proyecto
Este análisis utiliza los registros de nacimientos de 2024 del Sistema Nacional de Información en Salud (SINAC) de la Secretaría de Salud de México, así como el catálogo de unidades médicas (CLUES). 

Se centra en:
- Calcular la proporción nacional de cesáreas frente a partos vaginales.
- Mapear la distribución de cesáreas por estado y hospital.
- Evaluar la disponibilidad de gineco-obstetras en la atención de partos.
- Analizar la mortalidad materna según el tipo de parto.
- Generar insumos para el debate sobre políticas de salud materna y emergencias obstétricas.

## 2. Fuentes de datos
| Archivo                                      | Descripción                                         | Origen / Enlace                                           |
|----------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------|
| `Nacimientos_2024.csv`                       | Registros de nacimientos en México, año 2024        | SINAC Secretaría de Salud (descarga local)                |
| `sinac_catalogos_establecimientos_salud.xlsx`| Catálogo CLUES de unidades médicas                  | SINAC Secretaría de Salud (descarga local)                |

> **Nota:** Descarga y coloca ambos archivos en la carpeta raíz del proyecto antes de ejecutar el notebook.

## 3. Archivos generados
Tras ejecutar el notebook, se exportan los siguientes CSV para visualización y análisis:

- `dataset_nacimientos_2024.csv`: Base de datos depurada de nacimientos.  
- `tipo_parto_distribucion_2024_plot.csv`: Distribución de partos por tipo (vaginal, cesárea urgente, cesárea programada, etc.).  
- `porcentaje_total_cesareas_por_estado_ordenado_plot.csv`: Porcentaje de cesáreas por estado, ordenado de mayor a menor.  
- `top_10_ranking_hospitales_plot.csv`: Top 10 de hospitales con más partos sin gineco-obstetra (números absolutos).  
- `tipos_cesareas_mexico_2024_plot.csv`: Totales y porcentajes de las distintas categorías de cesárea.  
- `tipos_medico_muerte_materna_plot.csv`: Distribución de muertes maternas según tipo de profesional presente.  
- `hospitales_muertes_materna.csv`: Listado de hospitales con más de 2 muertes maternas registradas.  
- `muertes_maternas_por_tipo_parto.csv`: Muertes maternas desagregadas por tipo de parto.  

## 4. Metodología
1. **Carga y limpieza de datos**: Se importan los CSV y XLSX; se renombran columnas, se homogenizan formatos y se eliminan valores faltantes irrelevantes.  
2. **Cálculo de tasas y proporciones**:  
   - Tasa nacional de cesáreas frente a partos vaginales.  
   - Porcentaje de cesáreas por estado.  
3. **Análisis de saturación de gineco-obstetras**:  
   - Identificación de partos sin gineco-obstetra.  
   - Creación de un semáforo (rojo/amarillo/verde) por hospital según umbrales predefinidos.  
4. **Exploración de mortalidad materna**:  
   - Filtrado de muertes maternas (`SOBREVIVIO_PARTO_CVE == 2`).  
   - Conteo y porcentaje por tipo de parto y por profesional responsable.  
5. **Exportación de resultados**: Generación de CSV listos para visualización en dashboards o mapas.  

## 5. Hallazgos clave
- **Tasa nacional de cesáreas:** Más del 56% de los partos en 2024 fueron cesáreas, superando el umbral recomendado por la OMS (15%).  
- **Variación por estado:** [Estado más alto]% en [Estado A] vs. [Estado más bajo]% en [Estado B].  
- **Top 10 hospitales sin gineco-obstetra:** Hospital de la Mujer (Ciudad de México) lidera con 3,833 partos sin especialista.  
- **Mortalidad materna:** El 48.7% de las muertes maternas ocurrieron tras una cesárea de urgencia, indicando posibles retrasos en la atención de emergencias.  


## 6. Habilidades y herramientas utilizadas
- Python (pandas, matplotlib, openpyxl)  
- Limpieza y transformación de datos  
- Análisis estadístico de tasas y proporciones  
- Exportación de datasets para visualización  
- Diseño de semáforo de riesgo obstétrico  

## 7. Próximos pasos
- Incorporar datos de población y capacidad instalada hospitalaria para ajustar tasas.  
- Desarrollar mapas interactivos por estado y unidad médica.  
- Comparar tendencias con años anteriores (2020–2023).  
- Integrar análisis de factores socioeconómicos y geográficos.  
