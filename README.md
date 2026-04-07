```markdown
# Fashion MNIST Image Classification with Convolutional Neural Networks (CNNs)

This Colab notebook demonstrates building and training Convolutional Neural Networks (CNNs) for image classification on the Fashion MNIST dataset. It covers essential steps from data loading and preprocessing to model definition, training, and visualization of intermediate feature maps.

## Dataset

**Fashion MNIST**: A dataset of Zalando's article images, consisting of a training set of 60,000 examples and a test set of 10,000 examples. Each example is a 28x28 grayscale image, associated with a label from 10 fashion classes:

*   0: T-shirt/top
*   1: Trouser
*   2: Pullover
*   3: Dress
*   4: Coat
*   5: Sandal
*   6: Shirt
*   7: Sneaker
*   8: Bag
*   9: Ankle boot

## Notebook Contents

1.  **Data Loading and Initial Exploration**: 
    *   Loads the Fashion MNIST dataset using `tensorflow.keras.datasets`.
    *   Displays example images and their labels.
    *   Checks the shape and basic properties of the dataset.

2.  **Data Preprocessing**: 
    *   Normalizes pixel values to the range [0, 1].
    *   Reshapes image data to include a channel dimension (e.g., (28, 28) to (28, 28, 1)) for CNN input.

3.  **Basic CNN Model**: 
    *   Defines and compiles a simple CNN model with one `Conv2D` layer, one `MaxPooling2D` layer, a `Flatten` layer, and two `Dense` layers.
    *   Trains the model for 5 epochs and evaluates its performance.

4.  **Improved CNN Model**: 
    *   Introduces a more robust CNN architecture with two convolutional blocks.
    *   Each block includes `Conv2D`, `BatchNormalization`, and `MaxPooling2D` layers.
    *   Adds a `Dropout` layer after the first `Dense` layer to mitigate overfitting.
    *   Compiles and trains this improved model for 8 epochs.

5.  **Feature Map Visualization**: 
    *   Constructs a new Keras `Model` to extract intermediate outputs from the `Conv2D` layers of the improved CNN.
    *   Uses a sample test image to predict and visualize the feature maps learned by the first and second convolutional layers.
    *   This provides insights into what features the network is learning at different stages.

## Libraries Used

*   `tensorflow.keras`: For building and training the neural networks.
*   `matplotlib.pyplot`: For data visualization (displaying images and feature maps).
*   `numpy`: For numerical operations.

## How to Use

1.  Open the Colab notebook in Google Colaboratory.
2.  Run all cells sequentially to reproduce the data loading, model training, and feature map visualization steps.

This notebook serves as a practical example for understanding and implementing CNNs for image classification tasks, showcasing both basic and slightly more advanced architectures with regularization techniques.
```
