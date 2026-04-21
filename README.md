# Student Mental Analysis/Prediction

another small project to learn Data Analysis and classification, and learning over-fitting the hard way because i chose the wrong dataset.

- Dataset: [Student Mental Survey](https://www.kaggle.com/datasets/willianoliveiragibin/student-mental)
- Model Score: 91.4% Accuracy (±4.9% Standard Deviation via 5-Fold Cross-Validation)

## File structure

```text
    student-mental-health-prediction
        ├── 📂 data
        │   └── 📄 MentalHealthSurvey_new.csv
        ├── 📂 src
        │   └── 📓 main.ipynb
        ├── 📄 student_mental_health_bot.pkl
        ├── 📄 model_columns.pkl
        └── 📄 README.md
```

## Libraries Used:

- Numpy: Math and array operations.
- Pandas: Data loading, structuring, and heavy feature engineering.
- Matpotlib & Seaborn: Data visualization.
- Scikit-learn: Training models, evaluation, cross-validation.
- Pickle: Exporting trained model.

## Data Loading and Analysis

- The dataset is loaded from a CSV file using pandas.
- Exploratory Data Analysis is used to find correlations between variables like GPA, sleep, and anxiety, visualized using custom Seaborn plots.

## Data Preprocessing

- Multi-class variables (CGPA, Sleep hours) were converted to numbers using Ordinal Encoding.
- Text categories without a strict labels (like Degree Major) were splitted into binary columns using One-Hot Encoding.
- The depression scale was converted into a strict binary targer variable (0 = Unlikely Depressed, 1 = Likely Depressed).

## Model Used

- The core of this project is a Random Forest Classifier.
- Also tested and compared against Logistic Regression, Support Vector Machines (SVM), and Decision Trees to find the best fit for a small dataset.

## Evaluation Method
- 5-Fold Cross-Validation
