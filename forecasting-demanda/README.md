# 📦 Predicción de Demanda con Prophet

Este proyecto utiliza la librería Prophet para predecir la cantidad de unidades vendidas en los próximos 30 días. Está basado en el dataset de la competencia de Kaggle ["Predict Future Sales"](https://www.kaggle.com/competitions/competitive-data-science-predict-future-sales).

## 🎯 Objetivo del Proyecto

Predecir la variable `item_cnt_day` (cantidad diaria vendida) usando técnicas de análisis exploratorio, limpieza, transformación, entrenamiento con Prophet y evaluación con métricas.

## 📂 Estructura

```
forecasting-demanda/
├── Forecasting_Demanda.ipynb   # Notebook principal del proyecto
├── README.md                   # Este archivo
└── requirements.txt            # Librerías necesarias
```

## 🛠️ Librerías usadas

- `prophet`
- `pandas`
- `numpy`
- `matplotlib`, `seaborn`
- `scikit-learn`

## 🧪 Cómo usar

```bash
pip install -r requirements.txt
```

Abrir el notebook en Jupyter o Colab y ejecutar todas las celdas.

## 📊 Métricas obtenidas

- MAE: Error absoluto medio
- RMSE: Raíz del error cuadrático medio

---

Autor: **Facundo Salazar Garzón**