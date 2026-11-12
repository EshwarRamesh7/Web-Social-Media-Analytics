# Amazon Mobile Reviews — NLP & Sentiment Analytics
## Project explanation and interview preparation

### Project summary
This project analyses Amazon mobile-phone reviews for a manufacturer that wants to understand customer sentiment, product preferences and brand perception. The workflow combines text cleaning, TF-IDF feature extraction and a Multinomial Naive Bayes sentiment classifier with dashboard-based exploration of ratings, brands, products and review themes.

**60-second interview pitch**

“I analysed roughly 10,500 Amazon mobile-phone reviews to understand customer sentiment and the features customers discuss most often. I cleaned the text, removed stop words, applied lemmatisation and converted review text into TF-IDF features. I then used a Multinomial Naive Bayes classifier for sentiment prediction and combined the results with product metadata such as brand, price and rating. The goal was to turn unstructured review text into actionable themes for product and marketing teams.”

### Business problem
Star ratings alone do not explain why customers like or dislike a product. Review text can reveal recurring themes about battery life, camera quality, screen quality and performance. The project aims to organise those themes so product and marketing teams can understand customer feedback.

### Dataset and approach
The project describes approximately 10,500 reviews with brand, price, product features, review text, ratings, verified-purchase status, ranking and timestamps.

1. Clean the text and handle missing or duplicate reviews.
2. Remove stop words and apply lemmatisation.
3. Transform text into TF-IDF vectors.
4. Train a Multinomial Naive Bayes classifier.
5. Combine sentiment output with product metadata.
6. Explore ratings, sentiment and frequently discussed product features in Tableau/Power BI.

The original README reports approximately 85–87% accuracy and 75% positive sentiment. Verify the class definition, data split and evaluation approach against the notebook before quoting these values.

### Interview questions and suggested answers

**1. What is sentiment analysis?**  
It is the process of identifying the opinion or polarity expressed in text, for example positive, negative or neutral sentiment. It can help summarise large volumes of customer feedback.

**2. Why is text preprocessing important?**  
Raw reviews contain casing, punctuation, URLs, duplicates and common words that may add little signal. Consistent preprocessing can reduce noise, though the exact steps should fit the language and model.

**3. What are stop words?**  
Common words that may contribute little to a particular text-analysis task. Removing them can reduce feature noise, but should be tested because some words affect meaning.

**4. What is lemmatisation?**  
It reduces inflected words to a dictionary form, such as “running” to “run”, using linguistic analysis. It differs from stemming, which often truncates words using simpler rules.

**5. What is TF-IDF?**  
Term Frequency–Inverse Document Frequency weights a term based on how often it appears in a document and how rare it is across the corpus. It gives more weight to words that help distinguish documents.

**6. Why use Multinomial Naive Bayes?**  
It is a simple and efficient probabilistic classifier commonly used for non-negative text features such as term counts and TF-IDF. It assumes conditional independence among features given the class.

**7. What is the Naive Bayes assumption?**  
It assumes features are conditionally independent given the class. Natural-language terms are not truly independent, but the method can still be a useful baseline.

**8. What is data leakage in text classification?**  
It happens when information from the test set influences training, for example fitting the TF-IDF vocabulary on all data before splitting. Fit the vectoriser on training data only, ideally inside a pipeline.

**9. Why is accuracy not enough?**  
If positive and negative reviews are imbalanced, a model can achieve high accuracy by predicting the majority class. Precision, recall, F1 and a confusion matrix provide a fuller view.

**10. How would you handle neutral reviews?**  
Define the task explicitly. It could be a three-class model or a binary model with a documented rule for excluding or grouping neutral reviews. The decision should match the business use case.

**11. What are limitations of star ratings as sentiment labels?**  
Ratings are only a proxy for sentiment. Review text can be mixed, sarcastic or inconsistent with the rating. Label quality affects model quality.

**12. How would you improve the analysis?**  
Use a leakage-safe pipeline, examine class balance, inspect misclassified examples, test alternative models and add topic/aspect analysis to separate themes such as battery, camera and performance.

### Findings and business use
The project reports around 75% positive sentiment and recurring discussion of battery life, camera quality and performance. These are dataset-level findings. They can inform follow-up product analysis and communication strategies, but should not be generalised to all mobile-phone customers.

### Limitations
- Reported accuracy needs to be verified against the notebook's test procedure.
- Sentiment labels may be derived from ratings and can be noisy.
- TF-IDF and Naive Bayes are a useful baseline but do not capture context as deeply as advanced language models.
- Aspect-level sentiment is worth considering when reviews contain both praise and criticism.

### Resume bullet
Analysed Amazon mobile-phone reviews using Python NLP, TF-IDF and Multinomial Naive Bayes, combining sentiment classification with product metadata and dashboard visualisation to identify recurring customer feedback themes.

### Files
- [Notebook](../Capstone_web%26social%20final.ipynb)
- [Review workbook](../tableau_reviews_with_dictionary.xlsx)
- [Tableau workbook](../Capstone_project%20tableau%20(1).twbx)
- [Presentation](../Capstone%20Web%20%26%20Social%20Media%20Analytics%20(1)%20(1).pptx)
