# Arabic_digits
I found a data on kaggle that represents the hand written indian number symbols which is used by arabs now
Data could be found on https://www.kaggle.com/mloey1/ahdd1
I also found a hand written arabian letters and planning to make a model for it and merge it with this model somehow

## Using convlutional layers instead of max pooling
I have read this in a paper and I thought that it would be different from my mnist repository to try something new
The paper link:
https://www.researchgate.net/publication/334399497_Strided_Convolution_Instead_of_Max_Pooling_for_Memory_Efficiency_of_Convolutional_Neural_Networks

It worked so well, I know the data isn't that hard to see the effect,so I am planning to try it on a more difficult dataset and also comapare it to max-pooling on this dataset



# The structure
Model: "sequential_1"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d_1 (Conv2D)            (None, 26, 26, 64)        640       
_________________________________________________________________
activation (Activation)      (None, 26, 26, 64)        0         
_________________________________________________________________
conv2d_2 (Conv2D)            (None, 13, 13, 64)        16448     
_________________________________________________________________
conv2d_3 (Conv2D)            (None, 11, 11, 32)        18464     
_________________________________________________________________
activation_1 (Activation)    (None, 11, 11, 32)        0         
_________________________________________________________________
conv2d_4 (Conv2D)            (None, 5, 5, 16)          2064      
_________________________________________________________________
flatten (Flatten)            (None, 400)               0         
_________________________________________________________________
dense (Dense)                (None, 10)                4010      
_________________________________________________________________
activation_2 (Activation)    (None, 10)                0         
=================================================================
Total params: 41,626
Trainable params: 41,626
Non-trainable params: 0
_________________________________________________________________


## As you can notice there is an intteruption on the model's training cell but I saw the accuracy on the training set goes down and I was suspecting over fitting but I didn't need to import the best model because the accuracy was high after all


I got   loss: 0.0570 - accuracy: 0.9838 on train data 
I think that indicates that this model got a small avoidable bayes 
and got loss: 0.0856 - accuracy: 0.9758 on test data
so this indicates that the model have law variance




### for more illustration about how to build a simple convlutional neural network using keras read the readme file in my mnist repository https://github.com/Ahmedmostafa2000/MNIST

