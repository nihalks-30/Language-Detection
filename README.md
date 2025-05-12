# 🌐 Language Detection using NLP and Machine Learning

This project uses Natural Language Processing (NLP) techniques combined with machine learning to detect the language of a given text. It is trained on a multilingual dataset from Kaggle and demonstrates high accuracy using a Naive Bayes classifier.

---

## 📁 Dataset

- **Source**: [Kaggle - Language Detection Dataset](https://www.kaggle.com/datasets/basilb2s/language-detection)
- **Size**: 10,337 text samples across 17 different languages.
- **Columns**:
  - `Text`: The input sentence or paragraph.
  - `Language`: The actual language label.

---

## ⚙️ Workflow

### 1. **Setup & Data Loading**
- Used `kagglehub` to download the dataset.
- Loaded data with `pandas` and verified its shape and distribution.

### 2. **Preprocessing**
- Cleaned the text:
  - Removed special characters, digits, and unwanted symbols using regular expressions (`re` module).
  - Converted all text to lowercase.
- Encoded language labels using `LabelEncoder`.

### 3. **Vectorization**
- Converted text into numerical format using `CountVectorizer` (Bag of Words approach).

### 4. **Model Training**
- Split data into training and testing sets using `train_test_split`.
- Trained a `Multinomial Naive Bayes` classifier on the training data.

### 5. **Evaluation**
- Evaluated the model using:
  - `accuracy_score` (Achieved ~97.8% accuracy).
  - `confusion_matrix` with heatmap for visualization.
  - `classification_report` for precision, recall, and F1-score.

### 6. **Prediction Function**
- Created a function `lang_predict()` that takes a string input and returns the predicted language.

---

## 📊 Results

The model correctly predicted languages like:
- English
- Arabic
- Hindi
- Russian
- Spanish
- French
- German
- Malayalam

with high accuracy and robust performance across all language classes.

---

## 🛠️ Technologies Used

- **Python**
- **Pandas & NumPy**
- **Matplotlib & Seaborn**
- **scikit-learn** (CountVectorizer, MultinomialNB, LabelEncoder, train_test_split)
- **Regular Expressions (re)**

---

## 🚀 How to Use

1. Clone the repository.
2. Ensure Kaggle API is set up if running from Colab or locally.
3. Run the notebook or Python script.
4. Use the `lang_predict("your text here")` function to predict the language of any input sentence.

---

## 📌 Example

```python
lang_predict("Aujourd'hui va être très chargé car j'ai beaucoup de choses à faire.")
# Output: The langauge is in French
```
