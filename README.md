# Predicting Football Players' Positions Based on Player Attributes

## Overview
This repository contains the code, datasets, and documentation for the project **"Predicting Football Players' Positions Based on Player Attributes"**. The project explores how machine learning can classify football (soccer) players' primary on-field positions (e.g., striker, midfielder, defender) based on their physical and technical attributes.

The repository is structured to support both the original dataset (~19,000 instances) and the expanded dataset (~28,000 instances). The expanded dataset includes additional player statistics from an older dataset (FC21) to enhance data variability and model generalization.

---

## Repository Structure
```plaintext
.
├── README.md                       # Project overview and instructions
├── new_dataset_and_training_script
│   ├── expanded_all_players.csv    # Expanded dataset (~28k instances)
│   └── expanded-players-model-training.ipynb  # Training script for the expanded dataset
├── old_dataset_and_training_script
│   ├── all_players.csv             # Original dataset (~19k instances)
│   └── original-players-model-training.ipynb  # Training script for the original dataset
└── main.ipynb                      # Central notebook to reproduce the project workflow
```

---

## Datasets
- **Original Dataset:** `old_dataset_and_training_script/all_players.csv`
  - Contains ~19,000 player statistics.
  - Includes male and female players with attributes like Pace, Shooting, Passing, and Physicality.
  - Target variable: "Position" (12 unique classes).

- **Expanded Dataset:** `new_dataset_and_training_script/expanded_all_players.csv`
  - Combines the original dataset with player statistics from an older version (FC21).
  - Includes ~28,000 instances, increasing data diversity and historical variability.

---

## Main Notebook
The central notebook, `main.ipynb`, walks through the full project workflow, including:
1. **Data Overview:** Exploring datasets, attributes, and distribution of the target variable.
2. **Preprocessing:** Handling missing values, one-hot encoding, and scaling.
3. **Model Training & Evaluation:**
   - Logistic Regression
   - Random Forest
   - XGBoost
4. **Analysis of Results:**
   - Comparing models across the original and expanded datasets.
   - Evaluating the impact of PCA and SMOTE on model performance.
5. **Reproducibility:** Instructions for rerunning experiments using the training scripts.

---

## How to Reproduce the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo-url
   cd your-repo-folder
   ```
2. Open the `main.ipynb` notebook in Jupyter Notebook or JupyterLab.
3. Follow the workflow to explore datasets, preprocess data, and train models.
4. For dataset-specific training:
   - Use `old_dataset_and_training_script/original-players-model-training.ipynb` for the original dataset.
   - Use `new_dataset_and_training_script/expanded-players-model-training.ipynb` for the expanded dataset.

---

## Results Summary
- **Original Dataset (~19k Instances):**
  - Best Accuracy: ~79% (Logistic Regression, No PCA, No SMOTE)
  - PCA and SMOTE showed limited to no improvement.

- **Expanded Dataset (~28k Instances):**
  - Best Accuracy: ~87.3% (XGBoost with SMOTE)
  - Larger and more diverse data allowed XGBoost and Random Forest to outperform Logistic Regression.

Key insights and comparisons are detailed in the [Final Report](#).

---

## References
- Lucey, P., et al. (2014). *Quality vs Quantity: Improved shot prediction in soccer using strategic features from spatiotemporal data*.
- Pappalardo, L., et al. (2019). *PlayeRank: Data-driven performance evaluation and player ranking in soccer*.
- Rico-González, M., et al. (2023). *Machine learning application in soccer: A systematic review*.

---

## Author
**Joshua Zhang**

This project was completed as part of the IS597MLC course at the University of Illinois Urbana Champaign.
