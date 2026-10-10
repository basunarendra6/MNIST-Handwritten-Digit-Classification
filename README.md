# MNIST Handwritten Digit Classification

A machine learning project that classifies handwritten digits (0–9) from the MNIST dataset. The notebook demonstrates image preprocessing, model training with Logistic Regression, prediction, and evaluation.

## Project objective

Build a machine learning model that classifies handwritten digit images using image preprocessing techniques.

## Dataset

The project uses the MNIST dataset provided by `tensorflow.keras.datasets.mnist`.

- 70,000 grayscale images in total
- Image dimensions: 28 × 28 pixels
- 60,000 training images and 10,000 test images
- Labels represent digits 0 through 9

The dataset is downloaded automatically by Keras the first time it is loaded, so a separate dataset download is not normally required.

## Workflow

1. Load the MNIST dataset.
2. Inspect the data dimensions and visualize a sample image.
3. Normalize pixel values from the 0–255 range to the 0–1 range.
4. Flatten each 28 × 28 image into a 784-feature vector.
5. Train a Logistic Regression classifier.
6. Predict labels for the test set.
7. Evaluate accuracy and display a confusion matrix.
8. Test a sample image and optionally try a custom image.

## Repository contents

- `Image Preprocessing Case Study.ipynb` — main Jupyter notebook.
- `requirements.txt` — Python package dependencies.
- `.gitignore` — files and folders Git should ignore.

## Requirements

- Python 3.10 or newer recommended
- pip
- Jupyter Notebook or JupyterLab

## Setup and run

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
cd YOUR-REPOSITORY
```

Create and activate a virtual environment (optional but recommended):

**Windows**
```bash
python -m venv .venv
.venv\Scripts\activate
```

**macOS / Linux**
```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start Jupyter:

```bash
jupyter notebook
```

Open `Image Preprocessing Case Study.ipynb` and run the cells from top to bottom.

## Custom image testing

The final notebook section loads an image named `mnist_pic.jpg` from the current working directory. To use this feature, add your own image with that exact filename, or update the filename in the notebook. The image is converted to grayscale, resized to 28 × 28, normalized, and flattened before prediction.

For best results, use a clear image containing one centered digit. Depending on the image's background, contrast, and digit orientation, preprocessing may need to be adjusted to match MNIST-style images.

## Model and evaluation

The notebook uses `sklearn.linear_model.LogisticRegression` with `max_iter=1000`. It reports test accuracy and plots a confusion matrix. The actual accuracy depends on the runtime environment and execution; run the notebook to obtain the current result.

## Troubleshooting

- If TensorFlow cannot download MNIST, check your internet connection and try again.
- If Jupyter is not found, install the dependencies using `pip install -r requirements.txt`.
- If custom-image testing raises a file-not-found error, place `mnist_pic.jpg` next to the notebook or change the path in the relevant cell.

## License

No license is specified in this project yet. Add a license file if you want to define how others may use, modify, and distribute this repository.
