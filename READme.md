# Alphabet Soup Charity: Deep Learning Model

## Overview
This project involves creating a deep learning binary classification model to predict the success of funding applications for a fictional non-profit organization, Alphabet Soup. Using a dataset of historical funding application data, the model aims to identify key factors that contribute to successful funding outcomes.

---

## Project Objectives
- Preprocess the provided data to prepare it for training a deep learning model.
- Build, train, and evaluate a neural network using TensorFlow and Keras.
- Optimize the model to achieve at least 75% predictive accuracy.
- Save the model in HDF5 format and document its performance.

---

## Results

### Data Preprocessing
1. **Target Variable**: 
   - The target variable for this model is `IS_SUCCESSFUL`, which indicates if the funding application was successful (1) or not (0).

2. **Feature Variables**: 
   - All other columns, excluding `EIN` and `NAME`, were used as features after preprocessing.

3. **Columns Removed**:
   - Non-beneficial columns such as `EIN` and `NAME` were removed as they did not provide useful predictive information.

4. **Encoding**:
   - Categorical variables were encoded using `pd.get_dummies()` to convert them into numeric values.

5. **Splitting**:
   - The data was split into training and testing datasets with an 80-20 split.

6. **Scaling**:
   - Features were scaled using `StandardScaler` for better model performance.

---

### Model Architecture
1. **Input Features**:
   - The number of input features is equal to the number of columns in the scaled training dataset.

2. **Hidden Layers**:
   - **Layer 1**: 64 neurons with ReLU activation.
   - **Layer 2**: 32 neurons with ReLU activation.

3. **Output Layer**:
   - 1 neuron with a sigmoid activation function for binary classification.

4. **Optimizer**:
   - Adam optimizer was used for training the model.

5. **Loss Function**:
   - Binary Crossentropy was used to measure prediction error.

---

### Training and Evaluation
- **Epochs**: 50
- **Batch Size**: 32
- **Validation Split**: 20% of the training data was used for validation during training.

#### Performance Metrics:
- **Accuracy**: The final model achieved an accuracy of approximately 99% on the test data.
- **Loss**: The model’s binary crossentropy loss was minimal, indicating effective training.


## Conclusion
The deep learning model successfully predicts the success of funding applications with high accuracy. While the model performed exceptionally well, further optimization or feature engineering may improve predictions for rare cases.