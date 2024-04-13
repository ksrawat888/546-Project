# Twitter Sentiment Analysis
MIS-546 Project Portfolio 

### Introduction
COVID-19, a global pandemic caused by the coronavirus, has profoundly impacted the world through widespread illness, economic disruption, social upheaval, and highlighted systemic vulnerabilities in our world. It had an immense impact on the mental and physical health on people due to death, sickness, job layoffs, lockdowns, and limitations on daily activities.  

Twitter (now known as X) is a social media platform where users can post and interact with short messages known as tweets. Twitter allows users to express their opinions and concerns in text form. Due to people staying indoors more, there was a surge in social media usage. Due to this phenomenon, data scientists can collect structural data from Twitter. Whereas other platforms such as Instagram/TikTok provide us with unstructured data. Therefore, data scientists can use text analytics, sentiment analysis, and natural language processing to analyze tweets by the public and find insights in them.  

Traditional sentiment analysis, commonly used in the industry, often struggles to capture the subtleties and context embedded in social media language. For instance, a simple positive/negative categorization may overlook the complexities of sentiments expressed during a global crisis, leading to an incomplete understanding. Among all the social media, Twitter is the best data collection option. Additionally, users on Twitter are more likely to express more of their emotions than other social media where they are more likely to filter their expression, such as only expressing happy emotions. 

### Dataset
We are using OPENICOSR data set: COVID-19 Twitter Dataset with Latent Topics, Sentiments and Emotions Attributes. This is a large global dataset on people’s discourse and responses to the COVID-19 pandemic over the Twitter platform in the world. The dataset analyzed tweets with the words “corona”, “Wuhan”, “nCov” and “covid”. The dataset contains COVID-19 related tweets, analyzed for topics, sentiments, and emotions, useful for various interdisciplinary studies. The dataset that we have is already pre-processed by analyzing tweets. We will clean the dataset and perform data wrangling by extracting more features from the data available. 

### Visuals
In terms of visuals, we first wanted to visualize some basic information related to the dataset. These pie charts indicate : 

<div class="image-container">
    <div class="image-wrapper">
        <img src="https://raw.githubusercontent.com/ksrawat888/546-Project/main/piechart1.png" width="350" height="350">
        <p>Among the keywords, "COVID" is the most popular</p>
    </div>
    <div class="image-wrapper">
        <img src="https://raw.githubusercontent.com/ksrawat888/546-Project/main/piechart2.png" width="350" height="350">
        <p>Years most popular in terms of COVID related tweets</p>
    </div>
    <div class="image-wrapper">
        <img src="https://raw.githubusercontent.com/ksrawat888/546-Project/main/piechart3png.png" width="350" height="350">
        <p>The distribution of sentiments expressed in the tweets </p>
    </div>
</div>

## Correlation: 

##### Emotions with Emotions
We want to see the relationship between different emotions. We plotted scatterplots to visualize the relationships.

<img src="https://raw.githubusercontent.com/ksrawat888/546-Project/main/valence.png" width="600" height="500">

As expected, positive emotions tend to have a linear relation amongst each other. Similarly, negative emotions have a linear relation with each other. Conversely, positive and negative emotions have a non-linear relationship.

##### Emotions with time components
We wanted to see the correlation between different emotions and time components of our dataset. We used the correlation function to calculate the relationship and then generated a heatmap:

<img src="https://raw.githubusercontent.com/ksrawat888/546-Project/main/heatmap.png" width="600" height="500">

The results show that there doesn't seem to be any correlation between different emotions and time components.

## Time Series:
After this, we decided to go in detail and perform time series analysis to analyze how emotions were influened by the time components in the data

<img src="https://raw.githubusercontent.com/ksrawat888/546-Project/main/sentiment by time.png" width="700" height="500">
<img src="https://raw.githubusercontent.com/ksrawat888/546-Project/main/sentiment by month.png" width="700" height="500">
<img src="https://raw.githubusercontent.com/ksrawat888/546-Project/main/sentiment by day.png" width="700" height="500">
<img src="https://raw.githubusercontent.com/ksrawat888/546-Project/main/sentiment by hour.png" width="700" height="500">


<img src="https://raw.githubusercontent.com/ksrawat888/546-Project/main/emotion by year.png" width="700" height="500">
<img src="https://raw.githubusercontent.com/ksrawat888/546-Project/main/emotion by month.png" width="700" height="500">
<img src="https://raw.githubusercontent.com/ksrawat888/546-Project/main/emotion by day.png" width="700" height="500">
<img src="https://raw.githubusercontent.com/ksrawat888/546-Project/main/emotion by hour.png" width="700" height="500">


##### This image displays a set of time series graphs, each tracking the intensity of different emotions—Valence, Fear, Anger, Happiness, and Sadness—over a period from January 2020 to around July 2022.

The graphs show the trend analysis, noting if the intensity of each emotion has increased, decreased, or remained stable over time: 
<img src="https://raw.githubusercontent.com/ksrawat888/546-Project/main/timeseries.png" width="700" height="500">


Seasonality: Look for patterns that repeat at regular intervals which might indicate seasonal effects: 
<img src="https://raw.githubusercontent.com/ksrawat888/546-Project/main/decomposed.png" width="700" height="500">


*Autocorrelation Function (ACF)*:
   - ACF measures the correlation between observations at different lags.
   - Note the gradual decline in correlation as the lags increase, which is typical for a time series where immediate past values have a stronger relationship with the current value than the more distant past.
     
<img src="https://raw.githubusercontent.com/ksrawat888/546-Project/main/autocorrelation.png" width="600" height="500">

*Partial Autocorrelation Function (PACF)*:
   - PACF measures the direct relationship between an observation and its lag.
   - Explain the significance of the first lag having a high correlation and the subsequent lags falling within the confidence interval, suggesting that past values have a significant direct effect only at the first lag.

<img src="https://raw.githubusercontent.com/ksrawat888/546-Project/main/partial.png" width="600" height="500">




