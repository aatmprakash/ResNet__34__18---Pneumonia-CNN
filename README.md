# ResNet 34/18 - Pneumonia CNN

This repository contains the implementation of a Convolutional Neural Network (CNN) model based on the ResNet-34/18 architecture for detecting pneumonia from chest X-ray images.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Installation](#installation)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)


## Introduction

Pneumonia is a common respiratory infection that affects the lungs. It can be caused by various pathogens, such as bacteria, viruses, or fungi. Detecting pneumonia accurately and in a timely manner is crucial for effective treatment and patient management.

The traditional approach to diagnosing pneumonia involves visual examination of chest X-ray images by radiologists. However, this process can be time-consuming and subjective. With the advancements in deep learning and computer vision, automated methods have been developed to assist in pneumonia detection from chest X-ray images.

This project aims to build a deep learning model capable of accurately classifying chest X-ray images as either normal or pneumonia-infected using the ResNet-34/18 architecture. The ResNet architecture, with its residual connections, enables the training of deeper networks by addressing the vanishing gradient problem. By leveraging the power of deep learning, this model can potentially provide a fast and reliable solution for pneumonia detection.


## Dataset

The dataset used for training and evaluation is not included in this repository due to licensing and privacy restrictions. However, the code provided assumes that the dataset follows a specific directory structure. The dataset should be organized into two main folders: `train` and `val` (short for validation). Within each of these folders, there should be two subfolders: `NORMAL` and `PNEUMONIA`. The `NORMAL` folder contains X-ray images of healthy individuals, while the `PNEUMONIA` folder contains X-ray images of individuals with pneumonia.

It is important to note that the dataset should be obtained from reliable and ethical sources, ensuring proper consent and adherence to privacy regulations.

## Model Architecture

The repository provides two variations of the ResNet model: ResNet-34 and ResNet-18. These models are implemented using the PyTorch deep learning framework.

ResNet-34 consists of 34 layers, including residual blocks, while ResNet-18 has 18 layers. The residual blocks in ResNet allow for the efficient training of deeper networks by introducing skip connections that bypass several layers. These connections help address the vanishing gradient problem and promote the flow of gradients throughout the network.

The choice between ResNet-34 and ResNet-18 depends on the available computational resources and the desired trade-off between model complexity and accuracy.

## Installation

To use this repository, you need to follow these steps:

1. Clone the repository:

   ```
   git clone https://github.com/aatmprakash/ResNet__34__18---Pneumonia-CNN.git
   ```

2. Install the required dependencies using `pip`:

   ```
   pip install -r requirements.txt
   ```

3. Organize your dataset according to the provided directory structure, as described in the Dataset section.

4. Train the model by running the following command:

   ```
   python train.py --model resnet34
   ```

   You can replace `resnet34` with `resnet18` to train the ResNet-18 model.

5. After training, the trained models will be saved in the `saved_models` directory.

6. Evaluate the model on the validation set by running the following command:

   ```
   python evaluate.py --model resnet34 --checkpoint saved_models/resnet34.pth
   ```

   Replace `resnet34.pth` with the appropriate checkpoint file for the ResNet-18 model.

## Results

The evaluation script provided in the repository will output various metrics, such as accuracy, precision, recall, and F

1-score, to assess the performance of the trained model on the validation set. These metrics provide insights into how well the model is able to differentiate between normal and pneumonia-infected chest X-ray images.

It is important to interpret these results carefully and consider other factors such as the dataset's class distribution, false positives/negatives, and the intended use case when evaluating the model's performance.

## Contributing

Contributions to this repository are welcome. If you find any issues or have suggestions for improvements, please open an issue or submit a pull request. Collaboration and feedback from the community can help enhance the model's performance and make it more robust.

## License

This project is licensed under the [MIT License](LICENSE). You are free to modify, distribute, and use the code for both non-commercial and commercial purposes, with proper attribution to the original authors.
