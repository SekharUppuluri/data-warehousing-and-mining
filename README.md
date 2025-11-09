<h1 align="center">📦 DATA WAREHOUSING AND DATA MINING</h1>

<p align="center">
MCA Laboratory Work: Data Preprocessing, ETL, OLAP, Association Rule Mining, Classification, and Clustering implemented using WEKA and Data Warehouse Design Principles.
</p>

---


---

## 🚀 Project Overview

This repository contains the complete practical workflow for the **Data Warehousing and Data Mining (DMDW)** laboratory.  
It demonstrates how raw data is cleaned, transformed, stored in warehouse models, analyzed using OLAP operations, and mined for patterns using classification, clustering, and frequent itemset mining algorithms.

 <!--The work is aligned with **MCA Academic Curriculum** and structured for **exam submission, viva explanation, and portfolio presentation**. -->

---

## 🧠 Skills Demonstrated

- Data Cleaning (handling missing values, duplicates, irrelevant attributes)
- Data Transformation (Normalization, Standardization, Discretization, Encoding)
- Dimensional Modeling (Star & Snowflake Schema Design)
- ETL Pipeline Understanding **(Extract → Transform → Load)**
- OLAP Operations (Roll-Up, Drill-Down, Slice, Dice)
- **[Frequent Pattern Mining](./04-pattern-mining/)** using Apriori Algorithm
- **[classification](./05-classification/)** using Decision Tree (J48) and Naive Bayes
- **[Clustering](./06-clustering-outlier/)** using K-Means and Outlier Detection
- Evaluation & Interpretation of Data Mining Results

---

## 📂 Repository Structure

```plaintext
data-warehousing-and-mining/
│
├─ 01-datasets/                  # Raw and cleaned datasets
│   ├─ raw/
│   └─ processed/
│
├─ 02-preprocessing/             # Data Cleaning & Data Transformation observations
│
├─ 03-datawarehouse-olap/        # Star/Snowflake schema diagrams & OLAP notes
│
├─ 04-pattern-mining/            # Apriori Algorithm & Association Rule results
│
├─ 05-classification/            # Decision Tree / Naive Bayes model outputs
│
├─ 06-clustering-outlier/        # K-Means clustering and outlier detection results
│
└─ 07-screenshots/               # WEKA workflow screenshots for viva documentation
    ├─ cleaning/
    ├─ transformation/
    ├─ apriori/
    ├─ classification/
    └─ clustering/
```

## 🔗 Quick Access

| Folder | Purpose |
|--------|---------|
| **[01 datasets](./01-datasets/)** | Source datasets (raw and processed) |
| **[02 preprocessing](./02-preprocessing/)** | Data cleaning & transformation experiment files |
| **[03 datawarehouse-olap](./03-datawarehouse-olap/)** | Warehouse schema diagrams + OLAP operation notes |
| **[04 pattern-mining](./04-pattern-mining/)** | Apriori results & association rules |
| **[05 classification](./05-classification/)** | Decision Tree / Naive Bayes model evaluation |
| **[06 clustering-outlier](./06-clustering-outlier/)** | K-Means and outlier analysis |
| **[07 screenshots](./07-screenshots/)** | Proof of work for practical record & viva |


---

## 🛠 Tools Used

| Tool / Technology | Usage |
|--------------------|--------|
| **WEKA** | Data preprocessing, mining, modeling & evaluation |
| **VS Code** | Repository editing and documentation |
| **Git & GitHub** | Version control and project portfolio hosting |
<!--| **Draw.io / StarUML** | Data warehouse schema and OLAP modeling diagrams | -->

---

## 📑 How to Use This Repository

1. Begin from folder **[01](./01-datasets/)** and follow folder sequence in ascending order.  
2. Each experiment is documented in **`.md`** (Markdown) format.  
3. Screenshots in **[07-screenshots](./07-screenshots/)** should be referred during viva.  
4. Processed datasets are stored in **[01-datasets/processed](./01-datasets/processed)** for reproducibility.  
5. Models, rules, and clustering results are organized and named clearly.  

---

## 📜 License

This project is licensed under the **[MIT License](./LICENSE)**.  
You are free to use, modify, and distribute this work with attribution.  
See the `LICENSE` file for full terms.

---

## 🌟 Author

**Sekhar Uppuluri**

If this helped you, consider giving the repository a ⭐ on GitHub 🙂


