# 🌳 From Friedman’s Gradient Boosting to Modern Tree-Boosting Systems

### An experimental study of gradient boosting, tree complexity, loss functions, and modern GBDT implementations.

---

## 📌 About the Project

This project presents an experimental study inspired by Jerome Friedman's **Gradient Boosting framework** introduced in 2001.

The study investigates how gradient boosting behaves under different loss functions and tree sizes, validates a manual implementation against **scikit-learn**, and examines how the same core idea has evolved into modern Gradient Boosting Decision Tree (GBDT) systems.

The experiments are conducted using the **California Housing dataset**.

---

## 🛠️ Tech Stack

| Category | Technologies |
|---|---|
| Language | Python |
| Data Processing | NumPy, Pandas |
| Machine Learning | Scikit-learn |
| Modern GBDT | XGBoost, LightGBM, HistGradientBoosting |
| Visualization | Matplotlib |
| Environment | Jupyter Notebook |

---

## ⚙️ Work Implemented

🔹 Implemented a **Friedman-style gradient boosting** approach using regression trees.

🔹 Studied three loss functions:
- Least Squares (LS)
- Least Absolute Deviations (LAD)
- Huber Loss

🔹 Investigated the effect of **tree size (J)** on validation performance.

🔹 Studied the relationship between **tree complexity and boosting iterations**.

🔹 Used validation MAE for model selection with a held-out test set for final evaluation.

🔹 Evaluated multiple random seeds to study the stability of results.

🔹 Compared the manual implementation with **scikit-learn** under a controlled experimental setup.

🔹 Compared modern GBDT implementations:
- HistGradientBoosting
- XGBoost
- LightGBM

🔹 Evaluated modern systems using test MAE, RMSE, R², and training time.

🔹 Studied how the original gradient boosting idea has evolved into modern, optimized implementations.

---

## 📂 Dataset

### California Housing

The experiments use the **California Housing dataset** containing:

- **20,640 samples**
- **8 numerical features**
- Median house value as the target variable

The data is divided into:

```text
60% Training
20% Validation
20% Test
```

The validation set is used for model selection, while the test set is reserved for final evaluation.

---

## 🔬 Experimental Setup

### Manual Gradient Boosting

Tree sizes evaluated:

```text
J = 2, 3, 4, 6, 11, 21
```

Learning rate:

```text
η = 0.1
```

Maximum boosting iterations:

```text
3000
```

Early stopping patience:

```text
100 iterations
```

Random seeds:

```text
101, 102, 103, 104, 105
```

---

## 📊 Key Findings

🔹 **Huber loss** achieved the lowest validation MAE among the tested loss functions under the experimental setup.

🔹 Increasing tree size generally reduced validation error, although the improvement became smaller at larger tree sizes.

🔹 The manual implementation and scikit-learn produced **nearly identical validation MAE**, supporting the consistency of the manual implementation.

🔹 Modern GBDT systems achieved **very similar predictive accuracy**, while their measured training times differed.

🔹 In this experiment, **LightGBM achieved the lowest mean test MAE and the fastest measured training time** among the tested modern systems.

---

## 🧠 Research Conclusion

The experiments show that the fundamental idea behind gradient boosting has remained consistent: **build trees sequentially to reduce the remaining prediction error**.

What has evolved significantly is the **implementation and computational efficiency** of the boosting systems.

> **The core idea of gradient boosting remained remarkably stable; what changed most was how efficiently we implement it.**

---

## 📁 Project Structure

```text
gradient-boosting-study/
│
├── gradient_boosting_experiment.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

---

## 🚀 How to Run

Clone the repository:

```bash
git clone <repository-url>
cd gradient-boosting-study
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.venv\Scripts\activate
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter:

```bash
jupyter notebook
```

Open the `.ipynb` file and run the notebook cells.

---

## 👥 Project

Developed at **Pimpri Chinchwad College of Engineering (PCCOE), Pune**.

**124B1D058 Ayush Gade**
**| 124B1D059 Akash Gajare**
**| 124B1D063 Aayush Patil**
**| 124B1D064 Tejas Nemade**

### From a 2001 statistical framework to modern high-performance GBDTs.
