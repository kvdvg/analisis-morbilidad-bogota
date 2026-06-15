# 🏥 Análisis de Morbilidad en Bogotá D.C. (2022–2025)
### Proyecto de Análisis de Datos en Salud Pública | Python · SQL · Power BI · Excel

---

## 📋 Descripción

Análisis exploratorio, diagnóstico, predictivo y prescriptivo de la morbilidad en Bogotá D.C. a partir de los Registros Individuales de Prestación de Servicios de Salud (RIPS) publicados por la Secretaría Distrital de Salud en el portal de Datos Abiertos Bogotá.

El proyecto responde **16 preguntas de negocio** estructuradas en 4 niveles de análisis, sobre un dataset de **6,049,626 registros** de atenciones en salud entre 2022 y 2025, distribuidos en **18 zonas territoriales** de Bogotá.

---

## 🎯 Objetivos

- Identificar los diagnósticos más frecuentes y su evolución en el tiempo
- Detectar brechas de acceso a servicios de salud por localidad
- Proyectar la demanda de atenciones para 2025–2026
- Generar recomendaciones prescriptivas para la redistribución de recursos en salud

---

## 🗂️ Estructura del Repositorio

```
analisis-morbilidad-bogota/
│
├── 📓 analisis_morbilidad_bogota_rips.ipynb   # Notebook principal
│
├── 📊 exports/                                 # Resultados de consultas SQL
│   ├── q1_top_diagnosticos_por_ano.csv
│   ├── q2_volumen_por_localidad.csv
│   ├── q3_evolucion_anual.csv
│   ├── q4_sexo_grupo_edad.csv
│   ├── q5_tasa_por_habitante.csv
│   ├── q6_top_diagnosticos_por_localidad.csv
│   ├── q7_tipo_atencion_por_localidad.csv
│   ├── q8_afiliacion.csv
│   ├── q9_tendencia_cronicos.csv
│   ├── q10_tendencia_por_localidad.csv
│   ├── q11_tendencia_sexo_edad.csv
│   ├── q12_proyeccion_por_localidad.csv
│   ├── q13_brecha_atencion.csv
│   ├── q14_diagnosticos_crecientes.csv
│   ├── q15_redistribucion_oferta.csv
│   └── q16_perfil_cobertura.csv
│
├── 📈 graficas/                                # Visualizaciones en Python
│   ├── g1_top_diagnosticos.png
│   ├── g2_volumen_localidad.png
│   ├── g3_evolucion_anual.png
│   ├── g4_sexo_edad.png
│   ├── g5_tasa_habitante.png
│   ├── g6_tipo_atencion.png
│   ├── g7_cronicos.png
│   ├── g8_brecha.png
│   ├── g9_diagnosticos_crecientes.png
│   ├── g10_tendencia_localidad.png
│   ├── g11_proyeccion_localidades.png
│   ├── g12_proyeccion_cronicos.png
│   └── g13_metricas_modelo.png
│
├── 📑 reporte_ejecutivo_morbilidad_bogota.xlsx # Reporte Excel automatizado
├── 📊 trabajo_3.pbix                           # Dashboard Power BI
└── 📄 README.md
```

---

## 🔍 Preguntas de Negocio Respondidas

### 📊 Análisis Descriptivo (¿Qué pasó?)
| # | Pregunta |
|---|----------|
| 1 | ¿Cuáles son los 10 diagnósticos más frecuentes por año? |
| 2 | ¿Qué localidades concentran mayor volumen de atenciones? |
| 3 | ¿Cómo evolucionó la morbilidad entre 2022 y 2024? |
| 4 | ¿Cuál es la distribución de atenciones por sexo y grupo de edad? |

### 🔬 Análisis Diagnóstico (¿Por qué pasó?)
| # | Pregunta |
|---|----------|
| 5 | ¿Qué localidades tienen mayor tasa de morbilidad por habitante? |
| 6 | ¿Qué diagnósticos predominan por localidad? |
| 7 | ¿Qué tipo de atención concentra más carga por localidad? |
| 8 | ¿Cómo varía la morbilidad por tipo de afiliación? |

