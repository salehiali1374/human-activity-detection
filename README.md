# Project Name: Human Activity Recognition in Cars

## Description
This project aims to recognize human activities in car environments using deep learning techniques. The dataset contains imbalanced data of 10 types of human activities along with bounding box annotations for the actions in the images. The workflow involves data preprocessing, balancing the dataset using data augmentation, and implementing a multi-loss neural network for detecting both class labels and bounding boxes. The ResNet 101 architecture is utilized for this purpose.

## Results
After training and validation, the following metrics were achieved:

### Train Metrics:
- Bounding-box loss: 0.0024
- Classification accuracy: 0.7326
- Classification loss: 1.7306

### Validation Metrics:
- IOU (Intersection over Union): 0.3231
- Bounding-box loss: 0.0034
- Classification accuracy: 0.7822
- Classification loss: 1.6807

### Test Metrics:
- Confusion Matrix:
  ```
  [[21  1  1  0  0  0  0  0  0  0]
   [ 0 25  3  3  0  0  0  0  0  1]
   [ 0  0 28  5  0  1  0  1  0  0]
   [ 0  2  0 28  2  6  0  1  0  0]
   [ 1  0  0  0 26  1  1  0  0  0]
   [ 0  1  0  0  0 24  1  2  3  0]
   [ 0  1  0  0  0  0 20  1  2  1]
   [ 0  3  0  0  0  0  1 31  3  0]
   [ 1  1  2  0  0  1  1  2 19  1]
   [ 2  0  2  0  2  1  0  1  0 15]]
  ```
- Classification Report:
  ```
                precision    recall  f1-score   support

             0       0.84      0.91      0.87        23
             1       0.74      0.78      0.76        32
             2       0.78      0.80      0.79        35
             3       0.78      0.72      0.75        39
             4       0.87      0.90      0.88        29
             5       0.71      0.77      0.74        31
             6       0.83      0.80      0.82        25
             7       0.79      0.82      0.81        38
             8       0.70      0.68      0.69        28
             9       0.83      0.65      0.73        23

    accuracy                           0.78       303
   macro avg       0.79      0.78      0.78       303
weighted avg       0.78      0.78      0.78       303
  ```

## Usage
1. Clone the repository to your local machine.
2. Install the necessary dependencies specified in `requirements.txt`.
3. Preprocess the dataset using the provided scripts.
4. Train the multi-loss neural network using the balanced dataset.
5. Evaluate the model using the provided test dataset and observe the classification metrics.
