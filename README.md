# Spark (PySpark)

* Experiment 1: Basic Analysis and Joining Collections
  * Basic analysis of the given dataset (citeulike).
  * Joining of the collections for both RDDs and DataFrames.
  * Count word problems and shows the top 10 words for RDDs.

* Experiment 2: About the Collaborative Filtering Recommender System.
  * Calculated Sparsity of the Citeulike Dataset.
  * Plotted different Rank-Frequency Distributions; 1: No. of Users and No. of Ratings, 2: No. of Items and No. of Ratings.
  * Created Ratings Matrix
  * Used ALS algorithm of Spark ML-library to learn and generate recommendations.
  * For Evaluation, split the dataset into training and test set as 70, 30 respectively.
  * Then calculated RMSE over the test set.
  * Hyper-Parameter Tuning using the Spark Cross-Validator on multiple iterations using rank {10,25,50} and different maxIter values.
  
* Experiment 3: Text Processing with Spark.
  * Concatenation of Title and Abstract, Tokenization, Removal of Stop Words.
  * Stemming using PorterStemmer of NLTK
  * As the dataset was large, reduced it to words only appearing in atleast 20 papers and removed words appeared in more than 10% of papers.
  * Implemented Bag-of-Words Representation as Paper_Id, TermFrequencyVector.
  * Used IDF estimator of Spark ML to calculate TF-IDF Vectors.
  * For Latent Direchlet Allocation (LDA) to extract set of topics used Spark ML implementation of LDA.
  * Created user profiles for both TF-IDF and LDA
  * Performed Sampling and Data Prepration for next task that is Content Based Recommender System.

* Experiment 4: Evaluation of CBRS.
  * Implementation of the similartiy metric, Cosine Similarity.
  * Made Recommendations based on Cosine Similarity and then ranked results and recommended top-K results.
  * Implemented for both the user profiles TF-IDF and LDA
  * Calculated Offline Evaluation metrics, Precision, Recall and MRR.
  * Offline-Evaluation using the sampler from previous experiment. 
