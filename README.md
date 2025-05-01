# Helmet Detection using Roboflow and Google Colab

This project demonstrates the application of **object detection** using a **pre-trained Roboflow model** for detecting helmets in images. The system uses a Google Colab interface that allows users to upload images and get real-time predictions on whether a helmet is detected or not. It also visualizes the predicted bounding boxes around the detected helmets.

## 🛠 Project Architecture

1. **User Interface (UI)**: The project leverages `ipywidgets` in a **Google Colab** environment to provide a simple file upload interface.
2. **Model Integration**: The project utilizes **Roboflow's Object Detection Model** to predict helmet presence in images. The model uses a pre-trained **YOLO** (You Only Look Once) architecture for real-time object detection.
3. **Prediction Flow**: The image uploaded by the user is sent to the **Roboflow API**, which returns a list of predictions (including bounding boxes) for helmets detected in the image.
4. **Post-Processing**: The bounding boxes are drawn using **Pillow** (`PIL`) on the image for visualization.

## 🚀 Features

- **Real-time Helmet Detection**: The uploaded image is processed by the model in real time to predict the presence of helmets.
- **Bounding Box Visualization**: Detected helmets are highlighted with bounding boxes drawn on the image.
- **Confidence Threshold**: The prediction includes a confidence score, allowing users to specify a confidence threshold to control detection sensitivity.
- **Model Output**: Predictions return the class labels ("Helmet"), confidence score, and bounding box coordinates (x, y, width, height).

## 🔧 Requirements

To run this project, you'll need the following libraries:

- **Roboflow API**: For connecting to the model.
- **ipywidgets**: For creating the image upload interface.
- **Pillow**: For image processing (drawing bounding boxes).
- **Matplotlib**: Optional for visualizing the predictions.

Install dependencies (for local execution or if running in a different environment):

```bash
pip install roboflow ipywidgets Pillow matplotlib
