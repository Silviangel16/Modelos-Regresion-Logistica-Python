<h1 align="center">📊 Modelos Lineales Generalizados en Python</h1> <p align="center"> <img src="https://img.shields.io/badge/PYTHON-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/JUPYTER-NOTEBOOK-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter Notebook"> <img src="https://img.shields.io/badge/MLG-LOG%C3%8DSTICA%20BINARIA%20Y%20MULTINOMIAL-555555?style=for-the-badge" alt="Regresión logística"> <img src="https://img.shields.io/badge/EVALUACI%C3%93N-ENTRENAMIENTO%20%2F%20PRUEBA-2E8B3A?style=for-the-badge" alt="Evaluación"> </p> <p align="center"> Este proyecto aplica modelos lineales generalizados en Python (<code>statsmodels</code>, <code>scikit-learn</code>, <code>pandas</code> y <code>seaborn</code>) para responder dos preguntas: qué factores se asocian con el abandono de clientes de un banco (regresión logística binaria) y qué características químicas permiten diferenciar tres clases de vino (regresión logística multinomial). Los datos provienen de <em>Bank Customer Churn Prediction</em> (Kaggle): 10.000 clientes de Francia, Alemania y España, y de <em>Wine</em> (UCI Machine Learning Repository): 178 vinos de tres cultivares italianos. </p> <p align="center"> <a href="https://www.kaggle.com/search?q=Churn_Modelling.csv">Dataset: abandono de clientes</a> · <a href="https://archive.ics.uci.edu/dataset/109/wine">Dataset: vinos</a> </p>

## 🎯 Problema de Negocio y Objetivos

El proyecto aplica modelos lineales generalizados en Python (`statsmodels` y `scikit-learn`) a dos problemas distintos: uno de negocio bancario y uno de clasificación de productos.

### Ejercicio 1. Abandono de clientes (regresión logística binaria)

Un banco quiere entender por qué se van sus clientes. A partir de `Churn_Modelling.csv` (10.000 clientes de Francia, Alemania y España), el análisis busca responder:

1. **Factores del abandono:** ¿Qué características (edad, país, género, saldo, actividad) se asocian con una mayor probabilidad de abandonar el banco, y cuánto cambian los momios de abandono por cada una?
2. **Capacidad de detección:** Como solo una minoría de clientes abandona, ¿cuántos abandonos detecta realmente el modelo y qué se gana o se pierde al cambiar el umbral de clasificación?

### Ejercicio 2. Tipos de vino (regresión logística multinomial)

Una empresa vinícola quiere saber qué características químicas distinguen sus tres clases de vino. A partir de `wine.data` (178 vinos), el análisis busca responder:

1. **Diferenciación de clases:** ¿Qué tan bien permiten el alcohol, el ácido málico y la intensidad del color distinguir las tres clases, y cómo se comparan las clases 2 y 3 frente a la clase 1?
2. **Estabilidad del modelo:** Con solo 178 vinos, ¿cambian mucho la exactitud y el sentido de los efectos si se repite la partición entre entrenamiento y prueba?

## 📁 Estructura del repositorio

```text
modelos-lineales-generalizados-Python/
├── Data/                   # Bases de datos
│   ├── Churn_Modelling.csv #   Abandono de clientes (Kaggle)
│   └── wine.data           #   Vinos (UCI)
├── Actividad.pdf           # Informe del análisis en PDF
├── analisis_mlg.ipynb      # Cuaderno con el análisis completo (ejercicios 1 y 2)
├── requirements.txt        # Dependencias de Python
└── README.md               # Este archivo
```

> **Nota:** el cuaderno lee los datos desde la carpeta `Data`, que debe estar junto a `analisis_mlg.ipynb`. Si `wine.data` no está, se descarga de UCI.
