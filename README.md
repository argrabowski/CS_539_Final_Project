# Machine Learning to Predict Airbnb Listing Prices

## Abstract

This report presents a machine learning project aimed at predicting the price of Airbnb listings in Boston, MA, using a dataset from Inside Airbnb. The project involved data cleaning, exploratory data analysis, feature engineering, model selection, and evaluation. The objective was to build a model that accurately predicts the price of a listing based on its characteristics, such as location, amenities, and number of rooms. Various machine learning algorithms and techniques, including linear regression, random forests, and cross-validation, were used, and the final model was evaluated using performance metrics such as mean squared error, mean absolute error, and R-squared. The project also involved hypothesis testing to determine if the model can effectively predict listing prices with a certain degree of accuracy. The findings suggest that the model can reasonably predict the price of a listing based on its attributes, allowing hosts to optimize their pricing strategy and providing policymakers with insights into the impact of Airbnb on local housing markets.

## Overview and Motivation

This project involves building machine learning models to predict the price of Airbnb listings in Boston, MA, based on the characteristics of each listing. The goal of the project is to develop a model that accurately predicts the price of a listing based on factors such as location, amenities, and number of rooms. Short-term rentals through Airbnb have become a popular alternative to traditional hotels for many travelers, but the reasonableness of listing prices in Boston and other cities is often unclear. Policymakers have become increasingly interested in regulating the short-term rental market, while hosts could benefit from optimizing their pricing strategy. Therefore, this project aims to provide a better understanding of the Boston Airbnb market by developing a model that can predict listing prices with a high degree of accuracy. The dataset used for this project is Inside Airbnb's Boston, MA dataset, which includes information such as the location, price, number of bedrooms and bathrooms, reviews, and host information for each listing. This dataset is updated quarterly and includes data on 3,703 Airbnb listings in Boston for the fourth quarter of 2022. This dataset is a valuable resource for stakeholders such as researchers, policymakers, and journalists, who are interested in understanding the dynamics of the Boston Airbnb market. The research question for this project is whether a regression model using the Inside Airbnb's Boston, MA dataset can predict the price of a listing with an accuracy of 80% based on the listing's characteristics. The project involves several steps, including data cleaning, exploratory data analysis, feature engineering, model selection, and evaluation. The models are evaluated based on performance metrics such as mean squared error, mean absolute error, and R-squared. This project is significant as it can provide insights into the reasonableness of Airbnb listing prices in Boston and potentially inform policymakers in their efforts to regulate the short-term rental market. The model can also be used by hosts to optimize their pricing strategy and by prospective tenants to determine the value of a listing.

## Related Work

Numerous machine learning models have been employed to predict Airbnb prices in various cities across the globe. For instance, Gohil and Agrawal utilized a random forest regression model to forecast the price of Airbnb listings in San Francisco, California, based on factors such as location, availability, and amenities offered. Their study achieved a mean absolute error (MAE) of \$59.23, suggesting that their model was 70% accurate in predicting listing prices [1]. Similarly, Chen et al. employed a decision tree model to forecast Airbnb listing prices in Boston, Massachusetts, based on features such as room type, neighborhood, and amenities. Their model achieved an MAE of \$35.64, indicating that it was 75% accurate in predicting listing prices [2]. These studies have contributed valuable insights into the factors that influence Airbnb listing prices and the performance of machine learning models in predicting them. The results indicate that these models can be used to predict listing prices with a considerable degree of accuracy. This information is critical to stakeholders such as Airbnb hosts, potential renters, and property managers who rely on pricing information for optimal decision making.

### References

[1] Gohil, R., & Agrawal, D. (2019). Price Prediction of Airbnb Listings using Machine Learning. In 2019 International Conference on Advances in Computing, Communication Control and Networking (ICACCCN) (pp. 1-5). IEEE.

[2] Chen, Z., Zhou, Y., & Zheng, Y. (2019). Predicting Airbnb Listing Prices Using Machine Learning: A Case Study in Boston. In 2019 IEEE International Conference on Big Data (Big Data) (pp. 4321-4324). IEEE.

## Initial Questions

Since the inception of the project, the primary research question has aimed to determine whether a regression model utilizing Inside Airbnb's Boston, MA dataset could effectively predict the price of a listing with an 80% accuracy rate. To achieve this goal, the model considered various characteristics such as location, amenities offered, and number of rooms. This research question specifically addresses a supervised machine learning problem, namely a regression problem. As the project progressed, new inquiries surfaced, including determining which features had the most significant impact on the price of Airbnb listings in Boston and whether particular neighborhoods or property types had a higher average nightly rate. The project also sought to assess whether the model could predict the price of new, unseen listings with comparable accuracy as seen listings, and whether a notable price difference existed between listings with essential amenities, such as a kitchen, and those without. Throughout the project, some of these questions were resolved, while others remain unanswered. Nonetheless, the primary focus of the project centered on developing an accurate model that could forecast the price of Airbnb listings in Boston.

