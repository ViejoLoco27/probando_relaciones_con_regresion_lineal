# Curso de Data ScienceProbando: relaciones con regresion_lineal
Este repositorio contiene los temas vistos durante las lecciones del curso "Data Science: probando relaciones con regresión lineal". Adicionalmente, se agrego una evaluación final para poner a prueba los conocimientos adquiridos.
---

# 🏡 Proyecto de Precificación Inmobiliaria – Curso de Regresión Lineal

Este proyecto explora cómo construir modelos de regresión lineal para estimar el **precio de venta de inmuebles**, analizando variables estructurales y su impacto en la predicción. Se utiliza una base de datos inspirada en *House Prices* para poner en práctica los conceptos fundamentales vistos en clase.

---

## 🎯 Objetivos

- Comprender la relación entre variables estructurales y el precio de venta.
- Identificar las variables con mayor influencia en la precificación.
- Evaluar distintos modelos y su capacidad predictiva.
- Reflexionar sobre el alcance, límites y ética del modelado estadístico.

---

## 📁 Dataset

El conjunto de datos contiene 1438 registros con las siguientes variables:

- `area_primer_piso`: superficie en m² del primer piso.
- `tiene_segundo_piso`: binaria (1 = sí, 0 = no).
- `area_segundo_piso`: superficie del segundo piso (m²).
- `cantidad_banos`: número de baños.
- `capacidad_carros_garage`: cantidad de autos que caben en el garage.
- `calidad_de_cocina_excelente`: binaria (1 = excelente cocina, 0 = no).
- `precio_de_venta`: valor en USD.

---

## ⚙️ Proceso Metodológico

1. **Análisis Exploratorio**
   - Correlación de variables con `precio_de_venta`.
   - Visualización con `matplotlib`, `seaborn` y `plotly`.
   - Análisis de distribución y dispersión.

2. **Modelado**
   - Regresión simple: `precio_de_venta ~ area_primer_piso`.
   - Modelos múltiples con diferentes combinaciones de variables.
   - Evaluación del desempeño: R², residuos, significancia de coeficientes.

3. **Validación**
   - División en conjunto de entrenamiento y prueba (`train_test_split`).
   - Evaluación con `r2_score` y análisis del poder explicativo.

4. **Multicolinealidad**
   - Cálculo del VIF (`Variance Inflation Factor`) para detectar redundancias.

5. **Predicción**
   - Precificación de nuevos inmuebles usando modelos ajustados.
   - Predicción de casas ficticias y evaluación comparativa.

---

## 📊 Resultados Destacados

- El modelo simple con solo `area_primer_piso` obtuvo un R² ≈ 0.38.
- El modelo múltiple con seis variables alcanzó un R² ≈ 0.74.
- Variables con mayor peso explicativo: `capacidad_carros_garage`, `area_primer_piso`, y `calidad_de_cocina_excelente`.
- Se detectó multicolinealidad entre `area_primer_piso` y `area_segundo_piso`.

---

## 🤔 Reflexiones Finales

> *Modelar el precio de un inmueble es más que aplicar fórmulas. Cada coeficiente representa una interpretación social y estructural del valor. Pero también revela los límites de lo numérico frente a la complejidad del espacio, la subjetividad y el mercado.*

Este ejercicio plantea preguntas clave:

- ¿Qué no estamos viendo al ignorar ubicación o contexto social?
- ¿Cómo usar modelos como herramienta de decisión sin caer en reduccionismos?
- ¿Qué responsabilidad ética tenemos al implementar estos modelos en situaciones reales?

---

## 🧪 Recursos Técnicos Usados

- `pandas`, `numpy`, `matplotlib`, `seaborn`, `statsmodels`, `scikit-learn`, `plotly`

---

**Autor**: Guz  
**Fecha**: Julio 2025  
**Curso**: Regresión Lineal – Modelado Estadístico
