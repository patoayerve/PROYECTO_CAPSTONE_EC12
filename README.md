# PROYECTO_CAPSTONE_EC12
PROYECTO CAPSTONE EC12

INTEGRANTES:

- Cesar Ayerve
- Lizeth Peña

# Proyecto Capstone EC12 - Predicción de Valores Financieros

Este repositorio contiene el proyecto de análisis y predicción de valores financieros utilizando técnicas de regresión y series temporales. Se han implementado modelos de Ridge Regression y ARIMA para predecir valores futuros de ciertas variables financieras clave para el año 2024.

## Requisitos

Antes de ejecutar el notebook, es necesario tener las siguientes dependencias instaladas:

```bash
pip3 install scikit-learn pandas numpy scipy statsmodels matplotlib seaborn sqlalchemy ipython pyodbc joblib
```

## Ejecución del Notebook

1. **Clona el repositorio:**

   ```bash
   git clone https://github.com/patoayerve/PROYECTO_CAPSTONE_EC12.git
   cd proyecto_capstone_ec12
   ```

2. **Instala las dependencias:**

   Ejecuta el siguiente comando para instalar las dependencias necesarias.

   ```bash
   pip3 install scikit-learn pandas numpy scipy statsmodels matplotlib seaborn sqlalchemy ipython pyodbc joblib
   ```

3. **Ejecuta el Jupyter Notebook:**

   Inicia Jupyter Notebook desde el directorio del proyecto:

   ```bash
   jupyter notebook PROYECTO_CAPSTONE_EC12.ipynb
   ```

4. **Configuración de la base de datos (opcional):**

   Si deseas utilizar una base de datos SQL Server dockerizada en lugar del archivo CSV, asegúrate de que tu base de datos esté configurada y actualiza las cadenas de conexión en el notebook.

   ```python
   server = '127.0.0.1'
   database = 'DB_CAPSTONE_NTL'
   username = 'tu_usuario'
   password = 'tu_contraseña'
   driver = 'ODBC Driver 17 for SQL Server'

   connection_string = f'mssql+pyodbc://{username}:{password}@{server}/{database}?driver={driver}'
   engine = create_engine(connection_string)
   ```

   Para este caso, se debe utilizar un archivo CSV :

   ```python
   ruta_archivo = 'PYL_2020_2023_CLEAN_CAPSTONE.csv'
   datos = pd.read_csv(ruta_archivo)
   ```

## Descripción del Proyecto

Este proyecto sigue la metodología CRISP-DM y se estructura en las siguientes etapas:

1. **Comprensión del Negocio:**
   - Objetivo: Predecir valores futuros para varias columnas financieras.
   - Modelos utilizados: Ridge Regression y ARIMA.

2. **Comprensión de los Datos:**
   - Análisis de los datos, limpieza y preprocesamiento.

3. **Preparación de los Datos:**
   - Selección y transformación de variables para los modelos.

4. **Modelado:**
   - Implementación de modelos de regresión Ridge y ARIMA.
     
5. **Evaluación:**
   - Evaluación de modelos de regresión Ridge y ARIMA.

## Resultados

El notebook incluye análisis descriptivo, visualización de tendencias y predicciones utilizando los modelos mencionados.
