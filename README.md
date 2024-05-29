# Face Recognition System

## Overview

The Face Recognition System is a powerful and efficient solution for detecting and recognizing faces in real-time from various sources such as video feeds, images, and live camera streams.  
Leveraging state-of-the-art deep learning algorithms, this system offers high accuracy and fast processing speeds, making it suitable for a wide range of applications including security, authentication, and user interaction enhancements.

## Features

- **High Accuracy**: Utilizes advanced deep learning models to ensure precise face detection and recognition.  
- **Real-time Processing**: Capable of processing live video feeds with minimal latency.  
- **Scalability**: Easily scalable to accommodate multiple cameras and high-resolution images.  
- **User Management**: Supports a comprehensive database for storing and managing user profiles and facial data.  
- **Cross-Platform**: Compatible with various operating systems including Windows, Linux, and macOS.  
- **Easy Integration**: Offers RESTful APIs and SDKs for seamless integration with existing applications and systems.  
- **Privacy & Security**: Ensures data privacy and security with encrypted storage and secure communication protocols.  

## Installation

### Prerequisites

- Python 3.7 or higher  
- Create a `requirements.txt` file with the following content:
    ```
    numpy
    scipy
    scikit-learn
    dlib
    opencv-python ; extra == "webcam"
    openface ; extra == "projecting_faces"
    ```

### Steps

1. Clone the repository:
    ```sh
    https://github.com/Shubhiiiii/Face-Recognition-System.git
    ```
2. Install the required dependencies:
    ```sh
    pip install -r requirements.txt

### Training:
- Make sure you are in correct directory where the project is saved.
- Make folder training-images.
- Add images of each person you want to recognise to a folder by their name in training-images.
- Example:
 ```sh
    $ mkdir training-images
    $ cd training-images
    $ mkdir Name_Of_Person
```
Then copy all the images of that person in ./training-images/Name_Of_Person folder.
- Run on cmd python create_encodings.py to get the encodings of the images and the labels. This will create encoded-images-data.csv and labels.pkl files.
- Run on cmd python train.py to train and save the face recognition classifier. This will create classifier.pkl file. It will also create classifier.pkl.bak backup file if the classifier with that name already exists.

### Prediction:
- Make folder test-images which contains all the images you want to find people in.
- Run on cmd python predict.py to predict the faces in each image.

### Real-time Recognition
For real-time face recognition using a webcam:
```sh
    python webcam.py

