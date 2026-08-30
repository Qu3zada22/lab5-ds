# Laboratorio 5 - Minería de Textos y Análisis de Sentimiento

Clasificación de tweets como desastre real o no, usando el dataset "Natural Language Processing with Disaster Tweets" de Kaggle.

**Data Science · UVG 2026**

## Qué es esto

Notebook de Python completo que analiza tweets para determinar si hablan de un desastre real. Incluye limpieza, análisis exploratorio, n-gramas por documento, modelos de clasificación, sentimiento con VADER, comparación estadística y reentrenamiento con una variable de negatividad.

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

2. Sincroniza exactamente el entorno bloqueado (uv crea el entorno virtual automáticamente):

   ```bash
   uv sync --locked
   ```

3. Abre el notebook con JupyterLab:

   ```bash
   uv run jupyter lab Lab5_Completo.ipynb
   ```

El notebook comprueba y descarga de forma reproducible los recursos NLTK `stopwords` y `vader_lexicon` si no están disponibles localmente. La primera ejecución requiere acceso a internet para descargarlos; las siguientes usan la copia local.

## Reproducción completa

Para ejecutar todas las celdas desde cero y conservar resultados y tablas coherentes:

```bash
uv run jupyter nbconvert --to notebook --execute --inplace Lab5_Completo.ipynb
```

La ejecución regenera `train_cleaned.csv`, incluidas las columnas de VADER y `negativity`, y las figuras finales bajo `img/`.

## Qué hay hecho

- **Parte 1:** carga de datos, limpieza de texto (minúsculas, sin URLs/menciones/números/stopwords)
- **Parte 2A:** frecuencia de palabras por categoría, palabras discriminantes, nube de palabras
- **Parte 2B:** unigramas, bigramas y trigramas generados dentro de cada tweet, con frecuencia y probabilidad normalizada
- **Parte 3:** entrenamiento de 3 modelos (Naive Bayes, Regresión Logística, SVM), evaluación con métricas y selección del mejor modelo
- **Parte 4:** sentimiento VADER, 10 extremos positivos/negativos y comparación Mann–Whitney U por categoría
- **Parte 5:** reentrenamiento con `negativity`, comparación contra el baseline y función final `clasificar_tweet()` basada en la evidencia

## Estructura

- `Lab5_Completo.ipynb`: análisis reproducible y respuestas de los ejercicios 1–10.
- `train.csv`: datos originales de entrenamiento.
- `train_cleaned.csv`: datos procesados con sentimiento y negatividad.
- `img/`: figuras reproducibles generadas por el notebook.
- `docs/lab5.md`: consigna del laboratorio.
- `pyproject.toml` y `uv.lock`: dependencias directas y resolución exacta del entorno.

## Estado y entregables pendientes

Los ejercicios de código y análisis 1–10 están completos. Aún requieren gestión manual fuera del notebook:

- elaborar y entregar el informe final en PDF (ejercicio 11);
- agregar el enlace del documento colaborativo del grupo, si la plataforma lo exige;
- agregar o entregar el enlace del repositorio según las instrucciones del curso.
