# 📊 Bank Marketing Analysis – Segmentación y Optimización de Campañas

## 📌 Contexto del proyecto
Las campañas de marketing bancario suelen presentar tasas de conversión bajas y altos costos operativos debido a contactos poco segmentados. En este proyecto se analiza un dataset de campañas de marketing bancario con el objetivo de identificar patrones, segmentos de clientes y factores clave que influyen en la aceptación de productos financieros.

El análisis busca responder a la pregunta:
**¿Cómo puede una institución financiera mejorar la efectividad de sus campañas de marketing mediante el uso de datos?**

---

## 🎯 Objetivo
- Analizar el comportamiento de los clientes frente a campañas de marketing.
- Identificar variables relevantes asociadas a la aceptación de la campaña.
- Proponer segmentos prioritarios y recomendaciones accionables para mejorar la tasa de conversión y el ROI.

---

## 🗂️ Dataset
- **Observaciones:** ~41,000 clientes
- **Variable objetivo:** `y` (aceptación de la campaña: yes / no)
- **Tipo de variables:**
  - Numéricas (edad, indicadores macroeconómicos, número de contactos, etc.)
  - Categóricas (ocupación, educación, estado civil, canal de contacto, mes, etc.)

---

## 🧠 Metodología

### 1️⃣ Análisis Exploratorio de Datos (EDA)
- Revisión de calidad de datos (nulos y duplicados).
- Análisis de distribuciones numéricas y categóricas.
- Evaluación de outliers y su impacto.
- Análisis de asociación entre variables categóricas y el target mediante **Cramér’s V**.
- Análisis temporal por mes y día de la semana.

### 2️⃣ Feature Engineering
- Creación de variables derivadas como `age_group`.
- Evaluación de la utilidad real de las variables creadas.
- Selección de variables relevantes basada en evidencia estadística y de negocio.

---

## 🔍 Principales Insights

- La tasa de conversión global es baja (~11%), con un fuerte desbalance de clases.
- Variables como `month`, `poutcome`, `job` y `age_group` presentan una asociación relevante con la aceptación de la campaña.
- El canal de contacto celular muestra mayor efectividad que otros canales.
- Existen patrones de estacionalidad claros, con meses significativamente más efectivos.
- Algunos segmentos demográficos presentan mayores tasas de conversión, aunque ciertos resultados deben interpretarse con cautela debido al tamaño muestral.

---

## 📈 Recomendaciones Estratégicas

- Priorizar campañas dirigidas a segmentos con mayor probabilidad de conversión.
- Optimizar el calendario de contacto según estacionalidad y días más efectivos.
- Limitar el número de intentos de contacto por cliente para evitar saturación.
- Monitorear indicadores macroeconómicos antes de lanzar campañas masivas.

---

## 🛠️ Tecnologías Utilizadas
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- SciPy
- Scikit-learn
- Jupyter Notebook

