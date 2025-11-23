# Experiment 1: Data Cleaning Using WEKA

## Title
Implementing Data Cleaning Techniques on a Dataset using WEKA

## Objective
My objective in this experiment was to clean a dataset by identifying and resolving missing values, checking for duplicate records, optionally applying normalization, removing irrelevant attributes, and performing basic attribute conversion using WEKA.

## Software Used
-  WEKA (Waikato Environment for Knowledge Analysis) – Version 3.9.6
- Operating System: Windows 11
- Dataset Used: `weather.nominal.arff` (WEKA sample dataset)

---

## Theory (In My Words)

Before any data mining or machine learning can be done, the dataset needs to be cleaned.  
Real-world data often has problems like missing values, duplicated rows, or attributes that are not useful.  
Cleaning the data helps improve the accuracy of models and makes data more consistent.

During data cleaning, we mainly focus on:
- **Replacing Missing Values**
- **Removing Duplicate Entries**
- **Normalizing Data (only if numeric values exist)**
- **Removing Irrelevant Attributes**
- **Converting or Encoding Attributes when needed**

WEKA provides filters to carry out these tasks easily.

---

## Procedure (Steps I Performed)

### 1) Loading Dataset
- I opened WEKA → Explorer → Preprocess and loaded the dataset: **weather.nominal.arff**


### 2) Introducing Missing Values (for demonstration)
- I opened the **Edit** panel and manually removed some values so that they became `?` (missing).
- This allowed me to demonstrate how WEKA handles missing data.

📸 *Screenshot 1: dataset_with_missing.png*

![Dataset with Missing Values](/07-screenshots/cleaning/dataset_with_missing.png)

---

### 3) Replacing Missing Values
- I used the filter:
Filter → unsupervised → attribute → ReplaceMissingValues

- This filled the missing nominal values by using the **mode** (most frequent value).  
- After applying it, the missing value count became **zero**.

📸 *Screenshot 2: missing_replaced.png*

![Replaced Missing Values](/07-screenshots/cleaning/missing_replaced.png)

---

### 4) Removing Duplicate Records
- I applied the filter:
Filter → unsupervised → instance → RemoveDuplicates
- There were no duplicate rows in this dataset, so the total number of instances remained the same.

📸 *Screenshot 3: duplicates_removed.png*

![Removed Duplicate Values](/07-screenshots/cleaning/duplicates_removed.png)

---

### 5) Normalizing Data (Optional Step)
- I also applied:
Filter → unsupervised → attribute → Normalize
- However, since this dataset contains **only nominal attributes**, normalization **did not change the values**.  
- I still included this step to show awareness of when normalization applies.

📸 *Screenshot 4: normalized.png*

![Normalized Values](/07-screenshots/cleaning/normalize.png)

---

### 6) Removing an Irrelevant Attribute
- Next, I removed an attribute using:
- Filter → unsupervised → attribute → Remove
- I specified the attribute index to remove.  
- This helped reduce unnecessary features in the dataset.

📸 *Screenshot 5: attribute_removed.png*

![Remove Attributes](/07-screenshots/cleaning/filter_attribute_indices.png) 
![Remove Attributes](/07-screenshots/cleaning/attribute_removed.png)

---

### 7) Converting Nominal Attributes to Binary (Attribute Encoding)
- Finally, I applied:
Filter → unsupervised → attribute → NominalToBinary
- This converted categorical values into binary (0/1) format, which is helpful for algorithms that require numeric input.

📸 *Screenshot 6: nominal_to_binary.png*

![Nominal To Binary Values](/07-screenshots/cleaning/nominal_to_binary_[without_remove_attributes].png)
![Nominal To Binary Values](/07-screenshots/cleaning/nominal_to_binary_edit[without_remove_attributes].png)

---

### 8) Saving the Cleaned Dataset
- I saved the final cleaned dataset as:
**cleaned_weather_final.arff**

---

## Observation (My Understanding)

While performing this experiment, I observed that **WEKA 3.9.6** automatically handles missing nominal values using mode. The dataset did not contain duplicate instances, so removing duplicates did not affect the instance count. Normalization had no effect since all attributes were nominal. I also learned how removing attributes can simplify the dataset and how nominal values can be converted into binary form to make the data suitable for machine learning models.

---

## Result

The dataset was successfully cleaned and prepared for further data processing and data mining tasks.  
Missing values were handled, duplicate checks were done, unnecessary attributes were removed, and nominal attributes were encoded properly.

---
<!--
## Viva Notes (What I Will Say If Asked)

| Question | My Answer |
|---------|-----------|
| Why did normalization not change values? | Because the dataset contains only nominal (categorical) values. Normalization affects only numeric data. |
| How were missing nominal values replaced? | WEKA replaced them using the **mode**, which is the most frequent category. |
| Why convert nominal to binary? | To make categorical data usable in algorithms that require numeric input. |

-->
