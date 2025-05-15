<img src="https://stats.cusat.ac.in/assets/images/research_area/time_series.jpeg" alt="Imagen de Customer Segmentation" width="700"/>

# ⏳ Time-Series-Forecasting

Este proyecto tiene como objetivo realizar análisis y predicción de series temporales utilizando dos enfoques: **SARIMA** y **Prophet**. Se busca identificar patrones históricos y realizar predicciones precisas sobre los valores futuros de la serie.

## 📝 Descripción Detallada

El flujo de trabajo del proyecto se estructura en varias etapas:

- **Limpieza y preparación de datos (01_Cleaning.ipynb)**: Se carga y limpia el conjunto de datos original para su posterior análisis.

- **Análisis exploratorio (02_EDA.ipynb)**: Se realiza un estudio visual y estadístico de la serie temporal, detectando estacionalidades, tendencias y posibles relaciones.

- **Modelado  (03_Forecasting.ipynb)**: Se entrenan los modelos SARIMA y Prophet para predecir una de las series temporales del dataset

## 📂 Estructura del Proyecto


- **data/**
  - `cleandf.csv` # Dataset limpio y listo para el análisis
  - `generation_monthly.xlsx` # Raw data 

- **models**
  - `prophet_model.pkl`
  - `sarima_model.pkl` 

- **notebooks/**
  - `01_Cleaning.ipynb`
  - `02_EDA.ipynb`
  - `03_Forecasting.ipynb`

-  `README.md` # Documentación del proyecto

## 📥 Requisitos

Este proyecto requiere las siguientes bibliotecas de Python:

- pandas
- numpy
- matplotlib
- seaborn
- statsmodels
- pmdarima
- prophet

## 📊 Resultados y Conclusiones

Las métricas promedio obtenidas indican que el modelo **Prophet** presenta un rendimiento ligeramente superior respecto a **SARIMA**, especialmente cuando se evalúan los errores en relación al valor máximo de la serie:

| Métrica              | SARIMA  | Prophet | Diferencia | Mejora con Prophet |
|----------------------|---------|---------|------------|--------------------|
| MAE (% valor medio)  | 7.00%   | 6.54%   | 0.46%      | 6.57%              |
| RMSE (% valor medio) | 8.24%   | 7.82%   | 0.42%      | 5.10%              |
| MAE (% valor máximo) | 4.82%   | 3.07%   | 1.75%      | 36.31%             |
| RMSE (% valor máximo)| 5.67%   | 3.67%   | 2.00%      | 35.27%             |

### 📌 Conclusión Final

El modelo Prophet ha demostrado ser más eficaz, especialmente en su capacidad para reducir el error relativo sobre los valores más altos de la serie. Esto lo convierte en una herramienta valiosa para la predicción de series temporales donde las variaciones estacionales y las discontinuidades son frecuentes.

## 🚀 Próximos Pasos

- Probar diferentes hiperparámetros para ambos modelos
- Evaluar otros modelos de forecasting como XGBoost o LSTM
- Automatizar la actualización de predicciones con nuevos datos

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Si deseas mejorar el proyecto, por favor abre un pull request o una issue.

## 👨‍💻 Autor

**Sergio Delgado**  
📧 sergiodelamp@gmail.com  
🌐 [GitHub - Sergiio02](https://github.com/Sergiio02)
