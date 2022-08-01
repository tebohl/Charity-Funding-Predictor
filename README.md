# Charity-Funding-Predictor

## Description:  
A nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. Using machine learning and neural networks, the features in the provided dataset will be used to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.


## Process:  
### Step 1: Preprocess the Data  
Using Pandas and Scikit-learn, the data in charity_data.csv was read and prepared by dropping unecessary columns, unique values binned together and categorical variables were encoded. 

Target variable: 'IS_SUCCESSFUL'

Feature variables: 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS'

### Step 2: Compile, Train, and Evaluate the Model (Charity_Funding_NN.ipynb)  
Using TensorFlow and Keras, I designed a neural network to create a binary classification model that can predict if an Alphabet Soup–funded organization will be successful based on the features in the dataset. First assigning the number of input features and nodes for each layer, then creating the first hidden layer with an appropriate activation function and finally and output layer with an appropriate activation function. Then the model is compiled and trained. Lastly, I evaluated the model using the test data to determine the loss and accuracy.  
The results are saved to an HDF5 file in the Resources folder called AlphabetSoupCharity.h5.


### Step 3: Optimize the Model (AlphabetSoupCharity_Optimzation.ipynb)  
With TensorFlow, I attempted to optimize the model to achieve a target predictive accuracy higher than 75% using the following methods:

Data Adjustments:  
- Dropped additoinal column 'ASK_AMT' due to noise.  (This did not help the accuracy, so I replaced it in my second attempt)
- Created more bins for rare occurrences in column 'CLASSIFICATION' (I tried several bin quantities, but yielded a similar accuracy for each)
- Added one hidden layer (I also tried different quantities of nodes, but the accuracy remained close to 72%)
- Added 50 epochs to the training regimen  

The results are saved to an HDF5 file in the Resources folder called AlphabetSoupCharity_Optimization.h5).

### Step 4: Summary  
The purpose of this analysis was to create a tool that can help select the applicants for funding with the best chance of success.  
After reading the data, 'EIN' and 'NAME' columns were dropped since they do not contribute to the prediction of the target variable 'IS_SUCCESSFUL'. Unique values were binned together in the 'APPLICATION_TYPE' and 'CLASSIFICATION' columns since they contained many unique values. Categorical variables were then encoded.  
The model was compiled, trained and evaluated starting with two hidden layers, the first of which had twice as many nodes as features, the second with 15 nodes. Relu and sigmoid activation functions with 100 epochs were used to train the initial model. The accuracy was ~72.7%.  
I made several attempts to optimize the model (details are in Step 3), but the accuracy hovered around the same value. Since this accuracy is not exceptional, perhaps we could try another model to solve this classification problem. Both models are saved in HDF5 files as well.




