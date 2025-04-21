
#### **Table of Contents**
1. **Introduction**
2. **Data Description**
3. **Data Analysis**
4. **Visualizations**
5. **Conclusion**
6. **References**
---

### **1. Introduction**

Kyrgyzstan, a Central Asian country, has experienced significant urbanization and economic development in recent years. The real estate market in its capital, Bishkek, reflects these changes, with varying property prices influenced by factors such as location, size, and building type. This project aims to analyze a dataset of real estate listings to uncover key trends and predictors of property prices. The dataset was chosen for its relevance to understanding the dynamics of Kyrgyzstan's housing market and its potential to inform buyers, sellers, and policymakers.

---

### **2. Data Description**

The dataset used in this analysis contains real estate listings from Bishkek, Kyrgyzstan. It includes the following variables:

- **Price (`price`)**: The listing price of the property.
- **Area (`square`)**: The size of the property in square meters.
- **Price per square meter (`m2_price`)**: Calculated as `price / square`.
- **Number of Rooms (`rooms`)**: The number of rooms in the property.
- **District(`district`)**: The administrative district where the property is located.
- **Micro District (`micro_district`)**: 
- **Building Age (`building_age`)**: The age of the building in years.
- **Building Type (`building_type`)**: The construction material (e.g., brick, panel, monolithic).
- **Floor (`floor`)**: The floor number of the property.
- **Floors (`floors`)**: The total number of floors in the building.
- **Condition**: The condition of the property (e.g., renovated, good).
- **Floor to floors ratio (`floor_to_floors`)**: The ratio of the floor number to the total number of floors.
- **Is good floor (`is_good_floor`)**: A binary variable indicating if the property is on a desirable floor (e.g., not ground or top floor).
The dataset was sourced from publicly available real estate listings and preprocessed to handle missing values and outliers.

---

### **3. Data Analysis**

#### **Descriptive Statistics**
- **Price**: Mean = 72,511, Std. Dev. = 36,451, Min = 9,500, Max = 296,000.
- **Area**: Mean = 71.5 m², Std. Dev. = 34.2, Min = 10, Max = 347.
- **Price/m²**: Mean = 1026.6, Std. Dev. = 195.1, Min = 494, Max = 1,566.
- **Building Age**: Mean = 8.9 years, Std. Dev. = 47.02, Min = 0, Max = 75.

#### **Correlation Analysis**
- Strong correlation between:
  - **Price** and **Square** → `r = 0.90`
  - **Price** and **Price/m²** → `r = 0.27`


- Weak correlation :
  - **Price** and **Building age** → `r = -0.02`
  - **Square** and **Building age** → `r = -0.04`
  - **Square** and **price/m2** → `r = -0.13`
  - **Building age** and **Price/m²** → `r = 0.05`

- Weak correlation for floor-based features.

>  Heatmap confirms that **property size is the most important driver of price**.

#### **Regression Analysis**
- **R² = 0.827**: The model explains 82.7% of the variance in price.
- Significant predictors: `square`,`roooms`, `district`, `micro_district`,  `condition`, `building_type`, `buuilding_age` , `floor to floors` and `is good floor`.
- Non-significant predictors: All our significant help us to predict the price of the property.

#### **Hypothesis Testing**
- **Building Type 1 vs 2**: Prices differ significantly (`p < 0.001`).
- **1st Floor vs 5th Floor**: Prices differ significantly (`p ≈ 0.0006`).

---

### **4. Visualizations**

1. **Histograms**: Show the distribution of numeric features such as price and area. These highlight the skewness in price and the concentration of properties in specific size ranges.
2. **Boxplots**: Illustrate the variation in price across building types and floors, emphasizing the influence of these factors on pricing.
3. **Heatmap**: Displays the correlation matrix, confirming that property size is the most important driver of price.
4. **Scatter Plots**: Visualize the relationship between price and area, as well as price per square meter, highlighting the linear relationship between these variables.
5. **Bar Charts**: Compare average prices across different districts and building types, showcasing the impact of location and construction material on property values.
6. **Pay Charts**: Illustrate the distribution of prices across different conditions and building ages, revealing trends in property valuation based on these factors.

Each visualization provides insights into the dataset's structure and the relationships between variables, aiding in understanding the factors influencing property prices.

---

### **5. Conclusion**

This analysis highlights the key factors affecting real estate prices in Bishkek, Kyrgyzstan. Property size and condition are the most significant predictors of price, while building type and district also play important roles. The regression model developed in this project is effective for price prediction and market analysis. These findings can help stakeholders make informed decisions in the real estate market.

---

### **6. References**

1. Dataset: Publicly available real estate listings from Bishkek.
2. Tools: Python libraries such as Pandas, Matplotlib, Seaborn, and Statsmodels.
3. Additional Resources: Statistical analysis and machine learning documentation.

--- 
