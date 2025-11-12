# Utilizing-Numismatic-Trends
Simple Random Forest Regression Model implemented on 400 rows of manually cleaned data on various US coins. The goal of the project is to highlight specific coins that are over or undervalued, leading to potential opportunities to profit. 
▪ Built, cleaned and analyzed 400 rows of numismatic data using Excel, Python and Pandas.
▪ Performed statistical analysis, such as regression modeling, correlation matrices and hypothesis testing, to ensure accuracy for key metrics.
▪ Finetuned the model to eliminate overfitting, improving accuracy despite extreme outliers.
▪ Highlighted over and undervalued coins as potential revenue opportunities.
▪ Created a summary report with actionable insights, improving the client’s ability to profitably invest in coins.

The original project was written in Google Colab, which is why the dataset is imported from My Drive.

After the first test, I went back and added more rows of data, significantly reducing the high correlation between certain variables. This happened multiple times.
Faceval and composition have a correlation of 0.82. This is the highest one by far and is expected because coins of the same face value typically have the same compositions. This changed in the 1960s, so if I were to use newer coins in my dataset, this correlation value would drop.

There are a few rare coins that serve as outliers in the data set that throw off the model and heavily skew error metrics. There is nothing that the model can be trained on when given only a handful of extremely rare coins with values based more on demand than anything else. Therefore, to preserve the accuracy of the model, these rare coins are separated pre-model training. The model is still trained on them, but with knowing that they are different. That's the purpose of the rarem attribute.
R^2 and Mse metrics are stable around 0.9 and under 2,000.
