# Alphabet Soup Funding Predictor

## Project Overview

The **Alphabet Soup Funding Predictor** is a machine learning project aimed at helping the nonprofit foundation, Alphabet Soup, in selecting applicants for funding who have the best chance of success in their ventures. The project involves creating a binary classifier that predicts whether applicants will be successful if funded by Alphabet Soup.

The provided dataset contains information on more than 34,000 organizations that have received funding from Alphabet Soup. This dataset includes various columns that capture metadata about each organization, aiding the prediction process.

## Table of Contents

- [Project Overview](#project-overview)
- [Table of Contents](#table-of-contents)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Data Preprocessing](#data-preprocessing)
- [Model Building](#model-building)
- [Model Training](#model-training)
- [Model Evaluation](#model-evaluation)
- [Next Steps](#next-steps)

## Getting Started

### Prerequisites

Before running the project, you will need the following prerequisites:

- Python 3.x
- Required packages: `pandas`, `sklearn`, `tensorflow`

### Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/alphabet-soup-funding.git
   cd alphabet-soup-funding

### Install the required packages:
```sh
pip install pandas scikit-learn tensorflow
```

## Data Preprocessing
The **preprocessing.ipynb** notebook contains the necessary code for data preprocessing. It involves the following steps:

Loading the dataset using **pd.read_csv.**
Removing non-beneficial ID columns ('EIN' and 'NAME') that do not contribute to model prediction.
Binning low-frequency values in 'APPLICATION_TYPE' and 'CLASSIFICATION' columns into 'Other'.
Converting categorical data into numeric using one-hot encoding with **pd.get_dummies.** <br>

## Model Building
The **model.ipynb** notebook contains the code for building the neural network model. The model is constructed using TensorFlow and Keras. The architecture includes:

- Input layer with appropriate dimensions.
- Two hidden layers with ReLU activation functions.
- Output layer with a sigmoid activation function for binary classification. <br>

## Model Training
After building the model, it is trained using the training dataset. The training process includes:

- Splitting the preprocessed data into training and testing datasets.
- Standardizing the data using StandardScaler.
- Compiling the model with binary cross-entropy loss and the Adam optimizer.
- Training the model using the training data and monitoring its performance. <br>

## Model Evaluation
The trained model's performance is evaluated using the testing dataset. The evaluation involves:

- Calculating loss and accuracy metrics on the testing data.
- Printing the loss and accuracy of the model.

## Next Steps
To improve the model's accuracy, we can consider the following steps:

- Hyperparameter tuning: Experiment with different hyperparameters such as learning rate, batch size, and number of neurons.
- Model complexity: Try adjusting the number of hidden layers and neurons.
- Regularization techniques: Implement dropout or L2 regularization to prevent overfitting.
- Activation functions: Experiment with different activation functions for the hidden layers.

