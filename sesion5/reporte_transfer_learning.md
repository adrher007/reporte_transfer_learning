[reporte_transfer_learning.md](https://github.com/user-attachments/files/26491584/reporte_transfer_learning.md)
#Reporte de Transfer Learning
###¿Que es?
El transfer learning es una tecnica que se usa en 
Machine Learning que consiste en reutilizar un 
modelo que ya tiene varios data sets y modificarlo
para que se especialice en un ambito especifico 
(El que nosotros elijamos).
Por ejemplo, supongamos que cualquier persona tiene
la tecnologia como para crear chips de procesadores y graficas.
Al armar una PC de sobremesa nosotros podriamos crear nuestro
procesador y grafica pero seria sumamente caro y nos tomaria
tiempo, para eso mejor compramos componentes ya fabricados y
montamos todo en la placa madre. Eso es usar algo ya creado para 
ahorrar tiempo, dinero y energia.
Como en el ejemplo se explica, se usa algo "ya hecho", en el caso
de la IA tenemos diferentes herramientas, desde sencillas hasta
complejas, por ejemplo:
MobileNetV2.- Es un modelo pre-entrenado que es ligero y optimizado
para celulares y Google Colab.

Pero OJO, como se explica en el ejemplo, nosotros solo usamos lo que 
"ya esta hecho y lo destinamos para diversos usos" no desarmamos cada 
componente para volver a armarlo (En la vida real no pasaria nada,
pero seria una perdida de tiempo), esto es igual en IA, no tenemos que 
tocar mucho las capas ya entrenadas pues si se hace => catastrophic forgetting
solo usamos un 5% para entrenar y lo restante no se usa para proteger a
los datos ya procesados, es uina medida de seguridad.

###Resultados del experimento

Imagen: https://cataas.com/cat

Hice la prueba subiendo la imagen de un gato y el modelo arrojó estas 
predicciones:
1. Angora: 34.3%
2. Hamster: 15.8%
3. Persian_cat: 8.4% 
El modelo acertó en que es un gato (Angora), aunque la confianza fue baja (34%)
Es interesante ver que llegó a confundirse un poco con un hámster, 
probablemente por la textura del pelaje o la posición en la foto.
Lo que se tendria que hacer para aumentar la confianza es entrenar mas a la IA
para "especializarla" en reconocimiento de animales.

###Análisis de parámetros: Congelados vs. Entrenables

Parámetros totales: 
El modelo maneja más de 2.4 millones de parámetros en total.

Parámetros congelados (~93.2%): 
La gran mayoría se mantienen "congelados" 
para preservar lo que el modelo ya sabe 
y evitar el Catastrophic Forgetting 
(que olvide cómo reconocer formas básicas).

Parámetros entrenables (~6.8%): 
Solo entrenamos una pequeña parte, 
que es la "cabeza" nueva 
que le pusimos para que aprenda 
nuestra tarea específica.

###Aplicacion a Bolivia
Se me ocurrió que en el país podríamos usar
esto para algo importante: detección de 
rostros para encontrar personas desaparecidas
o identificar delincuentes.

Usaríamos Transfer Learning y solo lo 
especializaríamos con las fotos de las personas
que estamos buscando.
