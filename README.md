# Overview of the analysis:
This analysis involves using deep learning to classify the success of charitable donations based on given features. Different neural network models are optimized through various techniques, such as adjusting the number of neurons, layers, activation functions, and training epochs, in an attempt to achieve the best model performance.

# Data Preprocessing:
- What variable(s) are the target(s) for your model?
  - The target variable is 'IS_SUCCESSFUL'.
- What variable(s) are the features for your model?
  - The features include all other variables in the dataset except 'IS_SUCCESSFUL', 'EIN', and 'NAME'.
- What variable(s) should be removed from the input data because they are neither targets nor features?
  - The columns 'EIN' and 'NAME' were removed during preprocessing.

# Compiling, Training, and Evaluating the Model
- **How many neurons, layers, and activation functions did you select for your neural network model, and why?**
  - **In Model 1:**
    - Two hidden layers, one with 80 neurons and a second with 30 neurons. Both layers used the ReLU activation function. The output layer used a sigmoid activation function.
    - Loss: 0.5563241839408875, Accuracy: 0.7274635434150696
     <img width="944" alt="Screen Shot 2023-08-31 at 8 36 53 AM" src="https://github.com/loganlbarnes/deep-learning-challenge/assets/128556117/c0f5a61c-6a2a-4de0-a458-7220a1737376">

  - **In Optimization 1:**
    - Two hidden layers, each with 80 neurons, were used (increasing the number of neurons for the second layer to see if that has an affect on the accuracy). Both layers used the ReLU activation function. The output layer used a sigmoid activation function.
    - Loss: 0.5594645738601685, Accuracy: 0.7254810333251953
      <img width="967" alt="Screen Shot 2023-08-31 at 8 38 00 AM" src="https://github.com/loganlbarnes/deep-learning-challenge/assets/128556117/77883da2-8fb2-44c7-8268-ce8ac3dc97b9">

  - **In Optimization 2:**
    - Three hidden layers were used, all with ReLU activation, each having 80 neurons. The third layer was added to see if it has an affect on accuracy. The output layer used a sigmoid activation function.
    - Loss: 0.5780602693557739, Accuracy: 0.7254810333251953
   
     <img width="895" alt="Screen Shot 2023-08-31 at 8 39 42 AM" src="https://github.com/loganlbarnes/deep-learning-challenge/assets/128556117/9365d27a-6eeb-4287-bc4a-ee9bb9e488d0">

  - **In Optimization 3:**
    - Three hidden layers with 80 neurons each. The first layer used ReLU activation while the next two used tanh. The output layer used a sigmoid activation function. Epochs were also increased to 200 to see if that has an affect on accuracy.
    - Loss: 0.5582984089851379, Accuracy: 0.7258309125900269
    <img width="849" alt="Screen Shot 2023-08-31 at 8 40 14 AM" src="https://github.com/loganlbarnes/deep-learning-challenge/assets/128556117/ada4d496-bb84-43d4-862e-c9f505dc1f46">

- **Were you able to achieve the target model performance?**
  - No, none of the optimization attempts resulted in an accuracy above 75%.
- **What steps did you take in your attempts to increase model performance?**
  - Increased the number of neurons in the hidden layers.
  - Added an additional hidden layer.
  - Changed activation functions.
  - Increased the number of training epochs.

# Summary
The deep learning model was optimized through various techniques in an attempt to classify the success of charitable donations. Three different optimization attempts were made, adjusting the architecture and parameters of the neural network.

**Recommendation:**
Given the results from the provided optimizations, other potential approaches to improve model performance could include:
- Using ensemble methods or different architectures like convolutional or recurrent neural networks if appropriate.
- Gathering more data or engineering new features that could be beneficial for the model.
- Defining a function to loop through activations, neurons, and epochs to find the best fit for the model.
