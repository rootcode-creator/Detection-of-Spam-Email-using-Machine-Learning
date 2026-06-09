<h1 align="center">Spam Email Detection using Machine Learning</h1>

<p align="center">
  <img src="https://img.shields.io/badge/STATUS-READY-111827?style=flat-square&labelColor=0F172A" alt="Status" />
  <img src="https://img.shields.io/badge/DOMAIN-NLP%20%2F%20ML-111827?style=flat-square&labelColor=0F766E" alt="Domain" />
  <img src="https://img.shields.io/badge/LICENSE-ACADEMIC-111827?style=flat-square&labelColor=1D4ED8" alt="License" />
</p>

<p align="center">
  <img src="https://cdn.simpleicons.org/gmail/EA4335" alt="Email" width="36" />
  <img src="https://cdn.simpleicons.org/python/3776AB" alt="Python" width="36" />
  <img src="https://cdn.simpleicons.org/scikitlearn/F7931E" alt="Scikit-learn" width="36" />
  <img src="https://cdn.simpleicons.org/jupyter/F37626" alt="Jupyter" width="36" />
</p>

<p align="center"><i>Spam email classification with classical machine learning models.</i></p>

## Project overview

This repository contains a spam email classification workflow that predicts whether an email is spam or ham based on its text features. The project uses classical machine learning models from scikit-learn, along with preprocessing and feature extraction, to turn raw email content into a binary classification problem.

The goal is to provide a compact, reproducible example of email spam detection that can be trained, evaluated, and compared across multiple classifiers.

> **Quick visual summary**
> - Focus: email text classification for spam detection
> - Approach: preprocessing + feature extraction + ML classification
> - Outcome: compare several models and identify the best-performing classifier
> - Dataset: email/spam datasets shared through Google Drive because the file is larger than 25 MB

## Table of contents

- [Project overview](#project-overview)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Installation](#installation)
- [Tools](#tools)
- [Usage](#usage)
- [Results](#results)
- [Project flow](#project-flow)
- [Project structure](#project-structure)
- [Further reading & references](#further-reading--references)
- [License](#license)

## Dataset

The repository includes spam and ham email datasets under the `Datasets/` folder.

- `Datasets/mail_data.csv`
- `Datasets/spam.csv`
- `Datasets/spamham.csv`

Dataset download link: [Google Drive folder](https://drive.google.com/drive/folders/1uQhAePsAJmVBoIGsjlZXsc66UGB2ujP5?usp=sharing)

The data was cleaned and prepared before model training so the classifiers could learn from normalized, noise-reduced text features.

## Methodology

The project follows a standard machine learning pipeline for text classification:

1. Load the email dataset and inspect the label distribution.
2. Clean and preprocess the text data.
3. Transform email text into numerical features.
4. Train multiple classifiers such as Logistic Regression, Decision Tree, Random Forest, Gradient Boosting, AdaBoost, KNN, SVC, Multinomial Naive Bayes, and MLP.
5. Compare model performance and keep the best candidate for prediction.

## Project structure

```txt
.
├── CSE_498_R_PROJECT.ipynb
├── Datasets/
│   ├── mail_data.csv
│   ├── spam.csv
│   ├── spamham.csv
│   └── spam_email dataset link
├── IMAGES/
│   ├── AdaBoostClassifier().png
│   ├── DecisionTreeClassifier().png
│   ├── DecisionTreeClassifier(criterion='entropy').png
│   ├── DummyClassifier(strategy='most_frequent').png
│   ├── GradientBoostingClassifier().png
│   ├── KNeighborsClassifier().png
│   ├── LogisticRegression().png
│   ├── MLPClassifier().png
│   ├── MultinomialNB().png
│   ├── RandomForestClassifier().png
│   ├── SVC().png
│   └── Number of spam and ham mail in dataset plot.png
├── Model Example/
│   └── model.pkl
└── README.md
```

## Installation

```bash
git clone https://github.com/rootcode-creator/Detection-of-Spam-Email-using-Machine-Learning.git
cd Detection-of-Spam-Email-using-Machine-Learning
pip install numpy pandas scikit-learn matplotlib seaborn jupyter
```

If you want to open the notebook, launch Jupyter from the project directory and run `CSE_498_R_PROJECT.ipynb`.

## Tools

- **Python:** primary language used for data preparation and model training.
- **Pandas / NumPy:** dataset loading, cleaning, and feature handling.
- **Scikit-learn:** model training, feature extraction, and evaluation.
- **Matplotlib / Seaborn:** visual analysis and dataset inspection.
- **Jupyter Notebook:** interactive experimentation and reporting.

## Usage

1. Open `CSE_498_R_PROJECT.ipynb` in Jupyter or VS Code.
2. Run the preprocessing and training cells in order.
3. Compare the classifier outputs and plots saved in `IMAGES/`.
4. Use the saved model in `Model Example/model.pkl` for inference experiments.

## Results

The project compares several standard classifiers for spam detection. The images in `IMAGES/` show the model outputs and the label distribution, making it easier to evaluate which classifier performs best for this dataset.

Typical comparison points include:

- Accuracy and generalization across the test split
- Stability of tree-based models versus linear baselines
- Performance of Naive Bayes on text-style features
- Practical trade-offs between precision and recall for spam detection

## Project flow

```text
Email dataset
	↓
Text cleaning and preprocessing
	↓
Feature extraction / vectorization
	↓
Train multiple ML classifiers
	↓
Evaluate and compare results
	↓
Save the best model for prediction
```

## Further reading & references

- Kaggle dataset link included in `Datasets/spam_email dataset link`
- Scikit-learn documentation: https://scikit-learn.org/
- Pandas documentation: https://pandas.pydata.org/
- Jupyter documentation: https://jupyter.org/

## License

This project is intended for academic and educational use. Please credit the original dataset source and the libraries used if you reuse or extend the work.
