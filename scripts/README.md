# Analysis and Visualization Scripts

This directory contains the computational pipeline used for feature engineering, classification, and statistical evaluation.

## 1. Google Earth Engine Implementation (`analysis_gee.js`)
* **Feature Engineering:** Automated extraction of an 82-band hypercube (Spectral percentiles, GLCM Texture, and Topographic indices).
* **Training Logic:** Multi-source consensus logic utilizing ESA WorldCover and Dynamic World.
* **Classifier Execution:** Native implementation of RF, GBM, CART, MD, and SVM.

## 2. Python Visualizations (`Visualizations_SUAM.ipynb`)
This Jupyter Notebook performs post-classification analysis using `Matplotlib`, `Seaborn`, and `Pandas`. 

### Required Libraries
To run the notebook locally, install the following dependencies:
```bash
pip install matplotlib seaborn numpy pandas
