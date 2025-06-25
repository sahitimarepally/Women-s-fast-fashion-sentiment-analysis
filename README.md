# Analyzing Reddit sentiment on Women's fast fashion brands

 A simple low-code project of collecting Reddit conversations about women’s fast fashion brands and measuring the overall sentiment behind each one, using two methods: text blob and Google Natural Language API.

**Background**:

Reddit provides a vast amount of user-generated content, free from paid promotions, making it an invaluable source for understanding genuine consumer sentiment. By leveraging this authenticity, I have identified and analyzed the most popular and engaged subreddit focused on women’s fashion. I looked for mentions of fast fashion brands such as Zara, Gap, H&M, and Uniqlo to gain valuable insights into how shoppers feel about these clothing brands.


**Features**

- Collects ~9,800 Reddit comments about women’s fashion brands with PRAW (Reddit API) and saves them in a simple CSV (`brand` + `text`).
- Runs two sentiment analyses:
  - **TextBlob (open-source)** for basic positive/negative and subjective/objective scores  
  - **Google Cloud NLP (cloud)** for refined sentiment score and intensity
- Compares both methods to see which gives a clearer picture of customer opinions.
- Creates clear, easy-to-read charts with Matplotlib.



**Requirements**

Python 3.7+    
A Reddit API application (PRAW credentials)  
A Google Cloud project with Natural Language API enabled & service account key


**Analysis**

**Conclusion**

