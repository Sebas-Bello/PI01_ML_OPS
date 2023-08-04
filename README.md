![wink](https://github.com/Sebas-Bello/PI01_ML_OPS/blob/938ebe095c559a98118df50d8e47c9b7e3f8dfe2/MLOPS.gif)


## Índice 
<!-- TABLA DE CONTENIDO -->
<details>
  <summary>Tabla de contenido</summary>
  <ol>
    <li><a href="#Índice">Index</a></li>
    <li><a href="#Introducción">Introduction</a></li>
    <li><a href="#Objetivo">Objective</a></li>
    <li><a href="#ETL">ETL</a></li>
    <li><a href="#EDA">EDA</a></li>
    <li><a href="#funciones-api">Funciones API</a></li>
    <li><a href="#modelo-ml">Modelo ML</a></li>
    <li><a href="#Deployment">Deployment</a></li>
    <li><a href="#Video">Video</a></li>
  </ol>
</details>

## Introducción

### Proyecto MLOps: Desarrollo de API y Modelo de Predicción
¡Bienvenidos al emocionante mundo de MLOps! Este proyecto individual se encuentra en la apasionante etapa de Labs, donde asumirás el desafiante rol de un MLOps Engineer. Prepara tus herramientas y sumérgete en esta experiencia en la que explorarás el poder de la Ingeniería de MLOps en acción.

### Descripción General
En esta aventura tecnológica, he llevado a cabo un profundo análisis de datos y una meticulosa transformación de los mismos. A través de un EDA (Exploratory Data Analysis) minucioso y un ETL (Extract, Transform, Load) eficiente, he dado forma a los datos para obtener valiosos conocimientos y preparar el terreno para etapas posteriores.

### Desarrollo de API con FastAPI
Una de las piedras angulares de este proyecto es el desarrollo de una potente API utilizando el framework FastAPI. He ideado y construido seis funciones API cuidadosamente diseñadas para brindar acceso fluido a los datos procesados. Estas funciones no solo ofrecen información valiosa, sino que también representan una fusión perfecta de tecnología y diseño.

### Deployment Eficiente
Pero no solo construimos, ¡también desplegamos! A través de la plataforma Render, he llevado nuestras funciones API desde el entorno local hasta la web. Cada función ahora está disponible para su uso, no importa dónde te encuentres. La tecnología no conoce fronteras, y nuestras funciones API tampoco.

### Modelo de Predicción Avanzado
Además de nuestras funciones API, he incorporado un modelo de predicción que añade un toque de magia a todo el proyecto. Utilizando técnicas avanzadas de Machine Learning, he desarrollado un modelo capaz de realizar predicciones basadas en datos históricos. Esta característica agrega un nivel adicional de utilidad y sofisticación a nuestro ecosistema MLOps.

Estoy emocionado de compartir contigo este viaje a través de la ingeniería de MLOps. Ya sea que estés aquí para explorar, aprender o inspirarte, este proyecto tiene algo para todos. Así que adelante, navega por las secciones, prueba nuestras funciones API y déjate sorprender por la magia de la predicción.

¡Disfruta del recorrido y bienvenido al mundo de MLOps!

## ETL
The ETL process was performed on the given dataset to prepare it for analysis and querying, following the steps below:
1. To streamline the dataset and focus on relevant information, unnecessary columns including "video," "imdb_id," "adult," "original_title," "vote_count," "poster_path," and "homepage" were removed. 
2. Null values in the "revenue" and "budget" fields were replaced with 0, ensuring consistency in calculations. Null values in the "release date" field were removed to ensure data integrity.
3. To standardize the format, dates were transformed into the YYYY-mm-dd format. Moreover, a new column called "release_year" was created to extract the year from the release date, providing a separate field for temporal analysis.
4. A crucial metric, return on investment, was computed by dividing the revenue by the budget for each entry, resulting in a new column called "return." When data was unavailable to calculate the return, it was assigned a value of 0, maintaining consistency in the dataset.
5. The dataset contained nested fields such as "belongs_to_collection" and "production_companies," which needed to be unnested for easier data manipulation. 

All of this was developed locally in VSCODE using Jupyter Notebook, python, numpy and pandas.

## EDA
The resulting data from the ETL was used to conduct the Exploratory Data Analysis. All of the columns were analyzed with the help of the ydata_profiling library tool ProfileReport. Decisions like what to do with missing values, outliers and more were taken. Identifying patterns and relevant attributes was a vital step in setting the foundation for the subsequent development of the API Functions and the Recommendation System.

All of this was developed locally in VSCODE using Jupyter Notebook, python, numpy, pandas, matplotlib, seaborn, wordcolud and ydata_profiling.

## Funciones API
In this part of the project, the requested endpoints were developed as python functions in a Jupyter Notebook file. After installing FastAPI and uvicorn, a [main.py](https://github.com/ksfajardo/PI01_ML_OPS_API/blob/main/utils/functions.py) file was created with the structure needed to deploy the endpoints, I tested this locally on the uvicorn service in the port 8000 (the main.py file only has the declaration of the endpoints, there is another file called [funciones.py](https://github.com/ksfajardo/PI01_ML_OPS_API/blob/main/utils/functions.py) in which the code of the functions is located and grabbed by the endpoint upon deployment). These functions take as data source the csv file resulting from the EDA. 

PD: I did NOT create a virtual enviroment to test this, since I already had all the required libraries installed in my machine, I felt it was unnecesary.

All of this was developed locally in VSCODE using Jupyter Notebook, python, numpy, pandas, FastAPI and uvicorn.

## Modelo ML
The recommendation system was developed in a Jupyter Notebook file. The NLP tool RAKE was used to generate keywords from the overview column. These keywords were combined with the genres_name and title columns into a single string for each film. CountVectorizer was then used to calculate the cosine similarity matrix. Based on the similarity scores provided by the matrix, the algorithm recommends the top 5 most similar movies to the one provided by the user as input. This model was also made available as an endpoint on the API. The completed algorithm the API uses is located in a python file called recomendacion.py in the API repository. The development of the algorithm is on this repository: [Machine Learning Development](https://github.com/ksfajardo/PI01_ML_OPS/blob/main/MLmodel.ipynb) on this repository.

All of this was developed locally in VSCODE using Jupyter Notebook, python, numpy, pandas, rake-nltk and scikit-learn.

## Deployment
After having the main.py and the rest of the files with the model and functions complete, the API was deployed using Google Cloud Run, as it offers the flexibility to allocate a desired amount of RAM memory and CPUs to the application. Since Cloud Run is a container hosting service, it was necessary to set up the API environment in a docker file. To do this, a [requierements.txt](https://github.com/ksfajardo/PI01_ML_OPS_API/blob/main/requirements.txt) file was constructed inside of which all the dependencies and libraries necessary to run the endpoints were included. Then, the docker image was created locally and subsequently uploaded to Docker Hub. 
Next, on Google Cloud, a Cloud Run service was created with the link given by Docker Hub of the docker image. 16GiB of RAM memory and 4 CPUs were assigned to run the API. Whit this, Cloud Run itself deploys the application and generates a link to acces the [running API](https://moviesapp-oxeinkhcia-uc.a.run.app).  

PD: It is worth mentioning that even with all of this resources the service was unable to run the recommendation algorithm using the full dataset (the similarity matrix of the full dataset alone weighs almost 15GB). Even though I could have allocated even more resources to the API so that it runs in its full dataset glory, I did not because that would have meant having to search for a server (in all of the possible regions that Google Cloud has, which are A LOT) that could host it, because every region has a different limit of resources allowed per user. So, instead I decided to use a sample of the dataset (half its size to be precise) and deploy the API with it. You can find this part in the last section of the Jupyter Notebook where the recommedation system was developed ([here](https://github.com/ksfajardo/PI01_ML_OPS/blob/main/MLmodel.ipynb)).

## Video
If you would like to see the video of me giving an overview of this project, click on the YouTube logo below:

<div align="center">
  
[![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white)](https://www.youtube.com/watch?v=B-hJy58UnNY)
  
</div>

