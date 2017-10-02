# fashion-mnist Multi Layer Perceptron

The fashion-mnist dataset contains 60K train images (28x28 grayscale) and 10K test images of fashion items. They are labeled and contain 10 classes.

This project is the generation of a Multi-Layer Perceptron (dense) neural network **using TensorFlow** environment, **as a practice(!)** for this environment. 

The entire code is contained in a Jupyter notebook.
The code allows generic selection of layers, but the current dimensions I chose are: 
728-64-32-10

* I didn't use a validation set -> Worked directly with test set. 

## Best results with this MLP model

| Train Acc |  Test Acc  |
| :---      | :---:      |     
| 0.8775    | **0.8669** |

To prevent overfit, I used dropout with rate 0.11 between layers. 