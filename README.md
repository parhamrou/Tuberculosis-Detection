## Tuberculosis (TB) Chest X-ray Database: Image Classification using Transfer Learning
This project implements image classification of chest X-ray images from the Tuberculosis (TB) Chest X-ray Database dataset using transfer learning. 
The goal of this project is to train a deep learning model that can accurately classify these images as either TB-positive or TB-negative.

## Dataset
The Tuberculosis (TB) Chest X-ray Database dataset consists of chest X-ray images from patients with and without tuberculosis. 
The dataset can be downloaded from this [link](https://www.kaggle.com/tawsifurrahman/tuberculosis-tb-chest-xray-dataset).
The dataset contains 662 chest X-ray images with 336 TB positive and 326 TB negative images.

## Usage
1. Clone the repository:
```
git clone https://github.com/parhamrou/Tuberculosis-Detection.git
```
2. Install the required packages:
```
pip install -r requirements.txt
```
3. Run the notebook cells!

## Loading the model
You can use the trained model with its weights:
```
loaded_model = keras.models.load_model('my_model.h5')
```

## Implementation Details
The image classification model is implemented using transfer learning with a pre-trained VGG16 model. 
The VGG16 model is loaded with pre-trained weights from the imagenet dataset and the last few layers are removed.
We then add a few dense layers and train the model on our dataset. We also use the oversampling technique to balance the dataset and improve the generalization performance of our model.

The model is trained using binary cross-entropy loss and the Adam optimizer with a learning rate of 0.1. We train the model for 6 epochs.

After training, we evaluate the performance of the model using various metrics such as accuracy, precision, recall, and F1 score.

## Conclusion
In this project, we have implemented image classification of chest X-ray images from the Tuberculosis (TB) Chest X-ray Database dataset using transfer learning. 
We have trained a deep learning model that can accurately classify these images as either TB positive or TB negative. 
The model achieves good performance on the test set, and can potentially be used as a diagnostic tool for tuberculosis.
