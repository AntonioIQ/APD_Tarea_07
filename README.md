# Tarea 07 

## Instrucciones 

* Descarga los siguientes datos de [Yelp](https://www.yelp.com/dataset/download) 
  en JSON. Estos son los [metadatos del dataset](https://www.yelp.com/dataset/documentation/main).

* Utiliza el contenedor de PySpark para responder las siguientes preguntas.

**Nota:** Invierte tiempo en esta tarea porque te va a servir para el proyecto parcial de la materia, tanto para ir practicando la notración de Pyspark como para manejar los datos.

## Preguntas

1. Toma el archivo `review.json` JSON y cuantífica cuánto pesa el archivo en 
   disco.

2. Carga el JSON en Spark y cuantífica cuánto pesa el DataFramen en memoria RAM.

3. Guarda el DataFrame como parquet en disco y muestra cuánto pesa el archivo.
   Cómo se compara con el JSON crudo.

4. Utiliza el DataFrame, optimiza el tipo de dato que hay en cada columna (i.e. 
   `Int32`, `Int64`, `Float32`, `Float64`, `String`, `Categorical`) y guarda el 
   nuevo DataFrame como parquet. Cuántifica cuánto pesa el DataFrame en memoria 
   RAM y cuánto pesa en disco. Cómo se compara con el parquet crudo.

5. Utiliza el DataFrame optimizado, guarda en parquet una nueva versión del 
   DataFrame y particionalo por fecha (`date`). Otra versión por ciudad. Otra 
   por ciudad y fecha.

   * **Nota**: Para particionar por ciudad (`city`) será necesario que hagas un 
    join con la tabla `business.json`. 
   * **Nota:** Para particionar por fecha hazlo por año y mes. Para hacer esto 
    necesitas extraer el año y mes como columnas.

6. Ejecuta un query utilizando sobre la tabla filtrando por una de las ciudades y un años en particular. Registra el tiempo de ejecución. Aplica el query sobre 
   - la versión en JSON 
   - la versión particionada por fecha y luego 
   - sobre la versión particionada por fecha y lugar

   De todos los queries que ejecutaste cuáles fueron más rápidos.
