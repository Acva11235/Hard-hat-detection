# 🚧 Hard Hat Detection using Efficientdet D0 👷

## Overview: HatGuard AI
The **Hard Hat Detection Project** aims to enhance construction site safety by detecting workers not wearing hard hats through CCTV footage. Utilizing advanced object detection techniques, this project processes live video streams to identify safety violations in real-time. Each year, 12,000 workers die due to head injuries, and HatGuard AI helps solve this critical issue by ensuring that proper safety measures are followed.

## 🧠 Model and working
This project leverages the [TensorFlow Model Zoo](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md) with the EfficientDet D0 (512x512) model, trained on a dataset of 10,000 construction images comprising over 20,000 objects. The model was trained for 30,000 steps, ensuring high accuracy and robustness in diverse environments.

## 🚀 In action

![Example with hard hats](example_with_hard_hats.gif)
![Example without hard hats](example_without_hard_hats.gif)


## ⚡ Features
- **Real-Time Detection**: Processes live CCTV footage for immediate detection of hard hat violations.
- **Violation Logging**: Saves images of detected violations in a 'violations' folder for later review by managers.
- **Auditory Alert**: Plays a siren instantly upon detecting a worker without a hard hat, ensuring immediate awareness.

## 💻 Usage
To set up and run this project, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/hard-hat-detection.git
   ```
2. (a) **Load the model from checkpoint**:
    ```python
    ckpt.restore(os.path.join(PATH_TO_CKPT, 'ckpt-201')).expect_partial()
    ```
    More in detection section of [training file.](hard_hat_detection.ipynb)
2. (b) **Load from the "saved model" format**:
    ```python
    saved at: Tensorflow\workspace\hard_hat_detection\models\hard_hat_detector_efficientdet_d0_200k\export
    ```

3. **Use the model with footage**: As described in the Detection steps of the [training file.](hard_hat_detection.ipynb)

## ✨ Environment details for training
The following are are environment details as of 17/6/2024

- python: 3.9.19
- tensorflow: 2.10.0 (As updated by the [verification script](https://tensorflow-object-detection-api-tutorial.readthedocs.io/en/latest/install.html#test-your-installation) in doccumentation, initially 2.5.0)
- Protobuf: 3.12.3
- C++ Build tools: Visual studio 2015 community version (As in pycocotools [doccumentation](https://github.com/philferriere/cocoapi#this-clones-readme), for windows)
- COCOAPI: As cloned from [repo](https://github.com/philferriere/cocoapi)
- CUDA Toolkit: 11.2
- CUDNN: 8.1

I followed the setup given in the official object detection [doccumentation.](https://tensorflow-object-detection-api-tutorial.readthedocs.io/en/latest/)

## 📓 Dataset used

Dataset link: [link](https://universe.roboflow.com/universe-datasets/hard-hat-universe-0dy7t)

## 🙌 Acknowledgements

- Tensorflow model garden. [link](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md)
- Setup doccumentation. [link](https://tensorflow-object-detection-api-tutorial.readthedocs.io/en/latest/)
- Nicholas Renotte TFOD. [link](https://github.com/nicknochnack/TFODCourse)

## 📝 Author

**Achintya Varshneya**

I'm a passionate AI/ML enthusiast specializing in computer vision. This project showcases my expertise in object detection, model training, real-time video processing, and advanced safety monitoring features. Connect with me on [LinkedIn](https://www.linkedin.com/in/achintya-varshneya-396296247/) to know more about my work and future projects.