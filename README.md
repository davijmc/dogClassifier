# Dog Size Classification using K-Nearest Neighbors

## Description

This project aims to classify the size of dogs (small, medium, large) based on their height and weight using the K-Nearest Neighbors (KNN) machine learning algorithm. The model is trained on a dataset of dogs, and it can predict the size of a new dog based on its physical attributes.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [How it Works](#how-it-works)
- [Results](#results)

## Features

- Predicts the size of a dog based on height and weight.
- Easy to use with input from JSON files.
- Implements K-Nearest Neighbors algorithm for classification.

## Installation

To run this project, you need to have Python installed. You can also use a virtual environment to manage your dependencies. Follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/dog-size-classification.git
    cd dog-size-classification
    ```

2. Install the required packages:
    ```bash
    pip install numpy scikit-learn
    ```

## Usage

1. You can commit the `# Generate x dogs` function or `# Generate 1000 dogs` if you have your own files, but make sure the names match those used in the code.
2. Train the model using the training dataset (`dogs.json`).
3. Test the model with a separate dataset (`test.json`).
4. Use the following code to input the dog's height and weight and predict its size:

    ```python
    # User input
    new_height = int(input("Enter the dog's height (in cm): "))
    new_weight = int(input("Enter the dog's weight (in grams): "))

    # Predict and print the class
    predicted_class = predict_dog_class(new_height, new_weight)
    print(f'The predicted size status of the dog is: {predicted_class}')
    ```

## Dataset

The project uses two JSON files:

- **dogs.json**: This file contains the training dataset with attributes for height, weight, and size of the dogs.
- **dogs_test.json**: This file contains the test dataset for evaluating the model's performance.

### Sample Data Structure
```json
[
    {
        "size": "small",
        "height": 30,
        "weight": 5000
    },
    {
        "size": "medium",
        "height": 45,
        "weight": 15000
    },
    {
        "size": "big",
        "height": 70,
        "weight": 30000
    }
]
```

## How it Works
1.The dataset is loaded from JSON files.
2.The KNN model is trained using height and weight as input features.
3.The model is tested on a separate dataset to evaluate its accuracy.
4.Predictions can be made for new dog data based on height and weight.

## Results
- The model's accuracy can be evaluated by comparing the predicted sizes against the actual sizes from the test dataset.
- To see the percentage of correct predictions, run the model and observe the output.