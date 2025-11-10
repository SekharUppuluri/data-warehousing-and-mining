# Experiment 2: Data Transformation Techniques Using WEKA

## Title:
**Apply Data Transformation Techniques on a Given Dataset Using WEKA**

## Objective:
The objective of this experiment is to apply various data transformation techniques—such as normalization, standardization, discretization, and attribute encoding—on a dataset using WEKA, and to understand their impact on data distribution and analysis.

## Software and Tools Required:
- **Software**: WEKA (Waikato Environment for Knowledge Analysis) – Version 3.9.6
- **Platform**: Windows 
- **Dataset**: 
  - **iris.arff** (available in WEKA’s sample data folder)
---

## Theory (In My Words)

Data transformation in data mining is the process of converting raw data into a suitable format for analysis. Techniques like normalization, aggregation, and generalization are applied to ensure that the data is structured, consistent, and ready for mining algorithms. This preprocessing step improves data quality and accuracy, ultimately enhancing the performance of data mining tasks.

### Types of Data Transformation:
| **Transformation Type**      | **Description**                                                 | **WEKA Filter**                       |
|------------------------------|-----------------------------------------------------------------|---------------------------------------|
| **Normalization**             | Scales numeric attributes into a specific range (typically [0, 1]). | `unsupervised → attribute → Normalize` |
| **Standardization (Z-score)** | Transforms attributes to have mean = 0 and standard deviation = 1. | `unsupervised → attribute → Standardize` |
| **Discretization**            | Converts continuous attributes into nominal (categorical) intervals. | `unsupervised → attribute → Discretize` |
| **Nominal to Binary Conversion** | Converts categorical attributes into multiple binary attributes. | `unsupervised → attribute → NominalToBinary` |
| **Numeric to Nominal**        | Converts numeric attributes into nominal types.                | `unsupervised → attribute → NumericToNominal` |
| **Principal Components**      | Reduces dimensionality by projecting data onto principal components. | `unsupervised → attribute → PrincipalComponents` |

---


## Procedure (Steps I Performed)

### Step 1: Start WEKA
- Launch WEKA GUI Chooser → Click **Explorer**.

### Step 2: Load Dataset
- In the **Preprocess** tab, click **Open file** → Choose **iris.arff** (or your dataset).
- View attributes and check their types (numeric or nominal).

📸 *Screenshot 0: loaded.png*

![Iris Dataset Loaded](/07-screenshots/transformation/iris_dataset_loaded.png)
