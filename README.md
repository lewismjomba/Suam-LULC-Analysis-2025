# Suam LULC Analysis 2025: Comparative Machine Learning Performance

## 1. Project Overview
This repository contains the data and software used for a comparative Land Use/Land Cover (LULC) analysis in the Suam region (Mt. Elgon, Kenya/Uganda). The study utilizes a high-dimensional feature stack (82 bands) derived from **Landsat 9** and compares five machine learning classifiers: 
* Random Forest (RF)
* Gradient Boosting Machines (GBM)
* Classification and Regression Trees (CART)
* Minimum Distance (MD)
* Support Vector Machines (SVM)

## 2. Repository Structure
* **`/scripts`**:
    * `analysis_gee.js`: Google Earth Engine (GEE) JavaScript code for feature extraction and model training.
    * `visualizations.ipynb`: Jupyter Notebook for reproducing accuracy assessment figures.
* **`/data`**:
    * `training_points.csv`: 2,063 stratified training samples used for validation.

---

## 3. How to Reproduce the Results

### Step 1: Satellite Image Processing (GEE) - Use either step 1 or 2.
1. Copy the contents of `scripts/analysis_gee.js` and paste it into the [Google Earth Engine Code Editor](https://code.earthengine.google.com/).
2. A static snapshot of the script is available here: [https://code.earthengine.google.com/9cd46be3da82dc9030a23ac2e354f5ab]

### Step 2: Accuracy Visualizations (Python)
Open `scripts/visualizations.ipynb` in a Jupyter environment (VS Code, JupyterLab, or Google Colab) to generate the following:

#### Figure 3: Comparative Normalized Confusion Matrices
Diagonal elements represent the proportion of correctly classified pixels for each LULC class, illustrating class-specific omission errors across all five classifiers.

![Figure 3](scripts/Figure3_Confusion_Matrices.png)


#### Figure 4: Disagreement Analysis
Breakdown of Total Disagreement (TD) into Quantity Disagreement (QD) and Allocation Disagreement (AD), alongside the Map Agreement Index (MAI).

![Figure 4](scripts/Figure4_Disagreement.png)


#### Figure 5: McNemar’s Test
Statistical significance of performance differences between the reference classifier (RF) and the challengers.

![Figure 5](scripts/Figure5_McNemar.png)


---

## 4. Citation
If you utilize this code or data, please cite:
> *[paper's full citation will be provided here once published]*

## 5. License
This project is licensed under the **MIT License**.
