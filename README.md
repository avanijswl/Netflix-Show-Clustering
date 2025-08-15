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

## Why KMeans Clustering is used?

Grouping different Netflix shows into similar groups was based on : <br/>
-Genre -> type of content.<br/>
-Rating -> target audience preference.<br/>
-Duration -> how long the show is.<br/>

We used K-Means clustering because our task was an unsupervised learning problem, where there were no predefined labels like “comedy” or “action.” K-Means helps find natural groupings in the data without the need for such categories. Since features like genre were converted to numerical form through encoding, and ratings or durations were already numeric, K-Means could process them effectively. It is also simple, fast, and scalable, making it suitable for handling large datasets efficiently using Python’s scikit-learn library. Additionally, the results are interpretable, as the cluster centroids reveal the defining characteristics of each group—for example, one cluster might represent short, animated family shows, while another could represent long, mature dramas.

---

## 📊 Results
- The Elbow Method indicated that **k = 4** clusters give a good balance between simplicity and accuracy.
- Each cluster represents shows with similar:
  - Genre distributions
  - Duration ranges
  - Rating patterns

Example output (scatterplot):
![Netflix Show Clusters](https://github.com/avanijswl/Netflix-Show-Clustering/blob/main/clusters.png)


---

## 💡 Insights
- Short-duration, high-rating shows tend to cluster together regardless of genre.
- Certain genres like **Comedy** and **Romance** often overlap in clusters.
- Low-rated shows form distinct clusters, possibly due to niche appeal.

---

