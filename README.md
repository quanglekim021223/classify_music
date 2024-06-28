# Music Genre Classification

This project classifies music tracks into different genres using Convolutional Neural Networks (CNNs).

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Preprocessing](#preprocessing)
- [Model Architecture](#model-architecture)
- [Training](#training)
- [Evaluation](#evaluation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Overview

The goal of this project is to classify music tracks into their respective genres using MFCC features and a CNN model. The genres considered are: blues, classical, country, disco, hiphop, jazz, metal, pop, reggae, and rock.

## Dataset

The dataset used is the GTZAN dataset which contains 1000 audio tracks each having 30 seconds duration. The dataset is organized in 10 genres, each represented by 100 tracks.

## Preprocessing

- Audio files are divided into segments and MFCC features are extracted.
- The parameters for MFCC extraction include:
  - Number of MFCCs: 13
  - FFT window size (`n_fft`): 2048
  - Hop length: 512

## Model Architecture

The CNN model consists of:
- 3 Conv2D layers followed by MaxPooling2D and BatchNormalization layers.
- A Flatten layer to convert 2D matrix to 1D.
- Dense layers for classification with dropout regularization.

## Training

- Optimizer: Adam with a learning rate of 0.0001.
- Loss function: Sparse categorical cross-entropy.
- Metrics: Accuracy.
- Batch size: 32
- Number of epochs: 50

## Evaluation

The model is evaluated using a test set. Accuracy and a confusion matrix are used to assess performance.

## Usage

To use the model for predicting the genre of a new audio track:
1. Preprocess the audio track to extract MFCC features.
2. Load the trained model.
3. Predict the genre using the model.

## Results

The model achieves a test accuracy of approximately XX%. The confusion matrix is shown below:

![Confusion Matrix](path/to/confusion_matrix.png)

## Contributing

Feel free to submit issues or pull requests. Contributions are welcome!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
