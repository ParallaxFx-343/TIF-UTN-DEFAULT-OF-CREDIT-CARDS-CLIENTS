# 📊 Predicción de Default en Tarjetas de Crédito
### Trabajo Integrador Final — Curso de Data Science | UTN BA Centro de E-Learning

**Alumno:** Franco Palladino  
**Año:** 2026

---

## 🎯 Objetivo

Predecir si un cliente incumplirá el pago de su tarjeta de crédito el mes siguiente, utilizando datos históricos demográficos y de comportamiento de pago.

## 📁 Dataset

**Default of Credit Card Clients** — UCI Machine Learning Repository (Yeh & Lien, 2009)

- **30.000 registros** de clientes de una institución financiera de Taiwán (2005)
- **24 variables:** demográficas, límite de crédito, historial de pagos 6 meses, montos facturados y pagados
- **Variable objetivo:** `default` — 1 si el cliente incumple el pago el mes siguiente, 0 si no

## 🔧 Tecnologías

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.0-lightblue)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3-orange)
![Google Colab](https://img.shields.io/badge/Google%20Colab-notebook-yellow)

## 📋 Estructura del Proyecto

| Sección | Descripción |
|---|---|
| 0. Librerías | Importación del stack de Data Science (pandas, numpy, sklearn, seaborn) |
| 1. Selección del dataset | Justificación de la elección y descripción del problema |
| 2. Exploración de datos | Análisis de estructura, tipos y diccionario de variables |
| 3. Limpieza de datos | Tratamiento de valores atípicos en variables categóricas, decisiones justificadas |
| 4. Análisis estadístico | EDA completo con visualizaciones, tests de hipótesis (scipy.stats) |
| 5. Hallazgos iniciales | Patrones detectados: desbalance de clases, correlaciones, variables clave |
| 6. Definición del modelo | Justificación de la selección: Random Forest vs Regresión Logística |
| 7. Selección de features | Feature importance, correlaciones, manejo de multicolinealidad |
| 8. Entrenamiento | Split 80/20 estratificado, class_weight='balanced', cross-validation |
| 9. Resultados | Matrices de confusión, curvas ROC, tabla comparativa de métricas |
| 10. Propuestas | Scoring en tiempo real, alertas tempranas, segmentación de riesgo |

## 📈 Resultados

| Modelo | Accuracy | ROC-AUC | F1 (Default) |
|---|---|---|---|
| Regresión Logística (Baseline) | ~0.81 | ~0.77 | ~0.47 |
| **Random Forest (Principal)** | **~0.82** | **~0.78** | **~0.50** |

**Variable más predictiva:** `pay_0` (estado de pago más reciente) — confirma que el comportamiento reciente es el mejor predictor del riesgo futuro.

## 🚀 Cómo ejecutar

1. Abrí el notebook en Google Colab:  
   👉 [Abrir en Colab](https://colab.research.google.com/drive/1llNIlcNLOE_KVA9CZ4-sxcYivkSwaBCc)

2. Ejecutá todas las celdas en orden (`Runtime → Run all`)

3. El dataset se carga automáticamente desde URL pública — no hace falta descargar nada

## 📚 Referencias

- Yeh, I. C., & Lien, C. H. (2009). *The comparisons of data mining techniques for the predictive accuracy of probability of default of credit card clients*. Expert Systems with Applications, 36(2), 2473-2480.
- Documentación scikit-learn: https://scikit-learn.org
- UCI Machine Learning Repository: https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients

---
*Curso de Data Science — UTN BA Centro de E-Learning | 2026*
