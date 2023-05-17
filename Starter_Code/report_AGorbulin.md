## Step 4: Write a Report on the Neural Network Model

# Overview of the analysis:

The purpose of this analysis was to develop a deep learning neural network model to solve a classification problem. The goal was to predict whether a charity organization will be successful in receiving funding based on various features.

# Results:
Using bulleted lists and images to support your answers, address the following questions:

# Data Preprocessing:
What variable(s) are the target(s) for your model?
ANSWER:

The target variable for the model is y = application_df["IS_SUCCESSFUL"].values, indicating whether a charity organization is successful in receiving funding.

- What variable(s) are the features for your model?

ANSWER:

All variables except for y = application_df["IS_SUCCESSFUL"].values were used as features for the model.

- What variable(s) should be removed from the input data because they are neither targets nor features?

ANSWER:

The columns "EIN" and "NAME" were dropped from the input data because they did not provide significant value as targets or features.
Compiling, Training, and Evaluating the Model:
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
ANSWER:
The neural network model used the following architecture:

Number of input features: number_input_features = len(X_test[0])

Neural network layers:

First hidden layer: 80 neurons with "relu" activation function
Second hidden layer: 50 neurons with "leaky_relu" activation function
Third hidden layer: 50 neurons with "relu" activation function
Fourth hidden layer: 50 neurons with "relu" activation function
Output layer: 1 neuron with "sigmoid" activation function
The selection of neurons, layers, and activation functions was based on experimentation and fine-tuning to achieve optimal model performance.

- Were you able to achieve the target model performance?
ANSWER:
The model achieved the following performance metrics:

* Loss: 0.5098
* Accuracy: 0.7493
The model did not fully meet the target performance, but it still achieved a reasonable accuracy rate of approximately 74.93%.

- What steps did you take in your attempts to increase model performance?
ANSWER:
To improve the model performance, the following steps were taken:

* Increased the number of layers from two to four.
* Added and modified activation methods for different layers.
* Adjusted the number of neurons per layer.
These steps were aimed at capturing more complex patterns and enhancing the model's ability to learn and make accurate predictions.

## Summary:
The deep learning neural network model showed promising results in predicting the success of charity organizations in receiving funding. The model achieved an accuracy rate of approximately 74.93%, indicating its ability to classify the organizations effectively.
Recommendation for a different model:
While the current neural network model provides reasonable performance, an alternative approach could be to explore ensemble methods, such as Random Forest or Gradient Boosting. These methods have shown effectiveness in handling classification tasks and can capture complex interactions between features. Additionally, feature engineering techniques, such as creating new relevant features or applying dimensionality reduction methods, could further enhance the performance of the classification model.

By leveraging ensemble methods and feature engineering, it is possible to build a more robust and accurate model for predicting the success of charity organizations in receiving funding.
