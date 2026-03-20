# Model-Saving-Joblib-and-Pickle
# 💾 Model Serialization & Persistence (Pickle vs. Joblib)

Building a machine learning model is only half the battle; being able to save and reuse it is what makes it production-ready. This repository demonstrates how to serialize trained Python objects into files using **Pickle** and **Joblib**.

---

## 🛠️ The Persistence Stack
* **Python**: Core logic.
* **Scikit-Learn**: For training the initial model (Linear Regression).
* **Pickle**: The standard Python library for object serialization.
* **Joblib**: An optimized library specifically designed for large NumPy arrays and Scikit-Learn models.

---

## 📊 Project Workflow

### 1. Model Training
* A sample **Linear Regression** model was trained to provide a functional object for saving.
* Verified initial predictions to establish a baseline for post-loading accuracy.

### 2. Serialization with Pickle
* **Saving:** Used `pickle.dump()` to write the model to a `.pkl` file.
* **Loading:** Used `pickle.load()` to bring the model back into the memory of a new session.
* **Check:** Confirmed that the "reloaded" model produced identical results to the original.

### 3. Serialization with Joblib
* **Saving:** Used `joblib.dump()` to create a compressed model file.
* **Loading:** Used `joblib.load()` to restore the model.
* **Advantage:** Highlighted why Joblib is often preferred over Pickle for models containing large numerical datasets.

---

## 🧠 Why is this important?
In a real-world scenario, you don't want to retrain a model on millions of rows every time a user requests a prediction. Model persistence allows for:
* **Deployment:** Moving a model from a Jupyter Notebook to a web server (Flask/FastAPI).
* **Version Control:** Keeping track of different versions of a trained model.
* **Efficiency:** Instant loading of complex models.

---

## 🚀 How to Run

1. **Clone the repo:**
   ```bash
   git clone [https://github.com/Manaswi9123/Python-DataScience-Fundamentals.git](https://github.com/Manaswi9123/Python-DataScience-Fundamentals.git)
