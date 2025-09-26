# DS-4002-Project1
Classifying pet product reviews. Class project #1

## H2 
# 1. 
  We used Google Colab (Python) for this project. The packages that were installed to use our code were _____________________. Our project was performed on Windows laptops.

# 2.
  |- Data
  |- LICENSE
  |- Output
  |- README.md
  |- Scripts

  # 3.
1) The first step to reproduce our project is to download the data. Go to this website: https://cseweb.ucsd.edu/~jmcauley/datasets/amazon_v2/ . Scroll down until you reach the “small subsets for experimentation”. Find the row that says “Pet Supplies” and then click the link that says “5-core”. 

2) Navigate to the DS-4002_MI3.ipynb file in the Scripts folder. Open our notebook in Google Colab. Upload the downloaded data file to your Google Colab environment so it is available when running the notebook.

3) Run the notebook: execute initial cells in order for preliminary data processing. These cells will load the dataset into a dataframe, select and rename relevant columns, and create a Rating_Bucket variable (split numerical ratings into good (4-5) and bad (1-3)).

4) Reproduce the exploratory data analysis by running the EDA cells. These will produce a bar chart depicting the distribution of pet supplies ratings, a line graph depicting the number of reviews over time, and a stacked bar chart depicting review counts by month. 

5) After EDA, we performed more thorough data cleaning. We removed missing/blank reviews, normalized text (lowercasing, removing punctuation, standardizing whitespace), dropped duplicate reviews, ensured Rating_Bucket exists on the cleaned dataset, and exported the cleaned dataset into a CSV file (pet_supplies_reviews_cleaned.csv).

6) The next step is to train and evaluate the model. We used the cleaned dataset as (clean) with review_clean as features and Rating_Bucket as labels (Good vs. Not Good). We then split the data into training and test sets (80/20, stratified). We built a pipeline with TF-IDF vectorization (unigrams/bigrams, filtered terms) and logistic regression (class_weight="balanced", max_iter=300). We then trained the model and evaluated using a confusion matrix, classification report (precision, recall, F1), and ROC-AUC. The notebook also outputs the top predictive words for each class.

7) Model performance should be close to: Accuracy = 88%, ROC-AUC ≈ 0.94, F1 (Good) ≈ 0.92, F1 (Not Good) ≈ 0.73. Small variation may occur due to randomness in the train/test splitting.

