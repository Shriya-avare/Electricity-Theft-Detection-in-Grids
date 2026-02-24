# Electricity Theft Detection in Smart Grids

Detects electricity theft using real smart grid consumption data and machine learning.

## Dataset
- **Source:** State Grid Corporation of China
- **Size:** 42,372 electricity consumers
- **Duration:** 1,035 days (Jan 2014 – Oct 2016)
- **Labels:** FLAG = 0 (normal), FLAG = 1 (theft)
- **Download:** [henryRDlab/ElectricityTheftDetection](https://github.com/henryRDlab/ElectricityTheftDetection)

## How It Works
1. **Data Preprocessing** – Missing values filled by interpolating between neighboring days
2. **Feature Extraction** – Daily consumption values used as features
3. **Clustering** – KMeans (10 clusters) groups consumers by usage patterns
4. **Classification** – ExtraTreesClassifier detects theft vs normal usage
5. **Class Balancing** – SMOTE oversampling handles imbalanced classes
6. **Evaluation** – Accuracy score and F1 score

## Results
- Model: ExtraTreesClassifier
- Evaluation metrics: Accuracy + F1 Score
- Theft patterns show lower, irregular consumption compared to normal users

## Libraries Used
- Python, Pandas, NumPy
- Scikit-learn (KMeans, ExtraTreesClassifier, train_test_split)
- Imbalanced-learn (SMOTE)
- Matplotlib

## How to Run
1. Download dataset from [here](https://github.com/henryRDlab/ElectricityTheftDetection) (download all 3 zip files and extract together)
2. Place `data.csv` in the same folder as the notebook
3. Install dependencies:
```
pip install pandas numpy scikit-learn imbalanced-learn matplotlib
```
4. Open `theftdetection_fixed.ipynb` in Jupyter Notebook
5. Run All Cells
