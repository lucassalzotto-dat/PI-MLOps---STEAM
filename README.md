# PI_ML_OPS_STEAM
# <h1 align=center> **PROYECTO INDIVIDUAL Nº1** </h1>

# <h1 align=center>**`Machine Learning Operations (MLOps)`**</h1>

<p align=center><img src="portada.jpg"><p>

## **Introducción:**
Este proyecto se centra en el desarrollo de una API que emplea un modelo de recomendación para Steam, una plataforma de videojuegos de alcance internacional, fundamentado en técnicas de Machine Learning. El propósito principal consiste en construir un sistema de recomendación de videojuegos dirigido a usuarios de la plataforma. La API proporciona una interfaz intuitiva que facilita a los usuarios la obtención de información para el sistema de recomendación, así como datos relevantes sobre géneros y fechas específicas. Este enfoque busca mejorar la experiencia de los usuarios al ofrecer sugerencias personalizadas y acceso a detalles valiosos relacionados con sus preferencias de juego.

## **Herramientas Utilizadas**
+ Pandas
+ Matplotlib
+ Numpy
+ Seaborn
+ Wordcloud
+ NLTK
+ Uvicorn
+ Render
+ FastAPI
+ Python
+ Scikit-Learn

## **Paso a paso:**
### 1. ETL
En esta fase, llevamos a cabo un proceso integral de ETL (Extracción, Transformación y Carga), donde extraemos datos de diversas fuentes, los sometemos a transformaciones específicas acorde a los requisitos del proyecto, y finalmente, los cargamos en un destino final. Este enfoque garantiza la disponibilidad de datos consistentes y optimizados para su análisis y utilización en etapas posteriores del proyecto.
### 2. Deployment de la API
En esta etapa, hemos desarrollado una API mediante el uso del módulo FastAPI en Python, que incorpora cinco funciones para facilitar consultas específicas:
1. **PlayTimeGenre(genero: str):**
   - Devuelve el año con mayor cantidad de horas jugadas para el género especificado.
   - Ejemplo de entrada: "casual"
2. **UserForGenre(genero: str):**
   - Proporciona el usuario que acumula la mayor cantidad de horas jugadas para el género especificado, junto con una lista de la acumulación de horas jugadas por año.
   - Ejemplo de entrada: "action"
3. **UsersRecommend(año: int):**
   - Retorna el top 3 de juegos MÁS recomendados por usuarios para el año dado. Se consideran únicamente aquellos con reviews marcadas como recomendadas y con comentarios positivos o neutrales.
   - Ejemplo de entrada: 2012
4. **UsersNotRecommend(año: int):**
   - Ofrece el top 3 de juegos MENOS recomendados por usuarios para el año dado. Se incluyen únicamente aquellos con reviews marcadas como no recomendadas y con comentarios negativos.
   - Ejemplo de entrada: 2009
5. **sentiment_analysis(año: int):**
   - Según el año de lanzamiento, proporciona una lista con la cantidad de registros de reseñas de usuarios categorizados con un análisis de sentimiento.
   - Ejemplo de entrada: 2014

Estas funciones han sido diseñadas para ofrecer a los usuarios de la API información específica y relevante sobre el comportamiento de los juegos, facilitando así la toma de decisiones informadas y la exploración de datos detallados en la plataforma Steam.

Luego realizamos el deployement de esta API utilizando Render.

Recuerda por las dudas descargar la carpeta FastApi incluida en la rama Master.

### 3. EDA
En esta etapa, llevamos a cabo un proceso de EDA (Exploratory Data Analysis o Análisis Exploratorio de Datos), donde se exploraron y analizaron detalladamente los datos con el objetivo de obtener insights valiosos. Durante este proceso, nos enfocamos en identificar patrones, tendencias y relaciones dentro de los datos. El propósito fundamental fue adquirir un entendimiento profundo del conjunto de datos, buscando pistas significativas que pudieran orientar la creación de nuestro modelo de Machine Learning.
### 4. Modelo de Machine Learning
En la fase de construcción del Modelo de Machine Learning, hemos implementado un sistema de recomendación para juegos que se basa en algoritmos y técnicas avanzadas, incluyendo la similitud del coseno y la biblioteca scikit-learn. Este modelo tiene como objetivo proporcionar recomendaciones personalizadas y precisas, adaptadas a los gustos y preferencias individuales de cada usuario.
Si el enfoque es un sistema de recomendación item-item, hemos desarrollado la siguiente función:
- **recomendacion_juego(id de producto):**
  - Al ingresar el id de producto ('id'), esta función devuelve una lista con los 5 juegos recomendados más similares al juego ingresado.
  -  Ejemplo de uso: 76561198030567998
  
Si, en cambio, el sistema de recomendación es user-item, implementamos la siguiente función:

- **recomendacion_usuario(id de usuario):**
  - Al ingresar el id de un usuario ('user_id'), esta función proporciona una lista con los 5 juegos recomendados para ese usuario en particular.
  - Ejemplo de uso: 70
    
Estas funciones permiten que el modelo genere recomendaciones significativas y específicas, aprovechando la similitud entre juegos o la información de comportamiento de usuarios, según el enfoque adoptado. Este sistema ofrece una experiencia de recomendación más personalizada y adaptada a las preferencias individuales de los usuarios en la plataforma de Steam.
## **Más:**
- [Deploy de la API en Render](https://deploy-api-steam.onrender.com)
- [Video explicando el proyecto](https://www.youtube.com/watch?v=yNzYl2HeNfU)
## **LICENCIA:**
Lucas Salzotto
