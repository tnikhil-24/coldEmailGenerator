
# 📧 Cold Email Generator

This project automates the generation of personalized cold emails based on job postings scraped from career pages. It uses an LLM (via Groq), ChromaDB for semantic search, and Streamlit for a simple UI.

---

## 🚀 Features

- 🔍 Scrapes job data from a given career page URL.
- 🧠 Uses LLM (LLaMA 3 via Groq) to extract job descriptions.
- 🤖 Automatically generates a professional cold email in Mohan's voice (AtliQ BDE).
- 🧰 Matches relevant portfolio items using semantic search over a CSV file via ChromaDB.
- 💻 Simple, interactive UI built with Streamlit.

---

## 🧱 Tech Stack

- **Python**
- **LangChain**
- **Groq (LLaMA 3 model)**
- **ChromaDB (Vector Search)**
- **Streamlit (UI)**
- **Pandas**
- **Dotenv**

---

## 📂 Project Structure

```
coldemailgenerator/
│
├── app/
│   ├── chains.py          # LangChain logic for extraction and email generation
│   ├── portfolio.py       # Vector search for portfolio links
│   ├── utils.py           # Text cleaning utilities
│   ├── resource/
│   │   └── my_portfolio.csv  # Portfolio file (skills + links)
│   └── app.py             # Streamlit app entry point
│
├── vectorstore/           # ChromaDB persistence directory
├── .env                   # Contains your GROQ_API_KEY
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/coldemailgenerator.git
cd coldemailgenerator
```

### 2. Set Up a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Set Up Environment Variables

Create a `.env` file in the root directory and add:

```env
GROQ_API_KEY=your_groq_api_key_here
```

---

## 🛠️ How to Use

1. Launch the Streamlit app:

```bash
streamlit run app/app.py
```

2. Paste a job URL (e.g., from a company's careers page).
3. Click **Submit**.
4. A personalized cold email will be generated, tailored to the role.

---

## 📌 Notes

- Ensure that `my_portfolio.csv` contains two columns: `Techstack` and `Links`.
- The portfolio will be indexed into ChromaDB on first run.
- You can modify the tone or branding by editing `chains.py`.

---

## ✅ Example CSV Format

```csv
Techstack,Links
Python AI automation,"https://atliq.com/project-ai"
Data Engineering pipelines,"https://atliq.com/project-de"
```

---

## 🧑‍💻 Maintained by

**Mohan @ AtliQ**  
For questions, reach out to [your-email@atliq.com].

---

## 📜 License

MIT License
