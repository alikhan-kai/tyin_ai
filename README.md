# Tyin AI: Smart Credit Agent Advisor 🏦🤖

**Tyin AI** is an intelligent financial assistant designed to navigate the complex credit market of Kazakhstan. By leveraging **RAG (Retrieval-Augmented Generation)** and a **Multi-Agent Architecture**, it transforms natural language requests into precise financial insights and bank comparisons.

---

## 🚀 Project Overview
Comparing loan offers from different banks is often confusing due to varying interest rates, hidden fees, and complex calculations. **Tyin AI** solves this by allowing users to describe loan offers in plain text. The system extracts parameters, calculates the actual cost, and suggests better alternatives from a built-in vector database of Kazakhstani bank products.

---

## 🧠 Core Architecture: Multi-Agent Pipeline
The project utilizes a sophisticated three-stage agentic workflow to ensure depth and accuracy:

* **The Extractor:** Uses **GPT-4o-mini** to parse unstructured user input into a strictly typed JSON object, identifying loan sum, duration, and purpose.
* **The Analyst:** The "mathematician" of the system. It calculates monthly payments using the annuity formula and performs **Semantic Search** in **ChromaDB** to find similar or better banking products.
* **The Advisor:** Powered by **GPT-4-turbo**, this agent synthesizes all raw data and financial metrics into a human-friendly, localized recommendation.

---

## 🛠️ Technical Stack

| Component | Technology |
| :--- | :--- |
| **Backend** | FastAPI (Python) |
| **Orchestration** | LangChain |
| **Vector Database** | ChromaDB (for RAG) |
| **AI Models** | GPT-4o-mini & GPT-4-turbo |
| **Frontend** | HTML5/CSS3 (Single Page Chat Interface) |

---

## 📈 Financial Logic
To ensure 100% accuracy, the **Analyst Agent** utilizes the standard annuity payment formula for all calculations:

$$A = P \cdot \frac{r(1+r)^n}{(1+r)^n - 1}$$

* **A** = Monthly payment
* **P** = Principal (Loan amount)
* **r** = Monthly interest rate
* **n** = Number of months

---

## 🔧 Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/alikhan-kai/tyin_ai.git
cd tyin_ai
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Environment Configuration
Create a `.env` file in the root directory and add your OpenAI API Key:
```text
OPENAI_API_KEY=your_actual_key_here
```

### 4. Run the Application
```bash
python api.py
```
The application will be available at: `http://127.0.0.1:8000`

---

## 🎯 Project Goals (AI & Prompt Engineering)
* **Non-Triviality:** Implements a full RAG pipeline with vector embeddings for real-world data retrieval.
* **Prompt Engineering:** Features specialized system prompts for structured data extraction and financial persona acting.
* **Real-World Utility:** Specifically targets the Kazakhstan market with localized data from banks like Halyk and Kaspi.

---
