# mlogit-from-scratch

An implementation of the **multinomial logistic regression** model in python.

### What is the multinomial logistic regression

In statistics, multinomial logistic regression is a classification method that generalizes logistic regression to multiclass problems. For further information about this model visit this [link](https://en.wikipedia.org/wiki/Multinomial_logistic_regression).

### The implementation

In my python implementation of the model, I used Kullback–Leibler divergence as loss function, which in the case of the MNIST datset is equivalent to the **Cross Entropy** (Entropy is zero because the correct class is only one for each training instance). For training the weights, I used **mini-batch gradient descent** with a batch-size that can be defined in the object initialisation. Furthermore, I adopted l**earning rate decay** as epochs pass. 

### Performace
The model was trained and tested on the MNIST dataset. It was trained on the 60,000 training instances for 50 epochs with a mini-batch size of 256. Then, it was tested on 10'000 test instances and predicted the correct digit with an accuracy of the **91%**.
