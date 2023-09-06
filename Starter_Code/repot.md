# Analysis Report
Sequential Model

## Purpose
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With my knowledge of machine learning and neural networks, I used a dataset, containing more than 34,000 organizations that have received funding from Alphabet Soup over the years, to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

- What variable(s) are the target(s) for your model? 
y=application_df['IS_SUCCESSFUL'].values

- What variable(s) are the features for your model?  
X=application_df.drop(['IS_SUCCESSFUL'], axis=1).values

## The Process
- What variable(s) should be removed from the input data because they are neither targets nor features?
['EIN', 'NAME']

### Troubleshooting Low Accuracy
- What steps did you take in your attempts to increase model performance?  <br>
-Editing drop columns to keep 'names' column instead of dropping  <br>
-3rd hidden layer <br>
-Defined layers instead of using number_input_features calculation  <br>
-Relu in 1st hidden layer and Sigmoid in all others vs the Relu for all hidden and Sigmoid for outer  <br>

## Results
- How many neurons, layers, and activation functions did you select for your optimized neural network model, and why? 

-First Hidden Layer: <br>
Number of neurons: 100 <br>
Activation function: ReLU (Rectified Linear Unit) <br>
Purpose: Introduces non-linearity and captures complex patterns in the data. <br>

-Second Hidden Layer: <br>
Number of neurons: 30 <br>
Activation function: Sigmoid <br>
Purpose: Adds further non-linearity to the model. Sigmoid can squash values between 0 and 1. <br>

-Third Hidden Layer: <br>
Number of neurons: 10 <br>
Activation function: Sigmoid <br>
Purpose: Additional non-linearity, helping the model learn hierarchical representations. <br>

-Output Layer: <br>
Number of neurons: 1 <br> 
Activation function: Sigmoid<br>
Purpose: This is a binary classification problem (IS_SUCCESSFUL or not), and the sigmoid activation function is appropriate for estimating binary probabilities<br>

- Were you able to achieve the target model performance? 
No, but very close!

### Conclusion


Another possible model for this data would be
Random Forest as it has some helpful qualities for large datasets. Here are some examples of why it would be a good alternative model.<br>
1. Ensemble learning method based on decision trees.<br>
2. Robust, handles non-linear relationships, and automatically performs feature selection.<br>
