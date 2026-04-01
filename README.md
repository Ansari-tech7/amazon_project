# 🎧 Amazon Music Clustering

## 📌 Project Overview

With millions of songs available on music platforms, manually categorizing songs into genres is inefficient and time-consuming. This project uses **Unsupervised Machine Learning (Clustering)** to automatically group similar songs based on their audio features.

The goal is to identify patterns in music and group songs into meaningful clusters such as **chill, party, or instrumental**, without using predefined labels.

---

## 🎯 Problem Statement

Music streaming platforms handle massive song libraries. Assigning genres manually is not scalable.

This project solves that problem by:

* Analyzing audio features of songs
* Grouping similar songs together
* Creating clusters that represent music styles or moods

---

## 💡 Why I Built This Project

I built this project to:

* Understand how **unsupervised learning** works
* Learn **real-world data preprocessing**
* Explore how platforms like Spotify or Amazon recommend songs
* Practice clustering techniques like **K-Means**

---

## 🚀 Business Use Cases

### 🎵 Personalized Playlist Creation

Automatically group similar songs to create playlists.

### 🔍 Song Recommendation

Suggest songs with similar sound characteristics.

### 🎤 Artist Analysis

Help artists understand where their music fits.

### 📊 Market Segmentation

Analyze listener preferences and trends.

---

## 📂 Dataset Information

The dataset contains audio features of songs such as:

* danceability
* energy
* loudness
* speechiness
* acousticness
* instrumentalness
* liveness
* valence
* tempo
* duration_ms

It also includes text fields like:

* song name
* artist name
* genres (used for interpretation only)

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib / Seaborn
* Scikit-learn

---

## ⚙️ Project Workflow

### 1. Data Preprocessing

* Removed duplicates
* Dropped unnecessary columns (IDs, names, text fields)
* Cleaned and formatted data

---

### 2. Feature Selection

Selected only meaningful audio features:

```python
danceability, energy, loudness, speechiness,
acousticness, instrumentalness, liveness,
valence, tempo
```

👉 These features represent **music characteristics like mood, rhythm, and energy**

---

### 3. Feature Scaling

Used **StandardScaler** to normalize data.

#### Why?

Because clustering is distance-based and features have different ranges.

---

### 4. Clustering (K-Means)

* Applied **K-Means algorithm**
* Tested multiple values of K
* Selected best K using:

#### 📊 Silhouette Score

Measures how well clusters are separated.

👉 Best result:

```
k = 2 (highest score)
```

---

### 5. Cluster Evaluation

Used:

* Silhouette Score
* Inertia (Elbow Method)

---

### 6. Cluster Interpretation

Analyzed average values of features per cluster.

#### Example:

* Cluster 0 → Low energy, high acousticness → Chill songs
* Cluster 1 → High energy, high tempo → Party songs

---

### 7. Visualization

* PCA used for dimensionality reduction
* Scatter plots for cluster visualization
* Bar charts and heatmaps for analysis

---

## 📊 Results

* Successfully grouped songs into meaningful clusters
* Identified different music styles based on audio features
* Visualized clusters using PCA
* Derived insights like:

  * Chill vs Party music
  * Acoustic vs High-energy songs

---

## 🧠 Key Learnings

* Importance of **feature selection**
* Role of **data scaling in clustering**
* Understanding **unsupervised learning**
* Handling real-world messy data
* Interpreting clusters without labels

---

## 📁 Project Structure

```
Amazon-Music-Clustering/
│
├── data/
├── notebooks/
├── src/
├── outputs/
├── README.md
```

---

## 🔮 Future Improvements

* Build a recommendation system
* Deploy using Streamlit
* Use advanced clustering (DBSCAN, Hierarchical)
* Improve feature engineering

---

## 🙌 Conclusion

This project demonstrates how machine learning can automatically discover patterns in music data and group songs based on their sound characteristics.

It can be extended to real-world applications like recommendation systems and playlist generation.

---

## 👤 Author

**Mohammed Ansari**

---
