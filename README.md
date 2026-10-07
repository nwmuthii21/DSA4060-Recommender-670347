# DSA 4060 Personalized Movie Recommender

## Student Details
* **Name:** Nelisa Wacera Muthii
* **Student ID:** 670347
* **Assigned User ID:** 8

## Project Objective
This project implements a simple personalized content-based movie recommender system. It analyzes historical user ratings and movie genre information to identify user preferences and generate five sensible recommendations for unwatched movies.

## Datasets
* `movies.csv`: Contains movie IDs, titles, and pipe-delimited genre information.
* `ratings.csv`: Contains historical ratings from 40 users.

## Method / Approach
1. **User Profiling:** Filtered historical ratings for Assigned User ID 8 and identified top-rated preferences (ratings $\ge 4.0$).
2. **Feature Vectorization:** Converted movie genres into numerical features using `TfidfVectorizer`.
3. **Similarity Scoring:** Calculated cosine similarity between the user's liked movies and all available titles in the catalog.
4. **Filtering & Ranking:** Excluded already rated movies and extracted the top 5 highest-scoring recommendations.

## How to Run the Notebook
1. Clone or download this repository.
2. Ensure `movies.csv`, `ratings.csv`, and the `.ipynb` notebook file are in the same folder path.
3. Open the notebook in Jupyter Notebook or VS Code and run all cells sequentially from top to bottom.

## Recommendation Results

For **Assigned User ID 8**, the content-based recommender analyzed historical ratings ($\ge 4.0$) and generated the following 5 tailored movie recommendations:

| Rank | Recommended Movie | Genres | Reason |
| :---: | :--- | :--- | :--- |
| **1** | Blade Runner 2049 | Sci-Fi \| Drama | High genre overlap and matching thematic elements with your top-rated favorite movies. |
| **2** | Remember the Titans | Sports \| Drama | Shares core genre attributes with films you rated 4.0 or higher. |
| **3** | Creed | Sports \| Drama | Strong similarity in genre composition to movies you positively evaluated. |
| **4** | Titanic | Romance \| Drama | Aligns closely with the predominant stylistic tags of your liked catalog. |
| **5** | The Notebook | Romance \| Drama | Matches the structural genre profile of your highest-rated titles. |

### Brief Interpretation
The recommendations effectively capture User 8's preference for deeply character-driven and thematic storytelling, heavily featuring Drama combined with core elements of Sci-Fi, Sports, and Romance. All recommended titles successfully exclude movies already rated by the user while offering strong thematic continuity with their highest-rated favorites.

## Limitation and Suggested Improvement
* **Limitation:** Relies entirely on basic genre tags, ignoring directors, actors, and qualitative plot context.
* **Suggested Improvement:** Implement collaborative filtering or use NLP text embeddings on movie plot descriptions to capture deeper thematic preferences.