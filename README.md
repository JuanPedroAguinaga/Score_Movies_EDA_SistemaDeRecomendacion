<p align=center><img src=https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png><p>

# <h1 align=center> **PROYECTO INDIVIDUAL Nº1** </h1>

# Score Movies

## Enfoque del Proyecto

El proyecto se enfoca en el rol de MLOps Enginner, donde se pide el desarrollo de una API utilizando el framework FastApi
para comunicar y disponibilizar datos para el equipo de análisis de datos de una empresa. 
El objetivo principal es realizar transformaciones 
específicas en los datos y disponibilizarlos a través de endpoints accesibles mediante la API que finalmente fue desplegada en Render.
Una vez terminado el proceso y echo el deployment, realizamos un proceso de análisis exploratorio de los datos para luego, poder entrenar un modelo de machine
learning para armar un sistema de recomendacion de peliculas para usuarios.

[Ver mas sobre el proyecto y sus requerimientos](https://github.com/HX-PRomero/PI_ML_OPS/blob/main/Readme.md)

## Objetivos

Se lograron cumplir la gran mayoria de los objetivos propuestos, de forma especifica estos son ellos:

- [x] Tranformaciones en las bases de datos: [Link](https://github.com/JuanPedroAguinaga/Score_Movies_API-DEPLOYMENT/blob/master/tranformation.ipynb)

- [x] Desarrollo de la API

- [x] Deployment: [Link](https://score-movies-prueba8.onrender.com/docs)

- [x] Video: [Link]()

- [x] Exploraty Data Analysis-EDA: [Link](https://github.com/JuanPedroAguinaga/Score_Movies_EDA_SistemaDeRecomendacion/blob/main/EDA.ipynb)

- [x] Sistema de recomendación: [Link](https://github.com/JuanPedroAguinaga/Score_Movies_EDA_SistemaDeRecomendacion/blob/main/SistemaDeRecomendacion.ipynb)

- [ ] Deployment: 

- [x] Video: [Link]


## Requerimientos

1. Generar campo id: Cada id se compondrá de la primera letra del nombre de la plataforma, seguido del show_id ya presente en los datasets (ejemplo para títulos de Amazon = as123)
2. Los valores nulos del campo rating deberán reemplazarse por el string “G” (corresponde al maturity rating: “general for all audiences”
3. De haber fechas, deberán tener el formato AAAA-mm-dd
4. Los campos de texto deberán estar en minúsculas, sin excepciones
5. El campo duration debe convertirse en dos campos: duration_int y duration_type. El primero será un integer y el segundo un string indicando la unidad de medición de duración: min (minutos) o season (temporadas)

## Endpoints de la API

La API cuenta con los siguientes endpoints:

* Cantidad de veces que aparece una keyword en el título de peliculas/series, por plataforma.
  
* Cantidad de películas por plataforma con un puntaje mayor a XX en determinado año.
  
* La segunda película con mayor score para una plataforma determinada, según el orden alfabético de los títulos.
  
* Película que más duró según año, plataforma y tipo de duración
  
* Cantidad de series y películas por rating


## Deployment

Para realizar el deploy se utilizo [Render](https://render.com/)

Instrucciones: 

- Clonar el repositorio con (git clone https://github.com/JuanPedroAguinaga/Score_Movies_API-DEPLOYMENT)
- Acceder a la carpeta mediante linea de comandos (cd/ruta/hasta/el/proyecto/Score_Movies_API-DEPLOYMENT) una vez clonada o descargada
- Crear un ambiente virtual en la carpeta principal usando en comando (python -m venv venv --upgrade-deps) para que gestione un entorno de ambiente con las dependencias
- Activar el ambiente virtual creado con (source venv/Scripts/activate) o (./venv/Scripts/activate)
- Instalar las dependencias del proyecto mediante la ejecución de (pip install -r requirements.txt)
- Ejecutar el proyecto mediante el comando (uvicorn main:app --reload) asegurandose que tenemos instalado uvicorn mediante el comando pip install uvicorn
 para poder probar el proyecto en local accediendo al navegador en (localhots:8000)
- Una vez funcionando la API en local, debemos desplegarla en [Render](https://render.com/), para ello la subiremos directamente desde la
conexion de Render con nuestro archivo en GitHub. [Tutorial de Render](https://github.com/HX-FNegrete/render-fastapi-tutorial)

## EDA y Sistema de recomendación:

1. Recopilación y pocesamiento de datos: Recopilamos los datos de las diferentes plataformas de streaming y los procesaremos
para preepararlos para su uso en el modelo de recomendación.Esto incluye la eliminacion de datos faltantes, tranformacion de datos, nuevas columnas
y la creacion de nuevas caracteristicas.

2. Análisis exploratorio de los datos(EDA): Investigamos las variables y relaciones entre los datasets, analizamos si existen outliers o anomalias,
ademas buscamos algun patron interesante que valga la pena investigar.

3. Desarrollo del modelo de recomendación: Desarrollamos un modelo de recomendación utilizando tecnicas de Machine Learning.
El modelo de entrena utilizando los datos procesados y evaluamos su rendimiento.

4. Implementación del modelo: Lamentablente, no se logro cumplir con lo requerido "De ser posible, este sistema de recomendación debe ser deployado para tener una interfaz gráfica amigable para ser utilizada, utilizando Gradio para su deployment o bien con alguna solución como Streamlit o algo similar en local". Los tiempos de entrega fueron ajustados y no se logro este punto. En la brevedad se actualizara el proyecto con una disponibilización en una interfaz grafica.

## Conclusion


En resumen, el proyecto de machine learning enfocado en crear un modelo de recomendación personalizada a usuarios ha sido una experiencia muy enriquecedora y exitosa. A través de la aplicación de técnicas de aprendizaje automático, fui capaz de construir un modelo que es capaz de analizar y entender las preferencias de los usuarios, y así sugerir peliculas que se ajustan a sus gustos y necesidades específicas.

Este modelo de recomendación personalizada tiene el potencial de mejorar significativamente la experiencia del usuario, al permitirles descubrir peliculas o series que de otra manera podrían haber pasado por alto. Además, también puede ayudar a aumentar las ventas y la retención de clientes para la empresa, al ofrecer recomendaciones precisas y relevantes.

En definitiva, el modelo de recomendación personalizada desarrollado en este proyecto demuestra el valor del aprendizaje automático en la mejora de la experiencia del usuario y la eficacia de la estrategia de recomendación personalizada de la empresa.


## Nota

El proyecto esta dividio en dos archivos, [Score_Movies_API-DEPLOYMENT](https://github.com/JuanPedroAguinaga/Score_Movies_API-DEPLOYMENT) y [Score_Movies_EDA_SistemaDeRecomendacion](https://github.com/JuanPedroAguinaga/Score_Movies_EDA_SistemaDeRecomendacion) ya que al momento de querer disponibiizar la API en render, no podia cargar el archivo entero completo por razones desconocidas. 


## Contribuciones 
 
 Este tipo de proyecto es perfecto para desarrollar y aumentar habilidades de Data Engineering y Data Science, es de codigo abierto y esta abierto a posibles contribuciones. Si tenes intenciones de hacerlo:
 - Haga un fork del repo.
 - Cree una nueva rama con sus caracteristicas o correciones
 - Realize los cambios y asegúrese de seguir las mejoras prácticas de codificación y decumentación.
 - Realize un pull request y espera laaprobación

## Fuente de datos

- [Datasets](https://drive.google.com/drive/u/0/folders/1iY6oLzZXwQ-lR2LGJkKnXFfZQchtYlQx): La carpeta 'ratings' tiene varios archivos con las reseñas de los usuarios, la carpeta raíz tiene un dataset por proveedor de servicios de streaming. 




Aguinaga Juan Pedro - Estudiante Data Science
