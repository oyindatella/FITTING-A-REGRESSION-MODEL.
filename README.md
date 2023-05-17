# FITTING-A-REGRESSION-MODEL.
Fitting a regression model to understand the key drivers of customer satisfaction.
My client, a fictional online retailer, Tabithy is struggling to understand the key drivers of customer satisfaction on their e-commerce platform. As a result, I have decided to implement a data-driven approach using the CRISP-DM methodology to solve this business problem.
The first step in this process was to clearly define the problem statement, which involved identifying the factors that most significantly impact customer satisfaction. To achieve this, a regression analysis was conducted using data from customer feedback surveys, as well as information on customer demographics and purchase behavior.
Through this analysis, I will be able to help Tabithy identify the most significant drivers of customer satisfaction on its platform. However, the retailer is also struggling with how to allocate resources to these areas in order to improve customer satisfaction and loyalty.
Armed with this knowledge, I will able to help Tabithy develop targeted strategies to improve the overall customer experience and increase customer loyalty. By using the results of the regression analysis, the retailer will be able to make data-driven decisions about where to allocate resources in order to have the greatest impact on overall customer satisfaction.
In this article, I will walk you through the steps of fitting a regression model to understand the key drivers of customer satisfaction on an e-commerce platform. By following the CRISP-DM methodology, we can gain valuable insights into the factors that most impact customer satisfaction and develop data-driven solutions to improve the overall customer experience, while efficiently allocating resources.
Below are the steps of the CRISP-DM methodology applied to fitting a regression model to understand key drivers of customer satisfaction for a fictional online retailer:
Business Understanding: The first step is to define the business problem and identify the goals of the project. In this case, the online retailer is struggling to understand the key drivers of customer satisfaction and needs to allocate resources effectively to improve overall satisfaction.
Data Understanding: The second step is to collect and analyze the data that will be used to solve the business problem. In this case, I have collected relevant data on customer satisfaction surveys, as well as data on customer demographics and purchasing behavior.
Data Preparation: The third step involves cleaning, transforming, and formatting the data in preparation for analysis. This may involve removing missing values, checking duplicated values, and exploratory data analysis to understand the variables of the data sets better.
Modeling: The fourth step is to apply a regression model to the data to identify the key drivers of customer satisfaction. This involved using the Ordinary least squares (OLS) technique to identify the variables that have the most impact on customer satisfaction.
Evaluation: The fifth step involves evaluating the models developed in the previous step to determine their effectiveness in solving the business problem. This may involve using metrics such as R-squared, beta coefficient, and p-value to assess the goodness-of-fit of the model.
Deployment: The final step involves deploying the results of the analysis to the business. In this case, the retailer can use the insights gained from the regression model to allocate resources more effectively and improve overall customer satisfaction.
In this analysis, we will provide answers to the following questions:
Which independent variables have a significant impact on overall satisfaction?
How strong is the relationship between the independent variables and customer satisfaction?
Which aspects of Tabithy's offering should be allocated additional resources, and where Tabithy should disinvest or maintain their current allocation strategy.
Are there any caveats or limitations that could impact the results of the regression analysis?
DATA DESCRIPTION
I will briefly describe the dataset using the variable name and the variable description
Overall_Satisfaction: How satisfied a customer is with Tabithy on an overall basis (measured on a scale of 0–10)
Product_Satisfaction: How satisfied a customer is with the products they bought on tabithy.com (measured on a scale of 1–5)
Price_Satisfaction: How satisfied a customer is with the prices offered on tabithy.com (measured on a scale of 1–5)
Service_Satisfaction: How satisfied a customer is with the service provided by Tabithy customer service agents through online chats, email, or phone (measured on a scale of 1–5)
Navigation_Satisfaction: How satisfied a customer is with the ease of navigating the tabithy.com website (measured on a scale of 1–5)
Loyalty_Satisfaction: How satisfied a customer is with Tabithy's loyalty programmes (measured on a scale of 1–5)
Shipping_Satisfaction: How satisfied a customer is with the shipping of their purchases, including punctuality and delivery updates (measured on a scale of 1–5)
ProdVariety_Satisfaction: How satisfied a customer is with the product variety available on tabithy.com (measured on a scale of 1–5)
RevQuality_Satisfaction: How satisfied a customer is with quality of the reviews provided on tabithy.com (measured on a scale of 1–5)
FITTING THE REGRESSION MODEL
First we need to import all the relevant libraries and packages that will allow us to perform regression analysis and to visualise the results. The most commonly-used packages can be imported with the following lines of code.
Relevant python librariesNext, we import regression-specific packages that will be required to fit a regression model to the data set. This can be achieved with the following lines of code.
Setting pandas to show a maximum of 200 rows and 20 columns of data. Also setting the colours and palettes for the seaborn graphing package
Next, we import, read, and check the data file.
Next step is data wrangling. To do this, we would inspect the data frame info, check for missing and null values.
We can see that there are no null and missing values in the dataset.Once you are satisfied that the correct data file has been imported, we can then move on to performing some basic descriptive statistics before fitting the regression model. We can begin by calculating some descriptive statistics of the different customer satisfaction variables using the describe command. In this case, we will exclude the Customer_id and the customer descriptor variables and concentrate on the customer satisfaction scores alone.
Based on the mean scores reported for the eight areas of the company - product, price, service, navigation, loyalty, shipping, product variety, and review product satisfaction- are there any areas you would suggest that the company attempts to improve?
Ordinarily, with areas like product, loyalty, shipping, review product satisfactions with terribly low mean scores, might prompt a manager to allocate resources (time, money, training) to these areas to improve customer satisfaction. While mean scores are a good starting point, they are often flawed and misleading. It is very important to discern how important each attribute is to the customer.
One obvious way in which to address this is to ask customers directly about how important the various attributes are. For example, you might send out a survey that asks customers to rate areas of interest on a scale of 1–5, where:
1 = Not at all important
5 = Very important
Many years of marketing research studies have shown that such direct solicitation are often inaccurate for a variety of reasons. For example, a respondent might score all the attributes as a 5, which can overinflate its importance.
This is where regression analysis becomes very useful because it allows us to discern, without directly asking customers, which attributes have the most impact on customer decision-making and, by extension, which attributes they consider most important. In this instance, regression analysis allows indirect solicitation.
In the context of the tabithy.com case study, overall customer satisfaction will be designated as the dependent variable (or outcome of interest). In contrast, the remaining customer satisfaction variables - that is, product, price, service, navigation, loyalty, shipping, product variety, and review quality - will be designated as the independent variables that are presumed to have an impact on overall satisfaction. Regression analysis can help determine how important these attributes are in driving overall customer satisfaction.
With the following lines of code, we will be able to fit a regression model to the data in Python.
Regression results:

