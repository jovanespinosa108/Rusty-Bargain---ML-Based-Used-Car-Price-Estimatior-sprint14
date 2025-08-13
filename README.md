# Rusty-Bargain---ML-Based-Used-Car-Price-Estimatior-sprint14
Rusty Bargain is a second-hand car sales service developing a mobile application aimed at helping customers quickly estimate the market value of their used vehicles. This project involves building and evaluating machine learning models to predict car prices based on technical specifications, historical data, and other features available in the app.

The project compares multiple regression models — including linear regression, decision trees, random forests, and gradient boosting methods (CatBoost, LightGBM, and optionally XGBoost). Key factors considered are model accuracy (using RMSE), prediction speed, and training time. The ultimate goal is to deliver a reliable, fast, and efficient pricing model for Rusty Bargain's digital platform.

Rusty Bargain — Predicción de precios de coches usados / Used Car Price Prediction
📌 Descripción del proyecto / Project Description
ES:
Rusty Bargain es un servicio de venta de coches de segunda mano que está desarrollando una aplicación para atraer nuevos clientes. Gracias a la app, los usuarios pueden averiguar rápidamente el valor de mercado de su coche y acceder a información como historial, especificaciones técnicas, versiones de equipamiento y precios.

El objetivo de este proyecto es crear un modelo de Machine Learning que determine el valor de mercado de un coche con la mayor precisión posible, manteniendo tiempos de predicción y entrenamiento eficientes.

EN:
Rusty Bargain is a used car sales service developing an app to attract new customers. The app allows users to quickly find the market value of their car and access information such as history, technical specifications, trim versions, and prices.

The goal of this project is to build a Machine Learning model that predicts the market value of a car with the highest possible accuracy while keeping prediction and training times efficient.

🎯 Objetivos / Objectives
ES: Alta calidad de predicción, baja latencia de predicción y entrenamiento optimizado.

EN: High prediction accuracy, low prediction latency, and optimized training time.

📂 Dataset
Path: /datasets/car_data.csv

ES — Variables:

Columna	Descripción
DateCrawled	Fecha en la que se descargó el perfil
VehicleType	Tipo de carrocería
RegistrationYear	Año de matriculación
Gearbox	Tipo de caja de cambios
Power	Potencia (CV)
Model	Modelo
Mileage	Kilometraje (km)
RegistrationMonth	Mes de matriculación
FuelType	Tipo de combustible
Brand	Marca
NotRepaired	Con o sin reparaciones pendientes
DateCreated	Fecha de creación del perfil
NumberOfPictures	Número de fotos
PostalCode	Código postal
LastSeen	Última actividad del usuario
Price	(Objetivo) Precio en euros

EN — Features:

Column	Description
DateCrawled	Date the profile was downloaded
VehicleType	Body type
RegistrationYear	Registration year
Gearbox	Transmission type
Power	Power (HP)
Model	Vehicle model
Mileage	Mileage (km)
RegistrationMonth	Registration month
FuelType	Fuel type
Brand	Brand
NotRepaired	With or without pending repairs
DateCreated	Profile creation date
NumberOfPictures	Number of pictures
PostalCode	Postal code
LastSeen	Last user activity
Price	(Target) Price in euros

🛠️ Metodología / Methodology
ES: Exploración y limpieza de datos (valores ausentes, tipos de datos, outliers).
EN: Data exploration and cleaning (missing values, data types, outliers).

ES: Codificación de variables categóricas según el modelo (OHE, codificación interna de LightGBM/CatBoost).
EN: Encoding categorical variables according to the model (OHE, LightGBM/CatBoost native encoding).

ES: Entrenamiento de modelos:

Regresión Lineal (prueba base)

Árbol de Decisión

Bosque Aleatorio

LightGBM (Gradient Boosting)

CatBoost (opcional)

XGBoost (opcional)

EN: Model training:

Linear Regression (baseline)

Decision Tree

Random Forest

LightGBM (Gradient Boosting)

CatBoost (optional)

XGBoost (optional)

ES: Evaluación con RMSE, medición de tiempo de entrenamiento y predicción.
EN: Evaluation using RMSE, training time, and prediction time measurement.

📊 Resultados de los modelos / Model Results
Modelo / Model	RMSE (€)	Tiempo de Entrenamiento (s) / Training Time (s)	Tiempo de Predicción (s) / Prediction Time (s)
Linear Regression	2638.13	24.28	0.57
Ridge Regression	2637.90	4.48	0.80
Lasso Regression	2666.56	902.60	0.60
Decision Tree	2068.40	10.87	0.21
Random Forest	1678.38	383.22	5.15
LightGBM	1782.07	29.27	0.55
CatBoost	1695.03	50.93	0.30
Optimized Random Forest	1666.42	394.48	3.89
Optimized LightGBM	1740.05	20.02	2.25

ES — Interpretación:

El Random Forest optimizado logró el menor RMSE, lo que indica la mejor precisión.

LightGBM optimizado tuvo un buen equilibrio entre precisión y velocidad de entrenamiento.

Los modelos lineales sirvieron como referencia para validar mejoras.

Los modelos basados en árboles presentaron menor error que los modelos lineales.

EN — Interpretation:

Optimized Random Forest achieved the lowest RMSE, indicating the highest accuracy.

Optimized LightGBM had a good balance between accuracy and training speed.

Linear models were used as a baseline to validate improvements.

Tree-based models showed lower error compared to linear models.

📌 Observaciones / Notes
ES: La regresión lineal se usó como referencia. LightGBM y CatBoost aceptan variables categóricas nativamente, XGBoost requiere OHE. Se priorizó el ajuste limitado de hiperparámetros para reducir tiempo.

EN: Linear regression was used as a reference. LightGBM and CatBoost handle categorical variables natively, while XGBoost requires OHE. Limited hyperparameter tuning was prioritized to save time.

💻 Tecnologías / Technologies
Python 3.x

Pandas

NumPy

Scikit-learn

LightGBM

CatBoost

XGBoost (optional)

Jupyter Notebook

