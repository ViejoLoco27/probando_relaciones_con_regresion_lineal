
# 🧭 Bitácora de Regresión Lineal  
**Fechas de trabajo**: 14–17 de julio  
**Tema central**: Análisis del precio de viviendas mediante regresión lineal

---

## 1. 📁 Dataset y variables
- **Fuente**: Dataset de precios de viviendas (`price`, `sqft_living`, `bedrooms`, `bathrooms`, etc.)
- **Objetivo**: Modelar el impacto de variables estructurales en el precio de venta

---

## 2. ⚙️ Preparación de datos
- Detección y tratamiento de *outliers* en `sqft_living` y `price`
- Transformaciones aplicadas: logaritmo natural a `price` para estabilizar varianza
- Codificación de variables categóricas (`zipcode`, `condition`, etc.)

---

## 3. 📐 Modelo OLS
- **Fórmula base**:  
  $$ \log(\text{price}) = \beta_0 + \beta_1 \cdot \text{sqft\_living} + \beta_2 \cdot \text{bedrooms} + \ldots + \varepsilon $$
- **Evaluación de supuestos**:
  - Linealidad: visualización de residuos
  - Homocedasticidad: test de Breusch-Pagan
  - Normalidad de errores: histograma y Q-Q plot
  - Multicolinealidad: VIF

---

## 4. 📊 Visualizaciones
- Gráficos de dispersión con líneas de regresión
- Boxplots para comparar precios por `condition`
- Heatmap de correlaciones

---

## 5. 🧠 Reflexiones técnicas y filosóficas
- ¿Qué significa modelar una relación en términos de causalidad?
- ¿Cómo influye el sesgo de selección en la interpretación del modelo?
- ¿Puede un modelo estadístico capturar la complejidad del valor de una vivienda?

---

## 6. 🧪 Validación y ajuste
- División train/test
- Métricas: RMSE, R² ajustado
- Comparación entre modelos con y sin transformación logarítmica
