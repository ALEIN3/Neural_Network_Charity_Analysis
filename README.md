# Neural_Network_Charity_Analysis

# Overview
The purpose of this project is to use the deep-learning neural networks with the TensorFlow platform in Python to analyze the success of charitable donations.
To accomplish that, we use the following methods, preprocessing the data for the neural network model, train and evaluating the model, and optimize the model.
## Resources
•	Data Source: [charity_data](https://github.com/ALEIN3/Neural_Network_Charity_Analysis/blob/main/charity_data.csv)

•	Software: Python, Anaconda Navigator, Jupyter Notebook, VScode.

# Results

## Data Preprocessing

•	I dropped the columns EIN and NAME from the input data because they are identification information.

•	The column IS_SUCCESSFUL contains binary data referring to whether or not the charity donation was used effectively. This variable is then considered as the target for our deep learning neural network.

•	Encoding The columns APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT since they are the categorical variables

•	The columns APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT are the features for our model.

•	Then split into training and testing datasets, and standardization have been applied to the features.

## Training, and Evaluating the Model

•	This deep-learning neural network model is made of two hidden layers as follow:
hidden_layer1 = 90 neurons
hidden_layer2 = 40 neurons

•	The input data has 44 features and 25,724 samples.

•	We are using the activation function ReLU for the hidden layers. As our output is a binary classification, Sigmoid is used on the output layer.
For the compilation, the optimizer is adam , and the loss function is binary_crossentropy.

•	The model accuracy is less than 75%. And that does not meet the minimum threshold of the accuracy to consider sufficient to help predict the outcome of the charity donations.

•	To increase the performance of the model, we made the following attempt:

o	We tried to add neurons to layers, as follow:

hidden_layer1 = 120 neurons
hidden_layer2 = 45 neurons

o	We used a model with three hidden layers.

o	We also tried a different activation function (tanh) for the first and the second hidden layers.

After trying the previous methods, none of them helped improve the model's performance.

# Summary

The deep learning neural network model did not reach the 75% accuracy threshold. Considering that this target level is kind of average we could say that the model is not outperforming.
Since we are in a binary classification situation, we could try a supervised machine learning model and compare the results with the deep learning neural network model.
