# climate_change_impact_on_agriculture_2024
Analyzing climate change impact on global agriculture using predictive models.

---

### Project Overview:
This project explores the influence of climate change on global agricultural output by leveraging a dataset containing environmental, economic, and agricultural factors. Through data analysis and predictive modeling, we aim to quantify how variables such as temperature, precipitation, CO2 emissions, extreme weather events, and agricultural practices affect crop yield across different regions and countries.

### Key Steps and Workflow:
1. **Data Exploration & Preprocessing**:
   - Loaded and cleaned the dataset, which includes variables like `Year`, `Country`, `Region`, `Average_Temperature_C`, `Total_Precipitation_mm`, `CO2_Emissions_MT`, and `Crop_Yield_MT_per_HA`.
   - Conducted exploratory data analysis (EDA) to understand distribution, correlations, and trends across different regions and crop types.
   - Imputed outliers in various columns such as `Total_Precipitation_mm`, `CO2_Emissions_MT`, and `Crop_Yield_MT_per_HA` to handle skewed data.

2. **Feature Engineering**:
   - Created dummy variables for categorical features (`Country`, `Region`, `Crop_Type`, `Adaptation_Strategies`) using one-hot encoding.
   - Applied transformations to manage left-skewed data where necessary, including log transformation for certain columns.

3. **Model Development**:
   - Implemented several machine learning and deep learning models, including Random Forest, XGBoost, and deep learning models in PyTorch and fastai.
   - Trained and fine-tuned the models to predict `Crop_Yield_MT_per_HA` based on environmental factors.
   - Performed hyperparameter tuning, including the use of dropout, weight decay, and learning rate adjustments to improve model performance.
   - Achieved an R² score of approximately 0.55 after removing and refining features like `Country`.

4. **Evaluation**:
   - Validated the models using standard metrics such as **R² score** and **Mean Squared Error (MSE)**.
   - Analyzed the impact of feature selection, particularly the inclusion or exclusion of variables like `Country`, on model performance.

### Tools & Technologies:
- **Python**: For data manipulation, preprocessing, and analysis.
- **PyTorch**: Implemented deep learning models.
- **fastai**: Simplified model training and provided high-level optimizations.
- **scikit-learn**: Used for exploratory data analysis and classical machine learning models.
- **Matplotlib/Seaborn**: For visualizations and plotting results.

### Results:
- Achieved reasonable predictive accuracy with an R² score of 0.55.
- Developed insights into the effects of climate change factors like CO2 emissions, temperature, and extreme weather on crop yields.

### Future Work:
- Further fine-tuning the model with more advanced feature engineering techniques and cross-validation.
- Exploring more sophisticated architectures such as LSTMs or ensemble learning to improve predictions.
- Investigating additional external datasets to enrich the analysis and account for other potential factors.

--- 
