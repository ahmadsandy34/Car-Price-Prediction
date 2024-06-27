# Car-Price-Prediction

Objective   : Predict car price using linear regression model.

Dataset : `Car-Price-Prediction_Dataset.csv`

Description : This dataset contains the details of used cars and their prices.

| Column | Description |
| --- | --- |
| brand | Car brand |
| model | Car model |
| year | Year of purchase |
| price | Price in GBP |
| transmission | Gearbox type |
| mileage | Mileage in Kilometers |
| fuelType | Car fuel type |
| tax | Tax per year |
| mpg | Fuel consumption (Miles per gallon) |
| engineSize | Car engine size in litres |

## Libraries used:

- pandas and numpy for data manipulation 
- seaborn and matplotlib for data visualization
- winsorizer for outliers handling
- sklearn consisting of :
  - train test split for split datasets into train and test sets
  - standard scaler for feature scaling
  - one hot encoder for feature encoding
  - lasso for linear regression regularization
  - mean absolute error and r2 score for cost function/metrics
  - pickle and json for files and models save

## Files explanation :

- Car-Price-Prediction_Dataset.csv is the dataset that are used in this project 
- Car-Price-Prediction_Main.ipynb is the main file in this project. The content in this file are:
  - Introduction : Explain the objective and dataset used in this project
  - Import Libraries : Libraries that are used in this project
  - Data Loading : Data preparation and loading
  - Exploratory Data Analysis : Data exploration and visualization
  - Feature Engineering : Further data preparation for model training including outliers handling, feature scaling and feature encoding
  - Model Definition : Define the model used in this project. In this case I am using Linear Regression with Lasso Regularization
  - Model Training : Train the model using alpha hyperparameter
  - Model Evaluation : Evaluate the model using cost function. I am using Mean Absolute Error (MAE) and R2 Score for evaluation
  - Model Saving : Necessary files and model saving
  - Conclusion : The conclusion of this project based on the results found
- Car-Price-Prediction_Inference.ipynb is the file that is used to do model inference using files and model from Model Saving in Main file.
- lasso_lin_reg.pkl : Lasso Linear Regression model pickle file
- list_cat_cols.txt : List columns that are categorical text file
- list_num_cols.txt : List columns that are numerical text file
- model_encoder.pkl : One Hot Encoder pickle file
- model_scaler.pkl  : Standard Scaler pickle file

## How to use :
1. Download Car-Price-Prediction_Main.ipynb, Car-Price-Prediction_Inference.ipynb, and Car-Price-Prediction_Dataset.csv then store it in one file
2. In the Car-Price-Prediction_Main.ipynb, run all cells. There will be new files in the file consisting of lasso_lin_reg.pkl, list_cat_cols.txt,
   list_num_cols.txt, model_encoder.pkl, model_scaler.pkl. These files will be used to predict new car data in Car-Price-Prediction_Inference.ipynb
3. In the Car-Price-Prediction_Inference.ipynb, run all cells. You can change the content of data_inf or data_inf2 to experiment with different
    car specification

## The Model Strengths and Weakness :

### Strength : 
- Can decently predict middle prices (£10000~£30000) cars 

### Weakkness :
- Struggle to predict low prices (<£10000) and high prices (>£30000) cars
- In the case of very low-priced cars, it can predict a negative value
 
## Conclusion :
The model successfully predicts new car data from model inference, but there are many aspects that still need improvement, such as making the MAE score lower for more precise prediction and addressing negative prediction issues. The model can be improved in various ways, including:
- More feature engineering technique such as creating new features from existing features
- Feature selection by choosing only the most relevant features 
- Using a different regression model such as polynomial


