# Amazon Mobile Reviews — NLP & Sentiment Analytics

An analytics project using Amazon mobile-phone reviews to understand customer sentiment, product preferences and recurring themes in customer feedback.

**Tools:** Python · Pandas · NumPy · NLTK · scikit-learn · TF-IDF · Tableau · Power BI

## Business question

What do customers say about mobile products, which product features appear most often in reviews, and how can feedback be organised into useful product and marketing insights?

## Dataset

The project describes approximately 10,500 Amazon mobile reviews with brand and product information, prices, review text, star ratings, verified-purchase status, ranking and timestamps.

## Workflow

- Clean and preprocess review text.
- Remove stop words and apply lemmatisation.
- Convert text into numerical features using TF-IDF.
- Apply a Multinomial Naive Bayes sentiment classifier.
- Combine sentiment outputs with product metadata such as brand, price and ratings.
- Explore sentiment and review themes using dashboard visualisations.

## Findings recorded in the project

The original analysis reports approximately **75% positive sentiment** and identifies battery life, camera quality and performance as frequently discussed themes. It reports approximately **85–87% classifier accuracy**.

Treat these figures as results from this project dataset, not as general measures of customer sentiment or model performance on other products. Consult the notebook and presentation for the exact train/test split and class definition.

## Repository contents

- `Capstone_web&social final.ipynb` — analysis notebook.
- `tableau_reviews_with_dictionary.xlsx` — review data and dictionary.
- `Capstone_project tableau (1).twbx` — Tableau packaged workbook.
- `Capstone Web & Social Media Analytics (1) (1).pptx` — presentation.


## Author

**Eshwar Ramesh** · [GitHub](https://github.com/EshwarRamesh7) · [Portfolio](https://eshwarrameshportfolio.netlify.app) · [LinkedIn](https://www.linkedin.com/in/eshwar-ramesh-9a4652251)
