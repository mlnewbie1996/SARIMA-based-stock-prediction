# SARIMA-based-stock-prediction
SARIMA based model to predict price of stock
When talking about the methods of prediction & forecasting. One such method, which deals with time based data is Time Series Modeling. As the name suggests, it involves working on time (years, days, hours, minutes) based data, to derive hidden insights to make informed decision making.

Time series models are very useful models when you have serially correlated data. Most of business houses work on time series data to analyze sales number for the next year, website traffic, competition position, financial markets and  much more.

Stationary Series
There are three basic criterion for a series to be classified as stationary series :

1. The mean of the series should not be a function of time rather should be a constant. 
 ![Mean_nonstationary](https://user-images.githubusercontent.com/32235814/132614465-4d774895-7172-4850-bed7-89549db5fc83.png)

2. The variance of the series should not a be a function of time. This property is known as homoscedasticity.
![Var_nonstationary](https://user-images.githubusercontent.com/32235814/132614497-5c136a1a-2feb-4098-9065-18b63d368533.png)

3. The covariance of the i th term and the (i + m) th term should not be a function of time.
![Cov_nonstationary](https://user-images.githubusercontent.com/32235814/132614507-0591e7dc-5dc6-48e7-b363-e01738dcbfbd.png)

One of the biggest reason that we are considering stationarity is because time series forecasting can only be used to predict stationary processes.

Now why to do Dickey-Fuller Test you ask?
Dickey–Fuller test tests the null hypothesis that a unit root is present in an autoregressive time series model. The alternative hypothesis is different depending on which version of the test is used, but is usually stationarity or trend-stationarity.

Whoa whoa whoa !!!!!!!!! Now wait a minute those seems like a lot of heavy words to use in one sentence. Let me break it down them quickly
  Let's start with what is Hypothesis.
  1. Hypothesis is just a statement that we profess based on whatever that we observe in front of us. Since it's rainy season here in India, this would be a perfect example. You        wake up in the morning and see that the whole sky is cloudy. You say to yourself, "It's going to rain today". This is a hypothesis which you gave after watching the overcast      sky.
  2. Now it's not necessary that it will rain. so thus we will give two hypothesis: Null and Alternative.
     Null Hypothesis is what we consider that is supposed to be true and Alternative is the negation of NULL hypothesis.
     Now how do we measure whether to accept or reject NULL hypothesis? I'm so glad you asked.
          ===> For that we perform ADF or Augumented Dickey Fuller test. Now since we are using time series that means, we are working on the assumpotion that the data that we are                considering is stationary. So ADF just simply reinforces that whether the series is actually stationary or not.
          ===> And for accepting or rejecting NULL hypothesis we consider P value. 
               * A p-value, or probability value, is a number describing how likely it is that your data would have occurred by random chance (i.e. that the null hypothesis is                      true).
               * The level of statistical significance is often expressed as a p-value between 0 and 1. The smaller the p-value, the stronger the evidence that you should reject                    the null hypothesis.
               * A p-value less than 0.05 (typically ≤ 0.05) is statistically significant. 
               * It indicates strong evidence against the null hypothesis, as there is less than a 5% probability the null is correct (and the results are random). 
               * Therefore, we reject the null hypothesis, and accept the alternative hypothesis.
               *  However, if the p-value is below your threshold of significance (typically p < 0.05), you can reject the null hypothesis, but this does not mean that there is a                   95% probability that the alternative hypothesis is true. 
               *  The p-value is conditional upon the null hypothesis being true, but is unrelated to the truth or falsity of the alternative hypothesis.
                             ![Image36341_fmt](https://user-images.githubusercontent.com/32235814/132618191-a6205fda-8725-4658-bcce-ff26432ba6b2.png)