This analysis would help answer our first and second questions. Which are:
Which independent variables have a significant impact on overall satisfaction?

Answer: Product_Satisfaction: The coefficient is 1.0266, and the p-value is 0.000. This indicates that Product_Satisfaction has a significant positive impact on overall satisfaction.
Price_Satisfaction: The coefficient is 0.1399, and the p-value is 0.000. This suggests that Price_Satisfaction also has a significant positive impact on overall satisfaction.
Service_Satisfaction: The coefficient is 1.1324, and the p-value is 0.000. Service_Satisfaction is statistically significant and positively affects overall satisfaction.
Navigation_Satisfaction: The coefficient is 0.0628, and the p-value is 0.000. Navigation_Satisfaction shows a significant positive impact on overall satisfaction.
Loyalty_Satisfaction: The coefficient is 0.0936, and the p-value is 0.000. Loyalty_Satisfaction is statistically significant and positively influences overall satisfaction.
Shipping_Satisfaction: The coefficient is 0.0802, and the p-value is 0.000. Shipping_Satisfaction has a significant positive impact on overall satisfaction.
ProdVariety_Satisfaction: The coefficient is 0.0614, and the p-value is 0.000. ProdVariety_Satisfaction is statistically significant and positively affects overall satisfaction.
RevQuality_Satisfaction: The coefficient is 0.0171, and the p-value is 0.140. Although RevQuality_Satisfaction has a positive coefficient, the p-value is greater than 0.05, indicating that it is not statistically significant in this model at the 95% confidence level.
Based on these results, the variables Product_Satisfaction, Price_Satisfaction, Service_Satisfaction, Navigation_Satisfaction, Loyalty_Satisfaction, Shipping_Satisfaction, and ProdVariety_Satisfaction have a significant impact on overall satisfaction, while RevQuality_Satisfaction does not show statistical significance and should therefore, be removed.

2. How strong is the relationship between the independent variables and customer satisfaction?
The strength of the relationship between the independent variables and customer satisfaction can be evaluated by examining the R-squared value in the regression results. In the provided output, the R-squared value is 0.687, which indicates that approximately 68.7% of the variance in customer satisfaction can be explained by the independent variables included in the regression model. A high R-squared value suggests a strong relationship between the independent variables and the dependent variable (customer satisfaction in this case). It indicates that the selected independent variables collectively explain a significant portion of the variation in customer satisfaction.
Therefore, based on the R-squared value of 0.687, we can conclude that there is a relatively strong relationship between the independent variables (Product_Satisfaction, Price_Satisfaction, Service_Satisfaction, Navigation_Satisfaction, Loyalty_Satisfaction, Shipping_Satisfaction, and ProdVariety_Satisfaction) and overall satisfaction in the given regression model.
