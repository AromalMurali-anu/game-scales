 Video Game Sales Analysis & Feature Selection (Machine Learning Project)

This repository contains a complete data preprocessing and feature-selection workflow applied to a video-game sales dataset. The project includes:

Exploratory Data Analysis (EDA)

Handling missing values

One-Hot Encoding for categorical variables

Feature selection using SelectKBest

Visualisation of numeric features

Python script + Jupyter Notebook

📂 Project Structure
├── data/
│   └── game_sales.csv
├── notebooks/
│   └── game_sales.ipynb
├── scripts/
│   └── feature_selection.py
└── README.md

🧠 Project Description

This project analyses a video-game sales dataset containing information such as:

Game name

Platform

Genre

Publisher

Sales in NA, EU, JP, Other regions

Critic Score

User Score

The purpose is to:

Preprocess the dataset

Convert categorical columns using OneHotEncoder

Select the most important features using SelectKBest (f_regression)

Visualise numeric data trends

📊 Key Features
✔️ Exploratory Data Analysis (EDA)

The notebook includes:

Distribution plots

Category counts

Correlation heatmaps

Missing value checks

✔️ Data Preprocessing

Label encoding

One-hot encoding of non-numeric columns

Handling missing values

Converting object columns to numeric

✔️ Feature Selection

Using Scikit-Learn:

selector = SelectKBest(score_func=f_regression, k=10)
X_selected = selector.fit_transform(X_encoded, y)

✔️ Plotting All Numeric Columns
numeric_cols = df.select_dtypes(include=['int64', 'float64']).columns

for col in numeric_cols:
    plt.figure(figsize=(10, 5))
    plt.plot(df[col], label=col)
    plt.title(col)
    plt.xlabel("Index")
    plt.ylabel("Value")
    plt.legend()
    plt.show()

🛠️ Technologies Used

Python

Pandas

NumPy

Scikit-Learn

Matplotlib

Jupyter Notebook

🚀 How to Run This Project
1️⃣ Clone the repo
git clone https://github.com/your-username/game-sales-analysis.git
cd game-sales-analysis

2️⃣ Install dependencies
pip install -r requirements.txt

3️⃣ Run the Jupyter notebook
jupyter notebook

4️⃣ Run the Python script
python scripts/feature_selection.py

📈 Results

Successfully transformed categorical data with OneHotEncoder

Selected top k=10 most important features

Generated visualisations for all numeric columns

Clean and processed dataset ready for machine-learning models

📜 License

This project is licensed under the MIT License.

🤝 Contributions

Pull requests and suggestions are welcome!
