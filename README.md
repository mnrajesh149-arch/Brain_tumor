Brain Tumor Detection Using CNN

1. Project Title

**Brain Tumor Detection Using Convolutional Neural Network (CNN)**

2. Project Description

The Brain Tumor Detection** project is an image classification system developed using **TensorFlow and Keras**. The objective of the project is to classify brain images into two categories based on the dataset provided in the project.

The dataset is loaded from Google Drive using `ImageDataGenerator`. Images are resized to **224 × 224 pixels**, normalized by rescaling pixel values using `1./255`, and divided into training and validation sets. The dataset contains **2,400 training images and 600 validation images belonging to two classes**.

A Convolutional Neural Network (CNN)** is used for image classification. The model consists of three convolutional layers with **32, 64, and 128 filters**, respectively. Each convolutional layer is followed by a max-pooling layer. The extracted features are then flattened and passed through a dense layer containing 128 neurons, followed by a single sigmoid output neuron for binary classification.

The model is compiled using the **Adam optimizer**, **binary cross-entropy loss**, and **accuracy** as the evaluation metric. It is trained for **5 epochs**. During training, the validation accuracy improves from **83.50% in the first epoch to 99.17% in the fifth epoch**.

After training, the model is saved as `brain_tumor.h5` and later loaded for prediction. A test image is resized to 224 × 224 pixels, converted into an array, normalized, and passed to the trained CNN model. For the test image shown in the notebook, the prediction value is approximately **0.00000128**, which is below the 0.5 classification threshold, resulting in the notebook's output **"You do not have brain tumor."**

3. Objectives

* To develop an image-based brain tumor classification model.
* To preprocess and normalize brain images for CNN training.
* To extract image features using convolutional layers.
* To classify images into two categories using a sigmoid output layer.
* To evaluate the model using training and validation accuracy.
* To save and reload the trained model for prediction.

4. Technologies Used

* **Python**
* **TensorFlow**
* **Keras**
* **NumPy**
* **Matplotlib**
* **Google Colab**
* **Google Drive**
* **CNN (Convolutional Neural Network)**

5. Methodology

The project follows these main steps:

1. Import TensorFlow, Keras and required libraries.
2. Mount Google Drive.
3. Load the brain image dataset.
4. Resize images to **224 × 224**.
5. Normalize image pixels using `1./255`.
6. Split the dataset into training and validation sets.
7. Build the CNN model.
8. Train the model for 5 epochs.
9. Evaluate training and validation accuracy.
10. Save the trained model.
11. Load the saved model.
12. Provide a test image to the model.
13. Generate the prediction and classify the image using a threshold of 0.5.

6. CNN Architecture

The CNN implemented in the notebook contains:

* Conv2D – 32 filters
* MaxPooling2D
* Conv2D – 64 filters
* MaxPooling2D
* Conv2D – 128 filters
* MaxPooling2D
* Flatten
* Dense – 128 neurons
* Dense – 1 neuron with sigmoid activation

The model contains **11,169,089 total parameters**, all of which are trainable.

7. Training Results

The model was trained for five epochs. The recorded validation accuracy was:

| Epoch | Training Accuracy | Validation Accuracy |
| ----- | ----------------: | ------------------: |
| 1     |            79.54% |              83.50% |
| 2     |            92.71% |              96.67% |
| 3     |            97.50% |              98.83% |
| 4     |            98.17% |              99.50% |
| 5     |            99.33% |              99.17% |

These are the results reported by the uploaded notebook.

8. Prediction

The trained model is saved as:

`brain_tumor.h5`

For the test image used in the notebook, the model produced:

`1.2824535e-06`

Since this value is below the notebook's threshold of **0.5**, the resulting classification was:

**You do not have brain tumor.**

 9. Conclusion

The project demonstrates how a **Convolutional Neural Network can be developed using TensorFlow and Keras for binary classification of brain images**. The notebook covers image preprocessing, CNN model construction, model training, validation, model saving/loading, and prediction on a test image.

The model achieved high validation accuracy during the five training epochs, with the highest recorded validation accuracy being **99.50% in epoch 4**. The project therefore provides a practical demonstration of applying deep learning techniques to brain-image classification.

**Note:** This project is an educational image-classification model. Its prediction should not be treated as a medical diagnosis.
