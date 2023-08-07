![wink](https://github.com/Sebas-Bello/PI01_ML_OPS/blob/938ebe095c559a98118df50d8e47c9b7e3f8dfe2/MLOPS.gif)


## Índice 
<!-- TABLA DE CONTENIDO -->
<details>
  <summary>Tabla de contenido</summary>
  <ol>  
    <li><a href="#Introducción">Introduction</a></li>
    <li><a href="#Objetivo">Objetivo</a></li>
    <li><a href="#Ámbito-de-Proyecto">Ámbito de Proyecto</a></li>
    <li><a href="#Pila-de-Tecnologías">Pila de Tecnologías</a></li>
    <li><a href="#ETL">ETL</a></li>
    <li><a href="#EDA">EDA</a></li>
    <li><a href="#funciones-api">Funciones API</a></li>
    <li><a href="#modelo-ml">Modelo ML</a></li>
    <li><a href="#Deployment">Deployment</a></li>
    <li><a href="#Video">Video</a></li>
  </ol>
</details>

## Introducción

¡Bienvenidos al emocionante mundo de **MLOps!** Este proyecto individual se encuentra en la apasionante etapa de Labs para la carrera de **Data Science en la academia SOY HENRY** donde asumiré el desafiante rol de un **MLOps Engineer**. Sumérgete en esta experiencia que te permitirá explorar de primera mano el impacto dinámico de la Ingeniería de MLOps en plena acción.

Estoy emocionado de compartir contigo este viaje a través de la **ingeniería de MLOps**. Ya sea que estés aquí para explorar, aprender o inspirarte, este proyecto tiene algo para todos. Así que adelante, navega por las secciones, prueba nuestras funciones API y déjate sorprender por la magia de la predicción.

***¡Disfruta del recorrido y bienvenido al mundo de MLOps!***

## Objetivo

El objetivo central de este proyecto es desarrollar y desplegar un sistema de predicción de precios de juegos, aprovechando un conjunto de datos completo. El proyecto se enfoca en lograr los siguientes objetivos específicos:

- **Transformación y Limpieza de Datos:** Aplicar técnicas de Extracción, Transformación y Carga (ETL) para preprocesar y limpiar el conjunto de datos de juegos.

- **Análisis Exploratorio de Datos (EDA):** Realizar un análisis exhaustivo de los datos para obtener ideas sobre los atributos de los juegos, como características, género y plataforma. Identificar patrones clave que influyan significativamente en los precios y descubrir relaciones que puedan aprovecharse para una predicción precisa.

- **Desarrollo de API:** Diseñar e implementar un conjunto de funciones y una API que se integre perfectamente con el sistema de predicción de precios de juegos.

- **Modelo ML:** Desarrollar un modelo de aprendizaje automático que utilice técnicas de regresión para predecir con precisión los precios de los juegos en función de sus atributos.

- **Despliegue de la API:** Implementar la API del sistema de predicción de precios en un entorno de producción, garantizando su disponibilidad y accesibilidad para los usuarios. Aplicar mecanismos de escalabilidad adecuados para una experiencia de usuario fluida.

- **Mejores Prácticas de MLOps:** Establecer una infraestructura eficiente de MLOps para gestionar y operar sin problemas todo el ecosistema.

Este proyecto representa una inmersión completa en el campo de MLOps, abordando todas las etapas desde la transformación de datos hasta la implementación y el despliegue de soluciones de predicción de precios en un entorno dinámico.

## Ámbito de Proyecto

El proyecto se desarrolló siguiendo estos aspectos clave:
- Análisis exploratorio de datos y Preprocesamiento de datos: [EDA y ETL link](https://github.com/Sebas-Bello/PI01_ML_OPS/blob/a34baaa93eaa58fec1ccb5d8235f019e38dfc6a4/EDA_ETL.ipynb)
- Desarrollo de Funciones API: [Desarrollo de Funciones link](https://github.com/Sebas-Bello/PI01_ML_OPS/blob/24a6418c0f938539f9076c0278e0facfce9acae4/Funciones%20API.ipynb)
- Desarrollo de modelos de aprendizaje automático: [Machine Learning Desarrollo link](https://github.com/Sebas-Bello/PI01_ML_OPS/blob/4ec0ef5e0167ded1b25b711cd5e51134d4bd1121/Modelo%20ML.ipynb)
- Desarrollo de API: [API Repositorio](https://github.com/Sebas-Bello/PI01_ML_OPS_API.git) (Este contenido está alojado en un repositorio aparte en mi GitHub, pero se incluye aquí solo con el propósito de mantener una estructura ordenada para mí)
- Implementación de API: [Deployed API link](https://pi-ml-ops-1-2v8u.onrender.com/docs#/)
</br>

<div align="center">
  
![MLOPS](https://github.com/Sebas-Bello/PI01_ML_OPS/blob/cce65265af6c5ae8848b58da052922c105ed99d7/%C3%81mbito%20de%20Proyecto.png)

</div>
 
## Pila de Tecnologías

![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)
![Markdown](https://img.shields.io/badge/markdown-%23000000.svg?style=for-the-badge&logo=markdown&logoColor=white)

## ETL

Durante la fase de transformación y limpieza de datos (ETL), se han aplicado una serie de pasos esenciales para garantizar la calidad y coherencia de los datos. Estas acciones buscan preparar el conjunto de datos de manera óptima para su análisis posterior y para ser consumido por la API que se está desarrollando.

**1. Eliminación de Duplicados y Asignación de Índice Numérico:** Para asegurar la unicidad de las filas en el conjunto de datos, se han eliminado los duplicados. Además, se ha asignado un índice numérico secuencial a cada fila. Esta estrategia facilita la manipulación y el análisis eficiente de los datos.

**2. Filtrado de Fechas Inválidas:** Se ha realizado un filtrado riguroso en la columna 'release_date' para identificar y cuantificar los valores atípicos que no cumplen con el formato aaaa-mm-dd. Esto proporciona una comprensión clara de la calidad de los datos y posibles problemas en las fechas de lanzamiento.

**3. Creación de Columna de Año:** Como parte de la transformación, se ha creado una nueva columna llamada "año_release_date". Mediante el uso de expresiones regulares, se ha extraído el año de la columna "release_date". Esta columna es crucial para los endpoints de la API y proporciona un filtro eficaz para las solicitudes basadas en el año.

**4. Gestión de Valores Nulos:** Dado que los valores nulos en la columna "año_release_date" podrían afectar negativamente el funcionamiento de la API, se han eliminado de manera consciente. Esto garantiza que solo se consideren registros con años válidos al llamar a la API, previniendo resultados inesperados y errores en el procesamiento de datos.

**5. Identificación de Outliers:** Para asegurar la integridad de la columna "año_release_date", se ha revisado cuidadosamente mediante la ordenación y filtrado de los primeros y últimos valores. Esta inspección visual permite identificar posibles outliers o valores incoherentes que podrían requerir tratamiento adicional para su corrección o eliminación.

**6. Eliminación de Registros Incoherentes:** La eliminación de registros incoherentes es una medida importante para mantener la calidad de los datos. En caso de encontrar registros con valores nulos en todas las columnas relevantes para la API, se ha procedido a eliminarlos. Esto asegura que los análisis futuros se basen en datos confiables y coherentes.

El proceso de ETL ha resultado en un conjunto de datos limpio, coherente y optimizado para el análisis y la implementación en la API. La atención meticulosa a cada paso garantiza que los resultados sean confiables y útiles para futuras operaciones y cálculos.

*Todas estas etapas se llevaron a cabo de manera local en **Visual Studio Code (VSCODE)**, empleando **Jupyter Notebook** como nuestro entorno principal. Para la implementación de cada paso, contamos con la potencia de **Python** como lenguaje de programación, respaldado por las versátiles bibliotecas **numpy y pandas**, que fueron fundamentales para la manipulación y transformación eficiente de los datos. Estas herramientas esenciales se combinaron hábilmente para crear un flujo de trabajo fluido y eficaz, permitiendo que el proyecto tomara forma de manera coherente y organizada.*

## EDA

Utilizando los datos resultantes del proceso ETL, se llevó a cabo un análisis exploratorio de datos (EDA) que desveló fascinantes perspectivas y patrones subyacentes. Para potenciar este análisis, se empleó la herramienta ProfileReport de la librería ydata_profiling, que permitió una inspección exhaustiva de todas las columnas. Este proceso enriquecedor no solo iluminó las características fundamentales de los datos, sino que también ofreció una visión detallada de cómo abordar cuestiones como valores faltantes, valores atípicos y mucho más.

A medida que se desentrañaban los entresijos de los datos, se tomaron decisiones críticas que influyeron en la dirección del proyecto. La identificación de patrones y atributos relevantes se convirtió en un pilar esencial para construir la base de las funciones API y el sistema de recomendación que se desarrollaría posteriormente. La calidad del análisis realizado durante el EDA estableció el terreno para la creación de soluciones sólidas y eficientes que aprovecharían al máximo la información extraída de los datos procesados en la etapa de ETL.

Este proceso integral, que abarcó desde la transformación de datos hasta el análisis exploratorio y la construcción de soluciones tecnológicas avanzadas, encapsula la esencia misma del proyecto. Cada paso contribuyó de manera sinérgica para dar vida a una plataforma sólida y versátil, preparada para ofrecer recomendaciones precisas y una experiencia de usuario excepcional.

*Todo este proceso fue desarrollado localmente en **Visual Studio Code (VSCODE)** utilizando **Jupyter Notebook** como nuestro entorno de trabajo principal. La combinación de herramientas tecnológicas que empleamos incluye **Python** como lenguaje de programación, junto con bibliotecas esenciales como **numpy y pandas** para la manipulación eficiente de datos. Además, utilizamos **matplotlib y seaborn** para la creación de visualizaciones gráficas impactantes, que nos permitieron revelar patrones y tendencias ocultas en los datos de manera efectiva.*

## Funciones API

En esta fase del proyecto, se llevaron a cabo el desarrollo de los puntos finales solicitados mediante funciones en Python, dentro de un archivo de Jupyter Notebook. Tras la instalación de FastAPI y uvicorn, se creó un archivo [main.py](https://github.com/Sebas-Bello/PI01_ML_OPS_API/blob/9dcc0729126f97b70c01153f4be5f4203a967626/main.py) con la estructura necesaria para desplegar los puntos finales. Realicé pruebas de esta implementación a nivel local, utilizando el servicio uvicorn en el puerto 8000 (cabe destacar que el archivo main.py únicamente contiene la declaración de los puntos finales; el código de las funciones se encuentra en otro archivo llamado [my_functions.py](https://github.com/Sebas-Bello/PI01_ML_OPS_API/blob/9dcc0729126f97b70c01153f4be5f4203a967626/Funciones/my_functions.py) este código es invocado por el punto final al momento del despliegue.

Estas funciones se alimentan con datos del archivo CSV resultante del análisis exploratorio de datos (EDA) realizado anteriormente. 

*Todo este proceso de desarrollo se llevó a cabo de manera local en **Visual Studio Code (VSCODE)**, haciendo uso de **Jupyter Notebook**, **Python, numpy, pandas, FastAPI y uvicorn**. Esta amalgama de herramientas tecnológicas permitió dar vida a los puntos finales de la API, desplegando de manera exitosa el acceso a las funciones y capacidades desarrolladas en el proyecto.*

## Modelo ML

En cuanto a la **Construcción del Modelo:**

Nos sumergimos en la implementación de un enfoque de ensamblado, específicamente adoptamos el algoritmo de Bagging (Bootstrap Aggregating) para la tarea de predicción. La destreza del modelo radica en su entrenamiento basado en datos históricos, capturando características fundamentales como el género, el acceso temprano y otras métricas clave de cada videojuego. A través de este proceso, logramos generar predicciones precisas y confiables.

En el siguiente paso, **la Predicción de Precios y Evaluación:**

Una vez que nuestro modelo ha sido rigurosamente entrenado, desplegamos su capacidad para pronosticar precios. Dada una serie de características específicas de un videojuego, el modelo genera una predicción del precio esperado con notable precisión. No solo nos detenemos aquí: calculamos el precio promedio para videojuegos pertenecientes a géneros particulares. Además, evaluamos el rendimiento de nuestro modelo utilizando una métrica crucial: el error cuadrático medio (RMSE), aplicado a los datos de prueba. Este paso garantiza la confiabilidad y eficacia de nuestras estimaciones.

Finalmente, en las **Conclusiones:**

Este proyecto ejemplifica cómo aprovechar el aprendizaje automático para prever los precios de los videojuegos, basándonos en sus atributos distintivos. Nuestra atención especial en los géneros y el estado de acceso temprano resalta la habilidad del modelo para generar estimaciones de precios altamente personalizadas y ajustadas a diferentes categorías de videojuegos. Cada fase de este proceso, desde la construcción del modelo hasta la predicción y la evaluación, contribuye a una solución que no solo es poderosa, sino también altamente precisa y adaptada a las necesidades de la industria de los videojuegos.

El algoritmo completo que utiliza la API se encuentra alojado en un archivo de Python llamado **my_model_ML.py** en el repositorio de la API. El proceso de desarrollo de dicho algoritmo se encuentra detallado en el repositorio denominado: [Modelo ML](https://github.com/Sebas-Bello/PI01_ML_OPS/blob/05dcf22f0d7d8b1d323a3649461e48d717fa2dfa/Modelo%20ML.ipynb) en este mismo repositorio. En esta ubicación, encontrarás una inmersión profunda en la evolución del algoritmo, desde sus raíces conceptuales hasta su refinamiento y optimización, culminando en la implementación exitosa en el archivo **my_model_ML.py**. Este enfoque garantiza una comprensión completa del proceso y ofrece un recurso valioso para aquellos interesados en explorar más a fondo la lógica y la metodología detrás del algoritmo de recomendación.

*Todo este proceso fue desarrollado de manera local en **Visual Studio Code (VSCODE)** utilizando **Jupyter Notebook** como plataforma principal. Para la implementación, aprovechamos la versatilidad de **Python** como lenguaje de programación, respaldado por las bibliotecas esenciales como **numpy y pandas**, que resultaron fundamentales para el procesamiento y manipulación eficiente de los datos.*

*Además, la incorporación de **scikit-learn** potenció nuestras capacidades de aprendizaje automático, proporcionando algoritmos y herramientas esenciales para la creación y evaluación de modelos.*

*Esta combinación sinérgica de tecnologías, desde el ambiente de desarrollo hasta las herramientas específicas, dio como resultado un proceso robusto y eficaz que abordó cada fase del proyecto con precisión y eficiencia, permitiendo la creación exitosa de un ecosistema completo y funcional.*

## Deployment

Luego de completar la implementación de **main.py** y demás archivos que componen el modelo y las funciones, el despliegue de la API se realizó de manera exitosa a través de Render, siguiendo un proceso meticuloso y organizado:

**1. Creación de Entorno Virtual:** El proceso de despliegue comenzó con la creación de un entorno virtual aislado, lo cual permitió gestionar y separar las dependencias específicas de la API, evitando conflictos y asegurando la coherencia en el entorno de producción.

**2. Configuración de Archivos Necesarios:** Se llevaron a cabo las configuraciones necesarias para el despliegue, asegurando que todos los archivos esenciales estuvieran presentes y correctamente configurados. Esto garantizó una base sólida para el funcionamiento de la API en el entorno de Render.

**3. Inicialización de Git y Realización de Instalaciones:** Se inició un repositorio de Git para el proyecto y se realizaron las instalaciones pertinentes de las bibliotecas y paquetes necesarios para el funcionamiento de la API. Esto aseguró que la infraestructura estuviera lista para el proceso de despliegue.

**4. Generación de Lista de Dependencias (Pip Freeze):** Se generó una lista de las dependencias y versiones específicas utilizadas en el entorno virtual. Esta lista proporcionó un registro claro y conciso de las bibliotecas que respaldaban la API, simplificando la gestión y el mantenimiento. [requierements.txt](https://github.com/Sebas-Bello/PI01_ML_OPS_API/blob/9dcc0729126f97b70c01153f4be5f4203a967626/requirements.txt)

**5. Experiencia Render:** A través de Render, se llevaron a cabo los pasos necesarios para desplegar la API. Render proporcionó una plataforma eficiente y confiable para implementar aplicaciones, asegurando una experiencia de usuario optimizada y accesible. Render implementa la aplicación y genera un enlace para acceder a la [API en ejecución](https://pi-ml-ops-1-2v8u.onrender.com). **(Puedes agregar "/docs" al final del enlace para acceder a la documentación automática creada por FastAPI. Esto te brindará una interfaz interactiva y detallada que describe todos los endpoints, métodos y parámetros disponibles en la API de manera clara y concisa.)**

*Con la culminación exitosa de estos pasos, la API que se había construido y desarrollado con dedicación y precisión ahora está completamente preparada y lista para ser consumida. La combinación de todas estas etapas ha permitido llevar el proyecto desde su fase inicial hasta un estado funcional y accesible, donde los usuarios pueden aprovechar plenamente las funciones y capacidades de la API de manera confiable y eficiente.*

## Video

Si deseas ver el video donde proporciono una visión general de este proyecto, simplemente haz clic en el logotipo de YouTube a continuación:

<div align="center">
  
[![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white)](https://youtu.be/kBy6X4j6KVk)
  
</div>

