
---Recommender Systems with Content Based and SVD++

##  Datasets Used

- **Netflix Ratings Dataset**
  - Includes movie title, year, ratings, and user engagement stats.
  - Used for content-based recommendation using TF-IDF + cosine similarity.

- **Yelp Dataset**
  - Focused on restaurant reviews with `stars`, `useful`, `funny`, `cool` feedback.
  - Used in both content-based and collaborative filtering models.

---

## Features & Pipelines

### Content-Based Recommendation System
- **Netflix**:
  - TF-IDF on movie metadata + rating stats
  - Cosine similarity to recommend similar movies

- **Yelp**:
  - Nearest Neighbors on user interaction features (`stars`, `cool`, etc.)
  - Cosine similarity to find similar businesses

### SVD++ (Yelp)
- Matrix factorization with implicit feedback
- User/item biases, latent factors, and adaptive learning
- Early stopping & hyperparameter tuning
- Evaluation: RMSE, Precision@K, Recall@K, NDCG@K, Diversity, Novelty

---

## Evaluation Metrics

- **Accuracy-Oriented:**
  - RMSE
  - Precision@K
  - Recall@K
  - F1 Score
  - NDCG

- **Exploration-Oriented:**
  - Diversity (Intra-list)
  - Novelty (Self-information based on popularity)

---

Github public repo https://github.com/mandidisha/SDM.git
