# 📩 SpamShield AI – Email and SMS Classifier

A simple **Spam Message Classifier** built using **Python**, **Scikit-learn**, and **Streamlit**.  
It classifies incoming **emails or SMS messages** as **Spam** or **Not Spam** using a trained **Naive Bayes model**.

---

## 🚀 Features

- Streamlit web interface for real-time message classification  
- Preprocessing with tokenization, stopword removal, and stemming  
- TF-IDF vectorization for text representation  
- Trained **Multinomial Naive Bayes** model  
- Ready-to-run Docker setup  

---

## 📁 Project Structure

```
.
├── app.py                # Streamlit web app
├── spam-detection.ipynb  # Model training notebook
├── spam.csv              # Dataset (email/SMS labeled data)
├── model.pkl             # Trained ML model
├── vectorizer.pkl        # TF-IDF vectorizer
├── Dockerfile            # Container setup
└── README.md             # Project documentation
```

---

## ⚙️ Installation

### 1️⃣ Clone the repository
```bash
git clone https://github.com/<your-username>/spam-detection-ml.git
cd spam-detection-ml
```

### 2️⃣ Create a virtual environment
```bash
python -m venv venv
venv\Scripts\activate   # (Windows)
# or
source venv/bin/activate  # (macOS/Linux)
```

### 3️⃣ Install dependencies
```bash
pip install -r requirements.txt
```

---

## 🧠 How It Works

1. The input message is preprocessed:
   - Converts to lowercase  
   - Tokenizes text  
   - Removes stopwords and punctuation  
   - Applies stemming  

2. The cleaned message is transformed using the **TF-IDF vectorizer**  
3. The **Naive Bayes** model predicts whether it’s spam or not  

---

## ▶️ Run the App

```bash
streamlit run app.py
```

Then open the local URL shown in the terminal (usually http://localhost:8501).

---

## 🐳 Run with Docker

```bash
docker build -t spam-detector .
docker run -p 8501:8501 spam-detector
```

---

## 📊 Dataset

Dataset used: **spam.csv**  
It contains labeled text messages with columns like:
- `label`: "spam" or "ham"
- `message`: actual text content

---

## 📜 Model Details

- **Algorithm**: Multinomial Naive Bayes  
- **Vectorization**: TF-IDF  
- **Evaluation**: Trained and tested in `spam-detection.ipynb`  
- **Files**:
  - `model.pkl` → saved model  
  - `vectorizer.pkl` → TF-IDF transformer  

---

## 🧰 Tech Stack

- Python 3.9+
- Streamlit
- Scikit-learn
- NLTK
- Pandas
- Docker

---

## ✨ Example

**Input:**  
> “Congratulations! You have won a $1000 Walmart gift card. Click here to claim.”

**Output:**  
> 🛑 Spam

---

## 👨‍💻 Author

**KATOKOTA BISHNU PRASAD PATRO**  
Project: *SpamShield AI – Email and SMS Classifier*

