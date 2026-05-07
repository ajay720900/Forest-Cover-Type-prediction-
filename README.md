
# Forest Cover Type Prediction Using Machine Learning

## Project Overview

This project focuses on predicting **Forest Cover Types** using different Machine Learning algorithms. The dataset is trained on environmental and geographical features such as elevation, slope, soil type, and wilderness area.

The notebook performs:

* Data loading and preprocessing
* Exploratory data analysis
* Model training and testing
* Prediction system creation
* Model saving using Pickle

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Pickle
* Jupyter Notebook

---

## Dataset Information

The dataset contains different environmental attributes used to classify forest cover types.

### Features Used

Some important features include:

* Elevation
* Aspect
* Slope
* Horizontal Distance to Hydrology
* Vertical Distance to Hydrology
* Horizontal Distance to Roadways
* Hillshade values
* Horizontal Distance to Fire Points
* Wilderness Area
* Soil Type

### Target Variable

* `Cover_Type`

---

## Project Workflow

### 1. Import Libraries

The project starts by importing required Python libraries.

```python
import pandas as pd
import numpy as np
```

---

### 2. Load Dataset

```python
df = pd.read_csv('train.csv')
```

---

### 3. Data Exploration

The dataset is explored using:

```python
df.head()
df.info()
df.shape
df.isnull().sum()
df.duplicated().sum()
```

---

### 4. Split Features and Labels

```python
X = df.drop('Cover_Type', axis=1)
y = df['Cover_Type']
```

---

### 5. Train-Test Split

```python
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
```

---

## Machine Learning Models Used

### Logistic Regression

```python
from sklearn.linear_model import LogisticRegression
```

### Decision Tree Classifier

```python
from sklearn.tree import DecisionTreeClassifier
```

### K-Nearest Neighbors (KNN)

```python
from sklearn.neighbors import KNeighborsClassifier
```

### Random Forest Classifier

```python
from sklearn.ensemble import RandomForestClassifier
```

---

## Model Prediction

The project includes a prediction system where custom input values are passed to the trained model.

Example:

```python
prediction = rfc.predict(features)
```

---

## Saving the Model

The trained model is saved using Pickle.

```python
import pickle
```

---

## How to Run the Project

### Step 1: Clone the Repository

```bash
git clone <repository-link>
```

### Step 2: Install Dependencies

```bash
pip install pandas numpy scikit-learn jupyter
```

### Step 3: Run the Notebook

```bash
jupyter notebook
```

Open the notebook and run all cells.

---

## Project Structure

```
Forest-Cover-Type-Prediction/
│
├── train.csv
├── Forest Cover Type prediction Using Machine learning.ipynb
├── model.pkl
└── README.md
```

---

## Future Improvements

* Hyperparameter tuning
* Feature engineering
* Model deployment using Flask or Streamlit
* Accuracy improvement using advanced ensemble methods

---

## Author
Ajay Kumar
Email: ajay62015k@gmail.com
www.linkedin.com/in/ajay7209


This project is created for educational and learning purposes.
