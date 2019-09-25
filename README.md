# Single Neuron Neural-Network-Implementation-from-Scratch-in-Python-
It is a single neuron neural network implementation from scratch in Python It is using sample data of 2 dimensions to train and test It is just for understanding purpose
## Implementation of Neural Network with Sigmoid and cross entropy loss function 
Steps for the implementation are below:
- Created a class named as Neural_Network which will take input and output size as a parameter
  -  a Input size: is the size of feature vector which will be feed as input in our NN In our case
    it is 2, pass it as a parameter
  -  b Output size: is the size of output layer, number of neurons that will be in output layer
  -  c Randomly initialize W ie random weight matrix
- Below is the list of functions which we needed to implement within the class Neural_Network
  - Feedforward (self, X)
      - X is input feature(s)
      - Return predicted vector(s)
  - Backpropogation (self,X, Y, y_pred, lr):
      - X is input feature(s)
      - Y is actual label(s)
      - Y_pred is predicted value(s)
      - Lr is learning rate
  - Sigmoid(self, s)
      - Return sigmoid applied on s value(s)
  - Sigmoid_derivative(self, s)
      - Return derivate of sigmoid, on s
  - Crossentropy(self, Y, Y_pred)
      - Y is the actual label(s)
      - Y_pred is predicted label(s)
      - Return error based on crossentropy
  - Train(self, trainX, trainY,epochs = 100, learningRate = 0001, plot_err = True ,validationX = Null, validationY = Null)
      - trainX is the training feature dataset in row format
      - trainY is the label of the dataset
      - epochs is the number of times entire dataset will be passed to the network for training, default value is 100
      - learningRate is the constant used for weight updation
      - plot_err bool variable if you want to plot error on a graph or not
      - validationX is the validation feature dataset in row format, show validation error in each epoch
      - validationY is the validation label of the dataset
  - Save_model(self,name)
      - Save the model under the name of ‘name’
  - Load_model(self,name)
      - Load the model using ‘name’
  - Accuracy(self, testX, testY)
      - testX is dataset for testing
      - testY is the labels of test data
      - plot accuracy on an image
      - return accuracy
  - predict(self, testX)
      - testX is the test row feature
      - return predicted value on testX
    
<h3> Approach: </h3>
-Split Data into 70:30 ratio
-Data dimension is like (2 columns ,4000 rows) 2000 for class 1 and 2000 for class 0
-And then added an additional row of 1’s for bias And its dimensions become (3 columns ,4000 rows) 1st columns in now always will be 1 to tackle bias
-Randomly initialize the weight vector with dimension (1 * 2+1)
-Bias is added to column It is a row vector
-In feedword Calculated the dZ & dA
-And then update the W in backpropogate
