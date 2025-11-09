# Experiment 1: Data Cleaning Using WEKA

## Title
Implementing Data Cleaning Techniques on a Dataset using WEKA

## Objective
My objective in this experiment was to clean a dataset by identifying and resolving missing values, checking for duplicate records, optionally applying normalization, removing irrelevant attributes, and performing basic attribute conversion using WEKA.

## Software Used
- WEKA 3.9.6
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
I opened WEKA → Explorer → Preprocess and loaded the dataset: **weather.nominal.arff**


### 2) Introducing Missing Values (for demonstration)
I opened the **Edit** panel and manually removed some values so that they became `?` (missing).  
This allowed me to demonstrate how WEKA handles missing data.

📸 *Screenshot 1: dataset_with_missing.png*

![Dataset with Missing Values](/07-screenshots/cleaning/dataset_with_missing.png)



