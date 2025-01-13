# AI Enabled Face Mask Detector

This project provides a real-time face mask detection system using machine learning algorithms. The system detects whether a person is wearing a mask or not in images and video streams.

## Technologies Used

- **MobileNetV2** - A lightweight Convolutional Neural Network (CNN) used for image classification.
- **Haar Cascade Classifier** - Used for face detection in images.
- **OpenCV** - A library for computer vision tasks.
- **TensorFlow** - Framework for deep learning.
- **Keras** - Deep learning API used for building and training models.

## Setup and Usage

### 1. Data Collection
Collect labeled data (images of people with and without masks) to train the model. Ensure that the images are clear and the faces are visible. Organize the data into two folders: `with_mask` and `without_mask`.

### 2. Data Preprocessing
- Resize images to 224x224 pixels to ensure consistency in input size.
- Convert images to arrays and normalize them for better training performance.
- Perform one-hot encoding on labels for the binary classification of mask-wearing status.

### 3. Model Training
- Load the MobileNetV2 pre-trained model without the top layer (classification layer) and add a custom fully connected layer for mask detection.
- Freeze the layers of the pre-trained model to prevent modification during training.
- Compile the model using an optimizer like Adam and categorical cross-entropy loss function.
- Train the model using the labeled dataset. Monitor the training and validation accuracy and loss.

### 4. Model Testing
- Evaluate the trained model on a separate testing dataset to measure its performance.
- Calculate accuracy, precision, recall, and F1-score to understand the model’s effectiveness.

### 5. Real-time Detection
- Use OpenCV to access the webcam feed and detect faces in real-time using the Haar Cascade Classifier.
- Preprocess the detected faces and predict whether the person is wearing a mask or not using the trained model.
- Display the result with bounding boxes around faces and text indicating whether the person is wearing a mask.

## Conclusion
The AI-enabled face mask detector provides an efficient solution for detecting whether a person is wearing a mask in real-time using deep learning and computer vision. By leveraging the power of MobileNetV2 and Haar Cascade classifiers, the system offers a lightweight and fast solution suitable for various applications, especially in public health monitoring. With continued improvements and fine-tuning, this model can be adapted to different environments and used to further enhance safety measures.
