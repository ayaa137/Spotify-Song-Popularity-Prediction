# 🎵 Predicting Spotify Song Popularity Using Data Science and Machine Learning

This project explores how well measurable Spotify audio characteristics can explain and predict song popularity. It combines exploratory data analysis, temporal analysis, and machine learning on a large historical dataset of **170,653 tracks**.

## 🔍 Research Question

**How well do Spotify audio features explain and predict song popularity?**

The analysis examines audio characteristics including:

- Acousticness
- Danceability
- Energy
- Instrumentalness
- Liveness
- Loudness
- Speechiness
- Tempo
- Valence

Release year is also evaluated to investigate the role of temporal structure in popularity prediction.

## 📊 Project Overview

The project includes:

- Data quality assessment and preprocessing
- Exploratory data analysis
- Popularity distribution analysis
- Correlation analysis
- Temporal trends in music characteristics
- Linear Regression
- Random Forest Regression
- Histogram Gradient Boosting Regression
- Audio-only vs. audio + release year comparisons
- Model diagnostics
- Feature importance analysis
- Limitations and interpretation

## 🤖 Machine Learning Results

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Random Forest - Audio + Year | **6.695** | **9.534** | **0.810** |
| HistGradient Boosting - Audio + Year | 6.721 | 9.547 | 0.810 |
| Linear Regression - Audio + Year | 7.980 | 10.732 | 0.759 |
| Random Forest - Audio Only | 10.674 | 14.084 | 0.585 |
| HistGradient Boosting - Audio Only | 10.816 | 14.151 | 0.581 |
| Linear Regression - Audio Only | 13.112 | 16.308 | 0.444 |
| Mean Baseline | 18.564 | 21.875 | -0.000 |

The best-performing model was **Random Forest using audio features and release year**, achieving an **R² of 0.810**, **MAE of 6.695**, and **RMSE of 9.534**.

## 💡 Key Findings

- Audio characteristics contain meaningful predictive information about song popularity.
- Non-linear models outperform Linear Regression when using audio features alone.
- Release year provides substantial additional predictive information.
- Random Forest and Histogram Gradient Boosting achieve nearly identical top performance.
- The strong contribution of release year suggests that temporal structure is important when interpreting model performance.
- Results should not be interpreted as evidence that audio characteristics alone determine popularity.

## 🛠️ Technologies Used

- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn
- Jupyter Notebook

## 📁 Repository Structure

```text
Spotify-Song-Popularity-Prediction/
├── data/
│   └── data.csv
├── notebooks/
│   └── spotify_popularity_analysis.ipynb
├── reports/
│   └── spotify_popularity_analysis.html
├── index.html
└── README.md
```

## 🌐 Project Website

An interactive project website provides a concise overview of the analysis, key findings, and model performance.

**Live website:** Coming soon via GitHub Pages.

## 📓 Full Analysis

The complete analysis is available in:

- The Jupyter Notebook in the `notebooks/` directory
- The code-free HTML report in the `reports/` directory

## ⚠️ Limitations

Spotify popularity is influenced by many factors that are not captured by audio features, including marketing, playlist placement, artist recognition, social media exposure, and broader cultural trends.

The strong predictive contribution of release year also indicates that random train-test evaluation may benefit from temporal structure in the dataset. A time-aware validation strategy would provide a stronger test of performance on genuinely future releases.

## 👩‍💻 Author

**Aya Abdine**

MSc Data Science for Society and Business  
Constructor University, Bremen, Germany
