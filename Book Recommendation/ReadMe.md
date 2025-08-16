# 📚 Books Recommendation System

This project presents a **Book Recommendation System** built using **K-Nearest Neighbors (KNN)** to suggest similar books based on a user's input. It leverages collaborative filtering on user rating data to make personalized recommendations.

---

## 🔗 Dataset

- **Source**: [Kaggle - Book Recommendation Dataset](https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset/data?select=Books.csv)
- **Files Used**:
  - `Books.csv`: Contains metadata for each book (ISBN, Title, Author, etc.)
  - `Ratings.csv`: Contains user-book rating data

---

## 🧠 Project Objective

To develop a **content-based book recommender** using the KNN algorithm that:
- Filters out users with very few ratings
- Removes books with low number of ratings
- Uses user-item matrix and cosine similarity to identify and recommend similar books
- Returns **top 5 similar books** to a user-given book title

---

## 🛠️ Technologies Used

- Python 🐍
- pandas, NumPy
- scikit-learn
- Matplotlib
- SciPy
- Jupyter Notebook

---

## 📊 Data Preprocessing

- Removed null and duplicate values from the datasets
- Filtered:
  - Users with fewer than 200 ratings
  - Books with fewer than 100 ratings
- Created a **pivot table** with users as rows, books as columns, and ratings as values
- Filled missing values with `0`
- Mapped book ISBNs to their titles for better readability in the recommendation output

---

## 🔍 Model: K-Nearest Neighbors (KNN)

- **Similarity Metric**: Cosine similarity
- **Model**: `sklearn.neighbors.NearestNeighbors`
- Trained on the **book-user rating matrix**
- For a given input book, finds the **top 5 similar books**

---

## 🚀 How It Works

```python
# Get top 5 similar books
books = get_recommends("The Queen of the Damned (Vampire Chronicles (Paperback))")
print(books)
