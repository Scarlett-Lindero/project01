# When Giving Birth Becomes an Emergency: Obstetric Saturation in Mexico (2024)

In Mexico, childbirth is increasingly shaped by urgency—not choice.

This investigation analyzes more than **1.4 million births registered in public hospitals in 2024** to reveal a silent crisis: a health system under pressure, where emergency C-sections are the norm, specialists are often absent, and the safety of birthing people is compromised.

---

## Why This Matters

Maternal health is a human right. But in many hospitals across Mexico, that right is limited by systemic saturation.

- Most births in 2024 ended in a C-section.
- The majority of those were classified as **emergencies**.
- Many happened **without OB/GYNs present**.
- In some hospitals, there were **hundreds of births without any specialist at all**.

This isn’t just about medical protocols—it’s about access, inequity, and life-threatening gaps in care.

---

## 🔍 Key Findings

- **56.1%** of births in public hospitals were resolved via C-section.  
- Of those, **52.1%** were labeled as *emergency surgeries*.  
- **76 maternal deaths** were recorded during childbirth. Nearly half followed an emergency C-section.  
- Over **28,000 cases** had *no record* of the professional who attended the birth.  
- In several hospitals, **300+ births occurred without an OB/GYN**.

---

## Research Goals

1. Quantify the prevalence of C-sections and their classification.  
2. Identify states and hospitals with high rates of emergency interventions.  
3. Detect facilities where births routinely happen without medical specialists.  
4. Provide actionable evidence for public debate and policy around maternal care in Mexico.

---

## Methodology 

This project is based on the **2024 Birth Database** from SINAC (National Birth Certificate Information System), published by the Mexican Ministry of Health.

### Data Cleaning

- Original dataset: **1,413,203 births**  
- Excluded:
  - Records with `CLUES = 9998` (non-official medical units)
  - Rows with missing `CLUES` values
- Final dataset: **1,338,905 complete birth records**  

### Key Variables

- `TIPO_PARTO` → Type of delivery (vaginal or C-section)  
- `TIPOCESAREA` → Classification (scheduled, emergency, other)  
- `TIPOMEDICOATENDIO` → Type of attending medical professional  
- `SOBREVIVIOPARTO` → Whether the mother survived  
- `CLUES` → Medical unit identifier  
- `ENTIDADFEDERATIVAPARTO` → State of birth

---

## Visual Outputs

This project produced a series of interactive and visual tools:

- A **national map** showing hospitals with the highest saturation.
- A **ranking of facilities** with the most non-specialist-attended births.
- **State-level comparisons** of emergency C-section rates.
- **Bar charts** of medical staff presence during maternal deaths.

---

## Tools Used

- **Python & Pandas** – data processing and cleaning  
- **Jupyter Notebook** – reproducible code and documentation  
- **Datawrapper** – mapping and interactive visualizations  
- **GitHub Pages** – for publishing the microsite  

## Generated Datasets

| File Name                                       | Description                                                              |
|------------------------------------------------|--------------------------------------------------------------------------|
| `dataset_nacimientos_2024.csv`                 | Cleaned birth records dataset                                            |
| `tipo_parto_distribucion_2024_plot.csv`        | Delivery types (vaginal, emergency C-section, scheduled, etc.)          |
| `porcentaje_total_cesareas_por_estado_ordenado_plot.csv` | C-section rates by state, ranked                                 |
| `top_10_ranking_hospitales_plot.csv`           | Hospitals with the most births without OB/GYN                           |
| `tipos_cesareas_mexico_2024_plot.csv`          | C-section classification totals and percentages                         |
| `tipos_medico_muerte_materna_plot.csv`         | Maternal deaths by attending staff type                                 |
| `hospitales_muertes_materna.csv`               | Hospitals with >2 maternal deaths                                        |
| `muertes_maternas_por_tipo_parto.csv`          | Maternal deaths by delivery type                                        |

---

## Data Sources

| File                                           | Description                                | Source                                     |
|------------------------------------------------|--------------------------------------------|--------------------------------------------|
| `Nacimientos_2024.csv`                         | Birth records for 2024 in Mexico           | SINAC – Ministry of Health *(local file)*  |
| `sinac_catalogos_establecimientos_salud.xlsx`  | CLUES catalog of medical units             | SINAC – Ministry of Health *(local file)*  |

> **Note:** Place both files in your project root before running the notebook.

---

## What’s Next

- Add population data and hospital capacity to adjust C-section rates  
- Build interactive maps by state and medical unit  
- Compare trends with previous years (2020–2023)  
- Integrate geographic and socioeconomic context into the analysis  

---

##  Author

**Scarlett Lindero**  
Investigative & Data Journalist | *La Cadera de Eva*  
LEDE Fellow 2025 | Mexico City  

This project is part of a larger effort to uncover structural issues in maternal care and give visibility to stories hidden in the data.


