# ShopAnalyze_Predictive_Analytics: Predictive Analytics for E-Commerce Success

## Overview
ShopAnalyze is a data science project designed to predict whether an online shopping session will lead to revenue generation. Leveraging the power of machine learning models like K-Nearest Neighbor (KNN) and Decision Tree Classifier, ShopNalyze incrementally enhances prediction accuracy from 86% to 92%. The project uses a dataset sourced from the University of California, Irvine’s Machine Learning Repository, with feature engineering and model optimization as the core components for improved predictions. 

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

## Decision Tree Analysis and Findings
![image](https://github.com/user-attachments/assets/f6bd2c98-3130-42bd-a9ba-2a97fbd40324)

The decision tree model provides a comprehensive representation of how various features influence a user's likelihood of making a purchase on the e-commerce platform. Each node in the tree represents a decision point based on specific features, allowing us to trace the journey of a user and understand the factors that lead to a successful or unsuccessful purchase. Below is an in-depth explanation of the key decision points and findings from the decision tree:

### Key Findings
1. **PageValues as a Primary Split Feature**: The decision tree starts with the feature "PageValues," which represents the average value of a web page that a user visited before completing a transaction. A threshold value of 0.99 is used as the primary decision point, highlighting the importance of page value in predicting purchasing intent. Users visiting pages with a value below this threshold were less likely to make a purchase compared to those above it.

2. **Month of Visit (November)**: The feature "Month_Nov" plays a significant role in splitting further down the tree. This aligns with peak shopping periods such as Black Friday and Cyber Monday, which typically occur in November. Users visiting during this month showed a higher likelihood of making a purchase, especially when combined with a higher "ProductRelated_Duration," indicating strong interest in the product.

3. **Administrative Duration and Product-Related Pages**: For users with lower page values, the amount of time spent on administrative pages ("Administrative_Duration") and the number of product-related pages visited ("ProductRelated") were key determinants. Users who spent more time on administrative pages without high engagement in product-related activities generally did not make a purchase.

4. **Bounce Rates and Exit Rates**: The features "BounceRates" and "ExitRates" are crucial in predicting user behavior. Low bounce rates and exit rates indicate higher user engagement and are associated with successful purchases. In particular, users with a bounce rate of 0 and page values greater than 19.78 were highly likely to convert, suggesting effective engagement tactics on those pages.

5. **Thresholds for Product-Related Engagement**: The decision tree reveals specific thresholds for "ProductRelated" and "ProductRelated_Duration" features. For instance, users who visited more than 74 product-related pages with a duration exceeding 1183 seconds were likely to make a purchase. This indicates that higher interaction with product pages is a strong predictor of conversion.

6. **Influence of Exit Rates on Decision Pathway**: When considering users with a page value greater than 0.99, the feature "ExitRates" became significant. Users with an exit rate below 0.01, combined with long product-related engagement, were more likely to convert. However, when exit rates exceeded 0.02, the likelihood of conversion decreased sharply, highlighting the importance of optimizing page flow to minimize exits.

7. **New Visitors vs. Returning Visitors**: The "VisitorType_New_Visitor" feature played a role in differentiating users with low page values. New visitors showed a consistently lower likelihood of making a purchase compared to returning visitors, emphasizing the need for personalized marketing strategies aimed at first-time users to increase engagement and conversion.

### Insights from the Decision Tree
- **High Page Value is Crucial**: Users who interacted with pages that had a higher page value (above 0.99) were more likely to make a purchase, emphasizing the importance of showcasing valuable content and key product information effectively.
- **November as a Key Sales Driver**: The feature "Month_Nov" consistently showed positive influence on conversion rates. This reinforces the value of targeted marketing campaigns during high-sales months such as November.
- **Minimizing Bounce and Exit Rates**: Lower bounce rates and exit rates significantly increased the likelihood of purchases. This insight can guide website optimization efforts, such as improving page load times, enhancing content quality, and ensuring seamless navigation to reduce user drop-offs.
- **Engagement with Product Pages**: Users who interacted extensively with product-related content, both in terms of the number of pages visited and the duration of engagement, were more likely to make a purchase. This underscores the importance of enhancing product pages with detailed descriptions, high-quality images, and engaging multimedia content to maintain user interest.

The decision tree model serves as a powerful tool for understanding user behavior and identifying key leverage points for increasing sales conversion. By analyzing the pathways leading to both successful and unsuccessful transactions, e-commerce platforms can optimize their content and marketing strategies to drive more revenue.

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
   git clone https://github.com/reyiyama/shopanalyze_predictive_analytics.git
   ```
2. Open the Jupyter Notebook:
   ```bash
   jupyter notebook Assignment2.ipynb
   ```

## Installation
- Python 3.7+
- Jupyter Notebook
- Libraries: pandas, numpy, scikit-learn, matplotlib, seaborn

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

## Usage
- **Exploratory Analysis**: Use `Assignment2.ipynb` to understand the dataset and visualize key features.
- **Feature Engineering and Model Training**: Feature engineering steps are provided in the notebook, which helps users to retrain the model with their own configurations.
- **Decision Tree Visualization**: The decision tree model visualization helps interpret the pathways that lead to successful sales transactions.

## Results
The project demonstrated that the features "PageValues," "ProductRelated_Duration," and "Month_Nov" had a significant positive impact on the likelihood of a purchase. After applying feature engineering and using advanced modeling techniques such as Random Forest, the accuracy of predicting revenue generation was increased to 92%.

## Conclusion
ShopAnalyze provides online stores with the capability to understand visitor behavior and predict which interactions will result in sales. With robust machine learning models and comprehensive feature engineering, e-commerce websites can make data-driven improvements, enhance user experience, and ultimately boost their revenue.

## Citation
- [Sakar, 2018]: Sakar, C. O. et al. Real-time prediction of online shoppers’ purchasing intention using multilayer perceptron and LSTM recurrent neural networks. UCI ML Repository.
- [Baluch, 2023]: Baluch, A. (2023). Global E-Commerce Market Growth. Forbes.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
