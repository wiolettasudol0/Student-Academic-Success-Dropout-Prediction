# Student Academic Success & Dropout Prediction

This project implements, fine-tunes, and evaluates supervised classification algorithms to predict higher education student retention, academic success, and dropout rates using the Portalegre Polytechnic University dataset ($N = 4424$).

The analysis benchmarked three machine learning paradigms—**k-Nearest Neighbors (k-NN)**, **C5.0 Decision Trees** (with adaptive boosting), and **Naive Bayes Classifiers** (with Laplace smoothing)—identifying the primary demographic, economic, and academic indicators associated with student outcomes.

## Methods
* **Data Preprocessing & Encoding:**
  * **Feature Scaling:** Z-score standardization (`scale()`) across continuous features for distance-based k-NN optimization.
  * **Categorical Encoding:** Explicit factor transformations on socio-economic and demographic indicators (e.g., parental qualifications, occupation codes, scholarship status).
* **Supervised Classifiers:**
  * **k-NN:** Hyperparameter grid search across $k \in [1, 25]$ on standardized feature space.
  * **C5.0 Decision Trees:** Standard recursive partitioning vs. 10-trial AdaBoost ensemble boosting.
  * **Naive Bayes:** Gaussian/Categorical likelihood estimator vs. Laplace-smoothed regularized estimator (`laplace = 1`).
  * **Evaluation Metrics:** Multi-class Confusion Matrices (`gmodels::CrossTable`), class-level distributions, and overall prediction accuracy.

## Project Structure
* Academic performance records dataset (`students_data`)
* Model training and evaluation script (`Projekt_WdAD.Rmd`)
* Report with confusion matrix outputs (`Projekt_WdAD.pdf`)

## Authors
* Aneta Buszta
* Klaudia Czarny
* Wioletta Sudoł
