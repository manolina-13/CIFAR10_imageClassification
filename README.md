# CIFAR-10 Image Classifier with PyTorch

A simple convolutional neural network (CNN) built with PyTorch to classify images from the **CIFAR-10** dataset into 10 categories.

## Project Overview

This project demonstrates:

- Loading and preprocessing CIFAR-10 using `torchvision`
- Building a CNN with convolution, ReLU, max pooling, and fully connected layers
- Training the model with cross-entropy loss and SGD
- Evaluating overall accuracy and per-class accuracy
- Saving the trained model weights

## Dataset Classes

CIFAR-10 contains 10 classes:

- plane
- car
- bird
- cat
- deer
- dog
- frog
- horse
- ship
- truck

## Project Files

- `CIFAR10_imageClassifier.py` — main training and evaluation script
- `requirements.txt` — Python dependencies
- `results.txt` — sample training output and evaluation results
- `cifar_net.pth` — saved model weights after training (generated locally)

## Requirements

Install the dependencies with:

```bash
pip install -r requirements.txt
```

## How to Run

From inside the `Image_classification_CIFAR10` folder, run:

```bash
py .\CIFAR10_imageClassifier.py
```

The script will:

1. Download CIFAR-10 if needed
2. Show a sample batch of training images
3. Train the CNN for 2 epochs
4. Save the trained model to `cifar_net.pth`
5. Evaluate the model on the test set
6. Print per-class accuracy results

## Example Results

See `results.txt` for the output from one training run.

## Model Architecture

The CNN used in this project is:

- `Conv2d(3, 6, 5)`
- `ReLU`
- `MaxPool2d(2, 2)`
- `Conv2d(6, 16, 5)`
- `ReLU`
- `MaxPool2d(2, 2)`
- `Flatten`
- `Linear(16 * 5 * 5, 120)`
- `Linear(120, 84)`
- `Linear(84, 10)`

## Notes

- The script uses a Windows-safe configuration by wrapping execution in `if __name__ == "__main__":`.
- DataLoader workers are set to `0` to avoid multiprocessing issues on Windows.
- The model is trained for only 2 epochs, so accuracy is expected to be modest.

## Contact

Email: manolinadas2004@gmail.com
