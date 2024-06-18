# Project Overview: Sentiment Analysis on TripAdvisor Hotel Reviews

In this project, we focus on conducting Sentiment Analysis on hotel reviews sourced from TripAdvisor. The dataset used can be accessed [here](https://notebook.community/melqkiades/yelp/notebooks/TripAdvisor-Datasets).

## Project Pipeline:

1. **Data Preprocessing with MapReduce:**
   - We employ a MapReduce job for data preprocessing. This step involves aggregating hotel reviews based on their unique identifiers provided in the dataset.
   - All reviews corresponding to each hotel are merged under their respective identifiers to form a consolidated review dataset for each hotel.

2. **Hotel Evaluation:**
   - Post-aggregation, our objective is to identify the best hotels by analyzing two key metrics:
     - **Average Ratings:** Calculated from the collected review data.
     - **Sentiment Scores:** Derived from our Sentiment Analysis on the reviews.
     - **Other Measures:** That might involve the number of reviews and the sentiment score from the classifier.
  
3. **Data Filtering for Significance:**
   - To enhance computational efficiency and ensure meaningful results, we filter the dataset to include only hotels with more than 1,000 reviews. This threshold helps in avoiding skewed or insignificant data from hotels with fewer reviews.

4. **Ablative studies**:
 - We also implemented our own sentiment analysis model using PySpark ML to test this powerful library.

This approach allows us to effectively assess and rank hotels based on a combination of quantitative ratings and qualitative sentiment scores from user reviews.
