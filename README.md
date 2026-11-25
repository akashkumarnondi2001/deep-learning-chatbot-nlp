# 🤖 Intent-Based NLP Chatbot

A deep learning conversational chatbot built in **Python** using **TensorFlow/Keras** and **Natural Language Processing (NLP)**. The model classifies user queries into predefined intent categories and selects dynamic, context-appropriate responses.

---

### ⚙️ How It Works

1. **Text Preprocessing:**
   * Strips punctuation (`string.punctuation`) and converts all user input to lowercase.
   * Tokenizes sentences into integer sequences using Keras `Tokenizer`.
   * Applies sequence padding (`pad_sequences`) to ensure uniform input dimensions.
2. **Intent Classification Model:**
   * Uses a neural network trained on labeled conversational intents (`intents.json`).
   * Predicts probability distributions across intent classes and selects the highest-confidence tag via `argmax()`.
3. **Response Generation:**
   * Decodes the predicted class index back to its original intent label using `LabelEncoder` (`le.inverse_transform`).
   * Returns a randomized response mapped to the matched intent tag.

---

### 🛠️ Tech Stack

* **Language:** Python
* **Deep Learning:** TensorFlow / Keras (`Tokenizer`, `pad_sequences`, Sequential/Functional Model)
* **Data & Preprocessing:** NumPy, Scikit-learn (`LabelEncoder`), Python `string` & `random`

---

### 🚀 How to Run

1. Clone or download the repository:
   ```bash
   git clone https://github.com
   cd intent-based-nlp-chatbot
   ```
2. Install the required libraries:
   ```bash
   pip install numpy tensorflow scikit-learn
   ```
3. Run the Jupyter Notebook or Python script to train the model and start chatting in the console.

---

### 💬 Example Inference Flow

```text
User: "Hello, can you help me?"
  -> Preprocessed: "hello can you help me"
  -> Predicted Intent Tag: "greeting"
  -> Bot Response: "Hi there! How can I assist you today?"
```
