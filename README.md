# Introduction to Machine Learning and Applied Artificial Intelligence

![status](https://img.shields.io/badge/status-active--development-yellow)
![python](https://img.shields.io/badge/python-3.10%2B-blue)
![notebooks](https://img.shields.io/badge/notebooks-12-informational)

> Coursework, exercises, and worked solutions from **Introduction to Machine Learning
> and Applied Artificial Intelligence**, High School of Digital Culture, ITMO
> University.

This repository is a cleaned-up, tutorial-style rewrite of the course's practical
exercises. Every notebook was reworked from the original coursework into a
self-contained walkthrough: the task is restated in plain language, the code is
commented end to end, and each notebook ends with a short summary of what the results
actually mean — not just what number came out.

The topics move from basic statistics up through supervised learning, unsupervised
learning, ensembling, and a taste of computer vision — roughly the order you'd want to
learn them in.

---

## 📚 Notebooks

| # | Notebook | Topic | Key techniques |
|---|----------|-------|-----------------|
| 01 | [Introduction: Descriptive Statistics](01_Introduction_Descriptive_Statistics.ipynb) | Warm-up: mean, median, variance | `pandas`, basic descriptive stats |
| 02 | [PCA — Exercise 2.1](02_PCA_Exercise_2_1.ipynb) | Dimensionality reduction basics | `PCA`, explained variance |
| 03 | [PCA — Exercise 2.2](03_PCA_Exercise_2_2.ipynb) | Reconstructing an image from its principal components | PCA inverse transform, score/loading matrices |
| 04 | [Regression — Exercise 3.1](04_Regression_Exercise_3_1.ipynb) | Simple linear regression, derived by hand | Least squares, $R^2$ |
| 05 | [Regression — Exercise 3.2](05_Regression_Exercise_3_2.ipynb) | Predicting fish weight with feature engineering | PCA, non-linear feature transforms, one-hot encoding |
| 06 | [Classifiers: k-NN & Naive Bayes](06_Classifiers_kNN_NaiveBayes_Exercise_4.ipynb) | Distance-based & probabilistic classification | `KNeighborsClassifier`, manual Naive Bayes |
| 07 | [Logistic Regression — Exercise 5](07_Logistic_Regression_Exercise_5.ipynb) | Titanic survival prediction | `LogisticRegression`, missing-data strategies |
| 08 | [Clustering — Exercise 6.1](08_Clustering_Exercise_6_1_KMeans_MNIST.ipynb) | Unsupervised digit recognition | `KMeans`, `t-SNE`, cluster-to-label mapping |
| 09 | [Clustering — Exercise 6.2](09_Clustering_Exercise_8_Gaussian_Mixtures.ipynb) | Generating new digit images | `GaussianMixture`, AIC model selection |
| 10 | [Clustering 2 — Exercise 7](10_Clustering_Exercise_7_KMeans_Image_Compression.ipynb) | Image color quantization | `MiniBatchKMeans` |
| 11 | [Ensemble Learning — Exercise 9](11_Ensemble_Learning_Exercise_9.ipynb) | Comparing 6 ensemble methods | Random Forest, Voting, Bagging, Gradient Boosting, AdaBoost, Stacking |
| 12 | [Computer Vision — Exercise 11](12_Computer_Vision_Exercise_11.ipynb) | Evaluating an object detector | YOLOv3, precision/recall/F1 |

---

## 🗂️ Repository structure

```
.
├── README.md
├── requirements.txt
├── data/                                            # small/public datasets used by the notebooks
│   └── spb_st_isaacs_2.jpg
├── 01_Introduction_Descriptive_Statistics.ipynb
├── 02_PCA_Exercise_2_1.ipynb
├── 03_PCA_Exercise_2_2.ipynb
├── 04_Regression_Exercise_3_1.ipynb
├── 05_Regression_Exercise_3_2.ipynb
├── 06_Classifiers_kNN_NaiveBayes_Exercise_4.ipynb
├── 07_Logistic_Regression_Exercise_5.ipynb
├── 08_Clustering_Exercise_6_1_KMeans_MNIST.ipynb
├── 09_Clustering_Exercise_8_Gaussian_Mixtures.ipynb
├── 10_Clustering_Exercise_7_KMeans_Image_Compression.ipynb
├── 11_Ensemble_Learning_Exercise_9.ipynb
└── 12_Computer_Vision_Exercise_11.ipynb
```

---

## 🚀 Getting started

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
```

### 2. Set up the environment

```bash
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Download the datasets

Most notebooks pull their data directly from a public URL and need no setup at all.
A few originally relied on the course author's private Google Drive; for those, this
repo expects the file locally under `data/`. Grab each one from the link below and
place it as shown, and everything will run top to bottom:

| Notebook | Expected path | Source |
|---|---|---|
| 01 — Descriptive Statistics | `data/salary_and_population.csv` | [Google Drive link](https://drive.google.com/file/d/1YrEIn6JNWW0RG0r8nV0P6S55TBXcxSna/view?usp=drive_link) |
| 06 — k-NN / Naive Bayes | `data/adult_data_train.csv` | [Google Drive link](https://drive.google.com/file/d/1CEHmYbLl-rTw2noXfKTdzPu2_Jte6U19/view?usp=sharing) |
| 07 — Logistic Regression | `data/titanic_train.csv` | [Google Drive link](https://drive.google.com/file/d/1qTELQc2Nvl8gx_PRWhuuo22eskHL2za2/view?usp=sharing) |
| 11 — Ensemble Learning | `data/electricity_train.csv` | Provided with the original course materials |

`data/spb_st_isaacs_2.jpg` (used in notebook 10) is already included in this repo, so
that one works right out of the box.

Notebook 12 (Computer Vision) is a special case — instead of a dataset, its setup cell
clones two public GitHub repositories and downloads pretrained YOLOv3 weights
automatically. No manual download needed there either.

### 4. Run

```bash
jupyter lab
```

...and open any notebook. They're independent of each other, so feel free to jump
around rather than working through them in order.

---

## 🧭 How each notebook is organized

Every notebook follows the same shape, so once you're used to one, you're used to
all of them:

1. **Task** — the original assignment, restated plainly.
2. **Setup** — imports and data loading, with notes on any preprocessing decisions.
3. **Step-by-step sections** — each transformation or model gets its own section:
   a short explanation of *why* we're doing this step, followed by clearly commented
   code.
4. **Summary** — a closing recap of the results and what they actually tell us,
   including any surprising or counter-intuitive findings along the way.

Where the original coursework had a bug, an incomplete cell, or a Colab-only
dependency (Google Drive mounts, deprecated library parameters, etc.), it's been
fixed and flagged inline rather than silently patched over.

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat-square&logo=scipy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=flat-square&logo=keras&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat-square)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=flat-square)

---

## 📄 License & attribution

The exercises and datasets originate from the **Introduction to Machine Learning and
Applied Artificial Intelligence** course at the High School of Digital Culture, ITMO
University (`dc@itmo.ru`). This repository contains an independent, rewritten set of
solutions and explanations produced for personal study and portfolio purposes.

If you're taking this course yourself: use this repo to check your understanding
after attempting the exercises on your own — that's where the actual learning
happens.
