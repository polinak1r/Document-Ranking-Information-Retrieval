## Notebook Outline: Document Ranking & Information Retrieval

1. **Kaggle Setup and Data Download**  
   Kaggle credentials are configured, and competition files (documents, queries, qrels) are downloaded via the Kaggle CLI.

2. **Data Loading and Inspection**  
   All downloaded JSONL/JSON files are read into Python lists or dictionaries, and basic stats (document and query counts) are displayed.

3. **Evaluation Metric (P-Found)**  
   A function `pfound_score` is defined to measure retrieval performance, demonstrating how to compute a score based on ranked predictions.

4. **Text Preprocessing**  
   Titles plus a portion of content are tokenized, stemmed, and filtered for stopwords. A dictionary of document frequencies (df) is built, and very low-frequency tokens are removed.

5. **TF-IDF Construction**  
   A sparse TF matrix is created for each document, IDF values are computed, and both are combined to form the final TF-IDF matrix.

6. **Query Processing and Similarity Computation**  
   Queries undergo the same tokenization and stemming. Their term frequencies are assembled into a sparse matrix, and cosine-like similarity scores are calculated by multiplying document TF-IDF by query term frequencies.

7. **Submission File Creation**  
   (Query, document) pairs and their computed scores are gathered into a dataframe and saved as a CSV file for submission.
