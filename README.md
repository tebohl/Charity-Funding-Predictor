# Charity-Funding-Predictor

## Description:  
A nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. Using machine learning and neural networks, the features in the provided dataset will be used to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.


## Process:  
### Step 1: Preprocess the Data  
Using Pandas and Scikit-learn, the data in charity_data.csv was read and prepared by dropping unecessary columns, unique values binned together and categorical variables were encoded. 

Target variables: 'IS_SUCCESSFUL'

Feature variables: 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS'

### Step 2: Compile, Train, and Evaluate the Model  
Using TensorFlow and Keras, I designed a neural network to create a binary classification model that can predict if an Alphabet Soup–funded organization will be successful based on the features in the dataset. First assigning the number of input features and nodes for each layer, then creating the first hidden layer with an appropriate activation function and finally and output layer with an appropriate activation function. Then the model is compiled and trained and a callback that saves the model's weights every five epochs is created. Lastly, I evaluated the model using the test data to determine the loss and accuracy.  
The results are saved to an HDF5 file in the Resources folder called AlphabetSoupCharity.h5.


### Step 3: Optimize the Model (AlphabetSoupCharity_Optimzation.ipynb, AlphabetSoupCharity_Optimization.h5)  
With TensorFlow, I attempted to optimize the model to achieve a target predictive accuracy higher than 75% using the following methods:

Data Adjustments:  
Dropped additoinal column 'ASK_AMT'.  (This did not help the accuracy, so I replaced it in my second attempt)
Created more bins for rare occurrences in column 'CLASSIFICATION'. (I tried several bin quantities, but yielded a similar accuracy for each)
Added one hidden layer. (I also tried different quantities of nodes, but the accuracy remained close to 72%)
Added 50 epochs to the training regimen.  


### Step 4: Summary  
After reading the data in charity_data.csv, unecessary columns were dropped, unique values binned together and categorical variables were encoded. The target variable was 'IS_SUCCESSFUL'. I then complied, trained and evaluated the model. Starting with two hidden layers, the first of which had twice as many nodes as features, the second with 15 nodes, I used relu and sigmoid activation functions and 100 epochs to train the model. The accuracy was ~72.7%. I made several attempts to optimize the model (details are above), but the accuracy hovered around the same value. Both models are saved in HDF5 files as well.




