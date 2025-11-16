📚 Library Management Model – Data Preprocessing & Scaling (Python / ML)

This project demonstrates how to preprocess a dataset and apply different data-scaling techniques such as MaxAbsScaler, Label Encoding, and detection of numeric features using pandas. It is part of a Machine Learning pipeline for preparing clean and normalized data.

✨ Features
✅ 1. Data Cleaning

Detects numeric and non-numeric columns

Automatically encodes categorical features

Handles missing values (if added in future)

✅ 2. Feature Scaling

Uses MaxAbsScaler to scale numeric features into the range [-1, 1].

✅ 3. Label Encoding

Applies LabelEncoder on categorical columns automatically.

✅ 4. Modular & Easy-to-Understand Code

Clean steps that you can reuse in any ML project.

📂 Project Structure
Librarymodel.ipynb       # Jupyter Notebook containing the full project code
README.md                # Project documentation

🚀 Technologies Used
Library	Purpose
Pandas	Dataset manipulation
Scikit-learn	Scaling & Encoding
NumPy	Numerical operations
Jupyter Notebook	Code execution
🧠 Code Overview
🔹 Import Required Libraries
from sklearn.preprocessing import MaxAbsScaler, LabelEncoder
from pandas.api.types import is_numeric_dtype
import pandas as pd

🔹 Apply Label Encoding + MaxAbs Scaling
le = LabelEncoder()
scaler = MaxAbsScaler()

for col in df.columns:
    if is_numeric_dtype(df[col]):
        df[[col]] = scaler.fit_transform(df[[col]])
    else:
        df[col] = le.fit_transform(df[col])

🧪 How It Works

Checks each column type

If numeric → MaxAbsScaler

If categorical → LabelEncoder

Replaces original column with transformed values

Output is a clean, machine-learning-ready dataset

📊 Example Output
Column	Before	After
Price	1499	0.84
Category	"Science"	2
Stock	200	0.32
📘 Use Cases

Library Management Systems

Book Recommendation Models

Inventory Data Normalization

ML preprocessing tasks

🛠 How to Run

Install dependencies:

pip install pandas scikit-learn


Open the notebook:

jupyter notebook Librarymodel.ipynb


Run all cells to preprocess your dataset.

🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to improve.
