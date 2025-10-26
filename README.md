# PdfChatBot

🚀 Features

✅ Upload and process PDF files
✅ Extract and store embeddings in FAISS vector store
✅ Query the document content with natural language
✅ Stream responses using an LLM (Hugging Face)
✅ Modular and scalable backend with FastAPI

Project Structure 
fastapi-pdf-chatbot/
│
├── app/
│   ├── main.py                 # FastAPI entry point
│   ├── routes/
│   │   └── chat.py             # Chat and upload endpoints
│   ├── core/
│   │   ├── config.py           # Environment configurations
│   │   ├── llm_service.py      # sak_llm() and LLM interaction logic
│   │   └── pdf_service.py      # PDF parsing and embedding logic
│   ├── utils/
│   │   └── vector_store.py     # FAISS vector database logic
│   ├── models/
│   │   └── schemas.py          # Pydantic models for requests/responses
│   └── __init__.py
│
├── data/
│   └── uploads/                # Folder to store uploaded PDFs
│
├── requirements.txt
└── README.md

⚙️ Installation
1️⃣ Clone the repository
git clone https://github.com/yourusername/fastapi-pdf-chatbot.git
cd fastapi-pdf-chatbot

2️⃣ Create a virtual environment
python -m venv venv
source venv/bin/activate  # for Linux/Mac
venv\Scripts\activate     # for Windows

3️⃣ Install dependencies
pip install -r requirements.txt

🔧 Environment Variables
Create a .env file in the root directory:

HF_MODEL_URL="http://127.0.0.1:8000" 

Start the FastAPI app:
uvicorn app.main:app --reload

Then open your browser at:
http://127.0.0.1:8000

🧰 Dependencies

Key packages:

FastAPI – API framework
LangChain – LLM orchestration
FAISS – Vector database
PyPDF2 – PDF parsing
Uvicorn – ASGI server