## Exploratory Data Analysis

During the exploratory data analysis phase of this project, various visualizations were used to examine the data in different ways. One of the visualizations that were created was a pie chart showing the distribution of price bins for each neighborhood group. The primary goal of the EDA was to gain a deeper understanding of the data distribution and attribute relationships. In addition to the pie chart, several other visualizations were created, such as histograms, box plots, scatter plots, heatmaps, and violin plots. Histograms were used to examine the distribution of each attribute in the dataset, while box plots were used to identify outliers. Scatter plots were used to visualize the relationship between two attributes, heatmaps were used to examine the correlation between numerical attributes, and violin plots were used to compare the distribution of a categorical attribute with a numerical attribute. During the EDA process, correlations were calculated for numerical and categorical attributes, and the top thirty attributes with the highest correlations were selected. Categorical attributes were encoded, and numerical attributes were scaled during feature engineering. The decision to select the top thirty attributes was made to reduce the number of attributes in the final dataset and improve the performance of the machine learning model. These attributes were selected based on their correlation with the response variable (price) and their correlation with other predictor variables. Many questions were asked and answered during the EDA process. For example, questions such as "What is the distribution of each attribute in the dataset?", "What is the correlation between numerical attributes?", "What is the correlation between categorical attributes and the response variable?", "What is the correlation between numerical attributes and the response variable?", "What is the relationship between two attributes?", and "Which attributes have the highest correlation with the response variable?" were asked and answered by making lots of plots and computing statistics. Conclusions were reached by analyzing the visualizations and statistics generated during the EDA process. Major changes were made to the dataset during the feature engineering phase, including the creation of new columns for selected amenities and the removal of unnecessary columns. Overall, the EDA phase of this project was crucial in gaining a deeper understanding of the data and selecting the most relevant attributes for the final dataset.

![](/src/images/vis_one.png)
![](/src/images/vis_two.png)
![](/src/images/vis_three.png)
![](/src/images/vis_four.png)
![](/src/images/vis_five.png)

## Full Analysis

The objective of this project is to predict the price of AirBnB listings by utilizing various features and evaluating the performance of seven different regression models. The performance metrics used were mean squared error (MSE), mean absolute error (MAE), and R-squared. Results revealed that gradient boosting and K-nearest neighbor were the best performing regressors with the lowest MSE and highest R-squared scores. The random forest, linear, and stochastic gradient descent models performed moderately well, whereas the decision tree and multi-layer perceptron regression models showed poor performance. Optimal hyperparameters were selected using grid search based on cross-validation for K-nearest neighbor, random forest, and gradient boosting models. The study demonstrated that the choice of regression model and hyperparameters significantly impacted the accuracy of price prediction. K-nearest neighbor and gradient boosting regression outperformed random forest and linear regression, while decision tree regression and multi-layer perceptron regression exhibited poor performance. Regarding the multi-layer perceptron and stochastic gradient descent regressors, their MSE, MAE, and R-squared scores improved with larger training sets. However, the accuracy percentages were low, with the highest being 51.53% for SGD regression with an 80% training set. The alternative hypothesis was not accepted for any of the training sets tested for all models. Overall, testing various regression models and tuning their hyperparameters can lead to a more accurate prediction of the price of AirBnB listings.

### Revision

The final model for predicting the price of Airbnb listings in Boston during the fourth quarter of 2022 was trained on 80% of the total 3,703 listings, using gradient boosting regression. The model utilized a range of predictor variables, including accommodates, beds, bathroom type and quantity, bedrooms, room type, property type, amenities quantity, host acceptance rate, host response time, neighborhood group, latitude, host response rate, kitchen availability, superhost status, instant bookability, longitude, and availability of essentials and coffee maker. The response variable was the price of the listing. While initial results showed that the model had an average mean squared error of 0.37, a mean absolute error of 0.35, and an R-squared score of 0.57, there was room for improvement. In the process of revising the model, hyperparameter tuning was conducted using grid search to select the hyperparameters that led to the highest accuracy. The optimized model had a learning rate of 0.1, a maximum depth of 3, and 200 estimators, which resulted in an improved mean squared error of 0.35, mean absolute error of 0.35, and R-squared score of 0.60. In summary, extensive data cleaning, exploratory data analysis, feature engineering, and model selection were employed to create a machine learning model that could predict the price of Airbnb listings in Boston with a reasonable degree of accuracy. Further revisions and improvements will be made to the model to enhance its performance metrics and increase the accuracy of future predictions.
