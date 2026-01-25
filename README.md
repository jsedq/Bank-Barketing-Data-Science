# 📊 Bank Marketing Analysis con Machine Learning  
### Segmentación y Optimización de Campañas mediante Modelos Interpretables

Repositorio que analiza y modela datos de campañas de marketing bancario para estimar la probabilidad de aceptación de clientes usando Machine Learning interpretable en Python (Regresión Logística), con el objetivo de priorizar contactos y mejorar la eficiencia de las campañas.

---

## 📌 Problema de negocio

Las campañas de marketing bancario presentan una tasa de conversión naturalmente baja, lo que implica costos elevados por contactos poco efectivos. Este proyecto busca construir un modelo que permita priorizar contactos con alta probabilidad de aceptación, reduciendo costos y mejorando la eficiencia de la campaña.

El análisis busca responder a la pregunta:

**¿Cómo puede una institución financiera mejorar la efectividad de sus campañas de marketing mediante el uso de datos?**

El foco no es la predicción perfecta, sino la priorización efectiva de clientes.

---

## 🎯 Objetivo

- Analizar el comportamiento de los clientes frente a campañas de marketing.
- Identificar variables relevantes asociadas a la aceptación de la campaña.
- Construir un modelo interpretable que permita rankear clientes según su propensión a aceptar la campaña.
- Proponer segmentos prioritarios y recomendaciones accionables para mejorar la tasa de conversión y el ROI.

---

## 📂 Estructura del repositorio

- `Notebook/01_EDA.ipynb` – Análisis exploratorio de datos
- `Notebook/02_Modeling.ipynb` – Preparación, entrenamiento y evaluación de modelos de Machine Learning
- `data/` – Datos originales y limpios
- `README.md` – Documentación del proyecto

---

## 🗂️ Dataset

- **Fuente:** UCI Bank Marketing Dataset  
- **Observaciones:** ~41,000 clientes  
- **Variable objetivo:** `y` (aceptación de la campaña: yes / no)  
- **Tipo de variables:**
  - Numéricas (edad, indicadores macroeconómicos, número de contactos, etc.)
  - Categóricas (ocupación, educación, estado civil, canal de contacto, mes, etc.)

---

## 🧠 Metodología

1. **Análisis exploratorio de datos (EDA)**
   - Distribuciones, estadísticos descriptivos y análisis de outliers
   - Identificación de variables relevantes y patrones de comportamiento

2. **Selección y preparación de features**
   - Eliminación de fuga de información (`duration`)
   - Encoding de variables categóricas y escalado de variables numéricas
   - Uso de pipelines para garantizar consistencia y evitar data leakage

3. **Modelado Machine Learning**
   - Modelo baseline y final: **Regresión Logística** con `class_weight='balanced'`
   - Evaluación utilizando métricas adecuadas para datos desbalanceados (recall, F1-score y ROC AUC)

4. **Interpretación y uso del modelo**
   - Análisis de coeficientes para entender el impacto de cada variable
   - Generación de un score de propensión para priorización de clientes

---

## 🔍 Principales Insights

- La tasa de conversión global es baja (~11%), evidenciando un fuerte desbalance de clases.
- Variables como `month`, `poutcome` y `job` muestran una asociación relevante con la aceptación de la campaña.
- El canal de contacto celular presenta mayor efectividad frente a otros canales.
- Existen patrones claros de estacionalidad, con meses significativamente más efectivos.
- Algunas variables derivadas fueron útiles para el análisis exploratorio, pero no se incluyeron en el modelo final para evitar redundancia y mantener interpretabilidad.

---

## 📊 Resultados

- **ROC AUC:** 0.80 → el modelo muestra una buena capacidad para rankear clientes según su probabilidad de aceptación.
- **Recall (clase positiva):** ~65% → captura una proporción significativa de clientes que aceptarían la campaña.
- **Conversion rate en Top 20%:** ~36% (vs ~11% tasa base).

Estos resultados demuestran que el modelo permite priorizar contactos y mejorar significativamente la tasa de conversión frente a un enfoque aleatorio.

---

## 📈 Recomendaciones Estratégicas

- Priorizar campañas dirigidas a los segmentos con mayor score de propensión.
- Optimizar el calendario de contacto considerando estacionalidad y días más efectivos.
- Limitar el número de intentos de contacto por cliente para evitar saturación y pérdida de efectividad.
- Considerar el contexto macroeconómico antes de lanzar campañas masivas.

---

## 🛠️ Tecnologías Utilizadas

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- SciPy
- Scikit-learn
- Jupyter Notebook


