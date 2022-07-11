# Neural_Network_Charity_Analysis
# Project
## Overview
In this project, data from a charity organization was analyzed to determine key factors that effect success of award recipients and used to create a Neural Network Model to predict success of future recipients. The model was re-factored and optimized to attempt to increase accuracy 

### Purpose
The purpose of this project was to create a Neural Network model that predicted success with a 75% accuracy rate.

### Resources
**Data retrieval:** [Charity Data](/Resources/charity_data.csv)

**Data Output:** [Checkpoints](/Checkpoints/), [Model](/Checkpoints/AlphabetSoupCharity.h5)

**Tools:** Python, Jupyter Notebook, PANDAS, Sci-kit Learn, Tensorflow, Keras
<br>

## Results
### Data Preprocessing
 - What variable(s) are considered the target(s) for your model?
   - Target variable is the column "IS_SUCCESSFUL" because it directly shows which recpient showed success after receiving award. 
 - What variable(s) are considered to be the features for your model?
   - Features include: Application Type, Classification, Use-Case, Organization, Income Amount, Ask Amount, and Special Considerations
 - What variable(s) are neither targets nor features, and should be removed from the input data?
   - Removed Features: Name, EIN, Status
### Compiling, Training, and Evaluating the Model
 - How many neurons, layers, and activation functions did you select for your neural network model, and why?
    - Initially, 2 hidden layers with 80 neurons in the first layer and 30 neurons in the second layer with ReLu activation functions in both hidden layers and sigmoid function in the output layer. 
 - Were you able to achieve the target model performance?
   - No
   - Accuracy: 73.0%
 - What steps did you take to try and increase model performance?
   1. Attmept 1:
    - Increased hidden layers from 2 to 3 with 80 neurons, 40 neurons, and 20 neurons sequentially in each layer. 
    - Accuracy: 72.8%
   2. Attmept 2:
    - Altered activation function from ReLu to Leaky ReLu. 
    - Accuracy: 71.8%
   3. Attmept 3:
    - Transformed Data: 
        - Removed "Status" column
        - Re-categorized Use-Case and Income Amt columns 
    - Accuracy: 73.4%


## Summary
Overall, the model's accuracy remained at 72% - 73% despite optimization techniques. A better model might be used such as Random Forest to classify the success status. 

Transforming data yeilded the best results to accuracy, therefore an ensemble technique that fits and classifies model then compares overall results might yeild 75% or higher accuracy in the prediction. 