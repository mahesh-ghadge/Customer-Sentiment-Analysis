# Customer-Sentiment-Analysis
![enter image description here](https://raw.githubusercontent.com/mahesh-ghadge/Customer-Sentiment-Analysis/main/customer%20sentiments.PNG)
## Description
A large electronics company has been falling behind the competition in terms of providing good customer service to their customers.  They want to gain deeper audience insight, improve their customer engagement, provide improved customer service to their customers and also improve the success of their future marketing campaigns.  To achieve this, the management proposed analyzing the sentiment of different customers for different products but it's a hectic process when done manually.  So they want this task to automate the sentiment Analysis of future reviews.

We have provided customer review data of different electronic products sold on an E-commerce platform. 

The dataset contains information about the marketplace, customers, products and also the review information including the entire review text written by the customer. 

Also provided in the dataset is the star_rating. It is the 1-5 star rating of the review.

### Steps followed on given dataset
- We cleaned the reviews by:
  - **Changing** the **case** of each word to **lowercase**,
  - **Fixing** certain words,
  - **Removing** all the **punctuation marks** from each review, and
  - **Removing** any additional white space from each review.

- Then, we calculate the **polarity** and **subjectivity** values for each review.

- This allowed us to **analyze** our data **in-depth** to find relationship between various features like star rating and polarity.

  - **Distribution of Star Ratings**
		![enter image description here](https://raw.githubusercontent.com/mahesh-ghadge/Customer-Sentiment-Analysis/main/Proportional%20Distribution%20of%20Star%20Ratings.png)

   - **Distribution of Sentiments**
   ![enter image description here](https://raw.githubusercontent.com/mahesh-ghadge/Customer-Sentiment-Analysis/main/Distribution%20of%20Sentiments%20based%20on%20Polarity.png)
   ![enter image description here](https://raw.githubusercontent.com/mahesh-ghadge/Customer-Sentiment-Analysis/main/Proportional%20Distribution%20of%20Sentiments.png)
- We also calculated a **threshold** for the **subjectivity** value in our reviews.
- We then found out the **most common words** associated with different sentiments.
  -  **Most Common Words in Positive Reviews**
  
  ![enter image description here](https://raw.githubusercontent.com/mahesh-ghadge/Customer-Sentiment-Analysis/main/Most%20Common%20Words%20in%20Positive%20Reviews.png)
  
  -  **Most Common Words in Negative Reviews**
  
  ![enter image description here](https://raw.githubusercontent.com/mahesh-ghadge/Customer-Sentiment-Analysis/main/Most%20Common%20Words%20in%20Negative%20Reviews.png)
  
- After analyzing the data:
  - We **remove** all **redundant columns** from the data,

  - **Remove** all the **samples** having **subjectivity less than 0.3** i. e. the subjectivity threshold.

  - **Divide reviews into sentiments** based on star rating and polarity.

  - At last, we **split** the **data** into training and test sets.

- During model building, we first created a **TFIDF matrix** of our data and **trained** a **Multinomial Naive Bayes** model.

  - This model was then used to make **predictions** on the test set.

  - It achieved an **accuracy** of **92%** on both train and test sets.
  
  ![enter image description here](https://raw.githubusercontent.com/mahesh-ghadge/Customer-Sentiment-Analysis/main/TFIDF_Report.PNG)
  

  - This implied that model is not overfitting and is **generalizing** well on unseen data.

- At last, we used a **pre-trained** model to make sentiment predictions on a **small sample** of our data.
  
  - The pre-trained model was **slower** than the ML model we build, and gave **worse results**.
![enter image description here](https://raw.githubusercontent.com/mahesh-ghadge/Customer-Sentiment-Analysis/main/NaiveBayesAnalyzer.PNG)
- So, we **discarded** this model, and used our **TFIDF - Multinomial NB** model as our **final model**.
