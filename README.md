# iris_data_prediction

A machine learning project that uses **K-Means clustering** to explore patterns in the Iris flower dataset. It includes a Streamlit application, a Jupyter Notebook for clustering and analysis, the Iris dataset, and a saved clustering model.

## Overview

The project applies unsupervised learning to group Iris flower samples according to their measurements. K-Means assigns samples to clusters based on feature similarity; the clusters are not automatically the same as the known Iris species labels.

## Features

- Interactive Streamlit application.
- Uses a saved K-Means clustering model.
- Works with the Iris dataset.
- Includes a notebook for data exploration and clustering.
- Lets users explore clustering results through the web interface.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Streamlit
- Matplotlib / Seaborn (if used in the notebook)
- Jupyter Notebook
- Pickle

## Dataset

The project uses `Iris.csv`.

The standard Iris dataset contains measurements such as:

- Sepal length
- Sepal width
- Petal length
- Petal width

The dataset may also include a species label. K-Means is an unsupervised algorithm, so species labels are not required for clustering. Refer to the notebook and application for the exact columns selected for model input.

## Machine Learning Model

The saved model is:

```text
iris_kmeans_model.pkl
```

The project uses **K-Means clustering**, which groups samples into a chosen number of clusters based on distances between feature vectors.

The notebook `Iris_KMeans_Clustering_Corrected.ipynb` contains the clustering workflow. Consult the notebook for the chosen number of clusters, preprocessing steps, and visualizations. This README does not assume a specific clustering score.

## Repository Structure

```text
iris_data_prediction/
├── app.py
├── Iris.csv
├── Iris_KMeans_Clustering_Corrected.ipynb
├── iris_kmeans_model.pkl
└── README.md
```

The uploaded application file has a timestamp in its filename. Rename it to `app.py` in the repository, or update the run command to match the filename you use.

## Installation

Install the required libraries:

```bash
pip install streamlit pandas numpy scikit-learn matplotlib seaborn jupyter
```

If the app or notebook imports additional libraries, install those as well.

## Run the Application

Place `app.py` and `iris_kmeans_model.pkl` in the same project directory, then run:

```bash
streamlit run app.py
```

Open the local URL printed by Streamlit in your browser.

## How to Use

1. Start the Streamlit application.
2. Open the local application URL.
3. Follow the input controls to provide or explore Iris flower measurements.
4. Review the cluster assignment and any visualizations shown by the application.

The exact input fields and output details are defined in `app.py`.

## Project Files

| File | Purpose |
|---|---|
| `app.py` | Streamlit interface and clustering logic |
| `Iris.csv` | Iris flower dataset |
| `Iris_KMeans_Clustering_Corrected.ipynb` | Data exploration and K-Means workflow |
| `iris_kmeans_model.pkl` | Saved K-Means clustering model |
| `README.md` | Project documentation |

## Limitations

- K-Means cluster assignments depend on feature selection, scaling, and the number of clusters.
- Clusters represent similarity in the chosen measurements and do not automatically correspond to species labels.
- Results depend on the data and preprocessing used during model training.
- Only load Pickle files from trusted sources.

## Future Improvements

- Document the selected features and number of clusters.
- Compare clusters against known species labels for exploratory evaluation.
- Add suitable clustering evaluation metrics such as silhouette score.
- Improve input validation and visualization.
- Deploy the application online.

## Conclusion

`iris_data_prediction` demonstrates an unsupervised machine learning workflow using K-Means to explore Iris flower measurements, with a saved model and an interactive Streamlit application.
