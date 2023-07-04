# Potable Water

The project is part of the "learn by building" of the classification method section. We will classify the water as potable or not by using logistic regression and the K-NN method in R. Model evaluation will be described based on appropriate metrics performance and the ROC. Then, model improvement will be explored and analyzed. 

# End Result of The Project

You can check the end result or full analysis by visiting this link : https://rpubs.com/Fib_Gro/Potable_Water

# Dataset information

The dataset is collected from [the Kaggle website](https://www.kaggle.com/adityakadiwal/water-potability). The data contains 10 variables and 3,276 rows. The target variable is Potability. The possible predictors are pH, Hardness, Solids, Chloramines, Sulfate, Conductivity, Organic_carbon, Trihalomethanes and Turbidity. The following is the description of each variable: 

1. ph: pH of 1. water (0 to 14).
2. Hardness: Capacity of water to precipitate soap in mg/L.
3. Solids: Total dissolved solids in ppm.
4. Chloramines: Amount of Chloramines in ppm.
5. Sulfate: Amount of Sulfates dissolved in mg/L.
6. Conductivity: Electrical conductivity of water in μS/cm.
7. Organic_carbon: Amount of organic carbon in ppm.
8. Trihalomethanes: Amount of Trihalomethanes in μg/L.
9. Turbidity: Measure of light-emitting property of water in NTU.
10. Potability: Indicates if water is safe for human consumption. Potable - 1 and Not potable - 0

# Attachment Files

- Rmd files
- Image file
- Dataset (csv)

# Conclusion  

1. Based on the model with the stepwise backward method, Solids, Chloramines and Organic carbon have a significant contribution to portability. Also, this model produces a lower AIC value compared to logistic regression with glm().
2. Model with an imbalanced target class produces a biased accuracy value. This is valid for both models with the logistic regression method and K-NN method. Thus, AUC is a preferable value to compare the goodness of both models.
3. Model with the K-NN method performs better than a model with logistic regression to classify the potability of water in this dataset, confirmed by a higher number of the area under the ROC and precision value.
4. In this study, the imbalanced target class has been handled by using four different types of sampling (over, under, both and synthetic). For this dataset, the over-sampling method in logistic regression performs better in terms of accuracy and precision values compared to other sampling methods.
5. The optimum k value is obtained by using a precision plot to find the most favourable k value (k = 61). This is the point, where the precision indicates higher than the most frequently used k-value (square root of the total number of samples).
6. Adjusted threshold probabilities by using the Youden Index do not obtain the model with the highest accuracy. However, it can provide an unbiased accuracy metric.
