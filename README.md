# Laboratorio 5 - Minería de Textos y Análisis de Sentimiento

Clasificación de tweets como desastre real o no, usando el dataset "Natural Language Processing with Disaster Tweets" de Kaggle.

**Data Science · UVG 2026**

## Qué es esto

Notebook de Python que analiza tweets para determinar si hablan de un desastre real (terremoto, incendio, etc.) o no. Incluye limpieza de texto, análisis exploratorio, n-gramas, y un modelo de clasificación con una función que recibe un tweet nuevo y lo clasifica.

## Cómo correrlo

1. Instala `uv` si no lo tienes:

   - **macOS / Linux:**

     ```bash
     curl -LsSf https://astral.sh/uv/install.sh | sh
     ```

   - **Windows (PowerShell):**

     ```powershell
     powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
     ```

2. Instala las dependencias (uv crea el entorno virtual automáticamente a partir de `pyproject.toml`):

   ```bash
   uv sync
   ```

3. Descarga las stopwords de NLTK (solo la primera vez):

   ```bash
   uv run python -c "import nltk; nltk.download('stopwords')"
   ```

4. Abre el notebook:

   ```bash
   uv run jupyter notebook Lab5_Completo.ipynb
   ```

## Qué hay hecho

- **Parte 1:** carga de datos, limpieza de texto (minúsculas, sin URLs/menciones/números/stopwords)
- **Parte 2A:** frecuencia de palabras por categoría, palabras discriminantes, nube de palabras
- **Parte 2B:** bigramas y trigramas, análisis de contexto
- **Parte 3:** entrenamiento de 3 modelos (Naive Bayes, Regresión Logística, SVM), evaluación con métricas y selección del mejor modelo
- **Parte 4:** función `clasificar_tweet()` que recibe un tweet sin procesar y devuelve si es desastre real o no

## Qué falta

- **Ejercicio 8:** clasificación de sentimiento (positivo/negativo/neutro) de cada tweet
- **Ejercicio 9:** identificar los 10 tweets más negativos y los 10 más positivos, y en qué categoría están
- **Ejercicio 10:** crear variable de "negatividad" del tweet, agregarla al dataset y reentrenar el modelo de la Parte 3 para ver si mejora
