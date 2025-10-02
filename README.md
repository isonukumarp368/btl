# 📘 BTL – Bloom’s Taxonomy Based Automatic Short Answer Question Generator

**BTL (Bloom’s Taxonomy Learning Project)** is a Flask-based NLP application that automatically generates **short-answer questions and answers** from input text.  
The system aligns with **Bloom’s Taxonomy** (six cognitive levels), making it ideal for **educational assessments, smart quizzes, and e-learning platforms**.

---

## 🚀 Features

- 🌐 **Flask Web App** with clean UI  
- 📄 **Multiple Templates** (`index`, `resultPage`, `results`)  
- 🎨 **Custom Styling** with CSS  
- 🤖 **Automatic Q&A Generation** using NLP (NLTK + spaCy)  
- 🧠 **Bloom’s Taxonomy Alignment** – Generates questions across **six levels**:
  - Level 1: Remember  
  - Level 2: Understand  
  - Level 3: Apply  
  - Level 4: Analyze  
  - Level 5: Evaluate  
  - Level 6: Create  
- 📊 **Evaluation Metrics**: Precision, Recall, F1-score, Semantic Similarity  
- 📦 Export results to Excel  

---

## 📂 Project Structure

```
btl/
│── app.py                  # Main Flask app
│── requirements.txt         # Dependencies
│
├── core/                    # Core NLP & AI logic
│   ├── text_processing.py   # Tokenization, POS tagging, NER, SVO extraction
│   ├── question_generation.py # Q–A generation with Bloom’s taxonomy
│   ├── answer_extraction.py # Extracts short factual answers
│   ├── evaluation.py        # Precision, Recall, F1, BERT similarity
│   └── __init__.py
│
├── static/                  # CSS + JS + images
│   └── style.css
│
├── templates/               # HTML Templates
│   ├── index.html           # Input form
│   ├── resultPage.html      # Display Q&A
│   └── results.html
│
├── data/                    # Data outputs
│   ├── generated_questions.xlsx
│   └── evaluation_metrics.xlsx
│
└── notebooks/               # Jupyter prototypes
    ├── text_qg_prototype.ipynb
    └── evaluation_prototype.ipynb
```

---

## ⚙️ Installation & Setup

1. **Clone Repository**
   ```bash
   git clone https://github.com/isonukumarp368/btl.git
   cd btl
   ```

2. **Create Virtual Environment**
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # Mac/Linux
   venv\Scriptsctivate      # Windows
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Download spaCy Model**
   ```bash
   python -m spacy download en_core_web_lg
   ```

---

## ▶️ Usage

Run Flask App:

```bash
python app.py
```

Then open in browser:  
👉 http://127.0.0.1:5000/

### Workflow:
1. Enter a text passage.  
2. Select Bloom’s Level + number of questions.  
3. System generates **questions & answers** across levels.  
4. Results are displayed and saved in Excel.  

---

## 📊 Example

**Input**:  
```
Ravi is a boy. He loves reading books and playing cricket.
```

**Generated Output**:

- **Level 1 (Remember):** Who is Ravi? → Ravi is a boy.  
- **Level 2 (Understand):** Can you explain why Ravi loves reading books?  
- **Level 3 (Apply):** How would you apply Ravi’s habit of reading to your daily routine?  
- **Level 4 (Analyze):** What are the components of Ravi’s hobbies?  
- **Level 5 (Evaluate):** Do you agree reading makes Ravi a better student? Why/why not?  
- **Level 6 (Create):** Can you design a story where Ravi’s love for cricket changes his life?  

---

## 📸 Screenshots

(Add screenshots here once you run the project)

---

## 📌 Future Enhancements

- 📊 Integration with Tableau / Streamlit dashboards for visualization  
- 🖼 Support for **Image → Text → Q&A** (OCR + BLIP model)  
- 🤖 Transformer-based QG (T5, BART, Flan-T5) for more natural questions  

---

## 👨‍💻 Author

Developed by **[isonukumarp368](https://github.com/isonukumarp368)**  
Aligned with **Bloom’s Taxonomy** for educational Q&A.

---
