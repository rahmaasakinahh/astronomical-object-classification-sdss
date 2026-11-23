# **Astronomical Object Classification Based on SDSS Spectral Data**

---

A machine learning project that classifies astronomical objects into **Galaxy, Star, and Quasar (QSO)** using spectral and photometric data from the Sloan Digital Sky Survey (SDSS).

## **Project Overview**

---

This project compares six classification models across five feature-selection scenarios to evaluate how different astronomical features affect classification performance.

## **Dataset**

---

- **Source:** [SDSS DR17 dataset on Hugging Face](https://huggingface.co/datasets/AethronPhantom/Astro)
- **Total records:** 100,000 astronomical objects
- **Target classes:** Galaxy, Star, and QSO
- **Key features:** Redshift, photometric bands (`u`, `g`, `r`, `i`, `z`), and celestial coordinates (`alpha`, `delta`)

## **Methods**

---

- Exploratory Data Analysis (EDA) and feature selection
- Stratified data splitting (60% training, 20% validation, 20% testing)
- Feature scaling using `StandardScaler`
- Class imbalance handling using `SMOTE` on training data only
- Hyperparameter tuning and evaluation across five feature scenarios

**Models evaluated:** Random Forest, K-Nearest Neighbors (KNN), Multilayer Perceptron (MLP), XGBoost, LightGBM, and a Custom Dense Neural Network (DNN)

## **Results**

---

| Model | Best Scenario | Test Accuracy |
|---|---|---:|
| LightGBM | Extensive (8 features) | **97.66%** |
| XGBoost | Extensive (8 features) | **97.66%** |
| Random Forest | Extensive (8 features) | 97.60% |

The extensive feature scenario, combining redshift, photometric measurements, and celestial coordinates, achieved the highest overall performance. Using only spatial coordinates produced substantially lower accuracy.

## **Tech Stack**

---

**Python, Jupyter Notebook, Pandas, NumPy, Scikit-learn, Imbalanced-learn, XGBoost, LightGBM, TensorFlow/Keras, Matplotlib, and Seaborn**

## **How to Run**

---

1. Clone or download this repository.
2. Install the required Python packages:

   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn imbalanced-learn xgboost lightgbm tensorflow notebook
   ```

3. Download the dataset from the source linked above and save it as `star_classification.csv` in the same folder as the notebook.
4. Open `stellar_classification_150_157_180_201_222.ipynb` in Jupyter Notebook and run the cells in order.

## **Notes**

---

- The dataset is not included in the provided project files.
- The notebook includes model training, hyperparameter tuning, performance comparisons, and visualizations. Running the complete experiments may require substantial computing resources.
- The project report is included as a PDF in the repository.
