# TareaFinalMyA
<h1>Tarea Final de Modelos y Aprendizajes</h1>
<h3>Autor: Carlos Rosero</h3>

<h2>OBJETIVO Y ALCANCE</h2>

Supongamos que usted trabaja en el servicio de salud y recibe muestras que provienen de mujeres con cáncer de mama. Los médicos han extraído características y las han anotado, su trabajo es crear un modelo que sea capaz de identificar si un paciente tiene o no cáncer. El dataset y su descripción aparecen aquí:
https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29
Recordemos que un falso positivo no es tan preocupante como un falso negativo, ya que en el futuro se les hacen más pruebas a las pacientes y hay oportunidades de descubrir que estábamos en un error. Sin embargo, un falso negativo puede llevar a que el cáncer se desarrolle sin supervisión durante más tiempo del necesario y podría llevar a daños más graves o incluso la muerte de la paciente.
Teniendo esto en cuenta, desarrolla un modelo que funcione lo mejor posible y explica qué decisiones has tomado en su elaboración y por qué

DESARROLLO 
La ruta donde se encuentra el documento en formato Jupyter Notebook (.ipynb) es: https://github.com/CarlosRoseroC/TareaFinalMyA/tree/main Descripción del dataset. En base al link se revisa el sitio y se descarga el dataset; al revisar el dataset se encuentra que no tiene una cabecera con los nombres de los campos y para ello se añade en la primera fila los campos que se indican en la página. Tenemos varios campos como ID, Diagnosis, radius1, texture1, perimeter1, area1…fractal_dimension3. Un total de 32 campos y 569 registros.
Se hace la carga del dataset, se revisan los campos y sus valores.
- Se elimina el campo “ID” porque no le agrega valor a los modelos.
- En el histograma del campo “Diagnosis” vemos que hay mas registros benignos que malignos (M = maligno, B = benigno).
- No hay valores nulos.
- El campo “Diagnosis” solo tiene valor M o B.
- El resto de los campos tienen valores numéricos de tipo flotante.

Para el proceso de aprendizaje se separa el dataset en TRAIN y TEST con los parámetros test_size = 0.2 y random_state = 42. Los modelos que se usan para este ejercicio son:

Random_Forest.

SVM(Support Vector Machines).

Regresión Logisitica.

CONCLUSIÓN

Luego de revisar cada modelo sus métricas y matrices de confusión podemos concluir que el que tiene una mayor accuracy(97.368 %) y menor cantidad de falsos-negativos tanto en TRAIN(3) como TEST(2) es el modelo RandomForest, y este sería el recomendado para este ejercicio de cáncer de mama.

RECOMENDACIONES

Existe un mayor detalle de lo realizado en el documento PDF que se encuentra en este mismo sitio.

EXTRA

Se añade el archivo Bonus_carne.ipynb, que contiene el clasificador de tipos de carnes con comentarios dentro del código para su entendimiento.
