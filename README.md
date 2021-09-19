# Neural Network Charity Analysis

## Project Description
The purpose of this analysis is to use deep learning neural netoworks to create a binary classifier that can predict wehther applicants will be successful if funded by Alphabet soup.

## Resources:
* Alphabet Soup Charity dataset (charity_data.csv)
* Software: Tensorflow 2.6.0, Python 3.7.10, Jupyter notebook 6.3.10

## Results:
Data preprocessing:
1. EIN and NAME columns removed from the input dataset as they are identification information 
2. Target column: IS_SUCCESSFUL 
3. Feature columns: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT

Compiling, Training, and Evaluating the Model:
* In the last optimization attempt, the model consisted of 3 hidden layers of 120, 60, and 30 neurons respectively. All hidden layers included a "ReLU" activation function. Sigmoid activation was chosen for the output layer because this is a binary classification problem.
* The model was unable to achieve the target 75% accuracy and plateued at 72.4%. 
* Efforts to increase the accuracy include:
1. increasing the number of epochs from 100 to 200
2. increasing the number of neurons and the number of hidden layers
3. changing the optimizer used from Adam to Adagrad
4. changing the activation function of the hidden layers to tanh

## Summary 
In all attempts at optimization, the accuracy produced was ~72. Therefore, I'd recommend reducing the number of epochs back to 100 to decrease training time. Additionally, during pre-processing columns that may not contribute to learning can be dropped, which might improve accuracy. Additionally, using "dropout" might improce accuracy as it will force the neurons to learn new information. Additionally, a random forest classifier could be a more accurate model because it can combine multiple weak learners (ensemble learning) and is generally known to have high accuracy (tho it is prone to overfitting).


