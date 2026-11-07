# COVID-19 Detection from Chest X-Ray Images Using Deep Learning

A comparative study of custom Convolutional Neural Networks (CNNs),
lung-mask preprocessing, and ResNet152V2 transfer learning for
COVID-19 detection using chest X-ray images.

## Project Overview

This project explores the application of Deep Learning techniques
to classify chest X-ray images into two categories:

- COVID-19
- Normal

Five different deep learning models were developed and evaluated
to investigate the impact of CNN architecture, image preprocessing,
and transfer learning on classification performance.

The project aims to demonstrate how artificial intelligence can
support medical image analysis and assist in the development of
automated disease detection systems.

**Note:** This is an academic research project and is not intended
for clinical diagnosis or medical decision-making.

## Dataset

The project uses chest X-ray images from the COVID-19 Radiography
Dataset available on Kaggle.

The prepared dataset contains:

- 500 COVID-19 images
- 500 Normal images
- Total: 1,000 images

### Data Distribution

| Dataset | COVID-19 | Normal | Total |
|---------|----------|--------|-------|
| Training | 349 | 349 | 698 |
| Validation | 101 | 101 | 202 |
| Testing | 50 | 50 | 100 |

### Data Preprocessing

Several preprocessing techniques were applied:

- Resizing images to 224 × 224 pixels.
- Normalizing pixel values to the range [0, 1].
- Applying data augmentation during training.
- Using RGB images for standard CNN models.
- Applying lung segmentation masks for the masked-image model.

## Deep Learning Models

Five models were implemented and compared.

### Model 1: Baseline CNN

A basic Convolutional Neural Network designed to establish
an initial classification performance benchmark.

### Model 2: Deeper CNN

A deeper CNN architecture designed to extract more complex
features from chest X-ray images.

### Model 3: Custom CNN

A custom CNN architecture developed to improve feature
extraction and classification performance.

### Model 4: Lung-Masked CNN

A CNN trained on grayscale chest X-ray images with lung masks.

This approach focuses on relevant lung regions while reducing
background information.

### Model 5: ResNet152V2 Transfer Learning

A transfer learning model based on the ResNet152V2 architecture,
pretrained on ImageNet.

Custom classification layers were added for binary classification.

## Experimental Results

The models were evaluated using validation accuracy and
test-set confusion matrices.

### Performance Comparison

| Model | Validation Accuracy | Test Accuracy |
|-------|---------------------|---------------|
| Model 1 | 81.19% | 94% |
| Model 2 | 93.56% | 95% |
| Model 3 | 94.55% | 93% |
| Model 4 | 92.08% | 95% |
| ResNet152V2 | 92.57% | 94% |

Validation accuracy values are taken from the final project report.

Test accuracy values were calculated from the confusion matrices
saved in the project notebook, using 100 testing images.

### Key Findings

- Model 3 achieved the highest reported validation accuracy of 94.55%.
- Models 2 and 4 achieved the highest test accuracy of 95%.
- Custom CNN architectures demonstrated competitive performance.
- Lung masking provided an alternative approach for focusing on
  relevant anatomical regions.
- Transfer learning with ResNet152V2 demonstrated strong classification
  performance but did not outperform the best custom CNN models.

These results highlight the importance of model architecture
selection and image preprocessing in medical image classification.

## Technologies and Libraries

The project was developed using:

- Python
- Google Colab
- TensorFlow
- Keras
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- Pillow (PIL)
- Google Drive

## Project Implementation

The implementation includes:

1. Dataset loading and exploration.
2. Image preprocessing and augmentation.
3. Training and validation dataset preparation.
4. CNN model development.
5. Model training and optimization.
6. Performance evaluation.
7. Accuracy and loss visualization.
8. Confusion matrix analysis.
9. Comparison of model performance.

## How to View the Project

The complete implementation is available in the Jupyter Notebook:

`Covid_19_Mask_final_project_deep1.ipynb`

The notebook contains:

- Python source code.
- Deep learning model architectures.
- Training and validation results.
- Accuracy and loss graphs.
- Confusion matrices.
- Model evaluation outputs.

The saved notebook can be viewed directly on GitHub
without downloading the dataset.

## How to Run the Project

To reproduce the experiments:

1. Open the notebook using Google Colab.
2. Install the required Python libraries.
3. Download and prepare the dataset.
4. Mount Google Drive.
5. Update dataset paths if necessary.
6. Execute the notebook cells sequentially.

The dataset is required to rerun the complete training
and evaluation process.

Some environment-specific paths and model checkpoint settings
may require adjustments before reproducing the experiments.

## Project Contributors

This project was developed by:

- Mahmoud Allobani
- Montaser Ababneh
- Montaser Melhem

**Field:** Data Science

**University:** Jordan University of Science and Technology (JUST)

## Project Documentation

The complete methodology, experimental analysis, results,
and references are available in the accompanying Final Project Report.

**Report Title:**

Advanced Intelligent System for COVID-19 Detection Using Deep
Convolutional Neural Networks and X-ray Image Analysis.

## Disclaimer

This project was developed for educational and research purposes.

The results demonstrate experimental deep learning performance
on a limited dataset and do not establish clinical reliability.

The models should not be used as standalone medical diagnostic tools.
