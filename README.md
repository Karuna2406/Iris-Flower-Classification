# Iris Flower Prediction

## Overview

This is a simple web application built using Streamlit that predicts the species of an Iris flower based on user inputs for sepal length, sepal width, petal length, and petal width. The app utilizes a pre-trained Random Forest Classifier to make predictions and displays the predicted species along with the prediction probabilities.

## Features

- **User Input Parameters**: Allows the user to input custom values for sepal length, sepal width, petal length, and petal width using sliders in the sidebar.
- **Prediction Output**: Displays the predicted Iris flower species based on the user’s input.
- **Prediction Probability**: Shows the probability of the prediction for each class (species).
- **Simple Interface**: Easy-to-use interface powered by Streamlit for real-time predictions.

## Installation

To run this application, you need to have Python installed along with the following dependencies:

- **Streamlit**: For building the web app.
- **Pandas**: For handling data in tabular format.
- **Scikit-learn**: For machine learning model training and prediction.

Install the dependencies using the following command:

```bash
pip install streamlit pandas scikit-learn
```

## Running the Application

1. **Clone or download the code** to your local machine.
2. **Navigate** to the project directory and run the following command in the terminal:

```bash
streamlit run app.py
```

This will open the Streamlit app in your web browser.

## How the App Works

1. **User Input Parameters**:
   - The app provides sliders in the sidebar for users to input values for:
     - Sepal Length (range: 4.3 - 7.9)
     - Sepal Width (range: 2.0 - 4.4)
     - Petal Length (range: 1.0 - 6.9)
     - Petal Width (range: 0.1 - 2.5)
   
2. **Model Prediction**:
   - The app uses the built-in Iris dataset from Scikit-learn.
   - A Random Forest Classifier is trained on the Iris dataset to predict the species of the flower.
   - The prediction is based on the input parameters provided by the user.
   
3. **Prediction Output**:
   - The predicted class (species) of the Iris flower is displayed.
   - The app also shows the prediction probabilities for each species.

## Code Breakdown

- **Libraries Used**:
   - `streamlit`: For building the web app interface.
   - `pandas`: For creating a DataFrame of user input features.
   - `scikit-learn`: For loading the Iris dataset and using the RandomForestClassifier for predictions.

- **User Input**:
   - A function `user_input_features()` is used to collect user input via sliders in the sidebar, which are then converted into a DataFrame.

- **Model Training**:
   - The Iris dataset is loaded using `datasets.load_iris()`, and the features (`x`) and labels (`y`) are extracted.
   - A Random Forest Classifier (`clf`) is trained on the dataset.

- **Predictions**:
   - The model predicts the species of the flower based on the user input.
   - The app displays the prediction and the corresponding probabilities for each class.

## Example Usage

1. **Adjust the sliders** in the sidebar to input values for the sepal and petal dimensions.
2. Once the values are set, the app will automatically display:
   - The predicted species of the Iris flower.
   - The prediction probability for each species (Setosa, Versicolor, Virginica).

