AI-Powered Legal Query Agent for BNS
An offline-first legal information assistant that helps users find and understand relevant provisions of the Bharatiya Nyaya Sanhita (BNS), 2023. It accepts natural-language questions, retrieves relevant sections from the source document, and presents the result with references for verification.
Disclaimer: This project provides general legal information, not legal advice. It does not replace advice from a qualified lawyer. For a real case, consult a lawyer.

Features
- Natural-language queries about BNS provisions
- Semantic retrieval with Sentence Transformers (all-MiniLM-L6-v2)
- Section lookup and definition extraction from BNS text
- Answers grounded in retrieved legal material, with source references
- PDF links so users can inspect the source
- Basic intent handling for section, definition, and general questions
- A safety-oriented response layer for situation-based queries
- Flask web interface and API
- SQLite storage
- No paid API or GPU requirement
How it works
1. BNS PDF text is extracted with pdfplumber and parsed into sections.
2. Parsed sections are stored in SQLite.
3. A query is classified and normalized.
4. The system uses an exact lookup or semantic similarity search to retrieve relevant sections.
5. The response displays the retrieved legal text, a plain-language explanation where available, and a source link.
The retrieval design aims to keep answers traceable to the source. It cannot guarantee that every answer is complete or legally correct; users should verify the cited provision and seek professional advice when needed.
Technology
Area	Technology
Backend	Python, Flask
Storage	SQLite
Semantic search	Sentence Transformers, all-MiniLM-L6-v2
PDF processing	pdfplumber, regular expressions
Interface	HTML, CSS, JavaScript


Project structure
A suggested structure for the repository:
.
├── app.py                 # Flask application
├── data/                  # BNS PDF and processed data (not necessarily committed)
├── templates/             # HTML templates
├── static/                # CSS and JavaScript
├── requirements.txt       # Python dependencies
└── README.md
Adjust this tree to match the files in your repository.
Getting started
Prerequisites
- Python 3.9 or later
- pip
- The BNS, 2023 source PDF, used in accordance with its terms
Installation
1. Clone the repository:
   git clone <repository-url>
   cd <repository-directory>
2. Create and activate a virtual environment:
   python -m venv .venv
   Windows (PowerShell):
   .venv\Scripts\Activate.ps1
   macOS / Linux:
   source .venv/bin/activate
3. Install the project dependencies:
   pip install -r requirements.txt
4. Place the BNS PDF in the location expected by the application and run the project's ingestion or database initialization step, if required.
5. Start the Flask application using the command configured by the project. For a standard Flask entry point, this may be:
   flask --app app run
   Then open the local URL printed by Flask in your browser.
The exact PDF location, database initialization command, and run command depend on the implementation. Update these instructions to match the repository before publishing.

Example queries
- “What is the punishment for theft?”
- “Define cheating under the BNS.”
- “Which BNS section covers criminal intimidation?”
- “I was accused of theft. What general steps should I take?”
For questions about a real legal matter, the assistant should provide general information and encourage the user to contact a qualified lawyer. It should not present its response as a personalized legal strategy.
Data and source references
Use an authoritative copy of the BNS, 2023 text. Keep the source PDF and its attribution or source details clear in the application. Each retrieved section should link to the relevant PDF page or document location when the source file supports it.

Do not treat semantic similarity as proof that a provision applies to a user's situation. Retrieval can miss relevant text or return a nearby but inapplicable section.
Privacy
Before deploying the application, document what query data is stored, where it is stored, and how long it is retained. Avoid collecting personal or case-identifying information unless it is necessary and protected.
Limitations
- Retrieval quality depends on the quality of PDF extraction and section parsing.
- A similarity score indicates textual relevance, not legal applicability.
- The system may miss exceptions, amendments, cross-references, or relevant facts.
- Legal texts may change; keep the source document current and record its version.
- This is an informational project, not a substitute for a lawyer or official legal service.
Roadmap
- Multilingual query and response support
- Optional LLM-powered retrieval-augmented responses
- Mobile-friendly application
- Voice input and output
- Integration with verified case-law sources
Contributing
Contributions are welcome. Open an issue to discuss a bug or proposed change, then submit a pull request with a clear description of the update.
License
Add the license used by this repository. Until a license is included, the project should not be assumed to permit reuse or redistribution.
