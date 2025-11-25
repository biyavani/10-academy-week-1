# This is the notebook for Week 1 assessement

The Python notebook provides a comprehensive framework for **analyzing financial news data and its relationship to stock market performance**, integrating **data preprocessing, exploratory analysis, sentiment evaluation, and quantitative financial metrics**. The workflow is divided into several structured sections, each targeting a specific part of the analysis.



### **1. Data Loading and Preparation**

The notebook begins by importing essential **Python libraries** required for data handling, visualization, and analysis. These include:

* **pandas** for data manipulation and cleaning,
* **matplotlib** and **seaborn** for visual exploration, and
* **scikit-learn** for potential machine learning or feature processing tasks.

It then loads two primary datasets:

* A **financial news dataset** containing article headlines, publication dates, publishers, and sentiment-related metadata.
* **Stock market data** for multiple ticker symbols, providing daily price information such as opening, closing, high, and low values.

The data preparation stage includes handling missing or invalid entries, converting date columns into datetime format, and ensuring consistency between the timestamps in the news and stock datasets to enable future merging or correlation analysis.



### **2. Exploratory Data Analysis (EDA)**

The notebook performs an extensive descriptive analysis to uncover key characteristics and distribution patterns in the data:

* **Text statistics:** It computes and summarizes headline lengths in both characters and words, identifying extremes such as the longest and shortest headlines.
* **Publisher activity:** The analysis highlights the most and least active publishers, indicating which sources contribute most frequently to the dataset.
* **Temporal distribution:** It evaluates article frequency across different time intervals—by **year, month, and specific day**—to detect publication trends and spikes in activity.
* The data reveals that **March 12, 2020**, recorded the **highest number of articles**, aligning with major financial events that likely drove increased news coverage.

This stage provides an overall understanding of the dataset’s structure, helping identify potential biases or concentrations in the data.



### **3. Text Analysis**

The notebook delves into the **linguistic and sentiment aspects** of the headlines:

* It applies **sentiment analysis** using libraries such as TextBlob or VADER to assign **polarity scores** to each headline, classifying them as **positive**, **negative**, or **neutral**.
* It performs **bigram frequency analysis**, identifying common two-word combinations that appear frequently in the headlines. The most frequent bigrams include:

  * “52 week”
  * “price target”
  * “stocks moving”
  * “analyst ratings”
  * “earnings report”

These findings show that the news content predominantly revolves around **analyst actions, stock movements, and earnings-related updates**, indicating a focus on market performance and company analysis.



### **4. Time Series Analysis**

This section visualizes how the **volume of published articles changes over time**, offering insights into news activity patterns:

* It generates **time series plots** that show the count of articles grouped by **year, month, and week**, helping detect seasonal or event-driven trends.
* An hourly breakdown reveals that most articles are timestamped around **00:00 hours (midnight)**, likely due to automated publication or data processing schedules. Additionally, article frequency peaks during **morning hours**, aligning with financial market opening times.

Such analysis helps correlate the timing of news releases with trading activity and market reactions.



### **5. Publisher Analysis**

The notebook investigates both the **quantitative and qualitative characteristics** of the publishers:

* It computes **average sentiment scores per publisher**, identifying those with the most consistently positive or negative tones in their reporting.
* A **domain-level breakdown** reveals that **@benzinga.com** overwhelmingly dominates the dataset, contributing over **7,900 articles**, while smaller domains such as **@gmail.com**, **@andyswan.com**, and **@investdiva.com** appear infrequently.
* This suggests that a **single dominant organization (Benzinga)** provides the majority of the news, with **minor contributions from smaller independent or individual sources**.



### **6. Quantitative Stock Analysis**

The notebook transitions from textual data to **numerical financial analysis**:

* It loads **historical price data** for various stock tickers, including metrics like opening, closing, and adjusted closing prices.
* It computes two types of **moving averages** for trend detection:

  * **Simple Moving Average (SMA)** for smoothing short-term volatility.
  * **Exponential Moving Average (EMA)** for emphasizing more recent data points.
* Visualizations of these moving averages help identify **momentum shifts, long-term trends, and potential support or resistance levels** in stock prices.



### **Overall Summary**

The notebook provides a **comprehensive data-driven approach** to exploring how **news sentiment and publication trends** intersect with **financial market behavior**. By combining **textual insights** (from news headlines and sentiment) with **quantitative stock analysis**, it establishes a foundation for further predictive modeling, such as exploring correlations between sentiment scores and subsequent market movements.
