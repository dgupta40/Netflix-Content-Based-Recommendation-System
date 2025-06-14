# Netflix-Content-Based-Recommendation-System

A Jupyter Notebook pipeline that ingests, cleans, and models a Netflix catalog (8,800+ titles) to deliver personalized content-based recommendations—all implemented in a single notebook.

##  Features

* **End-to-End ETL in One Notebook**

  * Load raw dataset, handle missing metadata, parse dates & durations
  * Fetch missing IMDb ratings via OMDb API in parallel
* **Feature Engineering**

  * One-hot encode genres; MinMax scale release year, duration, and IMDb scores
* **Recommendation Methods**

  * Cosine similarity; k-Nearest Neighbors retrieval; Gaussian Naïve Bayes (≈84% accuracy); k-Means clustering (silhouette-based k selection); Apriori association rules
* **Ensemble Ranking**

  * Combine all signals into a single score for top-10 recommendations
* **User Preferences via Google Sheets**

  * Real-time ingestion of likes, dislikes, and rating thresholds

##  Usage

1. **Clone & install dependencies**

   ```bash
   git clone https://github.com/dgupta40/Netflix-Content-Based-Recommendation-System.git
   cd Netflix-Content-Based-Recommendation-System
   pip install -r requirements.txt
   ```
2. **Set environment variables**

   ```bash
   export OMDB_API_KEY="your_key"
   export GOOGLE_CREDENTIALS_JSON="/path/to/creds.json"
   ```
3. **Launch Jupyter and open**

   ```bash
   jupyter lab  # or jupyter notebook
   # then open RecommendationSystem.ipynb
   ```
4. **Run cells** to clean data, engineer features, run models, and generate recommendations.

## ⚙️ Dependencies

* Python 3.x
* pandas · scikit-learn · requests · gspread · jupyter

##  Contributing

Feel free to open issues or pull requests to enhance functionality or documentation.

