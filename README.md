# MNIST Handwritten Digit Classifier

A simple neural network built with TensorFlow/Keras that recognises handwritten digits (0-9), plus a small drawing app where you can draw a digit with your mouse and see the model's prediction.

## What it does

1. Loads the MNIST dataset (70,000 images of handwritten digits)
2. Scales pixel values to 0-1 and splits the data into training, validation (10%) and test sets
3. Trains a fully connected neural network
4. Evaluates it on unseen test data
5. Opens a drawing window (Tkinter) to test the model on your own handwriting

## Model

| Layer | Details |
|-------|---------|
| Input | 28x28 image, flattened to 784 values |
| Hidden 1 | 100 neurons, ReLU |
| Hidden 2 | 100 neurons, ReLU |
| Output | 10 neurons, Softmax |

- Optimizer: Adam
- Loss: Sparse categorical crossentropy
- Batch size: 100
- Epochs: 5

## Results

- Validation accuracy: ~98.2%
- Test accuracy: ~97.1%

## Drawing app

Draw a digit on the black canvas and click **Predict**. The app crops, resizes and centres your drawing into a 28x28 image (like MNIST), shows you what the model sees, and prints the prediction with a confidence score. Click **Clear** to start over.

Note: the drawing app opens a desktop window, so it needs to run locally (not in Google Colab).

## How to run

1. Install the requirements:
   ```
   pip install tensorflow tensorflow-datasets numpy pillow matplotlib
   ```
2. Open `MNIST Project.ipynb` in Jupyter Notebook or JupyterLab
3. Run the cells from top to bottom

## Tech used

Python, TensorFlow/Keras, TensorFlow Datasets, NumPy, Pillow, Matplotlib, Tkinter
