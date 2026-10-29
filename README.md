# ⚖️ AI-Powered Legal Query Agent (BNS)

##  Overview

The **AI-Powered Legal Query Agent** is a smart legal assistant designed to help users understand the **Bharatiya Nyaya Sanhita (BNS), 2023** through simple natural language queries.

Users can ask questions like:

* *"What is the punishment for theft?"*
* *"Define fraud under BNS"*
* *"I was caught stealing, what should I do?"*

The system retrieves accurate and relevant legal sections directly from the BNS document, ensuring **reliable and verifiable responses**.

---

## Features

*  **Natural Language Query Support**
*  **Semantic Search using Sentence Transformers**
*  **Direct Section Retrieval from BNS**
*  **Clickable PDF Links for Verification**
*  **Definition Extraction from Legal Text**
*  **Lightweight (No GPU / No Paid APIs)**
*  **Advice Layer for Situational Queries**
*  **Safety Disclaimer for Responsible AI Usage**

---

##  Tech Stack

* **Programming Language:** Python
* **Backend:** Flask
* **Database:** SQLite
* **NLP:** Sentence Transformers (all-MiniLM-L6-v2)
* **Data Processing:** pdfplumber, regex
* **Frontend:** HTML, CSS, JavaScript

---

##  System Architecture

1. **Data Layer** – Extracts and stores BNS sections from PDF
2. **Retrieval Layer** – SQL lookup + semantic similarity search
3. **Intelligence Layer** – Intent classification + query expansion
4. **Response Layer** – Formatting + advice + disclaimer
5. **Presentation Layer** – Flask API + Web Interface

---

##  How It Works

1. User enters a query
2. Query is classified (section / definition / general query)
3. System performs:

   * Exact lookup OR
   * Semantic search using embeddings
4. Relevant sections are retrieved
5. Response is enhanced with:

   * Explanation
   * Advice (if needed)
   * PDF reference link

---

##  Key Highlights

*  No hallucination (answers grounded in legal text)
*  Works completely offline
*  Fast and lightweight
*  User-friendly interface

---

##  Disclaimer

This system provides **general legal information only**.
It is **not a substitute for professional legal advice**. Please consult a qualified lawyer for legal matters.

---

##  Future Scope

*  Multilingual support
*  Integration with LLM-based RAG systems
*  Mobile application
*  Voice-based query support
*  Integration with case law databases

---

##  Contributors

* Prajjnaa Ray Choudhury
* Srija Chatterjee
