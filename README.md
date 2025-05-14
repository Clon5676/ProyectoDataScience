# ProyectoDataScience

- ** Integrantes:**
- Javier caniz
- Luis Villela

#  Predicción de Popularidad de Videojuegos en Steam

Este proyecto busca predecir si un videojuego publicado en Steam será **popular o no**, utilizando información disponible antes de su lanzamiento. La predicción se hace con un modelo de clasificación binaria que puede ayudar a desarrolladores y estudios a tomar decisiones sobre precios, características del juego y estrategias de publicación.

---

##  Repositorio

[GitHub - ProyectoDataScience](https://github.com/Clon5676/ProyectoDataScience)

---

## Problema a Resolver

> ¿Será popular un videojuego en Steam según sus atributos antes del lanzamiento?

Se define popularidad con base en la variable `Estimated owners`, que estima cuántos usuarios poseen el juego. El umbral que separa popular vs. no popular se define tras el análisis exploratorio (EDA), buscando un buen balance de clases.

---

## Dataset Utilizado

- **Nombre:** Steam Games Dataset  
- **Fuente:** [Kaggle - Steam Games Dataset](https://www.kaggle.com/datasets/fronkongames/steam-games-dataset)  
- **Observaciones:** ~110,000 videojuegos  
- **Features disponibles:** 39 columnas  
- **Features utilizadas en el modelo:** al menos 20, con tratamiento específico para cada una  
- **Features categóricas consideradas:**
  - `Genres`
  - `Categories`
  - `Tags`
  - `Supported languages`
  - `Developers`
  - `Publishers`
  - `Required age` (agrupada por rangos)

---

## Uso de large files
- **Link de como meter archivos grandes al git:** (https://docs.github.com/en/repositories/working-with-files/managing-large-files/configuring-git-large-file-storage) 

---

## Modelo Final

- **Tipo de modelo:** Regresión Logística
- **Target (variable objetivo):** `Estimated owners` (binaria: popular / no popular)
- **Tratamiento de datos:**
  - Transformación de variables categóricas a numéricas
  - Feature engineering en columnas como `price`, `release date`, `tags`, etc.
  - Feature selection mediante:
    - Heatmap de correlación
    - Importancia de coeficientes
    - WoE + IV

- **Métricas de evaluación:**
  - Accuracy
  - Precision
  - Recall
  - KS Score
  - Matriz de confusión + interpretación

