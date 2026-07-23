# Chinese Character Classification Using Neural Networks (Chinese MNIST)

## Project Overview

The goal of this project was to develop and compare deep learning models for recognizing Chinese characters using the **Chinese MNIST** dataset. The project covers the complete machine learning workflow, including data preparation, dataset construction, model development, training, evaluation, and performance comparison.

The Chinese MNIST dataset contains images of Chinese characters together with their corresponding labels. The objective is to correctly classify each character based on its image.

## Project Objectives

* Load and preprocess the Chinese MNIST dataset.
* Build a custom dataset using PyTorch.
* Split the data into training, validation, and test sets.
* Implement and compare three neural network architectures.
* Analyze the learning process of each model.
* Evaluate classification performance using accuracy and loss metrics.
* Compare the computational efficiency of different models.

## Dataset

This project uses the **Chinese MNIST** dataset, which contains images of Chinese characters and their associated labels stored in a CSV file.

The data preparation pipeline includes:

* loading images using the Pillow (PIL) library,
* transforming images into PyTorch tensors,
* applying preprocessing and normalization,
* creating a dataset compatible with the PyTorch ecosystem.

The dataset was built using the `TensorDataset` class, which stores image tensors together with their corresponding labels.

## Data Preparation

After creating the dataset, the data was divided into:

* training set,
* validation set,
* test set.

The `DataLoader` class was used to efficiently load batches of data during model training and evaluation.

## Model Architectures

Three models with different levels of complexity were implemented and compared.

### Worst Model

The simplest architecture used as a baseline for performance comparison.

### Medium Model

A moderately complex architecture designed to improve classification performance while maintaining reasonable computational costs.

### Best Model

The most advanced architecture implemented in the project, designed to achieve the highest classification accuracy.

## Training Process

The models were trained using the PyTorch framework.

To accelerate computations, training was performed on a GPU using CUDA.

During training, the following metrics were monitored:

* training loss,
* validation loss,
* classification accuracy,
* training time.

## Results

For each model, the following outputs were generated:

### Loss Curves

Plots showing the evolution of the loss function throughout the training process.

### Accuracy Curves

Plots illustrating classification accuracy across training and validation epochs.

### Model Comparison

The models were compared based on:

* final classification accuracy,
* validation performance,
* computational efficiency,
* training time.

This comparison highlights the trade-off between model complexity, predictive performance, and computational cost.

## Technologies Used

* Python
* PyTorch
* Torchvision
* Pillow (PIL)
* NumPy
* Pandas
* Seaborn
* Matplotlib


## Skills Demonstrated

* Data preprocessing for machine learning
* Image processing in Python
* Building custom datasets with PyTorch
* Using DataLoaders for efficient data handling
* Neural network design and training
* GPU acceleration with CUDA
* Model evaluation and performance analysis
* Data visualization
* Comparative analysis of machine learning models

## Future Improvements

* Implement more advanced convolutional neural network architectures
* Apply transfer learning techniques
* Perform automated hyperparameter optimization
* Introduce data augmentation methods
* Deploy the best-performing model as a web application or API
