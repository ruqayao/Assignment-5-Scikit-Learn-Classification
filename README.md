# Assignment-5-Scikit-Learn-Classification
# Purpose
The purpose of this project is to apply machine learning classification techniques to predict whether a breast tumor is malignant or benign. The project uses the built-in breast cancer dataset provided in Scikit-learn. Three different classification models were trained and evaluated to determine which model performs best for this dataset. Machine learning has become an important tool in healthcare because it can help identify patterns in medical data that support earlier disease detection and improved diagnostic accuracy.
# Dataset
This project uses the breast cancer dataset that is included with Scikit-learn. The dataset contains measurements computed from digitized images of breast tumor samples.

The dataset includes:
- 569 observations (tumor samples)
- 30 numerical features describing tumor characteristics such as radius, texture, perimeter, area, and smoothness
- 1 target variable indicating whether the tumor is malignant or benign

The dataset was split into training and testing sets using an 80/20 split so that the models could be trained on one portion of the data and evaluated on unseen data.
# Class Design and Implementation
The program uses two main classes to organize the workflow: a data loading class and a model training class.

CancerDataLoader Class

The CancerDataLoader class is responsible for loading and preparing the dataset.

Attributes
- data – stores the original dataset loaded from Scikit Learn
- X – stores the feature variables used for training the models
- y – stores the target classification labels

Methods
- load_data() – loads the breast cancer dataset from Scikit Learn
- get_features() – returns the feature dataset
- get_target() – returns the target labels

This class separates the data preparation process from the machine learning logic, making the code easier to organize.

ModelTrainer Class

The ModelTrainer class is responsible for splitting the dataset, scaling the data, training models, and evaluating their performance.

Attributes
- X – feature dataset
- y – target dataset
- X_train – training features
- X_test – testing features
- y_train – training labels
- y_test – testing labels
- scaler – a StandardScaler object used to normalize the dataset

Methods
- split_data() – divides the dataset into training and testing sets using an 80/20 split and applies feature scaling
- train_and_evaluate(model, name) – trains a machine learning model, generates predictions, and prints evaluation metrics

Feature scaling is performed using StandardScaler so that all variables are on a similar scale before training the models.

Machine Learning Models UsedMachine Learning Models Used

Three classification algorithms were implemented in this project.

Logistic Regression
- The model was configured with a higher maximum iteration value to ensure proper convergence during training.

Decision Tree Classifier
- The model was slightly adjusted by setting a maximum depth of 5. Limiting the depth helps prevent overfitting and improves the model’s ability to generalize to new data.

K-Nearest Neighbors (KNN)
- The number of neighbors was set to 7 instead of the default value to improve model stability and classification performance.

Evaluation Metrics

The models were evaluated using several common classification metrics:
- Accuracy – the percentage of correct predictions
- Precision – the proportion of correctly predicted positive observations
- Recall – the proportion of actual positives correctly identified
- F1 Score – the balance between precision and recall

These metrics were generated using the classification report provided by Scikit-learn.

Limitations

This project includes several limitations:
- The dataset is relatively small and may not represent all real-world cancer cases.
- The models were only trained on the built-in dataset and were not tested on external data.
- Only three classification algorithms were implemented.
- Hyperparameter tuning was minimal and limited to a few small adjustments.
- The program prints results to the console instead of storing them in files or visualizing them.
