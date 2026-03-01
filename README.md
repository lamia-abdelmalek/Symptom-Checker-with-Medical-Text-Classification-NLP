# 🩺 Symptom Checker with Medical Text Classification (NLP)

A Natural Language Processing (NLP) project that classifies user-described medical symptoms into possible diseases using deep learning models. The system is deployed as an interactive web application using Streamlit.

---

## 📌 Project Overview

This project applies NLP and Deep Learning techniques to build an intelligent symptom checker.
Users enter their symptoms in free text, and the model predicts the most likely diseases along with confidence scores.

The goal is to demonstrate how NLP can be applied in healthcare for automated medical text classification.

---

## 📂 Project Structure

```
├── app.py                         # Streamlit application
├── best_advanced_model.keras      # Saved advanced model
├── best_baseline_model.keras      # Saved baseline model
├── final_advanced_model.h5        # Final trained model
├── label_encoder.pkl              # Encoded disease labels
├── mini-projet-nlp.ipynb          # Model training notebook
└── README.md
```

---

## 📊 Dataset

* Dataset: `complete_medical_symptom_dataset`
* ~1.3 million records
* Columns:

  * `symptoms` (text)
  * `disease` (label)

---

## 🧹 Preprocessing

* Lowercasing
* Removing special characters
* Removing null values
* Lemmatization
* Handling class imbalance using class weights

---

## 🤖 Models Implemented

* LSTM
* GRU
* Baseline Feedforward Neural Network
* ✅ Advanced Dual-Input Model (BoW + BiLSTM) — Best performing model

### 🏆 Best Model Performance

| Model                     | Validation Accuracy |
| ------------------------- | ------------------- |
| LSTM                      | 72.64%              |
| GRU                       | 73.5%               |
| Baseline                  | 80%                 |
| **Advanced (BoW + LSTM)** | **89.43%**          |

---

## 🚀 Deployment with Streamlit

The model is deployed using **Streamlit** to create an interactive web interface.

Users can:

* Enter symptoms in a text box
* Get predicted diseases
* View confidence probabilities

---

## ⚙️ Installation & Running Locally

### 1️⃣ Clone the repository

```bash
git clone https://github.com/your-username/Symptom-Checker-with-Medical-Text-Classification-NLP.git
cd Symptom-Checker-with-Medical-Text-Classification-NLP
```

### 2️⃣ Install requirements

```bash
pip install -r requirements.txt
```

If you don't have a requirements file, install manually:

```bash
pip install streamlit tensorflow scikit-learn pandas numpy
```

### 3️⃣ Run the app

```bash
streamlit run app.py
```

The app will open automatically in your browser.

---

## 💡 Example Prediction

**Input:**

```
I have fatigue, yellowish skin, nausea.
```

**Output:**

* Hepatitis C — 57.9%
* Alcoholic Hepatitis — 27.2%
* Chronic Cholestasis — 7.4%

---

## 🎯 Future Improvements

* Improve model interpretability
* Add symptom duration & patient history
* Deploy online (Streamlit Cloud / Render / HuggingFace Spaces)
* Add multilingual support

---

## 👩‍💻 Authors

* Souad BOUKHAROUBA
* Sanaa BENSAID
* Lamia ABDELMALEK

Supervised by Dr. Rabab Bousmaha

---

## ⚠️ Disclaimer

This project is for educational purposes only and does not replace professional medical advice.
