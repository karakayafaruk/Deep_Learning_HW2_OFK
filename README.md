# CIFAR-10 Image Classification Using ResNet18

## Project Overview

This project presents an image classification system developed using a Convolutional Neural Network (CNN) based on the ResNet18 architecture. The model is trained and evaluated on the CIFAR-10 dataset using the PyTorch deep learning framework.

The objective of this project is to classify images into one of ten predefined categories from the CIFAR-10 dataset. Additionally, the trained model is deployed through a Gradio web application, allowing users to upload images and obtain predictions interactively.

---

## Dataset

**Dataset Name:** CIFAR-10

**Dataset Source:**  
https://www.cs.toronto.edu/~kriz/cifar.html

### Dataset Statistics

- Total Images: 60,000
- Training Images: 50,000
- Test Images: 10,000
- Number of Classes: 10

### Classes

1. Airplane
2. Automobile
3. Bird
4. Cat
5. Deer
6. Dog
7. Frog
8. Horse
9. Ship
10. Truck

---

## Model Architecture

The project uses a pretrained ResNet18 model available in the Torchvision library.

The final fully connected layer of the original network was replaced with a custom layer containing 10 output neurons corresponding to the CIFAR-10 classes.

### Architecture Details

- Base Model: ResNet18
- Framework: PyTorch
- Transfer Learning: Yes
- Output Classes: 10

---

## Data Preprocessing

The following preprocessing techniques were applied:

### Training Transformations

- Resize images to 224×224
- Random Horizontal Flip
- Convert image to Tensor
- Normalize using CIFAR-10 statistics

### Testing Transformations

- Resize images to 224×224
- Convert image to Tensor
- Normalize using CIFAR-10 statistics

---

## Training Configuration

| Parameter | Value |
|------------|------------|
| Model | ResNet18 |
| Optimizer | Adam |
| Loss Function | CrossEntropyLoss |
| Learning Rate | 0.001 |
| Batch Size | 64 |
| Epochs | 10 |
| Input Size | 224 × 224 |
| Framework | PyTorch |

---

## Performance Results

The trained model achieved the following results on the CIFAR-10 test set:

| Metric | Score |
|----------|----------|
| Accuracy | 91.49% |
| Precision | 91.72% |
| Recall | 91.49% |
| F1-Score | 91.55% |

---

## Confusion Matrix Analysis

The confusion matrix demonstrates that the model performs well across all ten classes.

### Strongest Classes

- Automobile
- Truck
- Horse
- Ship

### Most Challenging Classes

- Cat
- Dog

The model occasionally confuses cats and dogs because of their visual similarity, which is a common challenge in image classification tasks.

---

## Deployment

A web-based interface was developed using Gradio.

### Features

- Upload an image
- Run image classification
- Display confidence scores
- Show top predicted classes

The application allows users to interact with the trained model directly through a browser.

---

## Project Structure

```text
DeepLearning_HW2_OFK/

├── DL_HW2_OFK.ipynb
├── resnet18_cifar10.pth
├── README.md
├── requirements.txt
├── screenshots/
│   ├── confusion_matrix.png
│   └── gradio_interface.png
└── report/
    └── report.pdf
```

---

## Installation

Clone the repository:

```bash
git clone <repository-url>
cd DeepLearning_HW2_OFK
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Running the Project

Run the Jupyter Notebook or open the notebook in Google Colab:

```bash
jupyter notebook DL_HW2_OFK.ipynb
```

Execute all notebook cells sequentially to:

1. Download the dataset
2. Train the model
3. Evaluate performance
4. Save the trained model
5. Launch the Gradio application

---

## Libraries Used

- PyTorch
- Torchvision
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Gradio
- Pillow
- tqdm

---

## Future Improvements

Potential future enhancements include:

- Training for more epochs
- Hyperparameter optimization
- Data augmentation improvements
- Testing on larger datasets
- Deploying the application to Hugging Face Spaces

---

## Author

Ömer Faruk Karakaya

Computer Engineering Student

Deep Learning Course Project