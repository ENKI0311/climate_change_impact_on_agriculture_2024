
---

# Climate Change Impact on Agriculture 2024

## Overview
This project analyzes the influence of climate change on global agricultural output using a dataset containing environmental, economic, and agricultural factors. By applying data analysis and predictive modeling, the project quantifies how variables such as temperature, precipitation, CO2 emissions, and extreme weather events impact crop yields across different regions and countries.

---

## Workflow and Methodology

### 1. **Data Exploration and Preprocessing**
- Loaded and cleaned the dataset, which includes variables such as:
  - `Year`, `Country`, `Region`
  - `Average_Temperature_C`, `Total_Precipitation_mm`
  - `CO2_Emissions_MT`, `Crop_Yield_MT_per_HA`
- Conducted **Exploratory Data Analysis (EDA)** to examine distributions, correlations, and trends across regions and crop types.
- Addressed data quality issues:
  - **Outlier Handling**: Imputed outliers in `Total_Precipitation_mm`, `CO2_Emissions_MT`, and `Crop_Yield_MT_per_HA`.
  - **Normalization**: Transformed skewed data (e.g., log transformations) to improve model input.

### 2. **Feature Engineering**
- Created dummy variables for categorical features like:
  - `Country`, `Region`, `Crop_Type`, `Adaptation_Strategies`
- Applied one-hot encoding for non-numeric fields.
- Engineered new features to improve predictions, such as interaction terms and environmental indices.

### 3. **Model Development**
- Implemented various machine learning and deep learning models, including:
  - **Random Forest**: For feature importance and baseline predictions.
  - **XGBoost**: For boosted ensemble learning.
  - **PyTorch and fastai**: For custom deep learning architectures.
- Fine-tuned model hyperparameters:
  - Included **dropout**, **weight decay**, and **learning rate adjustments**.
  - Optimized feature selection by excluding less impactful features like `Country`.
- Achieved a final **R² score of 0.55**, demonstrating the model's capability to explain the variance in crop yield.

### 4. **Evaluation**
- Validated the models using:
  - **R² Score**: To assess the model's explanatory power.
  - **Mean Squared Error (MSE)**: To evaluate prediction accuracy.
- Explored the impact of different features on model performance, particularly variables like `Country` and `Region`.

---

## Tools and Technologies
- **Python**: Core language for data manipulation and modeling.
- **PyTorch & fastai**: Deep learning frameworks for model implementation and optimization.
- **scikit-learn**: Used for classical machine learning models and EDA.
- **Matplotlib & Seaborn**: For visualizations and trend analysis.

---

## Results
- Achieved reasonable predictive accuracy with an **R² score of 0.55**.
- Highlighted key insights:
  - Climate variables like CO2 emissions, temperature, and precipitation significantly affect crop yield.
  - Regional variability in the impact of climate factors on agriculture.

---

## Future Work
1. **Model Improvements**:
   - Incorporate advanced architectures such as **LSTMs** or **Transformer models** for time-series analysis.
   - Explore ensemble methods for combining the strengths of different models.
2. **External Data Enrichment**:
   - Integrate additional datasets for improved feature diversity (e.g., soil quality, irrigation patterns).
3. **Scenario Analysis**:
   - Model the impact of different climate change scenarios on crop yields.
4. **Policy Implications**:
   - Provide actionable insights for governments and organizations to mitigate agricultural risks.

---

## Installation and Usage

### Clone the Repository
```bash
git clone <repository_url>
cd climate_change_impact_on_agriculture_2024
```

### Install Dependencies
```bash
pip install -r requirements.txt
```

### Run the Project
1. Preprocess the data:
   ```bash
   python preprocess.py
   ```
2. Train the model:
   ```bash
   python train.py
   ```
3. Evaluate the model:
   ```bash
   python evaluate.py
   ```

---

## Project Structure
```
climate_change_impact_on_agriculture_2024/
├── data/                   # Raw and preprocessed datasets
├── notebooks/              # Jupyter notebooks for EDA and modeling
├── models/                 # Saved model checkpoints
├── scripts/                # Preprocessing, training, and evaluation scripts
├── results/                # Visualizations and evaluation outputs
├── requirements.txt        # List of dependencies
└── README.md               # Project documentation
```

---

## Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m "Add feature-name"`).
4. Push to your branch (`git push origin feature-name`).
5. Submit a pull request.

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

