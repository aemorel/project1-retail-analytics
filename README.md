# Análisis y Predicción de Ventas en una Tienda de Retail

## Introducción al Proyecto

Este proyecto tiene como objetivo realizar un análisis completo y predicción de ventas para una tienda de retail, utilizando técnicas de manipulación de datos, análisis exploratorio y algoritmos de machine learning. A lo largo de este proyecto, se emplearán herramientas como NumPy, Pandas, y técnicas de aprendizaje automático para aplicar conceptos clave de ciencia de datos. Este proyecto representa una excelente oportunidad para que los estudiantes desarrollen y demuestren sus habilidades en ciencia de datos y machine learning.

## Dataset

Para este proyecto, utilizamos el **Retail Sales Dataset** de Kaggle (2023-2024), que contiene información sobre las ventas diarias de varios productos en múltiples tiendas. El dataset incluye detalles como fecha, producto, cantidad vendida, y tienda. Puedes descargar el dataset desde Kaggle y guardarlo en la carpeta `data/` del proyecto para comenzar el análisis.

## Estructura del Proyecto

La estructura del proyecto está organizada de la siguiente manera:

- `data/`: Contiene los archivos de datos, como `retail_sales.csv`.
- `notebooks/`: Contiene los notebooks de Jupyter con el análisis exploratorio y las predicciones.
- `src/`: Contiene el código fuente, scripts y funciones utilizados en el proyecto.
- `README.md`: Este archivo.

## Configuración Inicial del Proyecto

### Crear un Repositorio en GitHub

1. Ve a GitHub y crea un nuevo repositorio, nombrado, por ejemplo, **retail-sales-analysis**.
2. Clona el repositorio en tu máquina local con el siguiente comando:

    ```bash
    git clone https://github.com/tu_usuario/retail-sales-analysis.git
    cd retail-sales-analysis
    ```

3. Crea y cambia a la rama `development` para trabajar en la versión de desarrollo:

    ```bash
    git checkout -b development
    ```

4. Agrega el archivo `README.md` y realiza un commit inicial:

    ```bash
    git add README.md
    git commit -m "Add README.md"
    ```

5. Sube los cambios a tu repositorio en GitHub:

    ```bash
    git push origin development
    ```

## Instrucciones de Instalación

1. Clona el repositorio (si aún no lo has hecho):

    ```bash
    git clone https://github.com/tu_usuario/retail-sales-analysis.git
    cd retail-sales-analysis
    ```

2. Instala las dependencias requeridas para el proyecto. Asegúrate de tener un entorno virtual activo y luego ejecuta:

    ```bash
    pip install -r requirements.txt
    ```

## Uso

1. Asegúrate de que los datos están en la carpeta `data/` (por ejemplo, `data/retail_sales.csv`).
2. Ejecuta los notebooks de Jupyter en la carpeta `notebooks/` para realizar el análisis de datos, visualizar resultados y generar predicciones.

## Guía de Desarrollo

### Parte 1: Análisis Básico con NumPy

En esta primera parte, realizaremos operaciones básicas de análisis y manipulación de datos utilizando NumPy.

#### Carga y Preprocesamiento de Datos

La función de carga de datos permite importar el archivo `retail_sales.csv` y realizar un preprocesamiento básico:

```python
import numpy as np

def cargar_datos(ruta_archivo):
    datos = np.genfromtxt(ruta_archivo, delimiter=',', skip_header=1)
    return datos

if __name__ == "__main__":
    ruta_archivo = 'data/retail_sales.csv'
    datos = cargar_datos(ruta_archivo)
    print(datos)