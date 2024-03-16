
# 🖼️ Basic Image  Classification for Tree Species (Bark) 🌳 using SVM Classifier

Here I am providing a basic script for image classification of tree species based on bark images using an SVM classifier. Please note that this script is intended for understanding the process involved in species classification, so accuracy may not be optimal. To achieve better accuracy, additional modifications and optimizations may be necessary.

###  ⬆️ Importing Libraries:
- **numpy:** To perform numerical operations
- **os:** Interacts with the operating system for handling file paths.
- **cv2:** To perfrom Image processing tasks.
- **pandas:** Data Analysis.
- **train_test_split:**  For splitting the dataset into training, testing and validation sets.
- **StandardScaler:** For scaling features.
- **SVC:** To use Support Vector Classification.
- **accuracy_score and classification_report:** Evaluating the model's performance.
- **matplotlib.pyplot:** Data visualization.

### Loading ↻ Data:
- Define the directory path (`dire`) and categories of images.
- Here reading images from the specified directory (location), after this resize the images into a standard size (`SIZE`), and store them in the `images` list.
- After this assigning labels to the loaded images based on their categories and store them in the `labels` list.

### 🔍 Feature Extraction:
- Define a function `feature_extractor` to extract features from images. Here we used GLCM (Gray-Level Co-occurrence Matrix).
- Iterate over each image in the dataset and calculate GLCM properties such as contrast, dissimilarity, homogeneity, and energy.
- Store the extracted features in a pandas DataFrame (`image_dataset`).

### 🛢 Data Splitting:
- Split the dataset into training and testing sets using `train_test_split`, with 15% of the data allocated for testing.
- Further split the training set into training and validation sets using `train_test_split`, with 10% of the training data allocated for validation.

### ⚖️ Feature Scaling:
- Scale the features in the training, validation, and test sets using `StandardScaler`.

### 🎯 Model Training:
- Initialize an SVM classifier (`SVC`) with a linear kernel and default hyperparameters.
- Train the SVM classifier on the scaled training data.

### 📋 Model Evaluation:
- Make predictions on the validation and test data using the trained model.
- Calculate the accuracy scores for the training, validation, and test sets.
- Print the training, validation, and test accuracies.
- Generate a classification report to evaluate precision, recall, and F1-score for each class.

### 📊 Visualization:
- Plot decision boundaries for the validation and test sets to visualize the SVM's classification.


## Conclusion:
This script provides a comprehensive workflow, including data loading, preprocessing, model training, evaluation, and visualization, to classify images of bark into different tree species.

