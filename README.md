# 🌸 Iris Classification ML Project with DVC Tracking and CI (GitHub Actions)

This project demonstrates a **production-style machine learning workflow** that combines:

- Data & model versioning with **DVC**
- Automated testing with **pytest**
- Continuous Integration using **GitHub Actions**
- Experiment reproducibility with **CML reports**

The repository simulates a real-world ML development lifecycle with **branch-based CI**, automated validation, and reproducible pipelines.

---

## 🎯 Assignment Objective

- Set up Iris Classification training pipeline in a GitHub repository  
- Maintain two branches: `dev` and `main`  
- Implement **data validation and model evaluation tests**  
- Configure **CI using GitHub Actions**  
- Fetch model and data from **DVC remote storage**  
- Trigger CI on push and pull requests for both branches  
- Generate sanity test report as a **CML comment**  
- Follow a proper **PR workflow from dev → main**

---

## 🗂️ Repository Structure

```
├── data/ # Dataset tracked with DVC
│ └── iris.csv
├── model/ # Trained model artifact
│ └── iris_model.pkl
├── src/
│ └── train.py # Training script
├── tests/
│ ├── test_data_validation.py # Data validation tests
│ └── test_model_evaluation.py # Model evaluation tests
├── requirements.txt # Dependencies for CI
├── .github/workflows/
│ ├── ci-dev.yml # CI pipeline for dev branch
│ └── ci-main.yml # CI pipeline for main branch
├── week4_GA_setup.ipynb # Setup notebook
└── README.md
```


---

## 📁 Files Description

### 1️⃣ data/

**Purpose:**  
Stores the Iris dataset (`iris.csv`) tracked with DVC.

---

### 2️⃣ model/

**Purpose:**  
Contains the trained Iris classification model artifact.

---

### 3️⃣ src/train.py

**Key Functions:**

- Loads dataset from `data/iris.csv`  
- Trains a `RandomForestClassifier`  
- Saves trained model to `model/` directory  

---

### 4️⃣ tests/

#### test_data_validation.py
- Validates schema, null values, and dataset integrity  

#### test_model_evaluation.py
- Evaluates model performance metrics  
- Ensures model meets minimum accuracy threshold  

---

### 5️⃣ requirements.txt

Contains dependencies required to run:

- Training pipeline  
- Unit tests  
- CI workflow  

---

### 6️⃣ GitHub Actions Workflows

#### `.github/workflows/ci-dev.yml`
- Runs CI on **push and pull request to dev branch**

#### `.github/workflows/ci-main.yml`
- Runs CI on **push and pull request to main branch**

**CI Pipeline Steps:**

1. Checkout repository  
2. Pull data and model from DVC remote  
3. Install dependencies  
4. Run pytest  
5. Execute sanity checks  
6. Generate CML report comment  

---

### 7️⃣ week4_GA_setup.ipynb

**Purpose:**  
Notebook used to set up the project environment.

**Includes:**

- Git repository initialization  
- Branch setup (`dev`, `main`)  
- DVC configuration with GCS remote  
- GitHub Actions workflow creation  
- Pushing code to GitHub  

---

## ⚙️ Tech Stack

- Python  
- Scikit-learn  
- DVC (Data Version Control)  
- Git & GitHub  
- GitHub Actions  
- Pytest  
- CML (Continuous Machine Learning)  
- Google Cloud Storage (GCS)  

---

## 🔄 CI Workflow Overview

1. Developer pushes code to `dev`  
2. CI pipeline runs automatically  
3. Tests validate data and model  
4. CML posts report on PR  
5. PR merged into `main`  
6. Main branch CI validates production pipeline  

---

## 🎥 Video Presentation  
[▶️ Click Here](https://drive.google.com/file/d/1CGeGB1toJF41kvyLthlVbEpgCEYZqJf2/view?usp=drive_link)
