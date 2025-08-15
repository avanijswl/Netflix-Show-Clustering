# 🎬 Netflix Show Clustering

## 📌 Overview
This project applies **K-Means clustering** to group Netflix shows into similar categories based on their **Genre**, **IMDb Rating**, and **Duration**.  
By analyzing and clustering shows, we can uncover patterns in Netflix content, such as which genres have similar popularity, which durations appeal to similar audiences, and more.

---

## 🛠 Tech Stack
- **Python 3.10+**
- **Pandas** – Data manipulation  
- **NumPy** – Numerical computations  
- **Matplotlib / Seaborn** – Data visualization  
- **Scikit-learn** – Machine learning (K-Means, StandardScaler)  
- **Google Colab** – Development environment

---

## 📂 Dataset
The dataset contains the following columns:
- `Title` – Name of the show
- `Genre` – Primary genre of the show
- `Rating` – IMDb or viewer rating (numeric)
- `Duration` – Duration in minutes (numeric)

> **Note:** The dataset was preprocessed to remove missing values before clustering.

---

## 🔍 Methodology
1. **Data Loading**  
   - Loaded Netflix dataset using Pandas.

2. **Data Preprocessing**
   - Converted categorical `Genre` into numeric form using One-Hot Encoding.
   - Removed rows with missing `Rating` or `Duration`.
   - Standardized features using `StandardScaler`.

3. **Finding Optimal Clusters**
   - Used **Elbow Method** to choose the best `k` for K-Means.

4. **K-Means Clustering**
   - Applied K-Means algorithm to group similar shows.
   - Added `Cluster` column to the dataset.

5. **Visualization**
   - Plotted inertia values for different `k` values.
   - Created scatterplots of clusters for visualization.

---

## 📊 Results
- The Elbow Method indicated that **k = 4** clusters give a good balance between simplicity and accuracy.
- Each cluster represents shows with similar:
  - Genre distributions
  - Duration ranges
  - Rating patterns

Example output (scatterplot):
![Netflix Show Clusters](https://raw.githubusercontent.com/avanijswl/Netflix-Show-Clustering/main/874af823-872d-400e-9b91-4f0b9cee40b0.png)


---

## 💡 Insights
- Short-duration, high-rating shows tend to cluster together regardless of genre.
- Certain genres like **Comedy** and **Romance** often overlap in clusters.
- Low-rated shows form distinct clusters, possibly due to niche appeal.

---

