# Lab 6 - IR-invertedmatrix-workshop

- **Members:**  Chao-Chung ,Liu
- **Course:** PROG8245 - Machine Learning Programming

## 🔍 Project Overview
In this lab, we built an **Inverted Index** system. This is the foundation of modern search engines. Our goal was to process real blog data from NASA and Python, and create a system that can find and rank documents based on word importance using **TF-IDF**.

## ⚙️ Core
* **Data Collection**: Used `feedparser` to fetch 20+ real-time blog posts from RSS feeds.
* **Text Processing**: 
    * **Tokenization**: Converting sentences into lists of words.
    * **Normalization**: Removing HTML tags, stop words, and using **Stemming** (e.g., 'software' becomes 'softwar').
* **Indexing Strategy**: 
    * **Inverted Index**: A dictionary to find which Document ID contains a word.
    * **Positional Index**: Recording the exact location of words for phrase searching.

## 📊 Mathematical Model (TF-IDF)
We use the **TF-IDF** formula to rank our search results:
1. **TF (Term Frequency)**: How many times a word appears in one document.
2. **IDF (Inverse Document Frequency)**: How rare a word is in the whole collection.
3. **Calculation**: $$\text{TF-IDF} = \text{TF} \times \text{IDF}$$

### Example Calculation (Document 0)
For the term **'softwar'** in **Document 0**:
- **TF ($n_{\text{softwar}, 0}$)**: 6
- **IDF**: 0.2231
- **Final TF-IDF Score**: $6 \times 0.2231 = 1.3389$

## 💡 Key Insights
* **Vocabulary Size**: Our system successfully indexed **1,884 unique terms**.
* **Search Logic**: We implemented **Boolean AND search** and **Phrase search**, allowing users to find specific word sequences.
* **Efficiency**: Using a positional index makes searching much faster than scanning every document manually.



## 📂 Project Structure
```text
IR-invertedmatrix-workshop/
├── .gitignore              # Files to ignore (venv/, sample_docs/)
├── README.md               # Project overview and team info
└── IR_InvertedMatrix_Workshop.ipynb # Main code with TF-IDF analysis
```

## 🛠️ Getting Started & Data Setup


Follow these steps to set up the project environment and prepare the dataset for analysis:

1. **Clone the Repository:**
   ```bash
   git clone [https://github.com/caatat741213/IR-invertedmatrix-workshop.git](https://github.com/caatat741213/IR-invertedmatrix-workshop.git)

2. **Create the Environment:**
   ```bash
   # Create a virtual environment
   python -m venv venv

   # Activate on Windows:
   venv\Scripts\activate

   # Activate on macOS/Linux:
   source venv/bin/activate

3. **Install all required libraries from the requirements file:**
   ```bash
   pip install -r requirements.txt
