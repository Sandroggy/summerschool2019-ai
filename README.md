# AI & Radioastronomy
## Requirements
1. Anaconda3
2. Python 3.6.x
3. jupyter notebook
4. Tensorflow 1.14
5. Keras 2.2.4
6. numpy 1.16.2
7. matplot 3.1.0
````python
import numpy as np
import tensorflow as tf
import matplotlib.pyplot as plt
````
## How to use
1. activate virtualenvironment with package management system such as pip or anaconda.
2. Run the jupyter notebook.
3. Run Exo.ipynb.
4. You can modify second block your own dataset about Exoplanet.
5. Run!

## Results
We got 99.12% accuracy on the test dataset

### Things we've tried to improve
1. Add an initializer to initialize every weight to a random number before training instead of 0 as default value.
  ````python
  tf.keras.initializers.RandomUniform(minval=-500, maxval=500, seed=None)
  ````
2. Playing with the optimizer by lowering the learning rate.
  ````python
  optimizer=(tf.keras.optimizers.Adagrad(lr=0.02, epsilon=None, decay=0.0)
  ````
3. Make more epochs with larger batches.
  ````python
  model.fit(data_train, label_train, validation_split=0.1, batch_size=100, epochs=5)
  ````
4. Make a deeper network with more layers. and changing the activation function.
  ````python
  tf.keras.layers.Dense(512, activation=tf.nn.relu),
  tf.keras.layers.Dense(64, activation=tf.nn.sigmoid),
  tf.keras.layers.Dense(2, activation=tf.nn.sigmoid)
  ````
5. Add dropout layers, it prevent for overfitting while allowing for better training.
  ````python
  tf.keras.layers.Dropout(0.5)
  ````

### Things you could try to improve
1. Change the loss function.
  ````python
  loss='binary_crossentropy
  ````
2. Change/Tweak the optimizer.
  ````python
  optimizer=(tf.keras.optimizers.Adagrad(lr=0.02, epsilon=None, decay=0.0)
  ````
3. Trying other type of network.
  ````python
  tf.keras.layers.Dense(512, activation=tf.nn.relu),
  tf.keras.layers.Dense(64, activation=tf.nn.sigmoid),
  tf.keras.layers.Dense(2, activation=tf.nn.sigmoid)
  ````
