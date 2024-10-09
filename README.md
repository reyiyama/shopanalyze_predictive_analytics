# ShopNalyze: Predictive Analytics for E-Commerce Success

## Overview
ShopNalyze is a data science project designed to predict whether an online shopping session will lead to revenue generation. Leveraging the power of machine learning models like K-Nearest Neighbor (KNN) and Decision Tree Classifier, ShopNalyze incrementally enhances prediction accuracy from 86% to 92%. The project uses a dataset sourced from the University of California, Irvine’s Machine Learning Repository, with feature engineering and model optimization as the core components for improved predictions.

### Features:
- Data-driven prediction of online shopper behavior using KNN and Decision Tree Classifier.
- Feature engineering for higher predictive accuracy.
- Incremental improvements through Grid Search, Synthetic Minority Over-sampling Technique (SMOTE), and Random Forest Classifier.
- A high-resolution decision tree visualization to explain the likely visitor pathways that lead to a successful purchase.

## Applications and Implications
### Wide-Ranging Applications:
- **E-Commerce Optimization**: Understanding key drivers of customer behavior allows online stores to optimize their websites, improve user engagement, and increase sales conversions.
- **Personalized Marketing**: Online stores can use this model to customize marketing strategies based on user behavior patterns, improving targeted promotions and offers.
- **Seasonal Campaign Planning**: Insights into the effectiveness of months like November (Black Friday, Cyber Monday) help optimize marketing campaigns and budgets during peak sales periods.

### Implications:
- **Revenue Enhancement**: By better predicting which users are more likely to make purchases, online stores can focus their resources on segments that have a higher likelihood of conversion.
- **Customer Behavior Insights**: ShopNalyze provides insights into which website pages—such as product pages or account-related pages—are key in driving revenue. Understanding these behaviors empowers decision-makers to make data-driven enhancements to their customer experience.
- **Engagement Analysis**: Identifying pages with higher bounce rates and exit rates can help website developers create better experiences, resulting in reduced abandonment and higher retention.

## How It Works
### Data Preprocessing
- **Dataset**: The dataset used includes 10 numerical and 8 categorical features, and "Revenue" is the target variable. The dataset was collected from an online bookstore built on an osCommerce platform.
- **Cleaning**: The data was meticulously checked for missing values and duplicates. The categorical variables such as "SpecialDay" were retained to evaluate the impact of holidays and special events on sales, while duplicate rows were retained as each represented unique user sessions.
- **Feature Engineering**: Selected features like "PageValues," "ProductRelated," "BounceRates," and "ExitRates" were used to create an initial set of predictive variables. Subsequently, more features were added and tested to observe their incremental impact on prediction accuracy.

### Data Exploration and Visualization
- Descriptive statistics were used to understand the distribution of the data.
- Stacked bar charts, correlation heatmaps, and histograms were employed for feature analysis and insights into visitor behavior trends.
- Exploratory data analysis revealed significant factors such as "PageValues," "TrafficType_2," "ProductRelated_Duration," and "Month_Nov" as having strong correlations with revenue generation.

### Modeling Approaches
- **K-Nearest Neighbor (KNN)**: Used as a starting point due to its ability to capture local patterns in the dataset. This model initially yielded an accuracy of 87%, identifying strong relationships between features like "PageValues" and "BounceRates."
- **Decision Tree Classifier**: A Decision Tree Classifier was used to provide clear, interpretable insights into how different features influenced purchasing behavior.
- **Grid Search & SMOTE**: Grid Search was used to optimize hyperparameters, while SMOTE was applied to handle class imbalance by oversampling the minority class (transactions resulting in revenue).
- **Random Forest**: Finally, a Random Forest Classifier was used for improved accuracy, achieving a maximum prediction accuracy of 92%.

### Visuals and Decision Tree
- A decision tree visualization was generated to illustrate the likely pathway a user takes on an e-commerce site that results in a transaction.
- Key nodes in the decision tree highlight important features and their thresholds, providing insights into what factors contribute to a user making a purchase.

## Importance of the Project
Understanding online shopper behavior and the dynamics that lead to revenue generation is crucial in the rapidly growing field of e-commerce, where competition is fierce. The rise in e-commerce due to the global pandemic of 2020 has accelerated this trend, with the global market expected to reach $6.3 trillion by 2023 ([Baluch, 2023](https://www.forbes.com)). Knowing what drives customer purchases—from website layout to visitor type and browsing duration—can make the difference between a thriving online business and a struggling one.

Predictive modeling allows companies to:
1. **Optimize Sales Funnels**: Target potential buyers with personalized marketing efforts, reducing waste in advertising spend.
2. **Enhance User Experience**: Identify which pages to improve for a better user journey, effectively reducing bounce rates and improving retention.
3. **Increase Conversion Rates**: Focus on actionable data to prioritize changes that have a direct impact on sales conversions.

Online stores can gain valuable insights into what factors—such as the time of the year, visitor type, or engagement with product-related pages—impact purchasing behavior. Understanding these factors is key to staying competitive in a rapidly expanding and constantly evolving marketplace.

## Getting Started
1. Clone the repository:
   ```bash
   git clone https://github.com/username/ShopNalyze.git
   ```
2. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebook:
   ```bash
   jupyter notebook ShopNalyze.ipynb
   ```

## Installation
- Python 3.7+
- Jupyter Notebook
- Libraries: pandas, numpy, scikit-learn, matplotlib, seaborn

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

## Usage
- **Exploratory Analysis**: Use `ShopNalyze.ipynb` to understand the dataset and visualize key features.
- **Feature Engineering and Model Training**: Feature engineering steps are provided in the notebook, which helps users to retrain the model with their own configurations.
- **Decision Tree Visualization**: The decision tree model visualization helps interpret the pathways that lead to successful sales transactions.

## Results
The project demonstrated that the features "PageValues," "ProductRelated_Duration," and "Month_Nov" had a significant positive impact on the likelihood of a purchase. After applying feature engineering and using advanced modeling techniques such as Random Forest, the accuracy of predicting revenue generation was increased to 92%.

## Conclusion
ShopNalyze provides online stores with the capability to understand visitor behavior and predict which interactions will result in sales. With robust machine learning models and comprehensive feature engineering, e-commerce websites can make data-driven improvements, enhance user experience, and ultimately boost their revenue.

## Citation
- [Sakar, 2018]: Sakar, C. O. et al. Real-time prediction of online shoppers’ purchasing intention using multilayer perceptron and LSTM recurrent neural networks. UCI ML Repository.
- [Baluch, 2023]: Baluch, A. (2023). Global E-Commerce Market Growth. Forbes.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

