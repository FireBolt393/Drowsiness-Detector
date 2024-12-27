# Drowsiness Detection Using CNN in Google Colab

This project uses a Convolutional Neural Network (CNN) to detect drowsiness in a person using a webcam. It continuously streams the webcam feed, detects the face, and labels the person as "Drowsy" or "Not Drowsy."

The project is built in Python using libraries like TensorFlow, Keras, and OpenCV and is designed to be run directly in Google Colab. The Google Colab environment is used to access the local webcam and handle the video stream. 

## Features

- **Real-time face detection**: Continuously streams the webcam and draws a box around the face.
- **Drowsiness detection**: Labels the person as either "Drowsy" or "Awake" based on facial features.
- **Pre-trained Model**: The model is trained on a large dataset (details below) and can be used for drowsiness detection on any webcam feed.

## How to Use

This project is designed to be run on Google Colab. Follow the steps below to set up and use the project:

### 1. **Open the Project on Google Colab**
   - Open `Drowsiness Detector.ipynib` in google colab.
   
### 2. **Download the Dataset and Pre-trained Model**

   - A pre-trained model is available and was trained on a machine with a powerful GPU to ensure fast and accurate predictions. Download the model from the link below and use it in Colab as shown in the setup instructions.
   - The dataset used for training the model is quite large, so it has been uploaded to my Google Drive. To use the dataset and pre-trained model in your Colab environment, follow these steps:
   
   - **Download the dataset from my Google Drive**:
     - [Dataset and Pre-trained Model (Google Drive)](https://drive.google.com/drive/folders/1Z1QyrOw8ggzNgaD0n8E0laSUutmEWVoa?usp=sharing)
   
   - **Upload the dataset to your own Google Drive**:
     - Go to Google Drive, click on "New" -> "File Upload", and upload the dataset.

   - **Connect Google Colab to your Google Drive**:
     - In Google Colab, use the following code to mount your Google Drive and access the dataset:
       
       ```python
       from google.colab import drive
       drive.mount('/content/drive')
       ```

   - Once mounted, you can access your files using the path `/content/drive/My Drive/`.

### 3. **Run the Project in Google Colab**
   
   - After mounting Google Drive and uploading the dataset, run the following code in the Colab cells to load and start the drowsiness detection system:
   
     ```python
     # Load the pre-trained model and dataset from Google Drive
     model_path = '/content/drive/My Drive/your-folder-path/model.h5'
     dataset_path = '/content/drive/My Drive/your-folder-path/dataset'
     
     # Load model, data, and other setup
     model = keras.models.load_model(model_path)
     ```
      
   - The model will start processing the webcam feed, detecting faces, and labeling whether the person is drowsy or not.

### 4. **Run the Webcam Stream**
   - If you prefer not to train the model again and directly use the pre-trained model, you can start running the code from Cell No. 15.
   - Once everything is set up, you will be able to see the live webcam feed with the face detection box drawn, and the label indicating whether you are "Drowsy" or "Not Drowsy".

### 5. **Ensure Webcam Access in Colab**

   - Google Colab uses JavaScript to access the webcam, and this part of the code will only run within Colab. Ensure your browser has webcam access permissions enabled.

## Dependencies

This project uses the following dependencies:

- Python 3.x
- JavaScript
- TensorFlow
- Keras
- OpenCV
- NumPy
