# Single Neuron Neural-Network-Implementation-from-Scratch-in-Python-
It is a single neuron neural network implementation from scratch in Python. It is using sample data of 2 dimensions to train and test. It is just for understanding purpose.
![](Images/SingleNeuron.png)
<h2>Implementation of Neural Network with Sigmoid and cross entropy loss function </h2>
Steps for the implementation are below:
- Created a class named as Neural_Network which will take input and output size as a parameter.
  -  a. Input size: is the size of feature vector which will be feed as input in our NN. In our case
    it is 2, pass it as a parameter.
  -  b. Output size: is the size of output layer, number of neurons that will be in output layer.
  -  c. Randomly initialize W i.e. random weight matrix.
2. Below is the list of functions which we needed to implement within the class Neural_Network.
  a. Feedforward (self, X)
      i. X is input feature(s)
      ii. Return predicted vector(s)
  b. Backpropogation (self,X, Y, y_pred, lr):
      i. X is input feature(s)
      ii. Y is actual label(s)
      iii. Y_pred is predicted value(s)
      iv. Lr is learning rate
  c. Sigmoid(self, s)
      i. Return sigmoid applied on s value(s)
  d. Sigmoid_derivative(self, s)
    i. Return derivate of sigmoid, on s
  e. Crossentropy(self, Y, Y_pred)
    i. Y is the actual label(s)
    ii. Y_pred is predicted label(s)
    iii. Return error based on crossentropy
  f. Train(self, trainX, trainY,epochs = 100, learningRate = 0.001, plot_err = True ,validationX
  = Null, validationY = Null)
    i. trainX is the training feature dataset in row format
    ii. trainY is the label of the dataset
    iii. epochs is the number of times entire dataset will be passed to the network for
    training, default value is 100.
    iv. learningRate is the constant used for weight updation
    v. plot_err bool variable if you want to plot error on a graph or not
    vi. validationX is the validation feature dataset in row format, show validation error
    in each epoch
    vii. validationY is the validation label of the dataset.
  g. Save_model(self,name)
    i. Save the model under the name of ‘name’
  h. Load_model(self,name)
   i. Load the model using ‘name’.
  i. Accuracy(self, testX, testY)
    i. testX is dataset for testing
    ii. testY is the labels of test data
    iii. plot accuracy on an image
    iv. return accuracy
  j. predict(self, testX)
    i. testX is the test row feature
    ii. return predicted value on testX
    
<h3> Approach: </h3>
- Split Data into 70:30 ratio. <br />
- Data dimension is like (2 columns ,4000 rows) 2000 for class 1 and 2000 for class 0 <br />
- And then added an additional row of 1’s for bias. And its dimensions become (3 columns ,4000 rows) 1st columns in now always will be 1 to tackle bias <br />
- Randomly initialize the weight vector with dimension (1 * 2+1) <br />
- Bias is added to column. It is a row vector. <br />
- In feedword Calculated the dZ & dA <br />
- And then update the W in backpropogate <br />
