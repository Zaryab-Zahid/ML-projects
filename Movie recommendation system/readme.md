Movie Recommendation System

A content-based movie recommendation system built using the MovieLens 100K dataset. 
The system recommends movies based on user preferences derived from their rating history 
and genre similarity between movies.

---

Project Overview

This project builds a recommendation engine that:
- Converts user star ratings into preference scores (liked / neutral / disliked)
- Builds a user-movie interaction matrix
- Calculates genre-based cosine similarity between movies
- Recommends top 5 movies a user hasn't watched yet based on their taste

---

Dataset

**MovieLens 100K** collected by the GroupLens Research Project at the University of Minnesota.

- 100,000 ratings from 943 users on 1,682 movies
- Ratings are on a scale of 1 to 5
- Download: [grouplens.org/datasets/movielens/](https://grouplens.org/datasets/movielens/)

### Files Used:

**u.data — User Ratings**
| Column | Description |
|--------|-------------|
| user_id | Unique ID for each user |
| movie_id | Unique ID for each movie |
| rating | Star rating given by user (1-5) |
| timestamp | Time of rating (dropped, not used) |

**u.item — Movie Information**
| Column | Description |
|--------|-------------|
| movie_id | Unique ID for each movie |
| title | Movie title with release year |
| release_date | Date movie was released |
| video_release_date | Video release date (dropped, not used) |
| imdb_url | Link to IMDB page (dropped, not used) |
| Action | 1 if movie is Action genre, 0 if not |
| Adventure | 1 if movie is Adventure genre, 0 if not |
| Animation | 1 if movie is Animation genre, 0 if not |
| Childrens | 1 if movie is Childrens genre, 0 if not |
| Comedy | 1 if movie is Comedy genre, 0 if not |
| Crime | 1 if movie is Crime genre, 0 if not |
| Documentary | 1 if movie is Documentary genre, 0 if not |
| Drama | 1 if movie is Drama genre, 0 if not |
| Fantasy | 1 if movie is Fantasy genre, 0 if not |
| Film_Noir | 1 if movie is Film Noir genre, 0 if not |
| Horror | 1 if movie is Horror genre, 0 if not |
| Musical | 1 if movie is Musical genre, 0 if not |
| Mystery | 1 if movie is Mystery genre, 0 if not |
| Romance | 1 if movie is Romance genre, 0 if not |
| Sci_Fi | 1 if movie is Sci-Fi genre, 0 if not |
| Thriller | 1 if movie is Thriller genre, 0 if not |
| War | 1 if movie is War genre, 0 if not |
| Western | 1 if movie is Western genre, 0 if not |

---

How It Works

1. **Load Data** — Load ratings and movie info from MovieLens files
2. **Clean Data** — Drop unnecessary columns, handle missing values
3. **EDA** — Visualize rating distribution, top movies, genre popularity
4. **Feature Engineering** — Convert ratings to preference scores:
   - Rating 1-2 → 0.0 (disliked)
   - Rating 3 → 0.5 (neutral)
   - Rating 4-5 → 1.0 (liked)
5. **User-Movie Matrix** — Build a 943 × 1682 interaction matrix
6. **Cosine Similarity** — Calculate genre similarity between all 1682 movies
7. **Recommend** — For any user, find movies similar to their liked movies that they haven't watched yet

---

Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

---

Results

The system successfully generates personalized top 5 movie recommendations for any of the 943 users based on their rating history and genre preferences.

---

How to Run

1. Clone the repository
2. Download MovieLens 100K from grouplens.org and place `u.data` and `u.item` in the project folder
3. Open `movie_recommendation.ipynb` in VS Code or Jupyter
4. Run all cells top to bottom

---

Author

**Zaryab Zahid** — ML Engineer in progress

- GitHub: [github.com/Zaryab-Zahid](https://github.com/Zaryab-Zahid)
- Portfolio: [zaryab-zahid.github.io](https://zaryab-zahid.github.io)
