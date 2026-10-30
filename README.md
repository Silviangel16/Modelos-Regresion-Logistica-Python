<h1 align="center">📊 Modelos Lineales Generalizados para Clasificación</h1> <p align="center"> <img src="https://img.shields.io/badge/PYTHON-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/JUPYTER-NOTEBOOK-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter Notebook"> <img src="https://img.shields.io/badge/MLG-LOG%C3%8DSTICA%20BINARIA%20Y%20MULTINOMIAL-555555?style=for-the-badge" alt="Regresión logística"> <img src="https://img.shields.io/badge/EVALUACI%C3%93N-ENTRENAMIENTO%20%2F%20PRUEBA-2E8B3A?style=for-the-badge" alt="Machine Learning"> </p> <p align="center"> Este proyecto aplica modelos lineales generalizados en Python (<code>statsmodels</code>, <code>scikit-learn</code>, <code>pandas</code> y <code>seaborn</code>) para responder dos preguntas: qué factores se asocian con el abandono de clientes de un banco (regresión logística binaria) y qué características químicas permiten diferenciar tres clases de vino (regresión logística multinomial). </p> <p align="center"> <a href="https://www.kaggle.com/search?q=Churn_Modelling.csv">Dataset: abandono de clientes</a> · <a href="https://archive.ics.uci.edu/dataset/109/wine">Dataset: vinos</a> </p>

 
### Caso 1. Abandono de clientes (regresión logística binaria)
<img width="1559" height="260" alt="image" src="https://github.com/user-attachments/assets/8b4e1038-c079-4547-a968-3d6f8eef9abe" />



### Caso 2. Tipos de vino (regresión logística multinomial)
<img width="1439" height="241" alt="image" src="https://github.com/user-attachments/assets/d41f1860-b515-4ba6-b665-c7d689efbf1f" />



## 📁 Estructura del repositorio

```text
modelos-lineales-generalizados-Python/
├── Enunciado_casos_1y2.pdf
├── Data/            
│   ├── Churn_Modelling.csv 
│   └── wine.data                 
├── Analisis_Python/ 
│   ├── 01_Analisis_Banco 
│   └── 02_Analisis_Vino
├── Reportes/
│   ├── 01_Reporte_Caso1.pdf
│   └── 02_Reporte_Caso2.pdf
├── Imagenes/    
└── README.md              
```


### Ejercicio 1. Abandono de clientes

<img width="923" height="137" alt="image" src="https://github.com/user-attachments/assets/12645c79-42f9-4f90-971b-cca4a9b783d4" />


### Ejercicio 2. Tipos de vino

| Hallazgo | Resultado | Lectura |
|:---|:---:|:---|
| Exactitud en prueba | 86,8 % | 46 de 53 vinos bien clasificados; por clase: 88,9 %, 85,7 % y 85,7 % |
| Intensidad del color, clase 3 vs. 1 | RRR 2,773 | Cada unidad adicional de color aumenta 177,3 % los momios de ser clase 3 |
| Alcohol, clase 2 vs. 1 | RRR 0,013 | Más alcohol hace mucho menos probable la clase 2 frente a la 1 |
| Ácido málico, clase 3 vs. 1 | RRR 5,685 | Cada unidad adicional multiplica por 5,7 los momios de ser clase 3 |
| Estabilidad de la exactitud (200 particiones) | 86,5 % ± 3,6 | El 95 % central de las particiones va de 79,2 % a 92,5 % |
| Estabilidad de los efectos | 100 % mismo signo, salvo uno | Solo el ácido málico en la clase 2 cambia de signo (66,5 %) |

<p align="center">
  <img src="Imagenes/alcohol_por_clase.png" alt="Alcohol por clase de vino" width="48%">
  <img src="Imagenes/color_por_clase.png" alt="Intensidad del color por clase de vino" width="48%">
</p>

<p align="center">
  <img src="Imagenes/probabilidades_clases_vino.png" alt="Probabilidades estimadas por clase" width="48%">
  <img src="Imagenes/curva_color_clases.png" alt="Probabilidad de cada clase según el color" width="48%">
</p>

<p align="center">
  <img src="Imagenes/estabilidad_exactitud.png" alt="Distribución de la exactitud en 200 particiones" width="60%">
</p>

> **Conclusión:** la edad, la actividad del cliente y el país explican bien quién abandona, pero con un umbral de 0,50 el modelo detecta pocos abandonos. En los vinos, la intensidad del color y el alcohol separan bien las tres clases; con solo 178 vinos, la exactitud es un rango y no un valor único, y el efecto del ácido málico en la clase 2 no es confiable.
>
> ## Los datos provienen de <em>Bank Customer Churn Prediction</em> (Kaggle): 10.000 clientes de Francia, Alemania y España, y de <em>Wine</em> (UCI Machine Learning Repository): 178 vinos de tres cultivares italianos.

