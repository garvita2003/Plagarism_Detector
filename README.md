# Plagiarism Detector 🧾🔍

## 📌 Introduction

**Plagiarism Detector** is a Python-based project that implements two practical plagiarism-checking approaches:
- A **machine learning + Flask web app** pipeline (Approach 1)
- A **Levenshtein distance-based CLI checker** with multiple scan modes (Approach 2)

The project demonstrates both model-driven text classification and direct string-similarity comparison workflows for detecting potentially copied content.

**Key Features:**
- ✅ Flask web interface for plagiarism prediction
- ✅ TF-IDF vectorization + trained model inference via pickle artifacts
- ✅ CLI-based document similarity checker using Levenshtein distance
- ✅ Three CLI modes: folder-vs-master, file-vs-file, and all-files-in-folder
- ✅ Configurable plagiarism threshold (percentage allowed)
- ✅ Example test files and sample dataset included

---

## 🔄 Process / Flow

**Approach 1 (ML + Flask):**
1. Load serialized model and TF-IDF vectorizer (`model.pkl`, `tfidf_vectorizer.pkl`)
2. User enters text in Flask web form
3. Input text is transformed using TF-IDF vectorizer
4. Model predicts plagiarism class (`1` or `0`)
5. Result is rendered back on the same HTML page

**Approach 2 (Levenshtein CLI):**
1. User selects mode from terminal menu
2. Program reads one or more `.txt` files
3. Text is normalized by removing spaces/newlines
4. Levenshtein distance is computed between text pairs
5. Similarity percentage is calculated and compared with threshold
6. Matched pairs/files above threshold are printed

---

## 🛠️ Technology Used

| Component | Technology |
|-----------|-----------|
| **Programming Language** | Python |
| **Web Framework** | Flask |
| **ML Utilities** | scikit-learn (TF-IDF + model inference) |
| **Numerical Computing** | NumPy |
| **Data Handling** | Pandas (used in notebook workflow) |
| **Similarity Algorithm** | Levenshtein Distance (custom implementation) |
| **Serialization** | Pickle |

---

## 🎓 Skills Gained

**Machine Learning Deployment:**
- ✅ Loading trained ML artifacts in production-style scripts
- ✅ Performing real-time text inference with TF-IDF + classifier
- ✅ Integrating model prediction into a Flask application

**Algorithmic Text Analysis:**
- ✅ Implementing edit-distance-based similarity checks
- ✅ Building threshold-driven plagiarism detection logic
- ✅ Comparing one-to-many and many-to-many document sets

**Python Application Design:**
- ✅ Designing menu-driven CLI flows
- ✅ Managing file-system operations for batch scanning
- ✅ Structuring project into separate approaches for experimentation

---

## 📂 Project Structure

```
Plagarism_Detector/
├── README.md                                      # Project documentation
├── Approach1/                                     # ML notebook + Flask deployment approach
│   ├── app.py                                     # Flask app for plagiarism prediction
│   ├── dataset.csv                                # Dataset used in notebook/model workflow
│   ├── Plagiarism_checker_using_Machine_Learning.ipynb  # Model training/experimentation notebook
│   └── Templates/
│       └── index.html                             # Web form UI for text input and result display
└── Approach2/                                     # Pure algorithmic CLI plagiarism checker
    ├── checker.py                                 # Levenshtein-based plagiarism detection script
    └── TestFile/
        ├── main.txt                               # Master/reference file sample
        ├── sample1.txt                            # Sample document for pairwise checks
        └── sample2.txt                            # Sample document for pairwise checks
```

---

## 📸 Demonstration

### Approach 1
- Logistic Regression:

![Screenshot 2025-01-08 124702](https://github.com/user-attachments/assets/8342df45-7aef-4c22-83f8-00f7f6e0f0aa)

- Random Forest:

![Screenshot 2025-01-08 124744](https://github.com/user-attachments/assets/8a9e95e7-9d2f-4d8d-ac9b-f811101fb7d4)

- Naive Bayes:

![Screenshot 2025-01-08 124814](https://github.com/user-attachments/assets/9e77a54f-db1f-44ce-8c5a-3b18ad048b60)

- Support Vector Machine:

![Screenshot 2025-01-08 124820](https://github.com/user-attachments/assets/b74109ff-3175-4cc7-b5dc-f49d502a510a)

- Implementation:

![Screenshot 2025-01-08 124835](https://github.com/user-attachments/assets/9737155c-88ad-4b52-bd38-70bf4b8c5211)

Flask Implementation:

![Screenshot 2025-01-08 125317](https://github.com/user-attachments/assets/c71ebe35-e77e-4ce5-905d-5efd85df10ff)
![Screenshot 2025-01-08 125344](https://github.com/user-attachments/assets/45d28b54-2153-4451-a1eb-ede296295daf)
![Screenshot 2025-01-08 125411](https://github.com/user-attachments/assets/27e7fe5e-7720-4dce-8c93-74cb0c7cc0ac)

### Approach 2
- Option 1:

![Screenshot 2025-01-08 124023](https://github.com/user-attachments/assets/7dae416c-972d-4e71-b05a-c60a4098562a)

- Option 2:

![Screenshot 2025-01-08 124307](https://github.com/user-attachments/assets/248eb335-a9fe-4286-af53-049e3db38a9e)

- Option 3:

![Screenshot 2025-01-08 124415](https://github.com/user-attachments/assets/db2206a0-6635-4589-bf1d-6db3de1046c1)

---

## ⚙️ Setup Instructions

### Prerequisites:
- Python 3.8+
- pip

### Approach 1 (Flask App)

**1. Navigate to project**
```bash
cd Plagarism_Detector-main/Approach1
```

**2. Install dependencies**
```bash
pip install flask scikit-learn==1.6.0 pandas numpy
```

**3. Ensure model artifacts exist**
- `model.pkl`
- `tfidf_vectorizer.pkl`

**4. Run Flask app**
```bash
python app.py
```

Open the local Flask URL shown in terminal and submit text for checking.

### Approach 2 (CLI Checker)

**1. Navigate to checker folder**
```bash
cd Plagarism_Detector-main/Approach2
```

**2. Run script**
```bash
python checker.py
```

**3. Choose mode in terminal**
- `1` = compare all files in a folder against a master file
- `2` = compare two specific files
- `3` = compare all files pairwise inside a folder

Provide required paths and plagiarism threshold when prompted.
