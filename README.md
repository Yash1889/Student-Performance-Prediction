# Student Performance Prediction using Machine Learning

**Project:** Student Performance Prediction  
**Candidate:** Yashraj Gupta  
**Program context:** AICTE | IBM SkillsBuild Data Analytics with AI Internship 2026 | BharatCares

This repository contains a machine-learning project that predicts a student's final mathematics grade (`G3`, on a 0–20 scale) using student demographic, family, study-habit, and prior-grade features. The repository includes a Jupyter notebook, Python dependencies, a project report, and this README.

> **Attribution note:** This repository is a copy/adaptation of an existing project. Please retain appropriate attribution to the original author and verify that reuse is permitted by the internship before submitting it as your own work.

## Required submission files

| File | Format | Purpose |
|---|---|---|
| `YashrajGupta_StudentPerformancePrediction.ipynb` | Jupyter Notebook | Project code and analysis |
| `requirements.txt` | Text | Python dependencies |
| `YashrajGupta_StudentPerformancePrediction_ProjectReport.docx` | Word document | Project report |
| `README.md` | Markdown | Project overview and instructions |

## Project overview

The project uses a Random Forest regression model to estimate the final grade (`G3`) from features in the Student Performance dataset. It includes data analysis and visualizations, preprocessing, model training, and evaluation. The repository also contains a Flask backend and a React/Vite frontend.

- **Language:** Python
- **Data analysis:** pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine learning:** scikit-learn
- **Model persistence:** Joblib
- **Backend:** Flask
- **Frontend:** React and Vite
- **Notebook:** Jupyter

## Dataset

The project references the UCI Student Performance dataset, commonly distributed through Kaggle:

- [Kaggle — Student Alcohol Consumption / Student Performance](https://www.kaggle.com/datasets/uciml/student-alcohol-consumption)
- [UCI Machine Learning Repository — Student Performance](https://archive.ics.uci.edu/dataset/320/student+performance)

The mathematics dataset (`student-mat.csv`) contains 395 records and 33 columns. The target is `G3`, the final grade on a 0–20 scale. Features include prior grades (`G1`, `G2`), study time, past failures, absences, and parental education. Check the dataset's terms and documentation before reuse.

## Model and evaluation

The project describes a `RandomForestRegressor` with 100 trees and `random_state=42`, an 80/20 train-test split, and one-hot encoding using pandas. The existing project README reported the following evaluation metrics; treat them as reported results and rerun the notebook to independently verify them against the included code and data.

| Metric | Previously reported value |
|---|---:|
| R² | 0.8148 |
| MAE | 1.1646 |
| MSE | 3.7977 |
| RMSE | 1.9488 |

## Project workflow

1. Load the student performance dataset.
2. Inspect and clean the data.
3. Perform exploratory data analysis and create visualizations.
4. Encode categorical variables and split the data into training and test sets.
5. Train the Random Forest regression model.
6. Evaluate predictions using R², MAE, MSE, and RMSE.
7. Save the model for use by the Flask API and frontend.

## Setup and run

Run commands from the repository root.

### 1. Create a virtual environment and install Python dependencies

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 2. Run the notebook

```bash
jupyter notebook YashrajGupta_StudentPerformancePrediction.ipynb
```

Open the notebook and run its cells in order. Confirm the dataset path used by the notebook matches the files in the `data/` directory.

### 3. Run the Flask backend

```bash
python backend/app.py
```

If this fails, check the backend's expected working directory, model-file path, and configuration before running it again.

### 4. Run the frontend

```bash
cd frontend
npm install
npm run dev
```

Use the local URL printed by Vite in the terminal. The port may vary depending on the frontend configuration.

## Repository layout

```text
.
├── backend/       # Flask API and model-training code
├── data/          # Dataset files (if included)
├── figures/       # Exploratory analysis and evaluation plots
├── frontend/      # React/Vite interface
├── models/        # Saved model artifacts
├── YashrajGupta_StudentPerformancePrediction.ipynb
├── YashrajGupta_StudentPerformancePrediction_ProjectReport.docx
├── requirements.txt
└── README.md
```

Some files or subdirectories may differ from this overview; the repository contents are the source of truth.

## Important before submission

- Ensure the notebook, report, and README agree on the project title, dataset, methods, and results.
- Confirm the notebook runs and its outputs are present.
- Do not describe reported metrics as independently verified unless you rerun the notebook.
- Preserve original authorship attribution and follow the internship's rules for reused or adapted work.
