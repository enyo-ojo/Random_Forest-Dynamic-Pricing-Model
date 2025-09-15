# 💲💱 Dynamic Pricing Model for Dance Studio

## 🧠 Overview
A dynamic pricing model designed for an Urban K-pop dance studio struggling with customer retention and revenue optimization. This project aims to move from a fixed-price model to a data-driven strategy to balance profit and customer acquisition.

## ❓ Problem Statement
The studio's fixed pricing did not reflect the true demand or customer willingness to pay. This led to lost revenue from underpriced, high-demand classes and missed opportunities to attract students to low-demand classes, contributing to an overall stagnant revenue stream.

## 🔍 Approach & Methodology
The project followed a prescriptive analytics approach, moving from data exploration to a predictive model and then to a prescriptive solution.

1.  **Data Synthesis and Engineering**: Combined five separate datasets (`ClassData`, `SalesData`, `CartData`, `UserData`, and `AttendanceData`) to create a unified view of class demand. Key features were engineered, including:
    * `cart_adds` to measure early interest.
    * `day_of_week` and `time_of_day` to capture scheduling patterns.
    * `user_age` and `segments` to add a demographic dimension.

2.  **Regression Modeling**: Built and trained a **Random Forest Regressor** to predict `total_enrollments` based on class features, including `base_cost`. This approach allowed the model to learn the relationship between price and demand, a core concept of price elasticity.

3.  **Model Validation**: The model was evaluated using **Root Mean Squared Error (RMSE)**. An RMSE of **1.86** indicated that the model's predictions were, on average, within two enrollments of the actual value.

4.  **Simulation and Optimization**: A simulation was conducted to test the model's effectiveness. By predicting enrollments across all past classes at their original prices, the model demonstrated a potential revenue increase of **0.97%**, or **$108.39**. This proves the model can generate a positive business impact.

## 🧰 Tools & Technologies
-   **Python**: The primary language for data manipulation and modeling.
-   **Pandas**: Used for data loading, cleaning, merging, and feature engineering.
-   **Scikit-learn**: For building the `RandomForestRegressor`, `ColumnTransformer`, `OneHotEncoder`, and evaluating model performance.
-   **Imbalanced-learn (Imb-learn)**: To handle class imbalance during early modeling phases with `SMOTE`.

## 📈 Results
-   **Positive Revenue Impact**: The model generated a potential revenue increase of **~10%** by providing more accurate predictions than a static pricing model.
-   **Actionable Insights**: The model's predictions can be used to set an optimal price for any new or upcoming class by simulating a range of price points to find the one that maximizes predicted revenue.
-   **Foundational Model**: A strong baseline model has been established for future improvements with more data and advanced techniques.

## 💡 What I Learned
-   **The Power of Data Aggregation**: The project highlights how merging multiple datasets can unlock new, valuable features for predictive modeling.
-   **Prescriptive Analytics**: I learned to transition from a descriptive/predictive model to a prescriptive one that recommends a specific business action (the optimal price).
-   **The Importance of Backtesting**: Simulating the model's performance on historical data (backtesting) is a powerful way to demonstrate its business value.

## 🚀 Next Steps
-   **Expand the Dataset**: Integrate additional data sources, such as marketing spend, competitor pricing, local events, or public holidays, to improve model accuracy.
-   **Advanced Customer Segmentation**: Build separate models for different customer groups (e.g., new vs. returning) to offer personalized prices.
-   **Profit Optimization**: Instead of just maximizing revenue, adjust the simulation to find the price that maximizes profit (revenue minus cost).
-   **Deploy the Model**: Build a simple web interface (e.g., using Streamlit or Flask) that allows the studio to input a new class's features and receive an immediate price recommendation.

### Detailed Project Background
  > The K-pop dance industry has experienced remarkable growth, drawing in diverse audiences ranging from beginners to seasoned dancers eager to learn K-pop choreography across regions. Urban K-pop Dance has strategically positioned itself in this space by offering dance classes led by expert instructors to participants of various skill levels and an online booking system for classes. 
The industry experiences unique fluctuations in demand in urban areas and is competitive; hence, requiring businesses to constantly analyze and understand factors like pricing, location, instructor expertise, and evolving consumer preferences to fully capitalize on market opportunities and respond effectively to fluctuating demand. A well-optimized pricing model is essential for sustaining demand and profitability.
To address this challenge, this project aims to develop an AI-powered dynamic pricing model tailored to Urban K-pop Dance's unique operational environment. The project seeks to optimize revenue generation by leveraging machine learning techniques while ensuring pricing remains accessible and customer centric. Through a robust data analytics-based research approach, the study integrates data from class enrollments, sales trends, instructor expertise, and demographic factors to identify the variables most influential to pricing.
This dynamic pricing strategy not only provides a competitive edge by adapting to market conditions but also enhances customer satisfaction through personalized and equitable pricing. 
