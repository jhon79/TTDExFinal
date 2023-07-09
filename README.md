# TTDExFinal
Autor: Juan Ibadango

Trabajo Final
Se toma las imágenes de la fuente CarneDataset/train y se las dividió en imágenes de entrenamiento 80% y validación 20%.
    train_generator
    val_generator
Se toma las imágenes de la fuente CarneDataset/test para probar el modelo.
Se usa ImageDataGenerator para variar algunas propiedades de las imágenes de entrada. Se crea el modelo con una variable de tipo secuencial, que utiliza redes convolucionales 2d, con una capada de entrada de 4 neuronas con activación relu, 16 capas ocultas y una capa de salida de 8 neuronas. Con este modelo se genera la matriz de confusión, dando como resultado un accuracy de 0.46 con los datos de train. 
Se prueba el modelo con los datos de test consiguiendo un accuracy de 0.43.

Modificamos la arquitectura del modelo a una capa de entrada de 4 neuronas con activación relu, 18 capas ocultas de diferente tipo, y una capa densa de salida de 8 neuronas con activación softmax. Con este modelos se consigue 0,46 de accuracy con los datos train.

Se aplica transferencia de aprendizaje, para lo cual se usa la red neuronal convolucional RESNET 50, se congela las capas del modelo base y se agrega las capas de salida de acuerdo al modelo requerido. Con esta técnica se consigue subir el accuracy a 0.83 con datos train. Con los datos de test se consigue un accuracy de 0.40.

Se prueba con otra red neuronal convolucional VGG16, de igual manera se congela las capas del modelo base y se agrega las capas de salida necesarias. Se consigue llegar a un accuracy de 0.94 con datos de train. 

Finalmente, se intenta aplicar la técnica de aumento de datos, que consiste en aplicar diversas transformaciones sobre las entradas originales, obteniendo muestras ligeramente diferentes pero en esencia iguales, que permite a la red desenvolverse mejor en la fase de inferencia.

Referencias:
https://www.youtube.com/watch?v=9Dur_oUMGG8
https://www.youtube.com/watch?v=DbwKbsCWPSg

