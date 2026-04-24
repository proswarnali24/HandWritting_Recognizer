# HandWritting Recognizer

A deep learning project for handwritten digit recognition using convolutional neural networks on the MNIST and SVHN datasets. The repository contains two end-to-end Jupyter notebook pipelines covering data preparation, model training, hyperparameter tuning, evaluation, visualization, and cross-dataset generalization experiments.

## Project Highlights

- Built CNN-based digit recognizers for both MNIST and SVHN.
- Performed train/validation/test splitting and model selection with hyperparameter tuning.
- Evaluated models with accuracy, precision, recall, confusion matrices, and classification reports.
- Visualized sample predictions, misclassifications, and softmax confidence distributions.
- Tested cross-dataset transfer to measure robustness across different handwritten and street-view digit domains.
- Included imbalance analysis experiments for selected classes.

## Results Summary

### MNIST Model

- Test accuracy: `98.94%`
- Weighted precision: `98.94%`
- Weighted recall: `98.94%`

### SVHN Model

- Test accuracy: `88.84%`
- Weighted precision: `88.90%`
- Weighted recall: `88.84%`

### Cross-Dataset Evaluation

- MNIST-trained model on SVHN test set: `7.15%` accuracy
- SVHN-trained model on MNIST test set: `58.81%` accuracy

These results show strong in-domain performance and also highlight the difficulty of transferring a model between datasets with very different image characteristics.

## Repository Structure

```text
HandWritting_Recognizer/
|-- CV_Assgn_2_MNIST.ipynb
|-- CV_Assgn_2_SVHN.ipynb
|-- images/
|   |-- mnist/
|   |-- svhn/
|   `-- cross/
`-- cv_assgn2 (1).pdf
```

## Notebooks

### `CV_Assgn_2_MNIST.ipynb`

Includes:

- MNIST data loading and preprocessing
- CNN architecture definition
- training and evaluation utilities
- hyperparameter tuning
- final training and testing
- misclassification analysis
- confusion matrix and classification report
- cross-dataset evaluation on SVHN
- imbalance analysis

### `CV_Assgn_2_SVHN.ipynb`

Includes:

- SVHN data loading and preprocessing
- CNN architecture for RGB digit images
- training and evaluation utilities
- hyperparameter tuning
- final training and testing
- prediction analysis and visualization
- confusion matrix and classification report
- cross-dataset evaluation on MNIST
- imbalance analysis

## Tech Stack

- Python
- Jupyter Notebook
- PyTorch
- Torchvision
- NumPy
- Matplotlib
- scikit-learn

## How to Run

1. Clone the repository.
2. Create and activate a Python virtual environment.
3. Install the required libraries:

```bash
pip install torch torchvision numpy matplotlib scikit-learn notebook
```

4. Launch Jupyter:

```bash
jupyter notebook
```

5. Open either notebook and run the cells in order.

## Notes

- The notebooks were designed as coursework-style experimental pipelines.
- Results may vary slightly depending on random seed, environment, and hardware.
- Dataset downloads are handled inside the notebooks through `torchvision`.

## Author

Created and maintained by Sornali Sen.
