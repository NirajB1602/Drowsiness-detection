# Drowsiness Detection

## Overview:
This project aims to detect drowsiness in individuals using computer vision techniques and a Convolutional Neural Network (CNN) model. Detecting drowsiness is critical, particularly in tasks like driving, where staying alert is essential for safety. The system monitors the user's eyes through a webcam feed, determining whether they are open or closed. When significant drowsiness is detected, an alarm alerts the individual.

## Installation:
To run the drowsiness detection system, ensure you have the following dependencies installed:

- OpenCV (`pip install opencv-python`)
- NumPy (`pip install numpy`)
- Keras (`pip install keras`)
- Pygame (`pip install pygame`)

## Usage:
1. Clone the repository to your local machine.
2. Ensure your webcam is connected and accessible.
3. Run the `drowsiness_detection.py or drowsiness_detection.ipynb` script.
4. A window will display your webcam feed with real-time drowsiness detection.

## Description:
- The `drowsiness_detection.py or drowsiness_detection.ipynb` script uses OpenCV to capture video frames from the webcam.
- It utilizes pre-trained Haar cascade classifiers to detect faces and eyes within each frame.
- The CNN model, loaded from the `cnncat2.h5` file, classifies whether each eye is open or closed.
- The script tracks the user's drowsiness score based on their eye states.
- If the drowsiness score exceeds a set threshold, an alarm is triggered using Pygame's mixer module.
- Additionally, a red bounding box alerts the user visually.

## CNN Model:
The CNN model used in this project is a sequential model, implemented with the Keras library. Sequential models in Keras allow for the straightforward stacking of layers in a neural network. The model's architecture (stored in `cnncat2.h5`) includes convolutional layers followed by max-pooling layers, flattening, and fully connected layers with dropout for regularization. The system achieves an approximate accuracy of 95.2%, ensuring reliable detection of drowsiness. This high accuracy, validated through extensive testing on diverse datasets, enhances safety, particularly in critical situations like driving.

## Contributors:
- [Niraj Bansal](https://github.com/NirajB1602)

Feel free to fork, contribute, and share this project with others interested in drowsiness detection and improving safety through technology. Thank you for using Drowsiness Detection system!

## Note:
Ensure the required Haar cascade XML files (`haarcascade_frontalface_alt.xml`, `haarcascade_lefteye_2splits.xml`, `haarcascade_righteye_2splits.xml`) are present in the `haar cascade files` directory, and the alarm sound file (`alarm.wav`) is available in the root directory.
