# 📰 News Article Research Tool  
_A Conversational App for Summarizing and Citing News Articles using Langchain, OpenAI, and FAISS_

![](NewsResearchTool1.jpg)
![](NewsResearchTool2.jpg)

## 📌 Project Overview

This tool allows users to input **three news article links** and a **custom query**. It summarizes the contents of those articles, uses **OpenAI’s LLM** to generate a response based on the information, and clearly states which article the answer was derived from.  
The tool is built using:
- 🧠 **Langchain** for chaining operations
- 💬 **OpenAI** for language modeling
- 🗂️ **FAISS** for vector-based semantic search
- 🌐 **Streamlit** (optional) for a simple web UI

### ✅ Key Features
- Input 3 article URLs + a user query
- Summarized content stored and searched using FAISS
- Natural language query answering based on the combined information
- Displays response along with the article source

---

## ⚙️ Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/TARUNELANGO/EquityResearchTool.git
cd EquityResearchTool
```

### 2. Install Required Packages
```bash
pip install -r requirements.txt
```

### 3. Add Environment Variables
Create a .env file and add your OpenAI key:
```bash
OPENAI_API_KEY=your_openai_api_key
```

---

## 🚀 How to Use
1. Run the application:
streamlit run main.py

2. The web app will open in your browser.
- On the sidebar, you can input news article URLs directly.
- Initiate the data loading and processing by clicking "Process URLs."
- Observe the system as it performs text splitting, generates embedding vectors, and efficiently indexes them using FAISS.
- The embeddings will be stored and indexed using FAISS, enhancing retrieval speed.
- The FAISS index will be saved in a local file path in pickle format for future use.

3. Get answer to your queries pertaining to the URLs
- One can now ask a question and get the answer based on those news articles along with the source article for transparency

---

## 📊 Example URLs and Queries
### URLs
  - https://www.moneycontrol.com/news/business/tata-motors-mahindra-gain-certificates-for-production-linked-payouts-11281691.html
  - https://www.moneycontrol.com/news/business/tata-motors-launches-punch-icng-price-starts-at-rs-7-1-lakh-11098751.html
  - https://www.moneycontrol.com/news/business/stocks/buy-tata-motors-target-of-rs-743-kr-choksey-11080811.html
### Queries
  - What is Tiago iCNG price?
  - Summarize KR Choksey's report on Tata Motors

---

## Project Structure
- main.py: The main Streamlit application script.
- requirements.txt: A list of required Python packages for the project.
- .env: Configuration file for storing your OpenAI API key.
