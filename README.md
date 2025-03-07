# Dogs vs Cats Image Classification

This project implements a Convolutional Neural Network (CNN) using PyTorch to classify images of dogs and cats.

## Dataset
The dataset used is the **Dogs vs Cats** dataset, which contains images of two classes:
- Dogs
- Cats

## Project Structure
```
├── train/            # Training images
├── test/             # Testing images
├── model.py          # CNN model code
└── main.py           # Training and testing pipeline
```

## Prerequisites
- Python 3.x
- PyTorch
- torchvision
- Pillow
- torchsummary

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/dogs-vs-cats.git
   ```
2. Install dependencies:
   ```bash
   pip install torch torchvision Pillow torchsummary
   ```

## Usage
### Training the Model
1. Place the training images inside the `/train` directory.
2. Run the training script:
   ```bash
   python main.py
   ```
3. The model will train for 10 epochs and print the training and validation accuracy.

### Predicting Images
To predict the class of an image, use the `predict_image` function:
```python
from model import predict_image
predicted_class, probability = predict_image('path_to_image.jpg', model, device)
print(f"Predicted: {predicted_class}, Probability: {probability:.2f}")
```

## Model Architecture
The model consists of:
- 3 Convolutional Layers
- Max Pooling Layers
- Fully Connected Layers
- Sigmoid Activation for Binary Classification

## Performance
- Training Accuracy: ~95%
- Validation Accuracy: ~92%

## License
This project is licensed under the MIT License.

