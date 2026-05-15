# PCA-Bioinformatics

Principal Component Analysis (PCA) for breast cancer gene-expression analysis using real biological datasets.

---

## Project Overview

This project performs Principal Component Analysis (PCA) on breast cancer gene-expression data from the GEO dataset **GSE5325**.

The analysis reproduces concepts from Figure 1 of the referenced breast cancer study by analyzing the expression patterns of:

- GATA3
- XBP1

The project demonstrates how dimensionality reduction can be used to visualize biological patterns and classify cancer subtypes.

---

## Biological Background

Breast cancer samples are commonly categorized into:

- **ER+ (Estrogen Receptor Positive)**
- **ER− (Estrogen Receptor Negative)**

Gene-expression biomarkers such as **GATA3** and **XBP1** help differentiate these cancer subtypes.

Using PCA, high-dimensional biological data can be projected into lower dimensions while preserving important variance patterns.

---

## Dataset

### GEO Accession
GSE5325

### Files Used

| File | Description |
|---|---|
| `class.tsv` | Patient class labels (ER+ / ER−) |
| `filtered.tsv.gz` | Gene-expression matrix |
| `columns.tsv.gz` | Gene ID to gene-name mapping |

---

## Objectives

- Extract expression levels of:
  - GATA3
  - XBP1
- Generate scatter plot of gene expression
- Apply PCA to the expression matrix
- Visualize projection on Principal Component 1 (PC1)

---

## Workflow

### 1. Data Loading
Gene-expression datasets and class labels were loaded using Pandas.

### 2. Gene Extraction
Expression values for:
- GATA3
- XBP1

were extracted for all patient samples.

### 3. Visualization
Scatter plots were generated to observe separation between ER+ and ER− breast cancer samples.

### 4. Data Standardization
Data was standardized using `StandardScaler` before PCA.

### 5. Principal Component Analysis
PCA was performed using Scikit-learn to project data onto PC1.

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Jupyter Notebook
- Git & GitHub

---

## Repository Structure

```text
PCA-Bioinformatics/
│
├── data/
│   ├── class.tsv
│   ├── filtered.tsv.gz
│   └── columns.tsv.gz
│
├── notebooks/
│   └── breast_cancer_pca.ipynb
│
├── figures/
│   ├── figure1a.png
│   └── figure1c.png
│
├── results/
├── src/
├── requirements.txt
└── README.md
```

---

## Figures

### Figure 1a
Scatter plot of:
- GATA3 expression
- XBP1 expression

colored by breast cancer subtype.

### Figure 1c
Projection of samples onto:
- Principal Component 1 (PC1)

after PCA transformation.

---

## Results

The PCA projection demonstrates partial separation between ER+ and ER− breast cancer samples based on gene-expression profiles.

The analysis highlights the importance of dimensionality reduction in biological data interpretation.

---

## Future Improvements

- PCA using complete gene-expression matrix
- t-SNE visualization
- Clustering analysis
- Machine learning classification
- Cancer subtype prediction
- Interactive visualization dashboards

---

## Running the Project

### Clone repository

```bash
git clone https://github.com/YOUR_USERNAME/PCA-Bioinformatics.git
```

### Move into repository

```bash
cd PCA-Bioinformatics
```

### Create environment

```bash
conda create -n pca_project python=3.11
```

### Activate environment

```bash
conda activate pca_project
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
notebooks/breast_cancer_pca.ipynb
```

Run all notebook cells sequentially.

---

## Author

Monika

---

## License

This project is intended for academic and educational purposes.
