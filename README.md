# 🎬 Movie Recommendation System

A machine learning-based movie recommendation system that suggests similar movies using **content-based filtering** and **cosine similarity**. Built with Python and Streamlit.

---

## 🚀 Features

- Recommend movies based on content similarity
- Interactive Streamlit web interface
- Displays movie posters using the TMDB API
- Fast and simple user experience

---

## 🛠️ Tech Stack

- Python
- Pandas & NumPy
- Scikit-learn
- Streamlit
- TMDB API

---

## 📂 Project Structure

```
movie_recommendation_system/
│
├── app.py                      # Streamlit app
├── movie recommender.ipynb     # Model building notebook
├── movie_dict.pkl              # Preprocessed movie data
├── similarity.pkl              # Cosine similarity matrix (generate via notebook)
├── tmdb_5000_movies.csv        # Dataset
├── tmdb_5000_credits.csv       # Dataset
├── requirements.txt
├── .env.example
├── .gitignore
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/Likhitareddy17/movie_reccomendation_system.git
cd movie_reccomendation_system
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Generate the similarity matrix

Run all cells in `movie recommender.ipynb` — this will generate `similarity.pkl` and `movie_dict.pkl` in the project folder.

> ⚠️ This step is required before running the app. The `similarity.pkl` file is too large to store in the repo directly.

### 4. Set up your TMDB API key

Create a `.env` file in the project root:

```env
API_KEY=your_tmdb_api_key_here
```

Get a free API key at [themoviedb.org/settings/api](https://www.themoviedb.org/settings/api).

### 5. Run the app

```bash
streamlit run app.py
```

---

## 🧠 How It Works

This project uses a **content-based recommendation system**:

1. Movie metadata (genres, keywords, cast, crew) is combined into a single feature string
2. `CountVectorizer` converts text into feature vectors
3. **Cosine similarity** is computed between all movie pairs
4. When a movie is selected, the top 5 most similar movies are returned with posters from the TMDB API

---

## 🔑 Environment Variables

| Variable | Description |
|---|---|
| `API_KEY` | Your TMDB API key |

---

## 📌 Future Improvements

- Add hybrid (collaborative + content-based) recommendation
- Deploy on Streamlit Cloud
- Add movie search autocomplete
- Improve UI/UX

---
