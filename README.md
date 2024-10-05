# 💻 Challenge-ML
## 📊 Proyecto: Análisis de Dataset de Contratos

### 📝 Descripción

Este proyecto tiene como objetivo analizar el dataset **CUAD_v1** proporcionado para el challenge. El dataset contiene información de contratos legales en diferentes formatos y está organizado en varias subcarpetas con documentos en PDF, TXT y datos estructurados en CSV y JSON. El propósito es aplicar un proceso ETL para extraer, transformar y analizar la información, generando reportes y conclusiones útiles a partir de los datos.

### 🎯 Objetivo del Proyecto

- Realizar un análisis exploratorio del dataset para identificar patrones y obtener insights útiles.
- Responder preguntas clave relacionadas con los contratos de los proveedores, tales como:
  - 📌 ¿Cuál es el proveedor con más contratos asociados?
  - 📌 ¿Cuál es el plazo de renovación de contrato más breve? ¿Y el más extenso?
  - 📌 ¿Cuál es la fecha de inicio de contrato más antigua?
  - 📌 ¿Cuál es el país asociado a la ley aplicable? ¿A qué continente pertenece?

Implementar el proceso ETL (Extracción, Transformación y Carga) para preparar los datos para el análisis.
Generar gráficos y reportes que ayuden a visualizar las respuestas a las preguntas clave.

### 🔄 Proceso ETL Implementado

El proceso ETL (Extracción, Transformación y Carga) se ha implementado de la siguiente manera:

1. **Extracción:** Descarga y carga del dataset desde Kaggle utilizando la API de Kaggle.
2. **Transformación:** Limpieza y estructuración de los datos en un DataFrame de pandas.
3. **Carga:** Almacenamiento de los datos transformados en un CSV limpio (`dataset_limpio.csv`), listo para su análisis.


## 📥 Proceso para descargar el dataset y aplicarlo en el colab
1. Obtener el API Token de Kaggle desde el perfil de Kaggle, lo cual generará el archivo `kaggle.json`.
2. Colocar el archivo `kaggle.json` en una carpeta de Google Drive.
3. Crear un notebook en Google Colab e iniciar con los siguientes pasos:
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

## 📌 Nota: Cómo Replicar el Análisis

Si deseas replicar los pasos y resultados obtenidos en este proyecto, simplemente sigue estos pasos:

1. **Abre el notebook en Google Colab** usando el enlace proporcionado en la sección de Enlaces del Proyecto.
2. **Ejecuta cada bloque de código en orden**. Los bloques ya están organizados de manera que guían el flujo del proceso ETL y análisis de datos. Cada bloque incluye comentarios para facilitar su comprensión y seguimiento.
3. Asegúrate de tener las librerías necesarias instaladas y la conexión a Kaggle configurada según las instrucciones indicadas.
4. **Observa los resultados y gráficos generados** después de ejecutar cada bloque de código, los cuales reflejarán el análisis de los datos según el proceso ETL implementado.

De esta manera, podrás obtener los mismos resultados y visualizaciones sin necesidad de realizar ninguna configuración adicional, más allá de los pasos iniciales de configuración del entorno.

### 🛠️ Logging Implementado

El proceso ETL incluye la funcionalidad de logging para registrar los eventos importantes del proceso, como inicio y fin del proceso, advertencias y errores. El archivo de logs se genera en `etl_process.log`.

### 📊 Análisis de Datos

- Se han generado gráficos y visualizaciones para responder a las preguntas del challenge.
- Se han incluido insights adicionales basados en el análisis exploratorio de los datos.


## 🔗 Enlaces del Proyecto
Puedes acceder al notebook y explorarlo a través de los siguientes enlaces:

-**Ver en GitHub**:
[notebook.ipynb](https://github.com/Fedesin/Challenge-ML/blob/main/Colab_challenge_meli.ipynb)
-**Abrir en Google Colab**:[Abrir en Google Colab](https://colab.research.google.com/github/Fedesin/Challenge-ML/blob/main/Colab_challenge_meli.ipynb)

### ⚙️ Requisitos Previos

1. **Entorno de desarrollo:**
   - Google Colab o entorno local con Python 3.7+
   - Conexión a internet para descargar el dataset desde Kaggle.

2. **Librerías necesarias:**
   - pandas
   - numpy
   - matplotlib
   - logging 

3. **Dataset:**
   - Descargue el dataset "Atticus Open Contract Dataset (AOK-Beta)" desde [Kaggle](https://www.kaggle.com/datasets/konradb/atticus-open-contract-dataset-aok-beta) y colóquelo en la carpeta `data/` del proyecto.


### 📌 Conclusiones
Este proyecto representó un desafío interesante y enriquecedor, ya que abordé una rama en la que no había trabajado anteriormente. A lo largo del proceso, pude aprender muchísimo sobre técnicas de ETL y análisis de datos aplicados a contratos legales. A pesar de ser un terreno nuevo, logré alcanzar resultados satisfactorios y obtener insights relevantes a partir del dataset. Sin dudas, fue una experiencia valiosa que me permitió expandir mis conocimientos y habilidades en análisis de datos.

### ℹ️ Aclaración final
Para la realización de este proyecto, se utilizaron herramientas de asistencia como ChatGPT para resolver dudas, mejorar la estructura del código y optimizar el análisis de datos. Todas las implementaciones fueron realizadas y verificadas manualmente para asegurar la comprensión y calidad del trabajo.

Aunque este proyecto podría haberse desarrollado en un entorno local utilizando Python, opté por utilizar Google Colab. La elección de Colab se debió a que, al investigar cómo descargar y procesar el dataset desde Kaggle, encontré que Colab es una herramienta muy utilizada para tareas de análisis de datos y machine learning. 

Además, al usar Colab, no tuve que preocuparme por la configuración de dependencias y librerías en mi entorno local, lo que me permitió concentrarme en el análisis y procesamiento del dataset de manera más eficiente.

