# Charity-Funding-Predictor

Description:  
A nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. Using machine learning and neural networks, the features in the provided dataset will be used to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.


Process:  
Step 1: Preprocess the Data  
Using Pandas and Scikit-learn, the data in charity_data.csv was read and prepared by dropping unecessary columns, unique values binned together and categorical variables were encoded. 

Target variables:

Feature variables:

Step 2: Compile, Train, and Evaluate the Model  
Using TensorFlow and Keras, I designed a neural network to create a binary classification model that can predict if an Alphabet Soup–funded organization will be successful based on the features in the dataset. First assigning the number of input features and nodes for each layer, then creating the first hidden layer with an appropriate activation function and finally and output layer with an appropriate activation function. Then the model is compiled and trained and a callback that saves the model's weights every five epochs is created. Lastly, I evaluated the model using the test data to determine the loss and accuracy.  
The results are saved to an HDF5 file in the Resources folder called AlphabetSoupCharity.h5.


Step 3: Optimize the Model (AlphabetSoupCharity_Optimzation.ipynb, AlphabetSoupCharity_Optimization.h5)  
With TensorFlow, I attempted to optimize the model to achieve a target predictive accuracy higher than 75% using the following methods:

Data Adjustments:  
Dropping more or fewer columns.  
Creating more bins for rare occurrences in columns.  
Increasing or decreasing the number of values for each bin.  

Add more neurons to a hidden layer.  
Add more hidden layers.  
Use different activation functions for the hidden layers.  
Add or reduce the number of epochs to the training regimen.  


Step 4: Report on the Neural Network Model  

Overview of the analysis:

Results: 

Data Preprocessing  
Target variables:

Feature variables:  
What variable(s) should be removed from the input data because they are neither targets nor features?

How many neurons, layers, and activation functions were selected and why?  
Was target model performance acheived?  
What steps were taken to increase model performance?  


Summary: 