🎵 Music Popularity Classification Project 🎵

Course: DA380A – Machine Learning, Seminar 2: Classification Models

Project Purpose:

The purpose of this project is to learn how to build, analyze, and evaluate classification models using a real dataset.

Objectives:

Explore the dataset and visualize interesting relationships.

Build at least two classification-based ML models to predict a target variable.

Analyze each model and answer the following:

How does the model perform? (evaluation metrics)

What steps were taken to improve the model?

What improvements were achieved after tuning?

Which algorithm is recommended for this dataset and why?

Dataset

The dataset contains music tracks with features related to popularity.

Target variable: popularity_target (0 = Low, 1 = High), derived from the median popularity.

Features include numeric audio descriptors and song metadata.

Columns removed during preprocessing: artist, song, album_name, release_date, hour, date, and others with >30% missing values.

Data Preprocessing

Removed duplicates and empty strings.

Dropped columns with >30% missing values.

Handled missing values using median imputation.

Handled outliers using IQR capping.

Features were scaled using StandardScaler for Logistic Regression.

Exploratory Data Analysis

Visualized distribution of numeric features.

Observed correlation between audio features and popularity.

Checked target distribution: fairly balanced after median split.

Models Built

Logistic Regression

Baseline and tuned with GridSearchCV over parameter C.

Decision Tree Classifier

Baseline with Gini and Entropy criteria.

Tuned using GridSearchCV over max_depth, min_samples_split, and min_samples_leaf.

Model Evaluation

Metrics used: Accuracy, Precision, Recall, F1-score.

Model	Accuracy	Precision	Recall	F1-score

Logistic Regression (baseline)	0.67	0.66	0.72	0.69

Logistic Regression (tuned)	0.67	0.66	0.72	0.69

Decision Tree (Gini baseline)	0.88	0.83	0.96	0.89

Decision Tree (Entropy baseline)	0.86	0.95	0.76	0.84

Decision Tree (tuned)	0.97	0.96	0.98	0.97


Confusion matrices and bar charts were used for visual comparison.

Feature importance plots highlighted the most influential features.

Steps Taken to Improve Models

Imputation for missing values.

Feature scaling for Logistic Regression.

Outlier treatment using IQR.

Hyperparameter tuning using GridSearchCV with cross-validation.

Results of Tuning

Logistic Regression showed no improvement after tuning (limited predictive power).

Decision Tree significantly improved:

Tuned DT achieved 97% accuracy, 96% precision, 98% recall, 97% F1-score.

Balanced performance between false positives and false negatives.

Recommendation

Tuned Decision Tree is recommended for this dataset:

High predictive performance.

Balanced precision and recall.

Easy to interpret via feature importance and tree visualization.

Logistic Regression can be used for baseline comparison or when model simplicity is needed.

How to Run

Clone repository:

git clone https://


Install dependencies:

pip install -r requirements.txt


Open the Jupyter notebook and run cells sequentially.

Project Highlights

End-to-end ML workflow: preprocessing → model training → evaluation → conclusions.

Clear documentation with comments explaining each code cell.

Visualizations: confusion matrices, F1-score comparison, feature importance, tree plot.
