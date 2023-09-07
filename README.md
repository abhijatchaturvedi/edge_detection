# Edge Detection Assignment README

This repository contains the code and results for the Edge Detection programming assignment. In this assignment, we aim to detect edges in natural images using convolution techniques inspired by Biological Vision.

## Getting Started

Follow the steps below to set up and run the code for edge detection:

### Prerequisites

- Python (recommended version: Python 3.x)
- Jupyter Notebook (if using the provided Colab template)
- Required libraries: NumPy, OpenCV (for image processing), Matplotlib (for visualization)

### Installing Dependencies

You can install the required libraries using pip:

```bash
pip install numpy opencv-python-headless matplotlib
```

### Clone the Repository
Clone this repository to your local machine:

```
git clone https://github.com/yourusername/edge_detection.git
```

### Directory Structure
The project directory structure is as follows:

edge-detection-assignment/
```
│
├── code/             # Code for edge detection
│   ├── edge_detection.ipynb
│   └── ...
│
├── images/           # Natural images (add your own or use provided samples)
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
│
├── results/          # Output images and screenshots
│   ├── result_image1.jpg
│   ├── result_image2.jpg
│   └── ...
│
└── README.md         # This README file
```
### Running the Code
1. Open the Jupyter Notebook provided in the code/ directory if you're using Colab/Python platform, or run your code using your preferred development environment for other programming languages.
2. Load a natural image from the images/ directory or use your own images.
3. Convert the loaded image to grayscale.
4. Define filters for edge detection at 0, 45, 90, and 135 degrees.
5. Implement Winner-Take-All (WTA) and normalization as described in Module 02-02, Slide no 20.
6. Produce the final edge detection output.
7. Experiment with at least two images, one of a natural object and one of a man-made object.
8. Save the resulting edge-detected images in the results/ directory.
