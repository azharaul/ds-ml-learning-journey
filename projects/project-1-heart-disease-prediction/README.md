# Heart Disease Prediction - End-to-End ML Project

A comprehensive machine learning project that predicts the presence of heart disease using various classification algorithms and techniques.

## 📋 Project Overview

This project demonstrates a complete end-to-end machine learning workflow for binary classification, predicting whether a patient has heart disease based on medical attributes. The project includes data exploration, preprocessing, model training, evaluation, and optimization.

## 🎯 Objective

The main goal is to build a predictive model that can accurately classify patients as having heart disease or not, using clinical and demographic features. This involves:

- Exploratory Data Analysis (EDA)
- Data preprocessing and feature engineering
- Training multiple classification models
- Model evaluation and comparison
- Hyperparameter tuning for optimal performance

## 📊 Dataset

- **Source**: `data/heart-disease.csv`
- **Records**: Multiple patient records with medical attributes
- **Features**: Various clinical measurements and demographic information
- **Target**: Binary classification (presence/absence of heart disease)

**Key Features**:

- Age, sex, chest pain type
- Resting blood pressure, cholesterol levels
- Maximum heart rate, exercise-induced angina
- ST depression, vessel count, thalassemia type
- And more clinical indicators

## 📁 Project Structure

```
project-1-heart-disease-prediction/
├── README.md                                    # Project documentation
├── data/
│   └── heart-disease.csv                       # Dataset
├── models/                                      # Trained models storage
└── notebooks/
    └── end-to-end-heart-disease-classification.ipynb  # Main analysis notebook
```

## 🚀 Getting Started

### Prerequisites

- Python 3.7+
- Jupyter Notebook
- Required packages (see requirements.txt in root directory)

### Installation

1. Clone or download the repository
2. Navigate to the project directory
3. Install dependencies:

    ```bash
    pip install -r ../../requirements.txt
    ```

4. Open the Jupyter notebook:
    ```bash
    jupyter notebook notebooks/end-to-end-heart-disease-classification.ipynb
    ```

## 📖 Usage

The main analysis is contained in the Jupyter notebook. Follow these steps:

1. **Data Loading**: Load and explore the heart disease dataset
2. **EDA**: Visualize data distributions and relationships
3. **Preprocessing**: Handle missing values, encode categorical variables, scale features
4. **Model Training**: Train multiple classification models:
    - Logistic Regression
    - Decision Tree
    - Random Forest
    - K-Nearest Neighbors
    - Support Vector Machine
    - And others...
5. **Model Evaluation**: Compare models using metrics like:
    - Accuracy
    - Precision, Recall, F1-Score
    - ROC-AUC
    - Confusion Matrix
6. **Hyperparameter Tuning**: Optimize the best-performing model
7. **Final Prediction**: Make predictions on new data

## 🔧 Technologies & Libraries

- **Python 3**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **Scikit-Learn**: Machine learning algorithms and tools
- **Matplotlib & Seaborn**: Data visualization
- **Jupyter**: Interactive notebook environment

## 📈 Results

The project trains and compares multiple classification models. The best model is selected based on:

- Cross-validation scores
- Test set performance
- Generalization capability

Model performance metrics and visualizations are included in the notebook.

## 💾 Saved Models

Trained models are saved in the `models/` directory for reuse and deployment purposes.

## 🎓 Learning Objectives

This project covers:

- Complete ML pipeline implementation
- Classification problem-solving
- Feature engineering and preprocessing
- Model selection and comparison
- Hyperparameter optimization
- Best practices in machine learning

## 📝 Notes

- The dataset is normalized to ensure fair model comparison
- Cross-validation is used to assess model generalization
- Various evaluation metrics are considered, not just accuracy
- The notebook includes detailed explanations and visualizations

## 🔗 Related Resources

This project is part of the DS-ML Learning Journey repository:

- Check `01-numpy-pandas/` for data manipulation tutorials
- See `02-data-preprocessing/` for preprocessing techniques
- Visit `03-machine-learning-basic/` for ML fundamentals
- Review `04-model-evaluation/` for evaluation methods
- Explore `05-hyperparameter-tuning/` for optimization techniques

## ✨ Author

Created as part of the Machine Learning learning journey.

---

**Happy Learning! 🚀**
