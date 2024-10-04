# Challenge-ML
## Proyecto: Análisis de Dataset de Contratos

## Descripción

Este proyecto tiene como objetivo analizar el dataset **CUAD_v1** proporcionado para el challenge. El dataset contiene información de contratos legales en diferentes formatos y está organizado en varias subcarpetas con documentos en PDF, TXT y datos estructurados en CSV y JSON. El propósito es aplicar un proceso ETL para extraer, transformar y analizar la información, generando reportes y conclusiones útiles a partir de los datos.

## Documentación paso a paso
1. Primero que nada necesitamos obtener de Kaggle nuestro API Token, el cual lo obtenemos desde nuestro perfil de Kaggle, Esto nos va a generar el archivo kaggle.json.
2. Luego necesitamos en una carpeta de google drive depositar el kaggle.json previamente generado, y luego procederemos a crear un google colab, en el cual vamos a hacer lo siguiente:
3. Descargamos el dataset dentro de nuestro google colab con los siguientes comandos:
```
! pip install kaggle
```
```
from google.colab import drive
drive.mount('/content/drive')
```
Creamos para mayor comodidad a la hora de trabajar una carpeta oculta .kaggle en el directorio raiz
```
!mkdir ~/.kaggle
```
En donde dice "Challenge ML" ahí deben poner el nombre de la carpeta donde guardaron el API Token de Kaggle
```
! cp /content/drive/MyDrive/"Challenge ML"/Kaggle_API/kaggle.json ~/.kaggle/
```
```
! chmod 600 ~/.kaggle/kaggle.json
```
Ahora con el siguiente comando vamos a descargar el dataset dentro de nuestro google colab
```
! kaggle datasets download konradb/atticus-open-contract-dataset-aok-beta
```
Lo descomprimimos
```
! unzip atticus-open-contract-dataset-aok-beta.zip
```
Y con esto ya tendriamos Descargado dentro de nuestro google colab el dataset.



## Enlaces del Proyecto
Puedes acceder al notebook y explorarlo a través de los siguientes enlaces:

-**Ver en GitHub**:
[notebook.ipynb](https://github.com/Fedesin/Challenge-ML/blob/main/Untitled0.ipynb)
-**Abrir en Google Colab**:[Abrir en Google Colab](https://colab.research.google.com/github/Fedesin/Challenge-ML/blob/main/Untitled0.ipynb)

### Requisitos Previos

1. **Entorno de desarrollo:**
   - Google Colab o entorno local con Python 3.7+
   - Conexión a internet para descargar el dataset desde Kaggle.

2. **Librerías necesarias:**
   - pandas
   - numpy
   - matplotlib
   - seaborn
   - PyMuPDF (si es necesario extraer texto de PDFs)

3. **Dataset:**
   - Descargue el dataset "Atticus Open Contract Dataset (AOK-Beta)" desde [Kaggle](https://www.kaggle.com/datasets/konradb/atticus-open-contract-dataset-aok-beta) y colóquelo en la carpeta `data/` del proyecto.

### Instalación de Dependencias

Ejecute el siguiente comando para instalar las dependencias del proyecto:
```bash
pip install -r requirements.txt

