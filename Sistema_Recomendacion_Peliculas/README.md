
# 🎬 Sistema de Recomendación de Películas (TMDB)

Este proyecto implementa un sistema de recomendación de películas utilizando el dataset de TMDB disponible en Kaggle.

---

## 🎯 Objetivo del proyecto

Construir un sistema de recomendación de películas basado en contenido textual, utilizando las descripciones (overview) de las películas para encontrar similitudes y sugerir títulos parecidos.

---

## 🧠 Lógica del modelo

El modelo está construido sobre dos componentes fundamentales:

- **TF-IDF (Term Frequency-Inverse Document Frequency)**: vectoriza el texto para representar cada película como un vector numérico según sus características textuales.
- **Cosine Similarity**: mide la similitud entre películas comparando el ángulo entre sus vectores.

Ambas herramientas permiten identificar qué películas son más parecidas entre sí según el contenido que se elija.

---

## 🔄 Modelo adaptable

Una de las fortalezas del sistema es su adaptabilidad: se puede modificar fácilmente el criterio de recomendación simplemente cambiando la columna de entrada textual.

Por ejemplo:
- Si se desea recomendar por **sinopsis**, se utiliza la columna `overview`.
- Si se desea recomendar por **género**, se utiliza la columna `genres` (preprocesada).
- También es posible usar columnas como `keywords`, `cast` o `director`, si se transforman previamente en texto plano.

📌 **Importante**: la columna utilizada debe estar en formato de **texto simple (string)**. Si está en formato estructurado (como listas en JSON), debe procesarse primero.

---

## 📌 Ejemplo de uso

Se probó el modelo con la película **"The Dark Knight"**, usando la sinopsis como base para calcular similitud:

```python
recomendar_peliculas("The Dark Knight", n=5)
```

Resultado (resumen simplificado):

| title                 | overview                                              |
|-----------------------|-------------------------------------------------------|
| The Dark Knight Rises | Continuación directa de la historia de Batman...     |
| Batman Returns        | Batman se enfrenta al Pingüino y a Catwoman...       |
| The Secret            | Película con tono introspectivo y filosófico...      |
| Batman Forever        | El caballero oscuro enfrenta nuevos enemigos...      |
| Batman                | Origen del personaje y su lucha contra el crimen...  |

Esto demuestra que el sistema puede identificar contenido relacionado tanto por saga como por estilo narrativo.

---

## 📁 Archivos incluidos

- `Sistema_Recomendación_Peliculas.ipynb`: notebook con el modelo completo
- `requirements.txt`: librerías necesarias para ejecutar el proyecto
- `README.md`: explicación detallada del proyecto

---

## 🧪 Cómo ejecutar

1. Cloná este repositorio o descargá el `.zip`.
2. Instalá las dependencias necesarias:

```bash
pip install -r requirements.txt
```

3. Abrí el notebook `Sistema_Recomendación_Peliculas.ipynb` y ejecutá celda por celda.

---

## 📊 Dataset utilizado

- [TMDB Movie Metadata - Kaggle](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

---

## 🛠 Tecnologías utilizadas

- Python 3
- Google Colab
- Pandas
- Scikit-learn

---
