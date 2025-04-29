# 🎬  Movies Data Analysis Project

This project is a comprehensive exploratory data analysis (EDA) of a movie dataset (`mymoviedb.csv`). The dataset contains metadata about movies including title, release date, genres, popularity scores, vote counts, and average votes. The objective is to clean, transform, and visualize the data to uncover meaningful insights.

---

## 📁 Dataset Information

- **Rows**: 9827 entries (expanded to 25,552 after genre explosion)
- **Columns**:
  - `Release_Date`: Original release date (transformed to year)
  - `Title`: Movie name
  - `Overview`: Movie description (dropped)
  - `Popularity`: Popularity score
  - `Vote_Count`: Total votes
  - `Vote_Average`: Average vote score
  - `Original_Language`: Movie language (dropped)
  - `Genre`: Movie genres (exploded to single entries)
  - `Poster_Url`: URL to the poster image (dropped)

---

## 🧹 Data Cleaning Steps

1. **Datetime Conversion**: Converted `Release_Date` to year format.
2. **Dropping Irrelevant Columns**: Removed `Overview`, `Original_Language`, and `Poster_Url`.
3. **Categorization**: Binned `Vote_Average` into:
   - `not_popular`
   - `below_avg`
   - `average`
   - `popular`
4. **Handling Genres**:
   - Split multiple genres into lists.
   - Used `explode()` to convert list values into individual rows.
   - Converted `Genre` to `category` datatype.

---

## 📦 Libraries Used

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`

---

## 📈 How to Run

1. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn
