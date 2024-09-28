# Alphabet Soup Charity Model Analysis
This repository contains a deep learning project for nonprofit foundation Alphabet Soup, aimed at predicting the success of funding applicants. Using machine learning and neural networks, the project develops a binary classifier to identify applicants with the highest likelihood of success, optimizing the foundation's funding decisions.

## Overview of the Analysis

The purpose of this analysis is to develop and optimize a deep learning model that predicts the success of charity organizations funded by Alphabet Soup. By analyzing historical data from past charity projects, we aim to build a neural network model that can accurately classify whether a future project is likely to be successful. The ultimate goal is to support decision-making for funding allocation by providing reliable predictions.

## Results

### Data Preprocessing

- **Target Variable:**
  - The target variable for the model is `IS_SUCCESSFUL`, a binary variable indicating whether a charity project was successful (`1`) or not (`0`).

- **Feature Variables:**
  - All other columns, except `EIN`, `NAME`, and `IS_SUCCESSFUL`, serve as features for the model. These include various characteristics of the charity projects and the organizations behind them.

- **Variables Removed:**
  - `EIN` and `NAME` were removed from the dataset because they are identifiers that do not contribute to predicting the success of a project. They do not contain any relevant information that would help the model make better predictions.

### Compiling, Training, and Evaluating the Model

- **Neurons, Layers, and Activation Functions:**
  - **Neurons and Layers:**
    - The final neural network model consists of 3 hidden layers with 128, 64, and 32 neurons, respectively.
    - The first attempt started with fewer neurons and layers but was increased to capture more complex patterns in the data, which led to better performance.
  - **Activation Functions:**
    - `ReLU` (Rectified Linear Unit) was used for the hidden layers to introduce non-linearity and handle complex patterns in the data.
    - `Sigmoid` activation function was used for the output layer because the task is a binary classification problem.

- **Model Performance:**
  - **Target Performance:** The target was to achieve an accuracy of at least 75%. Unfortunately, after multiple optimization attempts, the final model achieved an accuracy of 72% on the test dataset.
  - **Steps to Increase Performance:**
    - **Increased Neurons and Layers:** The model was initially simple but was later made more complex by adding more neurons and layers. This change helped in capturing more detailed patterns from the data.
    - **Adjusted Activation Functions:** The `ReLU` activation function was chosen for hidden layers because of its efficiency in deep learning models, while `tanh` was also tested for its ability to handle certain types of data better.
    - **Increased Epochs:** The number of epochs was increased to 150, allowing the model more time to learn from the data, which contributed to the improved accuracy.

## Summary

### Overall Results

The final deep learning model achieved an accuracy of 72%, which falls short of the target performance of 75%. While the model shows some capability in predicting the success of charity projects funded by Alphabet Soup, its accuracy is not high enough to be fully reliable for guiding funding decisions. As it stands, the model may not be the most effective tool for making informed funding choices.

### Recommendations for Fine-Tuning the Model

To improve the model's performance and potentially reach or surpass the target accuracy of 75%, the following fine-tuning strategies are recommended:

 **Increase Model Complexity:**
   - **Add More Layers:** Introducing additional hidden layers can help the model learn more complex patterns in the data.
   - **Increase Neurons per Layer:** Adding more neurons to each layer could enhance the model's ability to capture intricate relationships in the dataset.

**Experiment with Activation Functions:**
   - **Test Different Activation Functions:** Consider experimenting with different activation functions, such as `Leaky ReLU` or `ELU`, which may perform better than `ReLU` in certain scenarios.

**Increase Training Epochs with Early Stopping:**
   - **Train for More Epochs:** Extending the training period may allow the model to learn more, but use an **early stopping** callback to prevent overfitting.


By implementing these strategies, the model's accuracy could be improved, making it a more reliable tool for predicting the success of charity projects and supporting Alphabet Soup's funding decisions.


