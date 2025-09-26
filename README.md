# DS-4002-Project1
Classifying pet product reviews. Class project #1

## H2 
This repository has 5 folders. The README.md file contains all of the information someone would need to replicate our project. The LICENSE file talks about the licensing and how to cite our project. The Scripts folder contains the code to show how we got our results. The Data file tells you about the data and how to retrieve it (it was too large to store on GitHub). Lastly, the Output file shows the output of our logistic regression model.

# Section 1
  We used Google Colab (Python) for this project. The packages that were installed to use our code were pandas, gzip, json, matplotlib, calender, re, string, numpy, sklearn. Our project was performed on Windows laptops.

 
=======
# Section 2
```bash
├── Data
│   ├── Data.md
├── LICENSE
├── Output
│   ├── Output.md
├── README.md
├── Scripts
│   ├── DS_4002_MI3.ipynb
```
  
  # Section 3
1) The first step to reproduce our project is to download the data. Go to this website: https://cseweb.ucsd.edu/~jmcauley/datasets/amazon_v2/ . Scroll down until you reach the “small subsets for experimentation”. Find the row that says “Pet Supplies” and then click the link that says “5-core”. 

2) Navigate to the DS-4002_MI3.ipynb file in the Scripts folder. Open our notebook in Google Colab. Upload the downloaded data file to your Google Colab environment so it is available when running the notebook.

3) Run the notebook: execute initial cells in order for preliminary data processing. These cells will load the dataset into a dataframe, select and rename relevant columns, and create a Rating_Bucket variable (split numerical ratings into good (4-5) and bad (1-3)).

4) Reproduce the exploratory data analysis by running the EDA cells. These will produce a bar chart depicting the distribution of pet supplies ratings, a line graph depicting the number of reviews over time, and a stacked bar chart depicting review counts by month. 

5) After EDA, we performed more thorough data cleaning. We removed missing/blank reviews, normalized text (lowercasing, removing punctuation, standardizing whitespace), dropped duplicate reviews, ensured Rating_Bucket exists on the cleaned dataset, and exported the cleaned dataset into a CSV file (pet_supplies_reviews_cleaned.csv).

6) The next step is to train and evaluate the model. We used the cleaned dataset as (clean) with review_clean as features and Rating_Bucket as labels (Good vs. Not Good). We then split the data into training and test sets (80/20, stratified). We built a pipeline with TF-IDF vectorization (unigrams/bigrams, filtered terms) and logistic regression (class_weight="balanced", max_iter=300). We then trained the model and evaluated using a confusion matrix, classification report (precision, recall, F1), and ROC-AUC. The notebook also outputs the top predictive words for each class.

7) Model performance should be close to: Accuracy = 88%, ROC-AUC ≈ 0.94, F1 (Good) ≈ 0.92, F1 (Not Good) ≈ 0.73. Small variation may occur due to randomness in the train/test splitting.
  
  # References
[1] “Cross Validation in Machine Learning” GeeksforGeeksI, August 4, 2025. [Online]. Available:
	https://www.geeksforgeeks.org/machine-learning/cross-validation-machine-learning/.
	 [Accessed: Sep. 19, 2025]
   
[2] Grullón-Paz, “Recalled Pet Food May Be Linked to 130 Dog Deaths, F.D.A. Says”
New York Times, para. 1-2, August 19, 2021. [Online], Available: https://www.nytimes.com/2021/08/19/business/midwestern-pet-food-fda.html [Accessed Sept. 11, 2025].

[3] J.. Ni, J. Li, and J. McAuley, “Justifying recommendations using distantly-labeled reviews and fine-grained   
aspects,” Empirical Methods in Natural Language Processing (EMNLP), 2019. [Online]. Available:      https://cseweb.ucsd.edu/~jmcauley/datasets/amazon_v2/. [Accessed: Sep. 12, 2025].

[4] S. Thixton, “45 Pet Food Recalls over the Past Five Years,” Truth About Pet Food, July 17, 2025. [Online],
	Available: https://truthaboutpetfood.com/45-pet-food-recalls-over-the-past-five-years/. [Accessed Sept. 11, 
	2025].

[5] “Text Classification using Logistic Regression,” GeeksforGeeks, Jul. 23, 2025. [Online]. Available: 
https://www.geeksforgeeks.org/machine-learning/text-classification-using-logistic-regression/.[Accessed: Sep. 12, 2025].

[6] “Understanding TF-IDF (Term Frequency-Inverse Document Frequency)”, GeeksforGeeks, August 13, 2025. 
	[Online]. Available:
https://www.geeksforgeeks.org/machine-learning/understanding-tf-idf-term-frequency-inverse-document-frequency/. 
	[Accessed: Sep. 19, 2025]

