# Dashboard para Análisis de Órdenes de Trabajo DSL

Este proyecto proporciona una plataforma interactiva para el análisis y visualización de datos de órdenes de trabajo de la empresa DSL. Utilizando **Streamlit** para la interfaz y **Plotly** para la generación de gráficos, el objetivo es permitir a los usuarios realizar análisis exploratorios, crear gráficos personalizados y obtener una visión más clara de los datos.

## Requisitos

Para ejecutar este proyecto, necesitarás tener instaladas las siguientes librerías:

- `pandas`
- `plotly`
- `streamlit`
- `openpyxl` (para leer archivos Excel)

Puedes instalarlas utilizando el siguiente comando:

```bash
pip install pandas plotly streamlit openpyxl
```

# Descripción del Proyecto

Este dashboard permite analizar y visualizar diferentes aspectos de las órdenes de trabajo de la empresa DSL a través de gráficos interactivos, análisis exploratorio y dashboards personalizados. Las principales funcionalidades son:

- **Generación de Gráficos**: Permite crear gráficos de barras, líneas, boxplots, histogramas y gráficos de pastel para explorar los datos.
- **Análisis Exploratorio**: Proporciona estadísticas descriptivas, análisis de datos faltantes, correlación entre columnas y distribución de datos categóricos y numéricos.
- **Dashboard Personalizado**: Permite a los usuarios seleccionar métricas y filtros para crear un dashboard con la información más relevante.
- **Dashboard Anual**: Presenta un resumen de los datos con análisis por año.
- **Interactividad**: Los gráficos y análisis son interactivos, permitiendo a los usuarios filtrar y seleccionar diferentes parámetros.

## Estructura del Proyecto

El proyecto está dividido en varias funciones y componentes, los cuales permiten una interacción fluida con los datos y la visualización:

### 1. Funciones de Visualización

#### a) `grafico_boxplot(df)`
Genera un gráfico de cajas para analizar la distribución de valores de una columna seleccionada, agrupados por una columna categórica.

#### b) `grafico_lineas(df)`
Genera un gráfico de líneas para visualizar la relación entre dos columnas, mostrando los 10 valores más frecuentes en la columna seleccionada.

#### c) `grafico_histograma(df)`
Genera un histograma para una columna numérica seleccionada, permitiendo observar la distribución de los datos.

#### d) `grafico_pastel(df)`
Genera un gráfico de pastel que muestra la distribución de los valores más frecuentes en una columna categórica seleccionada.

### 2. Análisis Exploratorio
La función `analisis_exp(df)` realiza un análisis exploratorio completo de los datos:
- Muestra la cabecera del DataFrame.
- Proporciona estadísticas descriptivas de las columnas numéricas.
- Visualiza la cantidad de datos nulos en las columnas.
- Calcula la correlación entre columnas numéricas.
- Muestra la distribución de las columnas categóricas y numéricas.

### 3. Generación de Dashboard Personalizado
La función `crear_grafico(tipo, df)` permite al usuario seleccionar el tipo de gráfico que desea generar, desde gráficos de barras hasta gráficos de líneas o pastel, personalizando la visualización según las necesidades del análisis.

### 4. Función Principal
La función `principal()` carga los datos y gestiona la interfaz del usuario, permitiendo la selección del archivo de datos, el tipo de análisis a realizar y la generación de gráficos interactivos.
