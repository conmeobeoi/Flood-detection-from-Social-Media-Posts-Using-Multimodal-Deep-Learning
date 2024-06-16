# Flood-detection-from-Social-Media-Posts-Using-Multimodal-Deep-Learning
## Table of Contents

- [Introduction](#introduction)
- [Project Overview](#project-overview)
- [Dataset](#Dataset)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)

## Introduction

This project aims to detect floods using a multimodal approach, combining image data and text data. Flooding is a significant natural disaster that can cause severe damage to lives and property. Applying machine learning techniques for flood detection can help provide early warnings and take appropriate actions to mitigate the impact of flooding.

## Project Overview

In this project, we implement a system using a multimodal architecture for detecting flood from social media posts, specifically images and text. The system uses various data sources, such as satellite images, weather data, and other relevant information, to predict and monitor potential flood events. The goal is to create an accurate and reliable system for real-time flood detection.

## Dataset

The dataset used in this project is extracted from one task related to flood events: DIRSM (Disaster Image Recognition from Social Media) from the 2017 Multimedia Satellite Task. The DIRSM dataset includes images and metadata from the YFCC100M dataset, shared under Creative Commons licenses that allow redistribution. Each image in this dataset belongs to a single user to ensure the uniqueness of the samples. The images are classified into two categories: (1) Showing evidence of a flooding event and (2) Showing no evidence of a flooding event. This dataset comes with additional metadata and a development set of 5,280 image and a test set consisting of 1,320 images along with their metadata. This dataset is a crucial resource for developing and testing machine learning models in flood detection applications, providing the necessary tools to analyze and predict flood events based on images and satellite data. 

## Features

- **Input Image and Tweet**: We split the development set into 90% for training and 10% for validation.

- **Image Preprocessing**: All images are resized and preprocessed by scaling and normalizing pixel values. Various augmentation techniques are applied, including random horizontal flips, color jitter, and random rotations.

- **Visual Feature Extractor**: We use transfer learning with pre-trained models: ResNet50, DenseNet-201, EfficientNetB3
  
- **Textual Feature Extractor**: BERT, XLNet
  
- **Choosing Best-Performed CNN Model**: Models are trained with identical hyperparameters, and the one with the highest accuracy (EfficientNetB3) is selected.

- **Selecting Best-Performed Language Model** : BERT outperforms XLNet in this step and is chosen for the next phase.

- **Fusion and Classification**: Outputs from both the visual and textual parts are combined using late fusion to form a shared representation.
  
- **Evaluate the Final Model**: Performance is evaluated using accuracy, precision, recall, and weighted F1-score on validation set to assess and compare the model's effectiveness across different classes.
  
- **Result:** Create a csv file to store the result from model.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Python 3.6+
- Pytorch
- NumPy
- PIL (for image processing)
- Additional libraries as specified in the project's requirements file

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/miahh1103/Flood-detection-from-Social-Media-Posts-Using-Multimodal-Deep-Learning.git
   ```

2. Run it on the kaggle plattform:
   - Because of the problem about the device, i decide to run it on plattform for ML/DL.

## Usage

1. To use this flood detection system, follow the steps mentioned in the project documentation or Jupyter notebooks if provided.

2. Customize the model according to your specific use case and data sources.

3. Run the file on kaggle.

## Contributing

Contributions are welcome! If you would like to contribute to this project, please follow these guidelines:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and ensure they work as expected.
4. Commit your changes and create a pull request.
