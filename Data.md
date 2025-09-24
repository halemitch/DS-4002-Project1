# Metadata

## Data Summary
This dataset originally had 12 columns and 2,098,325 rows. We ended up narrowing the final dataset only to include 8 columns and 2,097,208 rows. One of the columns (Review_Buckets) was added to the original columns by assigning scores that were 1, 2, or 3 to “Not Good” and 4 or 5 to “Good”. This will be the variable that our model is trying to predict.

## Provenance
This dataset is accessible from a study done on Amazon reviews [1]. A JSON file is available for use via a link for download. We decided to use the smaller dataset for pet products because the larger one would not download for us properly (small datasets for experimentation).

## License
Anyone can use this data set as long as the data is cited somewhere in the report.

## Data Dictionary

| Column | Description | Potential Responses |
|:------:|:-----------:|:--------------------|
| Rating | This is the score written by the customer in their review on a scale of 1 to 5. | 1,2,3,4,5 |
| Date | This is the date at which the review was placed by the customer. | 12 2, 2016 |
| Reviewer_ID | This is the unique ID given to each customer who made a review. | A1X0IOOF3J0OXB, A3RMA1DD66JDRV |
| Product ID | This is the unique ID given to each product that was reviewed by the customers. | B01HIV7FC4, 0972585419 |
| Reviewer_Name | This is the name of the customer who made a review. | Pamela Mathers, Susan P. |
| Review | This is the whole review that the customer gave a product. | These are not rounded. I bought them for my little dog but shes not able to pick them up with her mouth. Also, in the picture they look solid. They are bigger than a jack ball. Otherwise, they might be good for someone else. |
| Summary_Review | This is a summarized review that the customer gave a product. | Read description carefully. |
|  Rating_Bucket | This variable contained either “Not good” or “Good” based on their scores. | Good, Not Good |
| Month | This variable gives us the month that a particular review was created. | January, February |
| review_clean | This variable gives us a clean version of the Review column. | 0395 a can decent deal and the cats love all the flavors |


## Exploratory Plots

<img width="800" height="500" alt="rating_distribution" src="https://github.com/user-attachments/assets/a7e92d2b-2dcc-4e7a-a975-757051d7a311" />

<img width="1200" height="600" alt="over_months" src="https://github.com/user-attachments/assets/191c2446-6621-4783-8bc6-8118dd54cf88" />
