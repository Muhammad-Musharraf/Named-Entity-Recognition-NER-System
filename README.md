# Named Entity Recognition (NER) using Deep Learning

## 📌 Overview

This project implements a **Named Entity Recognition (NER)** system using **TensorFlow/Keras** and **LSTM-based Deep Learning**. The model learns to identify and classify named entities in text such as persons, locations, organizations, and other predefined entity categories.

The project covers the complete machine learning pipeline including:

* Data preprocessing
* Vocabulary and tag encoding
* Sequence padding
* One-hot encoding of labels
* Train-test splitting
* Deep Learning model development
* Model training and evaluation
* Model saving and inference

---

## 🚀 Features

* Text preprocessing and cleaning
* Word-to-ID and Tag-to-ID mapping
* Sentence-level sequence generation
* Sequence padding for uniform input length
* One-hot encoding of NER tags
* LSTM-based sequence labeling model
* Early stopping to prevent overfitting
* Learning rate scheduling
* Automatic best model checkpoint saving
* Model evaluation and prediction functionality

---

## 📂 Dataset

The project uses an NER dataset containing:

| Column     | Description         |
| ---------- | ------------------- |
| Sentence # | Sentence identifier |
| Word       | Token/Word          |
| POS        | Part-of-Speech Tag  |
| Tag        | Named Entity Label  |

Example:

| Word    | POS | Tag   |
| ------- | --- | ----- |
| Ali     | NNP | B-PER |
| lives   | VBZ | O     |
| Karachi | NNP | B-LOC |

---

## 🛠️ Technologies Used

* Python
* TensorFlow / Keras
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn

---

## 📊 Data Preprocessing

The following preprocessing steps are performed:

1. Missing value handling using forward fill.
2. Creation of word vocabulary.
3. Creation of tag vocabulary.
4. Word-to-ID mapping.
5. Tag-to-ID mapping.
6. Sentence grouping.
7. Sequence padding.
8. One-hot encoding of output labels.

---

## 🧠 Model Architecture

The model is built using TensorFlow Functional API.

### Architecture Flow

Input Layer

⬇

Embedding Layer

⬇

LSTM Layer

⬇

Dense Layer

⬇

TimeDistributed Output Layer

⬇

Softmax Classification

### Training Enhancements

* EarlyStopping
* ReduceLROnPlateau
* ModelCheckpoint

These callbacks improve convergence and save the best-performing model automatically.

---

## 📈 Training

The dataset is split into training and testing sets using:

```python
train_test_split(
    test_size=0.1,
    random_state=42
)
```

Training configuration:

* Batch Size: 32
* Epochs: 30
* Validation Monitoring
* Best Model Saving

---

## 💾 Model Saving

Best model checkpoint:

```python
saved_model/best_ner_model.keras
```

Final model:

```python
ner_model.keras
```

Load model:

```python
from tensorflow.keras.models import load_model

model = load_model("ner_model.keras")
```

---

## 🔍 Prediction

Example:

```python
predict("Ali live in Karachi")
```

Expected Output:

```text
Ali      → B-PER
live     → O
in       → O
Karachi  → B-LOC
```

---

## 📁 Project Structure

```text
Named-Entity-Recognition/
│
├── Named_Entity_Recognition.ipynb
├── ner_model.keras
├── saved_model/
│   └── best_ner_model.keras
├── dataset/
│   └── ner_dataset.csv
├── README.md
└── requirements.txt
```

---

## 📊 Evaluation

The model is evaluated using:

* Loss
* Accuracy

```python
loss, accuracy = model.evaluate(
    test_statement,
    test_tag
)
```

---

## 🎯 Applications

Named Entity Recognition can be used in:

* Information Extraction
* Chatbots
* Search Engines
* Resume Parsing
* Question Answering Systems
* Document Analysis
* Medical Text Processing
* Financial Text Analytics

---

## 🔮 Future Improvements

* BiLSTM Architecture
* CRF Layer Integration
* Transformer-based NER
* BERT Fine-Tuning
* Attention Mechanisms
* Hyperparameter Optimization
* Deployment with FastAPI or Streamlit

---

## 👨‍💻 Author

**Muhammad Musharraf**

Machine Learning & Artificial Intelligence Enthusiast

Focused on building practical AI, Deep Learning, NLP, and Computer Vision projects.

