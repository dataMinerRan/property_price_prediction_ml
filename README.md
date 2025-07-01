# Beating the Assessors: Machine Learning Models for Property Sale Price Prediction

This project develops and evaluates machine learning models to improve the accuracy of property sale price predictions, with the goal of outperforming the existing models used by the Cook County Assessor’s Office (CCAO). The aim is to support fairer property tax assessments by reducing both the overall prediction error and the spread of estimated property values. In doing so, the project seeks to minimize both over-assessment, which leads to over-taxation, and under-assessment, which reduces critical public funding.

## 📌 Problem Statement

This project continues work on the Cook County Assessor’s Office (CCAO) property dataset with the goal of building machine learning models that can more accurately predict property sale values. These predictions support the CCAO’s responsibility to assess properties annually for taxation purposes — despite actual sale prices only becoming known when a property is sold.

Because over-assessment can lead to unfair tax burdens and under-assessment can reduce critical public funding, accurate and consistent valuations are essential. In particular, overestimation is considered more harmful and thus should be more heavily penalized. This makes model fairness and precision critical to the success of any assessment methodology.

The objective of this project is to develop regression models that outperform the CCAO’s current valuation approach using the available property features. Since the target variable — sale price — is continuous, this is approached as a regression problem. A variety of models are trained, tuned, and evaluated to identify the most effective one.

Evaluation metrics include standard regression measures such as:
	•	Mean Absolute Percentage Error (MAPE)
	•	R-squared (R²)

But the project also emphasizes a domain-specific metric used by assessors:
	•	Coefficient of Dispersion (COD) — which measures the uniformity of property assessments. A lower COD indicates more consistent and fair valuation. A COD under 15% is considered acceptable, with the goal being to achieve the lowest possible COD.

To ensure fair comparison, all data preprocessing steps applied to the machine learning models are also applied to the CCAO’s assessment data. The full data science pipeline — including EDA, data cleaning, feature engineering, model training, and evaluation — is used to support this analysis.

## 🧪 Approach

The notebook walks through a complete end-to-end data science pipeline, starting from data understanding to performance benchmarking against CCAO’s assessment:
	•	Exploratory Data Analysis (EDA)
	•	Feature engineering and data cleaning
	•	Model training using:
	•	Linear Regression
	•	Ridge Regression
  •	SVM Regressor 
	•	Random Forest
	•	XGBoost
	•	Hyperparameter tuning
	•	Performance evaluation and comparison with CCAO’s results

Each model is evaluated using standard regression metrics and the domain-specific Coefficient of Dispersion (COD), allowing for direct comparison with the CCAO’s valuation accuracy.

## 📁 Repository Structure

```
property_price_prediction_ml/
├── notebooks/
│   └── property_price_prediction_ml.ipynb            # Updated notebook name
├── results/                                          # Plots, model outputs, and comparison tables
├── requirements.txt                                  # Python package dependencies
├── .gitignore                                        # Ignore unnecessary files
├── README.md                                         # Project overview and instructions
└── LICENSE                                           # MIT License file
```

## 🚀 How to Run

1. Clone the repository:
```bash
git clone https://github.com/your-username/property_price_prediction_ml.git
cd property_price_prediction_ml
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Launch the notebook:
```bash
jupyter notebook notebooks/property_price_prediction_ml.ipynb
```

## 📊 Evaluation Metrics

- **R² Score**
- **Mean Absolute Percentage Error (MAPE)**
- **Mean Absolute Error (MAE)**
- **Coefficient of Dispersion (COD)**

The model with the lowest COD and competitive performance across other metrics is selected as the final model.

## 📈 Results Summary

- Random Forest and XGBoost outperformed CCAO's baseline.
- COD reduced significantly below the 15% benchmark.
- Feature importance insights aligned with domain expectations.

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 👤 Author

**Ran Huo**  
© 2025

