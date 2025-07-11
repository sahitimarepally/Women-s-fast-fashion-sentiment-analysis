# Analyzing Reddit sentiment on Women's fast fashion brands

 This is a  simple, low-code project that collects Reddit conversations about women’s fast fashion brands and measures the overall sentiment behind each one, using two methods: text blob and Google Natural Language API.

**Background**:

Reddit provides a vast amount of user-generated content, free from paid promotions, making it an invaluable source for understanding genuine consumer sentiment. By leveraging this authenticity, I have identified and analyzed the most popular and engaged subreddit focused on women’s fashion. I looked for mentions of fast fashion brands such as Zara, Gap, H&M, and Uniqlo to gain valuable insights into how shoppers feel about these clothing brands.


**Features**

- Extracted approximately 9,800 Reddit comments using the Reddit API (PRAW) and saved them in CSV format (brand, text).
- Applied two sentiment analysis methods:
    - **TextBlob**: For basic polarity and subjectivity scoring.
    - **Google Cloud Natural Language API**: For more advanced sentiment and magnitude scoring.
- Compared results from both methods to identify discrepancies and draw insights about accuracy and tone detection.
- Visualized key findings with Matplotlib charts.



**Requirements**

- Python 3.7+    
- A Reddit API application (PRAW credentials)  
- A Google Cloud project with Natural Language API enabled & service account key


**Analysis Comparison**

I compared TextBlob and Google Natural Language API because they take different approaches to understanding language. TextBlob is fast and easy to use, but relies on simpler rules and dictionaries, whereas Google NLP leverages machine learning and provides more nuanced sentiment detection.
There was a noticeable difference in the way the two tools recognized tone when I tested them on the same texts. TextBlob classified the majority of texts as positive or neutral, while the Google Natural Language API detected a higher number of negative sentiments

| Method         | Brand | Text                                                                                                                                                                                                                                                                              | Sentiment |
|----------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| TextBlob       | Zara  | 1 - stores like Aritzia and Zara tend to be trendier.<br><br>2 - people delude themselves into thinking that by buying through Aritzia and Zara it is somehow more 'ethical' than H&M. There's probably also a feedback loop into this one where I notice cheaper brands get downvoted more. Again, this false sense of sustainability. | positive  |
| Google NL API  | Zara  | 1 - stores like Aritzia and Zara tend to be trendier.<br><br>2 - people delude themselves into thinking that by buying through Aritzia and Zara it is somehow more 'ethical' than H&M. There's probably also a feedback loop into this one where I notice cheaper brands get downvoted more. Again, this false sense of sustainability. | negative  |<br>



In this case, we can see that Google’s tool picked up on the criticism, while TextBlob missed it, which shows that Google’s API provides a more accurate reading of complex language.

