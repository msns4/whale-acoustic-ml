# 🐋 Whale Acoustic ML

### Unsupervised Machine Learning for Exploring Whale Vocalizations

This project explores whether unsupervised machine learning can identify acoustic patterns in whale vocalization recordings using audio signal processing and machine learning.

Whale recordings are transformed into MFCC acoustic features and analyzed using K-Means clustering, Silhouette Analysis, and PCA.

## 🔬 Research Question

**Can unsupervised machine learning identify meaningful acoustic structure in whale vocalization recordings based only on their acoustic features?**

## ⚙️ Pipeline

Whale Audio  
↓  
Resampling to 22,050 Hz  
↓  
5-second Segmentation  
↓  
13 MFCC Features  
↓  
Feature Standardization  
↓  
K-Means Clustering  
↓  
Silhouette Analysis  
↓  
PCA Visualization

## 📊 Key Results

- 11 source whale recordings were analyzed.
- The recordings produced 62 five-second audio segments.
- Initial clustering achieved a Silhouette Score of **0.621**.
- After normalizing the sample rate, the strongest two-cluster solution achieved **0.603**.
- The pilot whale recording was identified as a strong acoustic outlier.
- After removing this recording for an additional exploratory analysis, the remaining 57 segments produced a three-cluster solution with a Silhouette Score of **0.574**.
- PCA visualization showed visible acoustic separation between the resulting groups.

### PCA Visualization

The PCA projection below visualizes the acoustic separation between the three clusters identified in the exploratory analysis.

<img width="2534" height="1869" alt="pca_whale_clusters" src="https://github.com/user-attachments/assets/0dec5311-6a5d-4f71-8914-c1a975f4d96f" />



## 🧠 Interpretation

The results suggest that MFCC-based unsupervised learning can detect acoustic differences within this small collection of whale recordings.

However, the clusters should **not** be interpreted as whale language, behavior, or specific call types. Differences may reflect species, recording conditions, background noise, equipment, or other acoustic factors.

## 🛠 Technologies

- Python
- Librosa
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

## 📁 Repository

- `whale_acoustics.ipynb` — complete analysis and experiments
- `whale_clustering_results.csv` — final clustering results
- `README.md` — project overview

## 🚀 Future Work

Future improvements could include larger datasets, log-Mel spectrogram features, alternative clustering algorithms, and supervised classification using labeled whale recordings.

## ⚠️ Limitations

This is an exploratory project based on only 11 source recordings. Multiple 5-second segments originate from the same recordings, so the 62 segments should not be treated as 62 independent biological samples.



## 📦 Dataset

Whale vocalization recordings used in this project were obtained from the
**NOAA Fisheries Whale Sound Records dataset** available on Kaggle.

Dataset source: [Whale Sounds Dataset on Kaggle](https://www.kaggle.com/datasets/asimmahmudov/whale-sounds-dataset)

The audio files are not included in this repository.



## ▶️ How to Run

1. Download the whale audio dataset.
2. Upload the WAV recordings to Google Colab.
3. Open `whale_acoustics.ipynb`.
4. Install the required Python libraries.
5. Run the notebook cells in order.
