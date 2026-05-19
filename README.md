# Orientation-Aware Edge Detection

Computer vision notebook for extracting edge structure from grayscale images using Difference of Gaussians preprocessing, oriented convolution filters, and winner-take-all response aggregation.

The project demonstrates a classical image-processing pipeline rather than a black-box model. It is useful for understanding how local contrast enhancement and orientation-selective filters can be combined to produce interpretable edge maps.

## Overview

The notebook implements the following workflow:

1. Load input images and convert them to grayscale.
2. Apply Difference of Gaussians filtering to enhance local intensity transitions.
3. Convolve the processed image with four orientation-selective filters: 0, 45, 90, and 135 degrees.
4. Aggregate filter responses using a winner-take-all strategy.
5. Visualize intermediate responses and final edge maps for different image categories.

## Repository Structure

```text
.
├── orientation_aware_edge_detection.ipynb
│                         # End-to-end experimentation notebook
├── requirements.txt       # Python dependencies for local notebook execution
├── LICENSE                # MIT license
└── README.md              # Project documentation
```

## Method

The pipeline combines two standard image-processing ideas:

- Difference of Gaussians: smooths the image at two different scales and subtracts the results to emphasize edge-like transitions.
- Oriented filtering: applies Sobel-style kernels in multiple directions so edge responses can be analyzed by orientation.

The final response is produced by combining orientation channels and normalizing them against the strongest local response. This makes the output less dependent on any single filter direction.

## Getting Started

### Prerequisites

- Python 3.9 or later
- Jupyter Notebook or JupyterLab

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run the Notebook

```bash
jupyter notebook orientation_aware_edge_detection.ipynb
```

The notebook currently expects images to be available from a Google Drive path when run in Colab. For local execution, update the `img_dir` variable in the image-loading cell to point to a local image directory.

## Inputs

Use a small set of natural and man-made object images for comparison. The implementation expects image files in a single directory and processes them into grayscale before applying the edge pipeline.

Supported formats depend on OpenCV, but common formats such as `.jpg`, `.jpeg`, and `.png` are suitable.

## Outputs

The notebook visualizes:

- grayscale input images
- Difference of Gaussians response
- orientation-specific edge responses
- winner-take-all response map
- final normalized edge map

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
