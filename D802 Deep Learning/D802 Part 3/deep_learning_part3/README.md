# Deep Learning Part 3 – Convolutional Neural Network (CNN)

## Project Overview
This project demonstrates the construction of a convolutional neural network (CNN) 
for image classification using an industry-relevant interactive development environment. 
The notebook focuses on building a reliable data pipeline, defining a CNN architecture, 
verifying model behavior, and producing a reusable processed data artifact.

PyTorch is used as the primary deep learning framework due to its flexibility and 
compatibility with the local development environment.


## Project Structure
deep_learning_part3/
│
├── notebook.ipynb # Executable Jupyter notebook
├── notebook.html # Exported executed notebook (HTML)
├── processed_data.npz # Processed dataset metadata
├── README.md # Project documentation
├── requirements.txt # Required Python libraries
│
└── data/
├── train/ # Image files (training + validation)
└── splits/
├── train_split.csv # Training split metadata
└── val_split.csv # Validation split metadata


## Files Produced
- `notebook.ipynb`  
  The primary Jupyter notebook containing all code for dataset loading, preprocessing, 
  CNN definition, and verification.

- `notebook.html`  
  An exported, executed version of the notebook displaying all outputs and verification steps.

- `processed_data.npz`  
  A compressed NumPy archive containing:
  - Training and validation image filenames
  - Encoded class labels
  - Class name mappings
  - Image preprocessing metadata (target image size)

  Image pixel data are stored separately on disk to avoid duplication and improve reproducibility.


## Tools and Libraries Used
### Development Environment
- PyCharm (Jupyter Notebook support)

### Core Libraries
- Python 3.11
- PyTorch (`torch`)
- Torchvision (`torchvision`)
- NumPy (`numpy`)
- Pandas (`pandas`)
- Pillow (`PIL`)

### Supporting Libraries
- torchinfo – used to generate a detailed model summary
- pathlib – robust cross-platform path handling


## Neural Network Architecture
The model implemented in this project is a convolutional neural network (CNN) consisting of:

- Three convolutional layers with ReLU activation
- Max pooling layers for spatial downsampling
- A fully connected classifier with dropout for regularization
- A final output layer with 10 units corresponding to the image classes

The model summary reports both layer output shapes and parameter counts, allowing analysis 
of model complexity.


## How to Run the Notebook
1. Create and activate a Python virtual environment.
2. Install dependencies: