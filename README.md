# IllnessPredictorDataGlaciersW4-5

# 🧠 Illness Prediction Web App

**Project Link:** [https://flasklogisticregressionappdataglaciers.onrender.com](https://flasklogisticregressionappdataglaciers.onrender.com)  
**Dataset:** [Kaggle - Toy Dataset](https://www.kaggle.com/datasets/carlolepelaars/toy-dataset)

---

## 📌 Project Overview

The **Illness Prediction Web App** is a machine learning-based Flask application designed to estimate the probability that a user is affected by an illness, based on demographic inputs like **City**, **Gender**, **Age**, and **Income**.

The model is trained using a logistic regression classifier and achieves an accuracy of **92.08%**.

---

## 📋 Table of Contents

- [Features](#features)  
- [Tech Stack](#tech-stack)  
- [Setup Instructions](#setup-instructions)  
- [How to Use](#how-to-use)  
- [Model Details](#model-details)  
- [Dataset](#dataset)  
- [Insights](#insights)

---

## 🚀 Features

- **Interactive User Input Form**  
  Users can select their City, Gender, and input their Age and Income.

- **Probability-based Predictions**  
  The app returns a **probability score** indicating the chance of the user being affected by an illness.

- **Machine Learning Integration**  
  Built using a Logistic Regression model trained on real-world demographic data.

---

## 🧰 Tech Stack

- **Backend:** Python, Flask  
- **Machine Learning:** scikit-learn (Logistic Regression)  
- **Frontend:** HTML, CSS (via Flask templates)  
- **Database:** None (static CSV dataset used)  
- **Version Control:** Git & GitHub  

---

## 🛠️ Setup Instructions

### Prerequisites

- Python (3.7 or higher)  
- pip (Python package installer)  
- Git (optional, for cloning the repo)  

### Steps to Run Locally

1. **Clone the Repository**
   ```bash
   git clone <your-repo-url>
   cd <your-project-folder>
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Train the Model**
   ```bash
   python train_model.py
   ```

4. **Run the Flask App**
   ```bash
   python main.py
   ```

5. **Visit the App**  
   Open your browser and go to [http://localhost:5000](http://localhost:5000)

---

## 📄 How to Use

1. Navigate to the app in your browser.  
2. Fill in the form with:
   - **City** (from dropdown)
   - **Gender**
   - **Age**
   - **Income**
3. Click **Submit**.
4. The app will return a **predicted probability** of the user having the illness.

---

## 📊 Model Details

- **Model Type:** Logistic Regression  
- **Accuracy:** 92.08% on test data  
- **Input Features:** City (top 10 categories + 'Other'), Gender, Age, Income  
- **Target Variable:** `Illness` (Yes → 1, No → 0)  
- **Encoding:** One-hot encoding for categorical features  

The model outputs a probability between **0 and 1**, where values closer to **1** indicate a higher likelihood of illness.

---

## 📁 Dataset

The dataset used is a publicly available toy dataset containing demographic information and illness status.

| City   | Gender | Age | Income | Illness |
|--------|--------|-----|--------|---------|
| City A | Male   | 34  | 40000  | Yes     |
| City B | Female | 56  | 55000  | No      |
| City A | Female | 23  | 30000  | Yes     |
| City C | Male   | 45  | 60000  | No      |
| City B | Male   | 30  | 45000  | Yes     |

The model simplifies city labels to the top 10 most common entries, encoding them via one-hot encoding. The target (`Illness`) is binarized for model training.

---

## 🔍 Insights

- During testing and experimentation, an interesting pattern was observed:
  
  **As income decreases, the predicted probability of illness tends to increase — regardless of age.**

  This suggests that lower income levels may be correlated with higher health risk in the dataset, potentially due to socio-economic factors. This is a valuable insight that could be explored further with additional data or domain expertise.
