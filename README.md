```markdown
# XLNet Intent Identifier

This repository focuses on **intent extraction and span classification** using a stacked labeling approach on tweet data. It specifically targets two types of intent:
- **Call to Action (CTA)**
- **Discrediting Entities (DE)**

The system uses human-annotated and weakly-annotated datasets and applies XLNet-based tokenization and labeling to identify actionable spans in social media posts.

---

## 📂 Repository Structure

```

├── human\_annotated\_cta.json         # Human-labeled CTA tweets
├── human\_annotated\_de.json          # Human-labeled DE tweets
├── weak\_annotated\_cta.json          # Weak-labeled CTA data
├── weak\_annotated\_de.json           # Weak-labeled DE data
├── combined\_data.csv                # Merged and processed dataset
├── dataset\_extraction\_NLP\_FTP.ipynb # Notebook to extract and process data
├── \[ACTUAL\_RUN]\_Sequence\_labeling\_stacked\_NLP\_FTP.ipynb # XLNet labeling and training

````

---

## 🔍 Features

- ✅ Parses annotated tweet data with subject-action span pairs.
- 📊 Combines weak and human annotations for model robustness.
- 🧠 Uses **XLNetTokenizerFast** for subword tokenization.
- 🏷️ Generates detailed token-level labels (BIO-style tagging).
- 📈 Evaluates classification performance using precision, recall, and F1-score.

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/XLNET-Intent-Identifier.git
cd XLNET-Intent-Identifier
````

### 2. Install Dependencies

Recommended environment: Python 3.8+

```bash
pip install -r requirements.txt
# OR install manually:
pip install pandas scikit-learn transformers torch
```

---

## 📘 Usage

### ➤ Data Extraction

Run the notebook `dataset_extraction_NLP_FTP.ipynb` to:

* Load JSON files
* Extract labeled spans
* Merge weak and human labels
* Export `combined_data.csv`

### ➤ Sequence Labeling & Modeling

Run `[ACTUAL_RUN]_Sequence_labeling_stacked_NLP_FTP.ipynb` to:

* Load combined dataset
* Tokenize and label tweets
* Train/test on intent tagging using XLNet
* Evaluate model performance

---

## 📊 Example Output

Each token in the tweet is labeled using BIO notation:

```
"Join/B-CTA-action the/I-CTA-action protest/I-CTA-action now/O !/O"
```

---

## 🤝 Contributing

Feel free to open issues or pull requests if you'd like to:

* Improve performance
* Extend to other intent types
* Add support for other languages

---

## 📄 License

This project is open-source and available under the MIT License.

---

## 👨‍💻 Author

**Your Name** – [@yourgithub](https://github.com/yourgithub)

---

## 📬 Contact

For any questions or collaborations, reach out at [your.email@example.com](mailto:your.email@example.com).

```
