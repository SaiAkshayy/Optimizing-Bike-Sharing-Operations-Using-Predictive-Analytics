# Capital Bikeshare Case Analysis

## Project Overview:

Capital Bikeshare systems rely on maintaining optimal availability of bikes and docking stations for users. This project addresses operational challenges by predicting bike and dock availability using weather and bike-share data from February to June 2023. The focus is on leveraging machine learning models to optimize resource allocation and improve service quality at the Foggy Bottom location.

The project’s primary goals include:

- Forecasting bike usage patterns based on weather conditions.

- Identifying the best predictive model using machine learning techniques.

- Providing actionable insights for cost minimization and quality maximization strategies.

## Data Preparation & Exploratory Analysis:

To build predictive models, daily weather data was combined with Capital Bikeshare system data. The dataset included variables such as temperature, wind speed, UV index, precipitation, and visibility. Exploratory data analysis focused on understanding the relationships between these factors and bike pickups/dropoffs.

### <ins> Key Findings:

- Higher temperatures and UV index levels correlated positively with increased bike usage, indicating that favorable weather encourages biking.

- Dew point and precipitation showed mixed effects, with extreme conditions potentially discouraging bike usage.

- Some weather factors, like visibility and wind speed, exhibited unclear trends and required further investigation.
<img src = "https://github.com/user-attachments/assets/9769e8aa-4e7b-48a2-b2ae-5cb5cb0b1611" width = 1200 height = 750>

## Predictive Modeling:

Five machine learning models were implemented to forecast bike movement:

- Linear Regression: Established baseline performance, demonstrating moderate predictive capability.

- Ridge Regression: Addressed multicollinearity and overfitting; emerged as the most robust model for predictions.

- LASSO Regression: Effective for feature selection by driving unnecessary coefficients to zero.

- Elastic Net: Combined strengths of Ridge and LASSO; performed well in balancing prediction accuracy and complexity.

- KNN Regressor: Demonstrated limited utility due to dataset characteristics and high variance in predictions.

### <ins> Model Comparison Metrics:

Mean Squared Error (MSE): Evaluates prediction error.

R² (R-Squared): Measures the proportion of variance explained by the model.

### <ins> Key Insights:

- Ridge Regression outperformed other models, achieving the lowest MSE and highest R² values.

- Elastic Net and LASSO showed strengths in feature selection and adaptability for operational strategies.

- KNN underperformed due to the high dimensionality and nature of the dataset.

  
<img src = "https://github.com/user-attachments/assets/93a1b17d-0bc8-453e-b3ec-b9efe09f115a" width = 450 height = 300> <img src = "https://github.com/user-attachments/assets/036bc41a-13c8-421d-9e3c-0e03056ae3c1" width = 450 height = 300>

### <ins> Decision Performance Evaluation:

Beyond technical accuracy, models were assessed based on their practical utility in two strategic scenarios:

### <ins> Cost Minimization Strategy:

- Focused on minimizing penalties for unsuccessful pickups/dropoffs.

- Elastic Net and LASSO excelled, achieving the lowest total costs.
<img src = "" width = 1000 height = 700>

### <ins> Quality Maximization Strategy:

- Prioritized maximizing the weighted average service level for pickups and dropoffs.

- Elastic Net and LASSO delivered the best results, optimizing service levels.
<img src = "" width = 1000 height = 700>


## Conclusion & Recommendations:

The analysis highlights the potential of predictive modeling to enhance the operational efficiency of bike-sharing systems. Key recommendations include:

- Ridge Regression should be employed for general prediction tasks due to its accuracy and reliability.

- Elastic Net and LASSO are ideal for decision-making strategies, balancing cost minimization and service quality.

Management can use these insights to allocate bikes and docks effectively, reducing operational costs and improving customer satisfaction.

### Management Impact:
By integrating these models, Capital Bikeshare can:

- Reduce costs associated with unsuccessful pickups/dropoffs.

- Improve user satisfaction by ensuring bike/dock availability.

- Leverage data-driven decision-making to anticipate demand and optimize resource allocation.

## Limitations & Future Work:

While this study provides actionable insights, it has some limitations:

- Assumes simultaneous pickups and dropoffs, whereas these events occur sequentially in real-world scenarios.

- Future studies could incorporate real-time data and hourly optimizations to account for dynamic system changes.

- Real-time dashboards for monitoring and adjusting predictions dynamically.

