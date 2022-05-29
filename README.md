### EX NO : 08
### DATE  :
# <p align="center"> XOR GATE IMPLEMENTATION </p>
## Aim:
   To implement multi layer artificial neural network using back propagation algorithm.
## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner /Google Colab

## Related Theory Concept:
Logic gates using neural networks help understand the mathematical computation by which a neural network processes its inputs to arrive at a certain output. This neural network will deal with the XOR logic problem. An XOR (exclusive OR gate) is a digital logic gate that gives a true output only when both its inputs differ from each other.

The information of a neural network is stored in the interconnections between the neurons i.e. the weights. A neural network learns by updating its weights according to a learning algorithm that helps it converge to the expected output. The learning algorithm is a principled way of changing the weights and biases based on the loss function.

## Algorithm:
1.Import the required libraries.

2.Create the training dataset.

3.Create the neural network model with one hidden layer.

4.Train the model with training data.

5.Now test the model with testing data.

<br>
<br>
<br>

## Program:
```python3
Program to implement XOR Logic Gate.
Developed by   : N Sandhya Charu
RegisterNumber : 212220230041

import numpy as np
from keras.models import Sequential
from keras.layers.core import Dense

training_data=np.array([[0,0],[0,1],[1,0],[1,1]],"float32")
target_data=np.array([[0],[1],[1],[0]],"float32")

model=Sequential()
model.add(Dense(16,input_dim=2,activation='relu'))
model.add(Dense(1,activation='sigmoid'))
model.compile(loss='mean_squared_error',
                    optimizer='adam',
                    metrics=['binary_accuracy'])
model.fit(training_data,target_data,epochs=1000)
scores=model.evaluate(training_data,target_data)

print("\n%s: %.2f%%" % (model.metrics_names[1],scores[1]*100))
print(model.predict(training_data).round())
```
## Output:
![image](https://user-images.githubusercontent.com/75235167/169463387-47304a6e-45b3-4a30-b2a6-f7ffcd6ce5cd.png)

## Result:
Thus the python program successully implemented XOR logic gate.