### 📈 Análisis Predictivo (¿Qué pasará?)
| # | Pregunta |
|---|----------|
| 9  | ¿Cuál es la tendencia de los diagnósticos crónicos 2022–2024? |
| 10 | ¿Qué localidades muestran tendencia creciente de morbilidad? |
| 11 | ¿Qué grupos de edad y sexo concentrarán más demanda futura? |
| 12 | ¿Cuál es la proyección de atenciones 2025–2026 por localidad? |

### 💡 Análisis Prescriptivo (¿Qué hacer?)
| # | Pregunta |
|---|----------|
| 13 | ¿Dónde priorizar recursos según brecha de atención? |
| 14 | ¿Qué diagnósticos requieren intervención preventiva urgente? |
| 15 | ¿Cómo redistribuir la oferta de servicios por localidad y tipo? |
| 16 | ¿Qué perfil de morbilidad diferencia las localidades de alta vs baja cobertura? |

---

## 💡 Hallazgos Principales

- **Chapinero y Teusaquillo** tienen tasas de ~20 atenciones por habitante, mientras **Usme, Bosa y Ciudad Bolívar** no llegan a 1.6 — una brecha de hasta **50 veces** en acceso a servicios de salud.
- Las **enfermedades infecciosas intestinales** crecieron un **87%** entre 2022 y 2024, siendo el diagnóstico con mayor urgencia de intervención preventiva.
- El **VIH** aumentó un 40% y los **trastornos de salud mental** (episódicos, neuróticos) muestran tendencia creciente sostenida.
- Las **mujeres** representan el 58% de las atenciones, con pico en el grupo de 25–29 años (edad reproductiva).
- **Engativá (+37%)** y **Usme (+25%)** son las localidades con mayor crecimiento de atenciones 2022–2024.
- En localidades de **baja cobertura**, las enfermedades bucales son el diagnóstico #1 (no los exámenes preventivos), lo que indica menor acceso a atención primaria.

---

## 🛠️ Tecnologías Utilizadas

| Herramienta | Uso |
|-------------|-----|
| Python (pandas, matplotlib, seaborn, sklearn) | Carga, limpieza, análisis y visualización |
| SQLite + SQLAlchemy | Base de datos relacional y consultas SQL |
| Power BI Desktop | Dashboard ejecutivo interactivo (4 páginas) |
| Excel (openpyxl) | Reporte ejecutivo automatizado |
| Google Colab | Entorno de desarrollo en la nube |

---

## 📦 Fuentes de Datos

| Dataset | Fuente | Registros |
|---------|--------|-----------|
| RIPS Bogotá 2022–2025 | [Datos Abiertos Bogotá](https://datosabiertos.bogota.gov.co) | 6,049,626 |
| Población por UPL 2022–2025 | [DANE / SDP](https://datosabiertos.bogota.gov.co) | 22,704 |

> **Nota:** Los datos de población corresponden a proyecciones DANE/SDP desagregadas por Unidad de Planeamiento Local (UPL). Se realizó un mapeo de las 33 UPL a las 18 zonas territoriales compatibles con el RIPS, documentado en el notebook.

---

## ▶️ Cómo Ejecutar

1. Abrir `analisis_morbilidad_bogota_rips.ipynb` en Google Colab
2. Ejecutar todas las celdas en orden (`Entorno de ejecución → Ejecutar todo`)
3. Los datos se descargan automáticamente desde Datos Abiertos Bogotá
4. Los CSVs y gráficas se exportan a `/content/exports/` y `/content/graficas/`

---

## 📊 Dashboard Power BI

El archivo `trabajo_3.pbix` contiene 4 páginas:

1. **Resumen Ejecutivo** — KPIs, evolución anual, distribución por tipo de atención
2. **Análisis por Localidad** — Volumen, tasa por habitante, brecha y tendencia
3. **Diagnósticos y Perfil Epidemiológico** — Top diagnósticos, sexo/edad, crónicos, crecimiento
4. **Prescriptivo y Recomendaciones** — Prioridades, diagnósticos urgentes, perfil por cobertura

---

## 👤 Autor

Proyecto desarrollado como parte de un portafolio de análisis de datos en salud pública.

---

*Datos abiertos · Análisis reproducible · Bogotá D.C., Colombia*
