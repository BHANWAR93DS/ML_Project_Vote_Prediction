# ML_Project_Vote_Prediction

Logistic Regression for Voting Intention Prediction
This project builds a binary classification model using Logistic Regression to predict voting intention (e.g., Labour vs Conservative) based on demographic, economic perception, and political attitude features.
The aim is to understand which factors influence vote choice and to create an interpretable baseline model using a survey dataset inspired by British Election Studies.

📁 Dataset
The dataset includes one target variable and several explanatory features.
Target
vote → encoded as 0/1 for the two major parties.
Features
Examples of predictors used:

age
economic.cond.national
economic.cond.household
Blair (leader evaluation)
Hague (leader evaluation)
Europe (EU attitude scale)
political.knowledge
gender
Place your CSV file in a data/ folder:

data/
└── voting_data.csv

🔍 Methods
Train–test split to evaluate generalization
Feature scaling (StandardScaler)
Logistic Regression (scikit-learn)
Evaluation metrics:
Accuracy
Precision
Recall
F1-score
Confusion Matrix
This creates a simple, interpretable baseline model.

📊 Results
Training Performance
Confusion Matrix

[[217 105]
[ 66 673]]

Metrics
Class 0
Precision: 0.77
Recall: 0.67
F1-score: 0.72
Class 1
Precision: 0.87
Recall: 0.91
F1-score: 0.89
Accuracy: 0.84
Model performs better on class 1, while class 0 is harder to classify.

Test Performance

Confusion Matrix
[[ 88  50]
[ 25 293]]
Metrics
Class 0 → F1: 0.70
Class 1 → F1: 0.89
Accuracy: 0.84
Training and test results are similar → no major overfitting.

🧠 Interpretation:

High recall for class 1 → model captures most class-1 voters (good when missing these voters is costly).
Lower recall for class 0 → room for improvement via:
Better feature engineering
Handling class imbalance
Trying more flexible models (tree-based, ensemble, etc.)

📂 Project Structure:
project/
├── data/
│   └── voting_data.csv
│
├── notebooks/
│   └── 01_logistic_regression_voting.ipynb
│
├── src/
│   ├── data_preprocessing.py
│   ├── train_model.py
│   └── evaluate_model.py
│
└── README.md

⚙️ How to Run:
1. Create and activate a virtual environment

python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows

2. Install dependencies
pip install -r requirements.txt

3. Run the notebook or script
Open the notebook in notebooks/
Or run: python src/train_model.py


