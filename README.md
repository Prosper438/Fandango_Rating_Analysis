# 🎬 Fandango Ratings Analysis

An exploratory data analysis project investigating whether Fandango artificially inflates movie ratings to boost ticket sales.

Based on the FiveThirtyEight article: [*Be Suspicious Of Online Movie Ratings, Especially Fandango's*](http://fivethirtyeight.com/features/fandango-movies-ratings/)

---

## 📌 Key Finding

**Fandango consistently displays higher ratings than every other platform**, particularly for poorly reviewed films. The biggest offender — *Taken 3* — received 4.5 stars on Fandango while averaging just 1.86 across all other platforms.

---

## 📂 Project Structure

```
├── 00-Capstone-Project.ipynb   # Main analysis notebook
├── fandango_scrape.csv         # Fandango ratings dataset
├── all_sites_scores.csv        # RT, Metacritic, IMDB ratings dataset
└── README.md
```

---

## 🔍 Analysis Breakdown

### Part 1 — Fandango Ratings
- Explored the relationship between movie popularity (votes) and ratings
- Extracted release year from film titles using regex
- Compared **displayed STARS** vs true **RATING** from votes
- Found Fandango rounds up displayed ratings, inflating scores

### Part 2 — Other Sites (RT, Metacritic, IMDB)
- Compared RT Critics vs RT User scores
- Measured mean absolute difference between critics and users
- Explored vote count distributions on Metacritic and IMDB

### Part 3 — Normalized Comparison
- Merged both DataFrames on the FILM column
- Normalized all ratings to a 0–5 scale for fair comparison
- Visualized distribution of all platforms side by side
- Identified the 10 worst reviewed films and compared ratings across platforms

---

## 📊 Visualizations

- KDE plots comparing rating distributions across platforms
- Count plot of STARS vs RATING differences
- Scatterplots for critic vs user scores
- Clustermap of all normalized scores
- Histogram of normalized ratings

---

## 🛠 Libraries Used

- `pandas` — data manipulation
- `numpy` — numerical operations
- `matplotlib` — plotting
- `seaborn` — statistical visualizations

---

## 🚀 How to Run

1. Clone the repository
2. Install dependencies: `pip install pandas numpy matplotlib seaborn`
3. Open `00-Capstone-Project.ipynb` in Jupyter Notebook or VS Code
4. Run all cells from top to bottom
