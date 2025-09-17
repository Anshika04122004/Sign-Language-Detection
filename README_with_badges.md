# 🖐️ Sign Language Detection

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![MediaPipe](https://img.shields.io/badge/MediaPipe-cvzone-yellow)
![License: MIT](https://img.shields.io/badge/License-MIT-lightgrey)

This project implements **real-time Sign Language Detection** using
**OpenCV**, **cvzone (MediaPipe wrapper)**, and **TensorFlow/Keras**.\
It allows capturing hand gesture data, training a deep learning model,
and testing live gesture classification.

------------------------------------------------------------------------

## 🚀 Features

-   Real-time hand tracking using **cvzone.HandTrackingModule**
    (MediaPipe)\
-   Dataset collection for custom gestures\
-   Preprocessing with **OpenCV & NumPy**\
-   Gesture classification with **TensorFlow/Keras model**\
-   Overlay of predictions on live webcam feed

------------------------------------------------------------------------

## 📂 Project Structure

-   `datacollection.py` → Script to collect gesture images\
-   `test.py` → Script to test real-time gesture classification\
-   `Model/keras_model.h5` → Pretrained model (to be added after
    training)\
-   `Model/labels.txt` → Labels corresponding to gestures\
-   `Data/` → Folder containing training images (e.g., Hello, Yes, Thank
    You)

------------------------------------------------------------------------

## ⚙️ Installation

Clone the repository and install the dependencies:

``` bash
git clone https://github.com/your-username/sign-language-detection.git
cd sign-language-detection
pip install opencv-python cvzone tensorflow numpy
```

------------------------------------------------------------------------

## 📊 Dataset Collection

Run the script to collect gesture images:

``` bash
python datacollection.py
```

-   Press **`s`** to save a captured hand image.\
-   Images are stored inside the selected folder (e.g., `Data/Yes/`).\
-   Repeat for each gesture class.

------------------------------------------------------------------------

## 🧠 Model Training

1.  Collect images for multiple classes (`Hello`, `Yes`, `Thank You`,
    etc.).\
2.  Train a CNN model using **TensorFlow/Keras** on this dataset.\
3.  Save the model as `Model/keras_model.h5` and create `labels.txt`
    containing class labels.

------------------------------------------------------------------------

## 🎯 Testing the Model

Run the script to test real-time detection:

``` bash
python test.py
```

-   Detects the hand, crops & resizes it.\
-   Passes the processed image to the trained model.\
-   Displays predicted label on screen (e.g., "Hello", "Yes", "Thank
    You").

------------------------------------------------------------------------

## 📸 Example Output

-   Hand cropped and resized for model input\
-   Prediction displayed on top of bounding box

*(You can add screenshots/GIFs inside a `screenshots/` folder and link
them here)*

------------------------------------------------------------------------

## 🛠️ Technologies Used

-   Python\
-   OpenCV -- Image preprocessing & webcam feed\
-   cvzone / MediaPipe -- Hand detection & tracking\
-   TensorFlow/Keras -- Deep learning model\
-   NumPy -- Image array handling

------------------------------------------------------------------------

## 📌 Example Gestures

-   ✋ Hello\
-   👍 Yes\
-   🤲 Thank You

------------------------------------------------------------------------

## 🔮 Future Work

-   Add more gestures for better vocabulary coverage\
-   Support **two-hand gestures**\
-   Extend to **full sentence sign recognition**\
-   Deploy as **web/mobile app**\
-   Add **real-time speech output** for accessibility

------------------------------------------------------------------------

## 📚 References

-   MediaPipe Hand Tracking →
    https://developers.google.com/mediapipe/solutions/vision/hand_landmarker\
-   cvzone Library → https://pypi.org/project/cvzone/\
-   TensorFlow CNN Tutorial →
    https://www.tensorflow.org/tutorials/images/classification\
-   OpenCV Documentation → https://docs.opencv.org/

------------------------------------------------------------------------

## 📜 License

This project is licensed under the **MIT License**.
