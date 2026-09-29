# Dataset Card

## 1. Dataset Information

**Dataset Name:** Brain Tumor MRI Dataset

**Source:** Kaggle

**URL:** https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset

**Author:** Masoud Nickparvar

**Dataset Type:** 2D brain MRI images

**Purpose:**
The dataset contains brain MRI images categorized according to the type of brain tumour: glioma, meningioma, pituitary tumour, and no tumour. It will be used in this project to investigate and compare different machine learning approaches for brain tumour classification.


## 2. Task, Input, and Output

**Task:** 4-class image classification

**Input:** 2D brain MRI image

**Output:** One of four predicted classes:

* Glioma
* Meningioma
* Pituitary tumour
* No tumour

The model will use these four classes as the target labels.


## 3. Dataset Structure

The dataset is divided into a **training set** and a **testing set**.

The training set will be used for model development and will be further divided into training and validation subsets. The testing set will be reserved for final evaluation.

The dataset is organized into the following directory structure:

```text
Testing/
├── glioma/
├── meningioma/
├── notumor/
└── pituitary/

Training/
├── glioma/
├── meningioma/
├── notumor/
└── pituitary/
```


## 4. Dataset Size

The exact number of images in each class have been verified programmatically from the downloaded dataset.

| Split     |  Glioma | Meningioma | No Tumour | Pituitary |   Total |
| --------- | ------: | ---------: | --------: | --------: | ------: |
| Training  |    1400 |       1400 |      1400 |      1400 |    5600 |
| Testing   |     400 |        400 |       400 |       400 |    1600 |
| **Total** | **1800** |    **1800** |   **1800** |   **1800** | **7200** |


## 5. Image Characteristics

The dataset consists of 2D brain MRI images.

| Property           | Value |
| ------------------ | ----- |
| File format        | jpg   |
| Image dimensions   | Variable   |
| Most common image dimension   | 512 x 512  |
| Colour modes      | L, RGB, RGBA, P   |
| Number of channels | Variable   |

The most common image dimension is 512 × 512 pixels. The dataset also contains images with other resolutions, and most images are stored as either grayscale (L) or RGB, with a small number using RGBA or palette-based (P) colour modes.

These differences will need to be handled during preprocessing before training the machine learning models.


## 6. Data Composition

The dataset is publicly available through Kaggle and consists of brain MRI images compiled from three publicly available sources:

1. [figshare brain MRI dataset](https://figshare.com/articles/dataset/brain_tumor_dataset/1512427) 
2. [SARTAJ dataset](https://www.kaggle.com/sartajbhuvaji/brain-tumor-classification-mri)
3. [Br35H dataset](https://www.kaggle.com/datasets/ahmedhamada0/brain-tumor-detection?select=no)

The use of images from multiple sources may introduce differences in image characteristics that could affect model performance and generalizability.


## 7. License

**License:** The Kaggle dataset is listed under CC BY 4.0. However, the dataset incorporates data from multiple sources with differing license/usage terms. The licenses of the underlying sources are documented seperately.


## 8. Known Limitations

Potential limitations of the dataset include:

* The images originate from multiple publicly available datasets.
* MRI images may have different resolutions or visual characteristics.
* The dataset may not represent the diversity of MRI scans encountered in clinical practice.
* Patient-level identifiers or clinical metadata are not available.
* Differences between the sources from which the images were collected may introduce variations that affect model performance and generalizability.
* The dataset may not reflect the conditions, equipment, or patient populations encountered in real-world clinical settings.

These limitations will be further investigated during the EDA and experimentation.
