# Iris Classification ML Project with DVC Tracking and Continuous Integration (CI) with GitHub Actions

**MLOps - Week 2 - Assignment - 21f1000344**

## Assignment Objective : 
- Setup IRIS Classification Training pipeline into a GitHub repository with two branches dev and main
- Create evaluation and data validation unit tests using pytest or unittest
- For evaluation and testing, configure the Continuous Integration (CI) with GitHub Actions to fetch the model and data needed for evaluation from DVC configured in Week-3
- Push inclusion of pytest code changes to dev branch and raise Pull Request to main branch
- Every branch should have its own CI on push or PR merge
- Run a sanity test using GitHub actions printing a report as a comment using cml


---

## Files

### 1. `data` folder
- **Key Utilities:**
  - Stores `iris.csv` data

### 2. `model` folder
- **Key Utilities:**
  - Stores the trained iris classification model

### 3. `src/train.py`
- **Key Utilities:**
  - Loads the `iris.csv` 
  - Trains a `RandomForestClassifier` model

### 4. `tests/test_data_validation.py` and `tests/test_model_evaluation`
- **Key Utilities:**
  - Runs unit tests using pytest on data and model

### 5. `requirements.txt`
- **Key Utilities:**
  - List of required packages for the Continuous Integration (CI) with GitHub Actions

### 6. `.github/worflows/ci-dev.yml` and `.github/worflows/ci-main.yml`
- **Key Utilities:**
  - YAML file for configuring GitHub Actions to perform Continuous Integration (CI)
  - `ci-dev.yml` perfroms CI for `dev` branch on push and pull request
  - `ci-main.yml` perfroms CI for `main` branch on push and pull request
  - On push, CI for the respective branch will be triggered
  - On pull request, CI for the both the branch be triggered
  - Fetches the model and data needed for evaluation from DVC
  - Runs sanity test and prints report as a comment using cml

### 7. `week4_GA_setup.ipynb`
- **Key Utilities:**
  - Created in Vertex AI workbench
  - Serves as an interface for performing actions local working directory
  - Setup Git Repository with `dev` and `main` branch
  - Setup DVC with GCS bucket as remote storage
  - Created YAML file for GitHub Actions

---
  - Pushed the local working directory to remote repo on GitHub

---
