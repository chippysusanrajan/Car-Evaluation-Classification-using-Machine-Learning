# 🚗 Car Evaluation Classification using Machine Learning

## 📌 Project Overview
This project simulates a real-world **automobile industry classification problem**, where the goal is to predict the **overall evaluation level of a car** based on its technical and safety-related attributes.

As a Data Scientist, the task was to build and evaluate a **supervised machine learning model** capable of classifying cars into one of four categories:
- **Unacceptable**
- **Acceptable**
- **Good**
- **Very Good**

The project demonstrates an end-to-end ML workflow including data preprocessing, model selection, training, and evaluation.

---

## 📊 Dataset Description
The dataset contains multiple car evaluations, with each record consisting of the following **categorical features**:

| Feature     | Description              | Role     | Values                          |
|------------|---------------------------|----------|---------------------------------|
| buying     | Buying price              | Feature  | vhigh, high, med, low           |
| maint      | Maintenance cost          | Feature  | vhigh, high, med, low           |
| doors      | Number of doors           | Feature  | 2, 3, 4, 5more                  |
| persons    | Passenger capacity        | Feature  | 2, 4, more                      |
| lug_boot   | Luggage boot size         | Feature  | small, med, big                 |
| safety     | Estimated safety level    | Feature  | low, med, high                  |
| class      | Car evaluation            | **Target**  | unacc, acc, good, vgood         |

📁 **Dataset file:** `car_evaluation.csv`

---

## 🎯 Objective
To evaluate the performance of a **classification model** (Decision Tree or Naive Bayes) in predicting car evaluation levels based on categorical features.

---

## 🛠️ Tech Stack
- **Programming Language:** Python  
- **Libraries:** Pandas, NumPy, scikit-learn  
- **ML Techniques:** Classification, Model Evaluation & Selection (Naive Bayes or Decision Tree) 
- **Metrics:** Accuracy, Precision, Recall, F1-score, Confusion Matrix  

---

## 🔄 Methodology

### 1️⃣ Data Splitting
- Split the dataset into **training and test sets** using an appropriate ratio to ensure unbiased evaluation.

### 2️⃣ Data Preprocessing
To ensure the dataset was suitable for machine learning, several preprocessing steps were applied:
- Standardised column names by converting all feature labels to lowercase
- Replaced ambiguous categorical values (`"more"`, `"5more"`) in `doors` and `persons` with their numeric maximum (`5`)
- Converted `doors` and `persons` into numerical variables
- Replaced missing values (`NaN`) with `0`
- Removed rows containing only missing values
- Encoded all categorical features into numerical format for model compatibility
  
These steps ensured consistency, reduced ambiguity, and improved model reliability.

### 3️⃣ Model Selection & Parameter Tuning
The dataset was split into:
- **80% training data**
- **20% testing data**

Two classification models were implemented and evaluated:

- **Decision Tree Classifier**
- **Naive Bayes Classifier**

Both models were trained on the same preprocessed dataset to ensure a fair comparison.

### 4️⃣ Model Training and Performance Comparison
| Model         | Accuracy |
|--------------|----------|
| Decision Tree | **97%**  |
| Naive Bayes   | 63%      |

The **Decision Tree Classifier** significantly outperformed Naive Bayes and was therefore selected as the final model.

### 5️⃣ Model Evaluation
Evaluated the model using:
- Classification Accuracy  
- Confusion Matrix  
- Precision, Recall, and F1-score  

These metrics provided insight into both overall performance and class-wise prediction quality.

---

## 📈 Results & Insights
- The model successfully classified cars into quality categories with strong predictive performance.
- **Safety, buying price, and maintenance cost** were identified as influential features.
- High precision and recall across most classes indicate a well-balanced and reliable classifier
- Strong performance on the **“good”** category, which is the majority class in the dataset
- Slightly lower performance on the **“very good”** class, likely due to fewer training samples
- The model handled incomplete or ambiguous records without significant degradation in performance

Overall, the classifier demonstrated **high accuracy with minimal false positives and negatives**.

---

## 💼 Business Impact
This model demonstrates how machine learning can assist automobile companies in:
- Automating car quality assessment
- Reducing manual inspection effort  
- Supporting pricing and product positioning strategies  
- Enhancing decision-making in manufacturing and sales pipelines
   
Such a model can be integrated into **manufacturing quality checks** or **pre-sale evaluation systems**.

---

## 📂 Repository Structure
├── data/  
│   └── car_evaluation.csv  
├── notebooks/  
│   └── car_evaluation_ml.ipynb    
├── report/  
│   └── car_evalutaion_ml_report.pdf    
├── README.md  

---

## 🚀 How to Run This Project

1. Clone the repository:

git clone https://github.com/chippysusanrajan/Car-Evaluation-Classification-using-Machine-Learning.git

2. Install dependencies

3. Run the notebook or script to train and evaluate the model.

---


---

## 👩‍💻 Author
**Chippy Susan Rajan**  
Master of Data Science and Decisions, UNSW  
📎 [LinkedIn](https://www.linkedin.com/in/chippy-susan-rajan-b1433ab2/)  
🐙 [GitHub](https://github.com/chippysusanrajan)

---

## 📄 License
This project is for academic and portfolio purposes.

