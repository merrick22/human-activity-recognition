# HUMAN ACTIVITY RECOGNITION

Human action recognition involves analyzing the video footage to predict or classify various actions performed by the person in that video. It is widely applied in diverse fields like surveillance, sports, fitness, and defense. 

Using smartphones dataset and an LSTM RNN.

Classifying the type of movement amongst six categories:

WALKING,

WALKING_UPSTAIRS,

WALKING_DOWNSTAIRS,

SITTING,

STANDING,

LAYING.

## RNN:

An RNN takes many input vectors to process them and output other vectors. It can be roughly pictured like in the image below, imagining each rectangle has a vectorial depth and other special hidden quirks in the image below. In our case, the "many to one" architecture is used: we accept time series of feature vectors (one vector per time step) to convert them to a probability vector at the output for classification. Note that a "one to one" architecture would be a standard feedforward neural network.

![image](https://user-images.githubusercontent.com/117385630/217293690-17764301-72d0-4322-92ad-b1449c201c67.png)

## LSTM:
 A type of Recurrent Neural Network (RNN), LSTM networks are capable of learning-order dependence in sequence-prediction problems. An RNN, as you can see below, has a chain of repeating neural-network modules. 


A Recurrent Neural Network with its chain of repeated neural-network modules

In the NN (neural network): 

--X0, X1, … Xt are the inputs, and h0, h1, … ht are the predictions.

--Every prediction at time t (ht) depends on the previous prediction and current input Xt.

RNN remembers the previous information and uses it optimally to process the current input. But the shortcoming of RNN is that it cannot remember long-term dependencies. 

LSTM also has a similar chain structure, but its neural-network module can easily handle long-term dependencies.

We use LSTM to do action classification on a sequence of keypoint detections from a video.

![image](https://user-images.githubusercontent.com/117385630/217294459-460c7cd9-6126-457e-940d-55b53b063ba6.png)

## Conclusion

The final accuracy is of 91%! And it can peak to values such as 93.25%, at some moments of luck during the training, depending on how the neural network's weights got initialized at the start of the training, randomly.


