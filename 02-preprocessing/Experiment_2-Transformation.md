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

---
### Step 3: Apply Normalization
- Go to **Filter → unsupervised → attribute → Normalize**.
- Click **Apply**.
- Observe that numeric attributes are now scaled between **0** and **1**.
- **Purpose**: Useful when attributes have different units (e.g., cm, kg).

📸 *Screenshot 1: normalization.png*

![Iris Normalized](/07-screenshots/transformation/normalized_iris.png)

---

### Step 4: Apply Standardization (Z-score)
- **Reset or reload** the dataset.
- Choose filter: **unsupervised → attribute → Standardize** → **Apply**.
- Values are now centered around **mean 0** with **standard deviation 1**.
- **Purpose**: Improves performance of distance-based algorithms like **KNN** or **SVM**.

📸 *Screenshot 2: standardization.png*

![Iris standardized](/07-screenshots/transformation/standardized_iris.png)

---
### Step 5: Discretize Attributes
- Reload the dataset.
- Choose **unsupervised → attribute → Discretize**.
- Click the filter name to open settings → choose the number of bins (e.g., **4**).
- Click **Apply**.
- Numeric attributes are now converted into categorical ranges (e.g., PetalLength → “low”, “medium”, “high”, “very high”).

📸 *Screenshot 3: discretized.png*

![Iris Discretized](/07-screenshots/transformation/discretized_iris.png)

---

### Step 6: Apply Nominal to Binary Conversion
- Choose **unsupervised → attribute → NominalToBinary** to convert categorical values into binary attributes.

📸 *Screenshot 4: nominal_to_binary.png*

![Iris Nominal To Binary](/07-screenshots/transformation/nominal_to_binary_iris.png[panel].png)

![Iris Nominal To Binary](/07-screenshots/transformation/nominal_to_binary_iris.png[edit].png)

### Step 7: Save the Transformed Data
- After applying transformations, click **Save** → name the file as **transformed_iris.arff** or **transformed_dataset.csv**.

<!-- 📸 *Screenshot 5: saved_transformed.png* -->

---

## Sample Example: Transformation Results

Here’s how the data looks before and after transformations:

| **Attribute**   | **Original Range** | **After Normalization (0–1)** | **After Standardization (Z-score)** |
|-----------------|--------------------|-------------------------------|-------------------------------------|
| **SepalLength** | 4.3 – 7.9          | 0.00 – 1.00                   | -1.87 – 1.96                       |
| **SepalWidth**  | 2.0 – 4.4          | 0.00 – 1.00                   | -2.43 – 2.48                       |
| **PetalLength** | 1.0 – 6.9          | 0.00 – 1.00                   | -1.56 – 1.74                       |
| **PetalWidth**  | 0.1 – 2.5          | 0.00 – 1.00                   | -1.45 – 1.63                       |

